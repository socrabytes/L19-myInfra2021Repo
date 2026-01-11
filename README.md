# Lab 19: Terraform Infrastructure (Archive)

> ⚠️ **ARCHIVED:** This repository is maintained for historical reference only. No future updates are planned.

## Overview
Advanced Terraform lab demonstrating infrastructure state management and automation for SonarQube.

## Key Features
- **Remote Backend:** S3 bucket (`dev-tf-state-bucket-l19`) with versioning enabled.
- **State Locking:** DynamoDB table (`l19-dynamodb-table`) for concurrency control.
- **Automation:** Jenkins pipeline for `init`, `plan`, and parameterized `apply`/`destroy` actions.
- **Infrastructure:**
  - **SonarQube Server:** EC2 (t2.micro) with Security Group opening ports 9000 (UI) and 22 (SSH).
  - **Elastic IP:** Dedicated static IP for the SonarQube instance.

## Usage
This repo was designed to be run via the included `Jenkinsfile`, accepting an `action` parameter (e.g., `apply`, `destroy`).
