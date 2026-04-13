# Goods Price Comparison Properties

Environment property files for [goods-price-comparison-service](https://github.com/RizkiRachman/goods-price-comparison-service).

## Usage

Run the application with the appropriate Spring profile:

```bash
# Development
mvn spring-boot:run -Dspring-boot.run.profiles=dev

# Or with Docker
docker run -v ./dev/application.properties:/app/config/application.properties ...
```

## Files

| Directory | Environment |
|-----------|-------------|
| `dev/` | Local development |
| `staging/` | Staging |
| `prod/` | Production |

## Security

- **Never commit real credentials** — use `.local` overrides (gitignored)
- Copy a properties file to `dev/application-local.properties` and fill in real values
- In CI/CD, inject secrets via vault or pipeline variables

```bash
cp dev/application.properties dev/application-local.properties
# Edit dev/application-local.properties with real credentials
```
