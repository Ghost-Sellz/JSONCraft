# JSONCraft

> Convert JSON into developer models instantly — in your browser.

JSONCraft takes raw JSON and generates production-ready data models across multiple languages and frameworks. No installs, no backend, no data ever leaves your machine.

🔗 **Live demo:** [js0ncraft.netlify.app](https://js0ncraft.netlify.app/)

---

## Features

- **10 output formats** — TypeScript, Python, GraphQL, SQL, Go, Rust, Java, Kotlin, Zod, Prisma
- **Live conversion mode** — output updates as you type
- **Drag & drop** JSON files directly onto the editor
- **Import from URL** — fetch JSON from any API endpoint
- **JSON formatter** — pretty-print with one click
- **JSON validator** — instant feedback on syntax errors
- **Nested object support** — deeply nested structures handled automatically
- **Array detection** — typed arrays and object arrays both supported
- **Smart type inference** — distinguishes `int` vs `float`, `String` vs `Any`, etc.
- **Copy & download** — download uses the correct file extension per language
- **Dark / light theme**
- **Zero dependencies** — pure HTML, CSS, and JavaScript
- **Offline capable** — clone and open `index.html`, no server needed

---

## Supported Conversions

| Format | Output |
|---|---|
| TypeScript | `interface` definitions |
| Python | `@dataclass` classes with type hints |
| GraphQL | `type` schema definitions |
| SQL | `CREATE TABLE` statements |
| Go | `struct` with JSON tags |
| Rust | `struct` with Serde derives |
| Java | Classes with getters and setters |
| Kotlin | `data class` definitions |
| Zod | Schema with `z.infer<>` type exports |
| Prisma | `model` schema blocks |

---

## Example

**Input:**

```json
{
  "user": {
    "id": 1,
    "name": "Alex",
    "email": "alex@mail.com",
    "active": true,
    "score": 9.5
  }
}
```

**TypeScript output:**

```ts
interface Model {
  user: ModelUser
}

interface ModelUser {
  id: number
  name: string
  email: string
  active: boolean
  score: number
}
```

**Go output:**

```go
package main

type Model struct {
  User ModelUser `json:"user"`
}

type ModelUser struct {
  Id     int     `json:"id"`
  Name   string  `json:"name"`
  Email  string  `json:"email"`
  Active bool    `json:"active"`
  Score  float64 `json:"score"`
}
```

**Rust output:**

```rust
use serde::{Deserialize, Serialize};

#[derive(Debug, Serialize, Deserialize)]
pub struct Model {
  pub user: ModelUser,
}

#[derive(Debug, Serialize, Deserialize)]
pub struct ModelUser {
  pub id: i64,
  pub name: String,
  pub email: String,
  pub active: bool,
  pub score: f64,
}
```

---

## Getting Started

**Run locally:**

```bash
git clone https://github.com/Ghost-Sellz/JSONCraft
cd JSONCraft
open index.html
```

No `npm install`. No build step. Just open the file.

---

## Project Structure

```
jsoncraft/
├── index.html   ← UI and layout
├── style.css    ← Theming, dark/light mode, responsive layout
└── script.js    ← All conversion logic and feature handlers
```

---

## Roadmap

- [x] TypeScript interface generator
- [x] Python dataclass generator
- [x] GraphQL schema generator
- [x] SQL table generator
- [x] Go struct generator
- [x] Rust struct generator
- [x] Java class generator
- [x] Kotlin data class generator
- [x] Zod schema generator
- [x] Prisma schema generator
- [x] Drag & drop JSON files
- [x] Import JSON from API URL
- [x] Live conversion mode
- [ ] Monaco editor integration
- [ ] CLI version
- [ ] Zod refinements and validations
- [ ] Prisma relations from nested objects
- [ ] Export as multiple files (one per model)

---

## Contributing

Contributions are welcome! See [CONTRIBUTING.md](CONTRIBUTING.md) for full guidelines.

Quick start:

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/your-feature`
3. Make your changes and test in the browser
4. Submit a pull request

---

## Security

JSONCraft runs entirely client-side. Your JSON never leaves the browser. See [SECURITY.md](SECURITY.md) for the full policy.

---

## License

[MIT](LICENSE)

---

## Why JSONCraft?

Developers constantly convert JSON API responses into typed data models. It's repetitive, error-prone, and a waste of time. JSONCraft removes that entirely — paste JSON, pick a language, and get clean output in under a second.

---

If JSONCraft saved you time, consider giving it a ⭐ on GitHub.
