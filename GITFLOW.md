# GitFlow Branching Strategy for DotNetExtensions.OAuth20

This document outlines the GitFlow branching strategy we use for managing our development and release processes. GitFlow helps us manage feature development, bug fixes, and releases in a clean, organized manner.

## Main Branches

1. **main**: This branch contains the latest stable release. All production-ready code is merged here.
   - All releases are tagged in this branch.
   - Only `release/*` or `hotfix/*` branches are merged into `main`.
   - **Protected Branch**: Merges to `main` can only be done through approved pull requests after passing tests and code reviews.

2. **develop**: This branch contains the latest ongoing development. All feature, bugfix, and hotfix branches are merged here.
   - This branch serves as an integration branch for features and bug fixes.
   - It is the basis for the next release.
   - Only `feature/*`, `bugfix/*`, `release/*`, and `hotfix/*` branches are merged into `develop`.
   - **Protected Branch**: Merges to `develop` can only be done through approved pull requests after passing tests and code reviews.

## Supporting Branches

Supporting branches help parallelize development. These branches are short-lived and only exist until their work is complete and merged back into `develop` or `main`.

1. **feature/***: These branches are used for developing new features.
   - Start from `develop`.
   - Merge into `develop` when the feature is complete and tested.
   - Branch naming convention: `feature/feature-name`
   - Example: `feature/user-authentication`

2. **bugfix/***: These branches are used to fix bugs that are not critical for immediate production.
   - Start from `develop`.
   - Merge into `develop` when the bug is fixed.
   - Branch naming convention: `bugfix/bug-description`
   - Example: `bugfix/fix-login-error`

3. **release/***: These branches are used to prepare a new release.
   - Start from `develop` when the develop branch is feature-complete for the next release.
   - Merge into both `main` and `develop` once testing and documentation are complete.
   - Branch naming convention: `release/release-version`
   - Example: `release/1.0.0`

4. **hotfix/***: These branches are used for urgent fixes in production.
   - Start from `main` when a critical bug in production needs to be resolved immediately.
   - Merge into both `main` and `develop` after the fix is complete.
   - Branch naming convention: `hotfix/hotfix-description`
   - Example: `hotfix/fix-critical-issue`

## Workflow

### Feature Workflow

1. Create a new branch from `develop` for the feature you are working on:
   ```bash
   git checkout -b feature/your-feature develop
   ```
2. Once the feature is complete, submit a pull request (PR) for review.
3. After review and approval, the feature branch is merged into `develop`.

### Bugfix Workflow

1. Create a new branch from `develop` for the bugfix:
   ```bash
   git checkout -b bugfix/bug-description develop
   ```
2. After fixing the bug, submit a pull request (PR) for review.
3. The bugfix branch is merged back into `develop`.

### Release Workflow

1. When the `develop` branch is ready for release, create a release branch:
   ```bash
   git checkout -b release/version-number develop
   ```
2. Perform final testing and documentation on the release branch.
3. After everything is verified, open **Pull Requests** (PRs) to merge the release branch into both `main` and `develop`.
   - Ensure the PRs pass all automated tests and receive the necessary approvals before merging.
   - Merges into both `main` and `develop` are only done through PRs on GitHub to ensure proper review and traceability.

4. Tag the release in `main`:
   ```bash
   git tag -a v1.0.0 -m "Release version 1.0.0"
   git push origin v1.0.0
   ```

### Hotfix Workflow

1. If a critical issue is discovered in production, create a hotfix branch from `main`:
   ```bash
   git checkout -b hotfix/fix-description main
   ```
2. Once the fix is complete, open **Pull Requests** to merge the hotfix into both `main` and `develop`.
   - As with releases, use PRs to ensure code reviews and tests are passed before merging.

3. Tag the hotfix release:
   ```bash
   git tag -a v1.0.1 -m "Hotfix version 1.0.1"
   git push origin v1.0.1
   ```

## Merging Strategy

- **Feature and bugfix branches** are merged into `develop` via pull requests.
- **Release branches** are merged into both `main` and `develop` via pull requests.
- **Hotfix branches** are merged into both `main` and `develop` via pull requests.
- Ensure all branches are rebased or updated from the latest `develop` or `main` before merging.
- **Protected Branches**: Merges into `main` and `develop` are only allowed via pull requests that pass code reviews and automated tests.

## Conclusion

By following this GitFlow strategy, we ensure that development stays organized, releases are handled methodically, and production code remains stable. This approach allows contributors to work in parallel while minimizing the risk of conflicts and issues in production.

## Additional Considerations

- **Rebasing**: Before submitting a pull request, always ensure your branch is up-to-date with the latest `develop` branch by rebasing it:
   ```bash
   git checkout develop
   git pull origin develop
   git checkout feature/your-feature
   git rebase develop
   ```

- **Tagging Releases**: Make sure to tag all releases in `main` with the appropriate version number. This helps track and identify releases easily.
