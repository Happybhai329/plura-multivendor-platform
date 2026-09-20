<div align="center">
  <img src="public/assets/plura-logo.svg" alt="Plura Logo" width="120" height="120" />
  <h1>🚀 Plura — Multi-Vendor SaaS Platform & Funnel Builder</h1>
  <p><strong>An all-in-one agency and subaccount management platform equipped with a drag-and-drop website & funnel builder, Stripe Connect multi-tenant billing, Kanban pipelines, and role-based access control.</strong></p>

  <p>
    <a href="https://plura-multivendor-platform.vercel.app" target="_blank">
      <img src="https://img.shields.io/badge/Live_Demo-plura--multivendor--platform.vercel.app-000000?style=for-the-badge&logo=vercel&logoColor=white" alt="Live Demo" />
    </a>
  </p>

  <p>
    <img src="https://img.shields.io/badge/Next.js_14-000000?style=for-the-badge&logo=nextdotjs&logoColor=white" alt="Next.js" />
    <img src="https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white" alt="TypeScript" />
    <img src="https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white" alt="Tailwind CSS" />
    <img src="https://img.shields.io/badge/Prisma-2D3748?style=for-the-badge&logo=prisma&logoColor=white" alt="Prisma" />
    <img src="https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white" alt="MySQL" />
    <img src="https://img.shields.io/badge/Stripe_Connect-635BFF?style=for-the-badge&logo=stripe&logoColor=white" alt="Stripe" />
    <img src="https://img.shields.io/badge/Clerk_Auth-6C47FF?style=for-the-badge&logo=clerk&logoColor=white" alt="Clerk" />
    <img src="https://img.shields.io/badge/UploadThing-E11D48?style=for-the-badge&logo=icloud&logoColor=white" alt="UploadThing" />
  </p>
</div>

---

## 📖 Overview

**Plura** is an enterprise-grade, multi-tenant B2B2B SaaS solution tailored for digital marketing agencies, freelancers, and software providers. It empowers agencies to host, scale, and manage their clients (**subaccounts**) from a unified command center.

Each subaccount operates within an isolated ecosystem featuring custom website/funnel creation, sales CRM pipelines, media storage, contact tracking, and independent Stripe merchant payment processing.

---

## 🌟 Key Features

### 🏢 Multi-Tenant Agency & Subaccount Hierarchy
- **Agency Management:** Global agency dashboard with real-time revenue stats, client goal tracking, and centralized settings.
- **Isolated Subaccounts:** Create and manage distinct client workspaces with dedicated data segregation, custom branding, and settings.
- **Granular Permissions & Team Control:** Assign role-based permissions (`AGENCY_OWNER`, `AGENCY_ADMIN`, `SUBACCOUNT_USER`, `SUBACCOUNT_GUEST`).
- **Team Invitations:** Seamless team onboarding via Clerk-powered email invitations with token verification and status tracking (`PENDING`, `ACCEPTED`, `REVOKED`).

### 🎨 Visual Drag-and-Drop Website & Funnel Builder
- **Rich Component Library:** Insert containers, sections, 2-column/3-column layouts, custom typography, video embeds, images, contact forms, and Stripe checkout elements.
- **Responsive Previews:** Real-time canvas toggle between Desktop, Tablet, and Mobile device modes.
- **Layers & Hierarchy Tree:** Tree view showing nesting order for intuitive DOM selection.
- **Live Style Inspector:** Deep customization controls for layout, spacing, typography, dimensions, borders, and CSS properties.
- **State Management:** Full Undo / Redo history stack and instant live preview mode.
- **Custom Domains & Subdomains:** Dynamic Next.js route rewriting (`/[domain]/[path]`) for publishing funnels to custom domains or brand subdomains.

### 💳 Stripe Connect & Subscription Billing
- **Marketplace Multi-Vendor Payouts:** Onboard subaccounts to Stripe Connect to enable automated charge routing, vendor commissions, and payouts.
- **Tiered SaaS Subscriptions:** Monetize agency operations through customizable recurring plans (e.g. Starter vs. Unlimited) and premium add-ons.
- **Webhook Automation:** Real-time event handling for product sync, subscription changes, and payment completions (`checkout.session.completed`, `customer.subscription.created/updated/deleted`).

### 📊 Kanban CRM & Sales Pipelines
- **Visual Pipeline Management:** Create and organize multiple sales or fulfillment pipelines per subaccount.
- **Drag-and-Drop Kanban Boards:** Move tickets fluidly across customizable lane stages.
- **Deal Values & Analytics:** Live calculation of pipeline values, win rates, and ticket metrics.
- **Tags & Customer Assignment:** Tag deals, assign designated team members, and link CRM contacts directly to tickets.

### 🗂️ Media Storage & Contact Management
- **Media Asset Library:** Fast, serverless image and file uploads powered by **UploadThing**.
- **Contact Directory:** Automated lead capture from funnel submissions with search and filtering.
- **Activity & Audit Logging:** Detailed notification and audit trail capturing agency and subaccount operations.

---

## 🛠️ Tech Stack

| Category | Technology | Description |
|---|---|---|
| **Framework** | [Next.js 14](https://nextjs.org/) | App Router, Server Components, Turbopack, Edge Middleware |
| **Language** | [TypeScript](https://www.typescriptlang.org/) | Strict type safety and autocompletion |
| **Authentication** | [Clerk](https://clerk.com/) | Authentication, Session Management, and Role-Based Access Control |
| **Database & ORM** | [Prisma](https://www.prisma.io/) + [MySQL](https://www.mysql.com/) | Schema definition, migrations, and type-safe relational database access |
| **Styling & UI** | [Tailwind CSS](https://tailwindcss.com/) + [Shadcn UI](https://ui.shadcn.com/) | Radix UI accessible primitives, customizable theme variables |
| **UI Components** | [Aceternity UI](https://ui.aceternity.com/) | High-performance landing animations (HeroScroll, BackgroundBeams, MovingCards) |
| **Payments** | [Stripe](https://stripe.com/) & [Stripe Connect](https://stripe.com/connect) | Subscriptions, customer portal, and vendor multi-account payouts |
| **File Storage** | [UploadThing](https://uploadthing.com/) | Type-safe file uploads and CDN asset management |
| **Forms & Validation** | [React Hook Form](https://react-hook-form.com/) + [Zod](https://zod.dev/) | Client & server schema validation |
| **Notifications** | [Sonner](https://sonner.emilkowal.ski/) | Beautiful and extensible toast notification system |
| **Deployment** | [Vercel](https://vercel.com/) | Production hosting and CDN distribution |

---

## 📂 Project Structure

```text
plura-multivendor-platform/
├── prisma/
│   └── schema.prisma              # Database schema definitions and relations
├── public/
│   ├── assets/                    # Platform logos, previews, and badges
│   └── stripelogo.png             # Provider brand assets
├── src/
│   ├── app/
│   │   ├── (main)/
│   │   │   ├── agency/            # Agency dashboard, billing, team, settings, launchpad
│   │   │   ├── subaccount/        # Subaccount workspaces (funnels, pipelines, media, contacts)
│   │   │   └── payment-successfull/
│   │   ├── [domain]/              # Custom domain and subdomain routing for published funnels
│   │   ├── api/
│   │   │   ├── stripe/            # Checkout sessions, customer creation, webhooks
│   │   │   └── uploadthing/       # UploadThing file router and core handler
│   │   ├── site/                  # Marketing landing page and pricing section
│   │   ├── globals.css            # Tailwind theme tokens and base styles
│   │   └── layout.tsx             # Root layout with Theme and Modal providers
│   ├── components/
│   │   ├── common/                # BlurPage, InfoBar, CustomModal, FileUpload, ModeToggle
│   │   ├── forms/                 # AgencyDetails, SubAccountDetails, TicketDetails, FunnelForms
│   │   ├── modules/
│   │   │   ├── editor/            # Visual drag-and-drop editor canvas, layers tree, settings tab
│   │   │   ├── funnels/           # Funnel steps, product tables, conversion charts
│   │   │   ├── landing/           # Aceternity landing modules (BackgroundBeams, HeroScroll)
│   │   │   ├── media/             # Media upload cards, gallery, and file picker
│   │   │   └── pipelines/         # Kanban board view, lanes, ticket cards, value metrics
│   │   ├── navigation/            # Collapsible sidebars, agency switchers, nav menus
│   │   ├── providers/             # AuthProvider (Clerk), ThemeProvider, EditorProvider
│   │   └── ui/                    # Shadcn UI primitives (Dialog, Button, Sheet, Table, etc.)
│   ├── config/                    # Pricing tiers, add-ons, editor settings, testimonials
│   ├── hooks/                     # use-editor, use-modal, custom state hooks
│   ├── lib/                       # Prisma client (db.ts), Stripe actions, UploadThing client
│   ├── queries/                   # Reusable Server Actions for Agency, Funnels, Tickets, Contacts
│   └── middleware.ts              # Route protection and multi-tenant domain rewriting
├── components.json                # Shadcn UI CLI configuration
├── next.config.js                 # Image domains, Turbopack, and build settings
├── package.json                   # Dependencies and scripts
└── tailwind.config.ts             # Tailwind color palettes and keyframe animations
```

---

## 📋 Prerequisites

Ensure you have the following installed on your development machine:
- **Node.js**: `>= 18.x` (or **Bun** `>= 1.0`)
- **Package Manager**: `npm`, `pnpm`, or `bun`
- **Database**: A MySQL instance (local MySQL, [PlanetScale](https://planetscale.com/), or [Aiven](https://aiven.io/))
- **Accounts & API Keys**:
  - [Clerk Dashboard](https://clerk.com/) (Authentication)
  - [Stripe Dashboard](https://stripe.com/) (Payments & Stripe Connect)
  - [UploadThing](https://uploadthing.com/) (Media file uploads)

---

## ⚙️ Installation & Local Setup

### 1. Clone the Repository
```bash
git clone https://github.com/Happybhai329/plura-multivendor-platform.git
cd plura-multivendor-platform
```

### 2. Install Dependencies
```bash
# Using npm
npm install

# Or using bun
bun install
```

### 3. Configure Environment Variables
Create a `.env` file in the root directory and configure the variables below:

```env
# -------------------------------------------------------------
# Database (MySQL / PlanetScale / Aiven)
# -------------------------------------------------------------
DATABASE_URL="mysql://username:password@localhost:3306/plura"

# -------------------------------------------------------------
# Clerk Authentication
# -------------------------------------------------------------
NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY=pk_test_...
CLERK_SECRET_KEY=sk_test_...
NEXT_PUBLIC_CLERK_SIGN_IN_URL=/agency/sign-in
NEXT_PUBLIC_CLERK_SIGN_UP_URL=/agency/sign-up
NEXT_PUBLIC_CLERK_AFTER_SIGN_IN_URL=/
NEXT_PUBLIC_CLERK_AFTER_SIGN_UP_URL=/

# -------------------------------------------------------------
# Application & Domain Configuration
# -------------------------------------------------------------
NEXT_PUBLIC_URL=http://localhost:3000
NEXT_PUBLIC_DOMAIN=localhost:3000
NEXT_PUBLIC_SCHEME=http://

# -------------------------------------------------------------
# Stripe Payments & Connect
# -------------------------------------------------------------
NEXT_PUBLIC_STRIPE_PUBLISHABLE_KEY=pk_test_...
STRIPE_SECRET_KEY=sk_test_...
STRIPE_WEBHOOK_SECRET=whsec_...
NEXT_PUBLIC_STRIPE_CLIENT_ID=ca_...

# Stripe Subscription Price IDs
NEXT_PUBLIC_PLATFORM_SUBSCRIPTION_PERCENT=1
NEXT_PUBLIC_PLATFORM_ONETIME_FEE=2
NEXT_PUBLIC_PLATFORM_AGENY_PERCENT=1

# -------------------------------------------------------------
# UploadThing (File & Media Storage)
# -------------------------------------------------------------
UPLOADTHING_SECRET=sk_live_...
UPLOADTHING_APP_ID=...
```

### 4. Initialize Database Schema
Generate the Prisma Client and push the schema to your MySQL database:

```bash
npx prisma generate
npx prisma db push
```

### 5. Start the Development Server
Launch the application with Next.js Turbopack:

```bash
npm run dev
# or
bun dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser.

---

## ⚡ Stripe Webhook Setup (Local Development)

To test Stripe checkout sessions, customer subscriptions, and multi-tenant connect webhooks locally:

1. Install the [Stripe CLI](https://stripe.com/docs/stripe-cli).
2. Authenticate the CLI:
   ```bash
   stripe login
   ```
3. Forward webhook events to your local API endpoint:
   ```bash
   stripe listen --forward-to localhost:3000/api/stripe/webhook
   ```
4. Copy the displayed webhook signing secret (`whsec_...`) and update `STRIPE_WEBHOOK_SECRET` in your `.env` file.

---

## 🚀 Available Scripts

| Command | Description |
|---|---|
| `npm run dev` | Starts the Next.js development server with Turbopack enabled (`--turbo`) |
| `npm run build` | Builds the optimized production application |
| `npm run start` | Starts the compiled production server |
| `npm run lint` | Runs ESLint to inspect code quality and conventions |
| `npm run postinstall` | Automatically executes `prisma generate` upon dependency installation |

---

## 🌐 Deployment

This application is optimized for deployment on the [Vercel Platform](https://vercel.com/):

1. Push your code to a GitHub repository.
2. Import the project into your Vercel Dashboard.
3. Configure the environment variables in Vercel project settings.
4. Set the Root Directory to `./` and framework preset to **Next.js**.
5. Enable Wildcard Subdomains in your DNS if using custom funnel subdomains (`*.yourdomain.com`).
6. Deploy!

A live production deployment is available at: **[plura-multivendor-platform.vercel.app](https://plura-multivendor-platform.vercel.app)**

---

## 🤝 Contributing

Contributions, issues, and feature requests are welcome!

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m "feat: Add some AmazingFeature"`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 📄 License

This project is currently distributed with no explicit open-source license. Please refer to the repository owner for permissions regarding commercial use or redistribution.

---

## 👤 Author

- **GitHub:** [@Happybhai329](https://github.com/Happybhai329)
- **Live Demo:** [plura-multivendor-platform.vercel.app](https://plura-multivendor-platform.vercel.app)
