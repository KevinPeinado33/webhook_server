# webhook_server

Servidor de webhooks en Rust con [axum](https://github.com/tokio-rs/axum).

## Requisitos

- [Rust](https://rustup.rs/) (incluye `cargo`)

## Instalación

```bash
git clone <url-de-este-repo>
cd webhook_server
cargo build
```

## Uso

Levantar el servidor:

```bash
cargo run
```

Queda escuchando en `http://0.0.0.0:3000`.

### Hot reload

Rust es compilado, no hay hot reload nativo. Para recompilar y reiniciar automáticamente al guardar cambios, instalá `cargo-watch` una vez:

```bash
cargo install cargo-watch
```

Y usalo en vez de `cargo run`:

```bash
cargo watch -x run
```

## Endpoints

| Método | Ruta      | Descripción         |
|--------|-----------|----------------------|
| GET    | `/health` | Chequeo de salud     |

Probar:

```bash
curl localhost:3000/health
```
