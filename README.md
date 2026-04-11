# franco-sample

A sample application used to test CI/CD pipeline state management.

## Purpose

This repository is a test bed for automating interactions with GitHub Actions workflows — specifically for observing deployment states:
- Is the PR check still running?
- Is the deployment in progress?
- Has it completed successfully?

## Files

- `Cache-pasting.txt` — The primary file used for testing. Make changes here, open a PR, and watch the pipeline.

## Workflows

- **PR Check** (`pr-check.yml`): Runs on every PR targeting `main`. Waits 10 seconds, then marks the check as passed. This is a required status check before merging.
- **Deploy** (`deploy.yml`): Runs on every push to `main`. Waits 10 seconds, then reports a successful deployment.
