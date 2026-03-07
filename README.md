# ALICE-BioSim

Molecular dynamics and materials design simulation platform

## License

AGPL-3.0

## Architecture

```
Frontend :3000  -->  API Gateway :8080  -->  Core Engine :8081
```

| Layer | Port | Technology |
|-------|------|-----------|
| Frontend | 3000 | Next.js 14, Tailwind CSS |
| API Gateway | 8080 | Rust, Axum |
| Core Engine | 8081 | Rust, Axum |

## ALICE Crate Integration

alice-bio, alice-atoms, alice-physics, alice-energy

## Endpoints

| Method | Path | Description |
|--------|------|-------------|
| `POST` | `/api/v1/fold` | タンパク質折りたたみ予測 |
| `POST` | `/api/v1/materials` | 材料特性→原子構造コンパイル |
| `POST` | `/api/v1/dynamics` | 分子動力学シミュレーション |
| `POST` | `/api/v1/energy` | エネルギー計算 |
| `GET ` | `/health` | ヘルスチェック |

## Quick Start

```bash
cd services/core-engine
cargo run --release
curl http://localhost:8081/health
```

## Author

Moroya Sakamoto
