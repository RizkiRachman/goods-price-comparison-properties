# Goods Price Comparison Properties

Environment property files for [goods-price-comparison-service](https://github.com/RizkiRachman/goods-price-comparison-service).

## Usage

Source the env file before running the application:

```bash
# Development
source .env.dev

# Then run
mvn spring-boot:run

# Or with Docker
docker run --env-file .env.dev ...
```

## Files

| File | Environment |
|------|-------------|
| `.env.dev` | Local development |
| `.env.staging` | Staging |
| `.env.prod` | Production |

## Security

- **Never commit real credentials** — use `.local` overrides (gitignored)
- Copy an env file to `.env.dev.local` and fill in real values
- In CI/CD, inject secrets via vault or pipeline variables

```bash
cp .env.dev .env.dev.local
# Edit .env.dev.local with real credentials
```
