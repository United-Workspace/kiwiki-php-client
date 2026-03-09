# KIWI API PHP SDK

PHP SDK for the KIWI API used for remote unlocking and administration of doors.

> [!NOTE]
> This SDK is generated from the KIWI API specification and maintained as an integration library.

## Features

- Full generated API client (models, API classes, and tests)
- Manual client regeneration via GitHub Actions
- Automatic tagging based on API spec version

## Installation (Consumer Project)

This package is **not published on Packagist**, so plain `composer install` in a different project will not fetch it automatically.

### Option A: Configure `composer.json` manually

Add this to your consuming project's `composer.json`:

```json
{
  "repositories": [
    {
      "type": "vcs",
      "url": "https://gitlab.com/sleevesup/kiwiki-php-client.git"
    }
  ],
  "require": {
    "sleevesup/kiwiki-api": "dev-main"
  }
}
```

Then run:

```bash
composer update sleevesup/kiwiki-api --with-all-dependencies
```

### Option B: Configure via Composer CLI

```bash
composer config repositories.kiwiki vcs https://gitlab.com/sleevesup/kiwiki-php-client.git
composer require sleevesup/kiwiki-api:dev-main
```

If the repository is private, ensure Composer can authenticate to GitLab (SSH key or access token).

## Getting Started

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

use KiwiKi\Configuration;
use KiwiKi\Api\AddressApi;
use GuzzleHttp\Client;

$config = Configuration::getDefaultConfiguration()
    ->setApiKey('Session-Key', 'YOUR_API_KEY');

$api = new AddressApi(new Client(), $config);
$result = $api->v1AddressesSearchGet('street', '1', 1010);
```

## Documentation

- Generated endpoint/model docs: `docs/`
- Generated client source: `lib/`
- Generated API snapshot README (created by generator): `API_README.md`

## Automated Generation & Release

- `Generate KIWI Client` workflow (`.github/workflows/generate-client.yml`)
  - Triggered manually
  - Regenerates client code from the configured Swagger spec
  - Opens a pull request with the changes
- `Tag Release` workflow (`.github/workflows/tag-release.yml`)
  - Triggered on pushes to `main`
  - Reads API version from spec and creates a matching Git tag if missing

Generator configuration and local generation script live in `.generator/`.
See `.generator/README.md` for details.

## Development (This Repository)

- Install local development dependencies: `composer install`
- Run tests: `./vendor/bin/phpunit`
