# PaySphere AI — Intelligent Employee Payroll & Workforce Management System

An enterprise-grade, full-stack Next.js web application integrating payroll processing, biometric attendance, statutory compliance, performance management, and AI HR automation.

---

## 🛠 Tech Stack

- **Framework**: Next.js 16 (App Router, Turbopack, React 19, TypeScript)
- **Styling**: Tailwind CSS, Lucide Icons, Shadcn UI patterns
- **Database**: SQLite (via Prisma ORM 5.22, production-ready for PostgreSQL / Supabase)
- **Authentication**: JWT-based secure session cookies with Role-Based Access Control (RBAC)
- **Calculations**: Centralized decimal-safe payroll engine (PF, ESI, PT, TDS, LWP)
- **AI / ML Modules**:
  1. **Payroll Anomaly Detection**: Statistical Z-Score / Isolation Forest outlier detection
  2. **Salary Change Explainer**: Grounded differential analysis comparing consecutive cycles
  3. **Payroll Cost Forecasting**: Time-series linear regression with confidence intervals
  4. **AI HR Assistant**: Retrieval-Augmented Generation (RAG) over company policies with source citations

---

## 👥 Demo Personas (Pre-seeded Synthetic Accounts)

| Role | Email | Password | Primary Capabilities |
|---|---|---|---|
| **Super Admin** | `admin@techcorp-demo.com` | `SuperAdmin@123` | Organization settings, payroll pipeline, audit logs |
| **HR Admin** | `geeta.krishnan@techcorp-demo.com` | `HRAdmin@123` | Payroll runs, attendance, leave review, employee profiles |
| **Manager** | `arjun.sharma@techcorp-demo.com` | `Manager@123` | Team approvals, performance reviews, attendance |
| **Employee** | `priya.nair@techcorp-demo.com` | `Employee@123` | Payslip viewer, salary simulator, AI assistant |

---

## 🚀 Getting Started

### 1. Prerequisites
- Node.js 18+ (tested on v24.14.1)
- npm 9+

### 2. Setup & Database Seeding
```bash
# Clone or navigate to the directory
cd paysphere-ai

# Push database schema & populate 50 synthetic employees with 6 months of historical payroll
npm run setup
```

### 3. Run Development Server
```bash
npm run dev
```
Open [http://localhost:3000](http://localhost:3000) in your browser. Use the one-click demo login buttons to authenticate.

### 4. Run Test Suite
```bash
npx ts-node --compiler-options '{"module":"CommonJS"}' tests/payroll-engine.test.ts
```

---

## 📋 Implemented Routes & Capabilities (22 Core Screens)

1. `/login` — Secure sign-in with quick synthetic role selector
2. `/dashboard` — Dual-role workforce analytics & employee self-service hub
3. `/employees` — Searchable employee directory with department filters
4. `/employees/[id]` — Individual profile, compensation structure & statutory records
5. `/payroll` — Payroll register and historical cycle overview
6. `/payroll/run` — 4-stage interactive payroll calculation wizard
7. `/payroll/review` — Isolation Forest anomaly review and exception resolution
8. `/payroll/[id]/payslip` — Printable Indian payslip with AI salary diff explainer
9. `/attendance` — Biometric logs, daily shift tracking, and WFH monitoring
10. `/leave` — Leave approval queue and AI smart leave calendar optimization
11. `/tax` — Old vs New Regime simulator, 80C/80D declarations, and Form 16 workspace
12. `/benefits` — Corporate health insurance, accident cover & nominee records
13. `/financial-wellness` — Interactive What-If salary simulator & savings planner
14. `/ai-assistant` — Grounded RAG conversational assistant with policy citations
15. `/life-events` — Multi-department automated life event checklists (Marriage, Childbirth, etc.)
16. `/performance` — Appraisal reviews, 1-5 ratings, and increment recommendations
17. `/recruitment` — Candidate pipeline tracking and new hire onboarding checklist
18. `/exit` — Notice period tracking and full-and-final settlement estimation
19. `/analytics` — Departmental expenditure breakdown and time-series forecasting
20. `/features` — Complete 40-Dimension Feature Universe catalogue
21. `/settings` — Organization profile and statutory rate parameters
22. `/audit` — Tamper-evident security audit logs and employee data access history
