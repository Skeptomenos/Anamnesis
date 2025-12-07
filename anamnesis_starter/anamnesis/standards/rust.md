# Rust Standards

> **Read this when:** Writing or reviewing Rust code.
> **Also read:** `global.md` for language-agnostic rules.

---

## 1. Code Style & Formatting

### 1.1 Tooling
- **Formatter:** `rustfmt` — Run `cargo fmt` before committing
- **Linter:** `clippy` — Run `cargo clippy` and fix all warnings
- **Edition:** Rust 2021

### 1.2 Naming Conventions
- **Functions/Variables:** `snake_case`
- **Types/Traits:** `PascalCase`
- **Constants:** `SCREAMING_SNAKE_CASE`
- **Modules:** `snake_case` (file names match module names)

---

## 2. Error Handling

### 2.1 Use Result Types
```rust
// GOOD: Use Result with context
fn parse_config(path: &str) -> Result<Config, ConfigError> {
    let content = std::fs::read_to_string(path)
        .map_err(|e| ConfigError::ReadFailed(e.to_string()))?;
    // ...
}

// BAD: Unwrap in production code
let config = std::fs::read_to_string(path).unwrap(); // Never do this
```

### 2.2 Error Libraries
- Use `thiserror` for custom error types
- Use `anyhow` for application-level error propagation
- Reserve `.unwrap()` for tests only

---

## 3. Memory & Safety

### 3.1 Ownership Best Practices
- Prefer borrowing (`&T`) over cloning when possible
- Use `Cow<'_, T>` for conditionally owned data
- Avoid `Rc`/`Arc` unless shared ownership is genuinely needed

### 3.2 Forbidden Patterns
| Pattern | Reason |
|---------|--------|
| `unsafe` blocks | Security risk — avoid unless absolutely necessary and document extensively |
| `.unwrap()` in prod | Use `?` or `.expect()` with context |
| Global mutable state | Use proper state management patterns |

---

## 4. Async Patterns

### 4.1 Async Runtime
- Choose one runtime (tokio, async-std) and stick with it
- Never block in async context — use `spawn_blocking` for CPU-intensive work

### 4.2 Example
```rust
// GOOD: Non-blocking async
async fn fetch_data() -> Result<String, Error> {
    let response = reqwest::get("https://api.example.com")
        .await?
        .text()
        .await?;
    Ok(response)
}

// GOOD: Offload blocking work
let result = tokio::task::spawn_blocking(|| {
    heavy_computation()
}).await?;
```

---

## 5. Testing

### 5.1 Unit Tests
```rust
#[cfg(test)]
mod tests {
    use super::*;

    #[test]
    fn test_parse_valid_input() {
        let result = parse("valid");
        assert!(result.is_ok());
    }
}
```

### 5.2 Integration Tests
- Place in `tests/` directory
- Use `#[tokio::test]` for async tests

---

## 6. Dependencies

### 6.1 Common Approved Crates
| Crate | Purpose |
|-------|---------|
| `serde` / `serde_json` | Serialization |
| `thiserror` | Custom error types |
| `anyhow` | Error propagation |
| `tokio` | Async runtime |
| `tracing` | Structured logging |
| `clap` | CLI argument parsing |

### 6.2 Before Adding Dependencies
- Check maintenance status (recent commits?)
- Evaluate transitive dependencies (bloat?)
- Consider compile time impact
