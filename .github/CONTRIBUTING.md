# Contribution Guidelines for WebSave-AI-Powered-Read-It-Later-Browser-Extension

As an Apex project, `WebSave-AI-Powered-Read-It-Later-Browser-Extension` demands engineering excellence. We enforce strict adherence to the **Apex Technical Authority** standards to ensure future-proof, high-velocity development. By contributing, you agree to uphold these principles.

## 1. The Apex Philosophy: Zero-Defect, High-Velocity

All contributions must align with the core tenets:

*   **SOLID Principles:** Code must demonstrate high cohesion and low coupling. Favor Dependency Inversion.
*   **DRY (Don't Repeat Yourself):** Abstract common logic rigorously.
*   **YAGNI (You Ain't Gonna Need It):** Implement only what is strictly required for the current feature scope.
*   **Security First:** Treat user data (especially saved content) with the highest security standards. All network interactions must be secured (HTTPS/WSS).

## 2. Development Environment Setup (Leveraging Apex Toolchain)

To contribute, ensure your local environment mirrors the CI standards defined in `.github/workflows/ci.yml` and the directives in `AGENTS.md`.

1.  **Clone the Repository (using new name):**
    bash
    git clone https://github.com/chirag127/WebSave-AI-Powered-Read-It-Later-Browser-Extension.git
    cd WebSave-AI-Powered-Read-It-Later-Browser-Extension
    

2.  **Dependency Management (TypeScript/Node Focus):**
    Since this is a browser extension leveraging TypeScript/Node, we utilize modern tooling for speed.
    bash
    # Install dependencies (Assume npm/yarn/pnpm based on project standard)
    npm install
    

3.  **Code Quality Enforcement:**
    Before committing, you **MUST** ensure all linting and formatting checks pass locally. Failure to pre-validate quality will result in CI failure and rejection.
    bash
    # Run Linter and Formatter (Biome or ESLint/Prettier)
    npm run lint
    npm run format

    # Run Unit Tests (Vitest recommended)
    npm run test:unit
    

## 3. Contribution Workflow

We follow a strict **Feature Branch Workflow** integrated with detailed Pull Request scrutiny.

1.  **Branching:** Create a new feature or fix branch off `main`:
    bash
    git checkout main
    git pull
    git checkout -b feat/descriptive-feature-name
    

2.  **Development & Verification:** Implement changes. Ensure **100% test coverage** for new code paths (see `AGENTS.md` for verification protocols).

3.  **Commit Messages:** Commit messages must follow the **Conventional Commits Specification** (e.g., `feat: add save-to-MongoDB endpoint`, `fix: resolve memory leak in parsing`).

4.  **Pull Request (PR) Submission:**
    *   **Target:** Always target the `main` branch.
    *   **Template:** Use the provided `.github/PULL_REQUEST_TEMPLATE.md` and fill out all sections completely.
    *   **Linking:** Link any associated GitHub Issues using `Closes #<issue-number>`.

5.  **Review:** Your PR will undergo mandatory checks: automated CI/CD execution, static analysis, security scan, and manual review by an Apex Architect for adherence to design patterns and performance benchmarks.

## 4. Reporting Bugs and Requesting Features

Use the provided templates for all submissions:

*   **Bugs:** Use `.github/ISSUE_TEMPLATE/bug_report.md`. Provide detailed reproduction steps.
*   **Features:** Create a new Issue describing the **Value Proposition** and the **High-Level Architecture** you envision for the solution.

## 5. Security Disclosure Policy

We take security extremely seriously. If you discover a vulnerability, **DO NOT** create a public issue. Follow the process outlined in `.github/SECURITY.md` for responsible disclosure.

--- 

*Thank you for helping maintain the integrity of the Apex ecosystem.*