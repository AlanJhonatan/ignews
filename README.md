# 📰 ig.news

> A dynamic subscription-based news platform showcasing advanced full-stack development, secure payment integration, and modern content delivery.

<p align="center">
  <img src="./public/images/logo.svg" alt="ig.news" width="200" />
</p>

---

## 🚧 Project Evolution & Modernization

> [!IMPORTANT]
> This project is undergoing active modernization. Initially developed with Next.js 12 and FaunaDB, I am strategically updating its core dependencies to align with contemporary best practices while preserving the established architecture.

### 🗺️ Modernization Roadmap

| Layer | Current (Legacy) | Target (Modernization) |
| :--- | :--- | :--- |
| **Framework** | Next.js 12 (Pages Router) | **Next.js 15 (Pages Router)** |
| **Database** | FaunaDB (NoSQL) | **Neon / Planetscale (SQL)** |
| **Auth** | NextAuth.js v3 | **Auth.js v5 (Beta)** |
| **CMS Client** | Prismic v5 | **Prismic v7** |
| **Styles** | Sass Modules | **Tailwind CSS / Vanilla CSS** |

---

## 🚀 Key Accomplishments & Features (Current v1.0)

This project demonstrates the ability to:

-   **Architect and develop a scalable SaaS platform** with subscription-based content access using **Stripe**.
-   **Design and implement robust backend APIs** for authentication, billing, and access control, leveraging **Next.js API Routes**.
-   **Integrate real-time webhook-based workflows** to automate subscription lifecycle events (e.g., `checkout.session.completed`, `customer.subscription.updated`).
-   **Implement secure user authentication** using **NextAuth.js** with GitHub OAuth.
-   **Manage dynamic content effectively** through **Prismic CMS**, utilizing its API for articles and previews.
-   **Optimize front-end performance** with **Next.js's Static Site Generation (SSG)** for improved load times and **Server-Side Rendering (SSR)** for dynamic content.

## 🛠 Current Tech Stack

![Next.js 12](https://img.shields.io/badge/Next.js%2012-000000?style=for-the-badge&logo=nextdotjs&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![FaunaDB](https://img.shields.io/badge/FaunaDB%20(Legacy)-3A1FB1?style=for-the-badge&logo=fauna&logoColor=white)
![Stripe](https://img.shields.io/badge/Stripe-635BFF?style=for-the-badge&logo=stripe&logoColor=white)
![Prismic](https://img.shields.io/badge/Prismic%20v5-484A91?style=for-the-badge&logo=prismic&logoColor=white)

## 📐 Why the Modernization?

*   **FaunaDB ➔ Neon/Planetscale:** Transitioning to modern serverless SQL databases like Neon or Planetscale offers enhanced relational data modeling capabilities and broader ecosystem tooling, moving away from FaunaDB's NoSQL limitations.
*   **Next.js 12 ➔ 15 (Pages Router):** Upgrading Next.js ensures access to the latest performance improvements, security patches, and developer features while strategically maintaining the Pages Router to minimize refactoring efforts during this critical update.
*   **NextAuth v3 ➔ Auth.js v5:** Adopting the newest Auth.js standards provides better TypeScript support, improved security, and enhanced compatibility with the evolving Next.js ecosystem.
*   **Prismic v5 ➔ v7:** Upgrading the Prismic client ensures compatibility with the latest API features and performance optimizations provided by the CMS.

---

### **How to Run (Legacy Version)**

1.  **Clone & Install:** `yarn install`
2.  **Environment Variables:** Setup `.env.local` based on `.env.example`.
3.  **Run Development:** `yarn dev`
