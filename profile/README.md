<div align="center">

  # Doxynix Intelligence

  **Next-Gen Repository Analysis & Documentation Engine**
  
  [![CI Status](https://github.com/doxynix/doxynix/actions/workflows/ci.yml/badge.svg)](https://github.com/doxynix/doxynix/actions)
  [![Mutation Score](https://img.shields.io/badge/Mutation_Score-High-success?style=flat&logo=stryker&logoColor=white)](https://github.com/doxynix/doxynix)
  [![Architecture](https://img.shields.io/badge/Architecture-FSD-orange?style=flat)](https://feature-sliced.design/)
  [![License](https://img.shields.io/badge/license-MIT-blue?style=flat)](LICENSE)

  <p align="center">
    <b>Analyze. Understand. Document.</b><br>
    A serverless-first platform for automated code analysis, <br>
    built on event-driven microservice patterns.
  </p>

</div>

---

### ⚡ Tech Stack

We utilize a cutting-edge **2026** stack to ensure maximum performance, fault tolerance, and developer experience.

| Domain | Technologies |
| :--- | :--- |
| **Frontend Core** | ![Next.js](https://img.shields.io/badge/Next.js_16-black?style=for-the-badge&logo=next.js&logoColor=white) ![React](https://img.shields.io/badge/React_19-20232A?style=for-the-badge&logo=react&logoColor=61DAFB) ![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white) |
| **UI & UX** | ![Tailwind CSS](https://img.shields.io/badge/Tailwind_4-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white) ![Shadcn/UI](https://img.shields.io/badge/shadcn%2Fui-000000?style=for-the-badge&logo=shadcnui&logoColor=white) ![FSD](https://img.shields.io/badge/Arch-FSD-orange?style=for-the-badge) |
| **Backend & API** | ![tRPC](https://img.shields.io/badge/tRPC-2596BE?style=for-the-badge&logo=trpc&logoColor=white) ![NextAuth](https://img.shields.io/badge/NextAuth.js-black?style=for-the-badge&logo=next.js&logoColor=white) ![GitHub API](https://img.shields.io/badge/GitHub_API-181717?style=for-the-badge&logo=github&logoColor=white) |
| **Data & Queue** | ![Prisma](https://img.shields.io/badge/Prisma_6-2D3748?style=for-the-badge&logo=prisma&logoColor=white) ![Neon](https://img.shields.io/badge/Neon_Postgres-00E599?style=for-the-badge&logo=postgresql&logoColor=black) ![Upstash](https://img.shields.io/badge/Upstash_QStash-00E9A3?style=for-the-badge&logo=upstash&logoColor=black) |
| **Quality Gate** | ![Zod](https://img.shields.io/badge/Zod-3068B7?style=for-the-badge&logo=zod&logoColor=white) ![Stryker](https://img.shields.io/badge/Stryker-Mutator-red?style=for-the-badge&logo=stryker&logoColor=white) ![ZenStack](https://img.shields.io/badge/ZenStack-Policy-yellow?style=for-the-badge) |

---

### 🏗 Architecture

The system follows **Feature-Sliced Design (Simplified)** principles for scalability and maintainability.

```mermaid
graph LR
    User((User)) --> NextJS[Next.js App Router]
    NextJS -- tRPC --> Backend
    Backend -- ORM --> NeonDB[(Neon Postgres)]
    Backend -- Async Task --> QStash{Upstash QStash}
    QStash -- Webhook --> Backend
    Backend -- REST/GraphQL --> GithubAPI[GitHub API]
```

### 🚀 Key Features

-   **End-to-End Type Safety**: Complete type safety from database to UI components via **tRPC + Prisma + ZenStack**.
-   **Serverless First**: Zero-maintenance scaling with **Neon** (Postgres) and **Upstash** (Queues).
-   **Async Processing**: Heavy analysis tasks are offloaded to background workers via **QStash** for non-blocking UX.
-   **Enterprise Security**:
    -   🔐 **NextAuth** with GitHub OAuth provider.
    -   🛡️ **ZenStack** for declarative Access Control Policies (RBAC/ABAC).
    -   🧪 **Mutation Testing** ensures high reliability of the test suite.

<div align="center">
  <br>
  <sub>Built with ❤️ by the Doxynix Team.</sub>
</div>
