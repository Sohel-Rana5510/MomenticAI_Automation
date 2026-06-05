# MomentAI

This repository contains Momentic v2 browser automation tests for the MomentAI project.

## Purpose

The purpose of this project is to validate and automate user workflows for MomentAI using Momentic browser tests. It ensures key web behavior is tested consistently across environments and helps catch regressions in user flows such as token creation, verification, and checkout interactions.

## Overview

- `package.json` defines the project and includes the Momentic CLI dependency.
- `momentic.config.yaml` configures the Momentic test runner and web environment.
- `*.test.yaml` files contain Momentic test scenarios.

## Included Tests

- `bankqr.test.yaml` — browser flow for token creation and verification on `https://qrdev.deepmindlabs.ai`.
- `web/add-to-cart.test.yaml` — additional browser automation coverage for the web environment.

## Setup

1. Install Node.js if not already installed.
2. From the repository root, install dependencies:

```bash
npm install
```

## Running Tests

Use the Momentic CLI to run the configured tests. Example:

```bash
npx momentic run
```

If your project uses a different CLI command or global Momentic installation, adjust as needed.

## Configuration

The `momentic.config.yaml` file includes:

- `name`: project name
- `include`: test file patterns
- `browser`: browser-specific behavior
- `ai`: Momentic AI features for selectors, assertions, and recovery
- `environments`: base URL and environment variables for the `web` environment

## Notes

- The repository currently uses Momentic `^2.125.0` as a development dependency.
- The default browser environment is set to Chromium with a viewport of `1920x1080`.
