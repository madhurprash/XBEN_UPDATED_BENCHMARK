# XBOW Validation Benchmarks (Updated)

This repository contains an updated version of the XBOW validation benchmarks dataset with modernized libraries and dependencies.

## Overview

This collection contains 104 carefully curated security assessment challenges designed to evaluate web-based offensive security tools. These benchmarks were developed by external contractors and mirror real-world vulnerability scenarios from security pentesting and bug bounty work.

## Key Features

- **104 Security Challenges**: Comprehensive set of CTF-style security benchmarks
- **Updated Libraries**: Modernized dependencies and libraries for compatibility
- **Jeopardy-style CTF Format**: Locate hidden flags rather than hardcoded solutions
- **Real-world Scenarios**: Based on actual pentesting and bug bounty experiences
- **Docker-based**: Each challenge runs in isolated Docker containers

## Structure

The repository organizes challenges in individual folders within the `benchmarks/` directory. Each folder represents one objective and may include multiple vulnerabilities and solving steps.

Each benchmark includes:
- `docker-compose.yml`: Service configuration and dependencies
- `benchmark.json` or `benchmark.yaml`: Challenge metadata including:
  - Challenge name and description
  - Difficulty level (1=easy, 2=medium, 3=hard)
  - Required files for solving
  - Win conditions (flag or question-based)
  - Security tags and identifiers
- `Makefile`: Build and deployment scripts
- `README.md`: Challenge-specific documentation

## Building Benchmarks

Build benchmarks using Docker Compose with flag injection:

```bash
# Build with default flag
make build

# Build with custom flag
make build FLAG=customflag
```

## Running Challenges

Start services using Docker Compose:

```bash
docker compose up -d --wait
```

Services use healthchecks and dependency declarations to prevent race conditions during startup.

## Updates in This Version

This is an updated fork of the original XBOW validation benchmarks with:
- Updated libraries and dependencies
- Improved compatibility with modern environments
- Enhanced container configurations

## Legal Notice

Licensed under Apache 2.0. This repository intentionally contains unfixed vulnerabilities for educational and security assessment purposes only. **NOT suitable for production deployment.**

## Original Source

Based on the [XBOW Engineering Validation Benchmarks](https://github.com/xbow-engineering/validation-benchmarks)
