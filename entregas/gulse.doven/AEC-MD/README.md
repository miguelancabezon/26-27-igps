# EstateGate 🏠

**Reliable listings. The right address.**

![Status](https://img.shields.io/badge/status-in_development-orange)
![TypeScript](https://img.shields.io/badge/built_with-TypeScript-3178C6)

![House illustration](https://raw.githubusercontent.com/microsoft/fluentui-emoji/main/assets/House/3D/house_3d.png)

*Illustration: [Microsoft Fluent Emoji](https://github.com/microsoft/fluentui-emoji), licensed under [MIT](https://github.com/microsoft/fluentui-emoji/blob/main/LICENSE).*

## Project Overview

**EstateGate** is a real estate web platform where verified real estate agencies can publish property listings. It helps people explore properties and contact verified agencies through a clear, accessible interface.

Its main objective is to improve trust in online property searches by checking agency documentation before granting publishing access. Visitors can browse listings, while registered users can save properties. Agency representatives manage their listings, and administrators handle verification and moderation.

EstateGate is a fictional project created for this Markdown documentation activity, inspired by my interest in real estate platforms. The features, development status and configuration below describe an imagined prototype.

## Table of Contents

- [Project Overview](#project-overview)
- [Main Features](#main-features)
  - [Development Status](#development-status)
- [Installation and Configuration](#installation-and-configuration)
- [Technologies Used](#technologies-used)
- [Architecture and Functionality](#architecture-and-functionality)
- [Usage Examples](#usage-examples)
  - [Example 1: Finding a Property](#example-1-finding-a-property)
  - [Example 2: Publishing a Listing](#example-2-publishing-a-listing)
- [Additional Information](#additional-information)
- [Contact](#contact)

---

## Main Features

- **Agency verification**
  - Agencies submit business and tax registration documents.
  - Administrators review the documents before enabling publishing access.
- **Property listing management**
  - Authorized agencies create, edit and remove listings.
  - Property descriptions, prices and photo galleries help users compare options.
- **Property search**
  - Visitors filter listings by criteria such as location, price and property type.
  - Sorting helps users navigate results.
- **Saved properties**
  - Registered users add interesting listings to their favorites.
- **Moderation and reporting**
  - Users report suspicious or inappropriate listings.
  - Administrators review reports and manage listing visibility.
- **Account protection**
  - Role-based permissions separate visitor, user, agency and administrator access.
  - Multi-factor authentication protects privileged operations.

### Development Status

The following checklist represents the development roadmap of the fictional prototype. Checked items indicate features considered complete within this project scenario.

- [x] Listing creation, editing and removal.
- [x] Public listing details and photo galleries.
- [x] Search, filtering and sorting.
- [x] Favorites.
- [x] Agency verification and moderation workflows.
- [x] Role-based access and multi-factor authentication mechanisms.
- [ ] Complete email address verification.
- [ ] Finalize production email and SMS provider integration.
- [ ] Complete independent security testing before public release.
- [ ] Add property video support.

## Installation and Configuration

The following steps illustrate how the fictional project would be installed. The repository URL, environment values and npm scripts are examples; this assignment contains documentation rather than executable application code.

1. Install **Node.js 22.x** and **Docker Compose v2**.
2. Clone the example repository and open the project directory:

   ```bash
   # Example URL: replace with the project repository when available
   git clone https://github.com/example/estategate.git
   cd estategate
   ```

3. Install backend and frontend dependencies:

   ```bash
   npm install
   cd frontend
   npm install
   cd ..
   ```

4. Create a `.env` file in the project root. The example configuration assumes PostgreSQL is exposed on port `5432` and Redis on port `6379`:

   ```dotenv
   NODE_ENV=development
   PORT=3000
   DATABASE_URL=postgresql://estategate:example_password@localhost:5432/estategate
   REDIS_URL=redis://localhost:6379
   ```

   The imagined `compose.yml` uses the same development database name and credentials. Real passwords must never be committed to Git.

5. Start the PostgreSQL and Redis services defined in the project's example deployment design:

   ```bash
   docker compose up -d postgres redis
   ```

6. Apply database migrations and start the backend:

   ```bash
   npx prisma migrate dev
   npm run start:dev
   ```

7. Open a second terminal and start the frontend:

   ```bash
   cd frontend
   npm run dev -- --port 3001
   ```

   In this scenario, the frontend is available at `http://localhost:3001` and the backend at `http://localhost:3000`. The frontend configuration points to that backend address. Upload storage and scanning would require additional service configuration before deployment.

## Technologies Used

These are proposed major versions for the fictional prototype, not claims about an existing repository or the latest available releases.

| Technology | Version | Description | Project Usage |
|:-----------|:-------:|:------------|:--------------|
| **Node.js** | `22.x` | JavaScript runtime | Runs the backend and development tools. |
| **NestJS** | `11.x` | Backend framework | Organizes authentication, listings and administration modules. |
| **Next.js** | `15.x` | React web framework | Provides property browsing and account interfaces. |
| **TypeScript** | `5.x` | Typed JavaScript | Supports structured frontend and backend development. |
| **Prisma** | `6.x` | Database toolkit | Defines models, queries and database migrations. |
| **PostgreSQL** | `16.x` | Relational database | Stores accounts, agencies, properties and verification records. |
| **Redis** | `7.x` | In-memory data store | Supports request rate limiting. |

## Architecture and Functionality

In the proposed architecture, the **Next.js frontend** communicates with the **NestJS backend**. The backend checks authentication and permissions before accessing PostgreSQL through Prisma. Redis supports request limiting, while uploaded documents and media use private object storage. Upload scanning is part of the security design and would help detect unsafe files.

Only verified agencies can publish listings. This simple flowchart shows how an agency adds a property:

```mermaid
flowchart TD
    A[Agency signs in] --> B[Enter property details]
    B --> C[Add photos]
    C --> D{Required details complete?}
    D -->|No| B
    D -->|Yes| E[Publish listing]
    E --> F[Users view the property]
```

A verified agency status checks publishing eligibility; it does not guarantee that every statement in a listing is accurate. Moderation and reporting remain necessary.

## Usage Examples

The JSON examples below illustrate the information used in the fictional application. They describe sample data rather than a public API contract.

### Example 1: Finding a Property

1. Open the property search page.
2. Select a location and an apartment property type.
3. Enter a maximum price and review the results.
4. Open a listing and save it to favorites after signing in.

Example search preferences:

```json
{
  "location": "Selected area",
  "propertyType": "apartment",
  "transactionType": "rent",
  "maximumPrice": 1200,
  "currency": "EUR"
}
```

The frontend sends the selected criteria to the backend, which returns matching public listings.

### Example 2: Publishing a Listing

1. Sign in as a verified agency representative.
2. Create a listing with a title, description, price and property details.
3. Add property photographs.
4. Submit the listing and correct any validation errors.

Example listing information:

```json
{
  "title": "Bright two-bedroom apartment",
  "description": "Apartment with a balcony and nearby public transport.",
  "propertyType": "apartment",
  "transactionType": "sale",
  "price": 185000,
  "currency": "EUR",
  "bedrooms": 2
}
```

Publishing permission is checked by the backend. Hiding a button in the interface alone is insufficient to restrict access.

Related documentation:

- [Next.js documentation](https://nextjs.org/docs)
- [NestJS documentation](https://docs.nestjs.com/)
- [Prisma documentation](https://www.prisma.io/docs)
- [Mermaid flowchart syntax](https://mermaid.js.org/syntax/flowchart.html)

---

## Additional Information

> **Recommendation:** Keep agency verification documents private and review the property's details before contacting an agency. Never include real passwords or personal documents in public documentation.

<details>
<summary>Security design and remaining release work</summary>

The security design includes separate user roles, privileged account MFA, private document storage and short-lived access links. Administrative operations require appropriate permissions.

The proposed protections include request rate limiting, upload scanning, audit logging and encrypted backups. Production readiness also depends on completing email verification, configuring real messaging providers and carrying out security testing.

This README uses illustrative property data and an example contact address. It does not expose real customer records or private verification documents.

</details>

<!-- Fictional project documentation prepared for the AEC-MD activity. -->

### Markdown Formatting Example

Escaping Markdown characters displays them literally: \*verified agency\* and \#property.

Without escaping, *verified agency* is italic text. Technical identifiers such as `DATABASE_URL` use inline code.

## Contact

**Project author:** Gülse Döven

- Example email: [contact@estategate.example](mailto:contact@estategate.example)
- Academic context: [Universidad Europea del Atlántico](https://www.uneatlantico.es/)

*The email address is a documentation example and is not an active support channel.*

