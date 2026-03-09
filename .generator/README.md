# KIWI API Client Generator

This folder contains the configuration and scripts used to automatically generate the PHP client library for the KIWI API using the [Swagger Codegen](https://github.com/swagger-api/swagger-codegen) project.

## How it Works

1.  **Configuration**: `.generator/swagger-config.json` defines the client language (`php`), namespaces (`KiwiKi`), and other generator-specific options.
2.  **Selective Extraction**: To prevent the generator from overwriting custom repository configuration (for example `composer.json` and the root `README.md`), the scripts extract only the core library components:
    -   `lib/`: The generated PHP Models and API classes.
    -   `docs/`: The generated API documentation.
    -   `test/`: The generated unit tests.
3.  **Local Generation**: You can run `.generator/generate-local.sh` to update the library on your local machine.

## GitHub Actions Integration

We use two workflows to automate client updates and releases:

### 1. Generate KIWI Client (`generate-client.yml`)
This workflow is triggered manually via **workflow_dispatch**.
-   **Function**: It fetches the latest API specification, triggers code generation, and extracts the generated code into the repository.
-   **Result**: It automatically creates a new branch and a Pull Request for review.

### 2. Tag Release (`tag-release.yml`)
This workflow runs automatically whenever code is pushed to the `main` branch.
-   **Function**: It checks the version number in the swagger specification.
-   **Result**: If the tag does not exist yet, it creates and pushes a Git tag (for example `1.0.0(Stable)` after whitespace cleanup).

## Repository Setup

To ensure the workflows run successfully, verify the following in GitHub repository settings:

1.  **Workflow Permissions**:
    -   Go to **Settings > Actions > General**.
    -   Under **Workflow permissions**, select **Read and write permissions**.
    -   Enable **Allow GitHub Actions to create and approve pull requests**.
2.  **Branch Protection**:
    -   It is recommended to protect the `main` branch so generated updates are reviewed through pull requests.
