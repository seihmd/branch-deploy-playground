# Branch Deploy Playground

This repository demonstrates the usage of [github/branch-deploy](https://github.com/github/branch-deploy) action.

## How to test branch deployment

1. Create a pull request
2. In the PR comments, use these commands:
   - `.deploy` - Deploy to production environment
   - `.deploy staging` - Deploy to staging environment  
   - `.deploy development` - Deploy to development environment
   - `.noop` - Run a noop deployment (dry run)
   - `.lock` - Lock deployments
   - `.unlock` - Unlock deployments

## Available environments

- `production` (default)
- `staging`
- `development`

## Permissions

Only users with `write`, `maintain`, or `admin` permissions can trigger deployments.