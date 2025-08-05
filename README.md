# Branch Deploy Playground

This repository demonstrates the usage of [github/branch-deploy](https://github.com/github/branch-deploy) action.

## How to test branch deployment

1. Create a pull request
2. In the PR comments, use these commands:
   - `.deploy` - Deploy to production environment
   - `.deploy staging` - Deploy to staging environment (requires manual confirmation)
   - `.deploy development` - Deploy to development environment
   - `.noop` - Run a noop deployment (dry run)
   - `.lock` - Lock deployments
   - `.unlock` - Unlock deployments

### Staging deployment with manual approval

When deploying to staging:

1. Comment `.deploy staging` in the PR
2. The staging deployment will complete automatically
3. **Manual verification step**: A GitHub issue will be created for approval
4. Verify the staging environment manually
5. Comment `.confirm-staging` in the **original PR** to approve and close the approval issue

## Available environments

- `production` (default)
- `staging`
- `development`

## Permissions

Only users with `write`, `maintain`, or `admin` permissions can trigger deployments.