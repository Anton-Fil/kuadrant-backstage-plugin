# Contributing

For general contribution guidelines, PR requirements, and issue triage rules, see the [Kuadrant contributing guide](https://github.com/Kuadrant/.github/blob/main/CONTRIBUTING.md).

## Issue Policy

**Do not start work on an issue unless it has been assigned to you by a maintainer.**

Issues go through a triage and planning process before they are ready for contribution. Working on unassigned issues — whether manually or via AI coding agents — wastes your time and ours.

**Pull requests submitted against unassigned issues will be automatically closed and will not be reopened.**

If you're interested in contributing to an issue, leave a comment and wait for a maintainer to assign it to you before starting any work.

Issues labelled `maintainers-only` are reserved for the maintainer team and are not available for external contribution.

## Contributions

We welcome code and non-code contributions to our project. Non-code contributions can come in the form of documentation updates, bug reports, enhancement requests, and feature requests.

### Finding Issues to Work On

The best place to start is to look through our issues for [bugs](https://github.com/Kuadrant/kuadrant-backstage-plugin/issues?q=is%3Aopen+is%3Aissue+label%3Akind%2Fbug), [good first issues](https://github.com/Kuadrant/kuadrant-backstage-plugin/issues?q=is%3Aopen+is%3Aissue+label%3A%22good+first+issue%22), and [help wanted](https://github.com/Kuadrant/kuadrant-backstage-plugin/issues?q=is%3Aopen+is%3Aissue+label%3A%22help+wanted%22). These are a great starting point for new contributors.

Remember: only work on issues that are `triage/accepted` and assigned to you.

### Bug Reporting

If you found a bug, please submit an [issue](https://github.com/Kuadrant/kuadrant-backstage-plugin/issues/new) describing the problem. Include:

- Steps to reproduce the bug
- The `app-config.yaml` that is being used (**remember to remove all secrets before sharing**)
- Any relevant logs

### Enhancement Requests

If you want an enhancement of a feature or workflow, submit an [issue](https://github.com/Kuadrant/kuadrant-backstage-plugin/issues/new) describing the enhancement. Include:

- What you are wanting to see improved
- The current behavior
- The new behavior you wish to see

### Feature Requests

If you want to see a new feature, file an [issue](https://github.com/Kuadrant/kuadrant-backstage-plugin/issues/new) detailing the new feature. Include:

- What you are trying to achieve with the new feature
- What you will need
- Who will have access
- Any relevant documentation or information on the new feature

### Documentation

If there is documentation that is unclear or could use some improvements, please raise an issue or submit a pull request.

### Pull Requests

If you want to submit code changes to the project, here are some guidelines:

1. **Create a Branch**

   ```bash
   git checkout -b your-feature-branch
   ```

2. **Implement Your Changes**

   Make your code changes, ensuring that you follow the project's coding standards and best practices.

3. **Testing**

   Ensure all tests pass before committing.

   ```bash
   yarn test                       # run unit tests
   ```

   For E2E tests (requires a running kind cluster and app):

   ```bash
   cd e2e-tests
   yarn test                       # run kuadrant e2e tests
   yarn test:smoke                 # run smoke tests only
   ```

4. **Linting and Formatting**

   Ensure your code passes linting and formatting checks.

   ```bash
   yarn lint:check                 # check for linting errors
   yarn lint:fix                   # fix linting errors
   yarn prettier:check             # check formatting
   yarn prettier:fix               # fix formatting
   ```

5. **TypeScript Compilation**

   Ensure the project compiles cleanly.

   ```bash
   yarn tsc                        # run type checks across all packages
   ```

6. **Ensure CI Passes**

   Your contributions will need to pass the Continuous Integration (CI) tests for pull requests.

7. **Commit Changes**

   Use meaningful commit messages following the [Conventional Commits](https://www.conventionalcommits.org/) specification.

   ```bash
   git commit -m "feat: add new feature"
   ```

8. **Push to Your Fork**

   ```bash
   git push origin your-feature-branch
   ```

9. **Open a Pull Request**

   Go to the original repository and click on **New Pull Request**. Provide a clear description of your changes, including any issues your PR fixes, acceptance criteria, and any special notes to the reviewers.

## Commit Messages

Follow the [Conventional Commits](https://www.conventionalcommits.org/) specification:

- `feat`: A new feature.
- `fix`: A bug fix.
- `docs`: Documentation changes.
- `style`: Code style changes (formatting, missing semi-colons, etc.).
- `refactor`: Code changes that neither fix a bug nor add a feature.
- `test`: Adding or correcting tests.
- `chore`: Changes to the build process or auxiliary tools.
