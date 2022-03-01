# Composer Builder

Composer builder image with PHP and Composer.

## Tags

* PHP 7.4: `7`, `7.4`
* PHP 8.0: `8.0`
* PHP 8.1: `latest`, `8`, `8.1`

## Usage

Example usage

```bash
docker run --rm -v "$(pwd):/app" ghcr.io/olkitu/composer-builder:8.0 composer install
```

### Using in Gitlab CI/CD

You can use with Gitlab CI/CD example:

```yml
build:
  image: ghcr.io/olkitu/composer-builder:8.0
  script:
  - composer install --no-dev --no-progress
```