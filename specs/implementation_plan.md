# Implementation Plan

## Objective

This document defines how the personal website should be implemented based on the finalized homepage and resume content structures.

The implementation should produce:

- A homepage that follows the editorial direction defined across the homepage specs and reference comparisons.
- A resume page that reflects the existing resume structure clearly and consistently.
- A dedicated projects page linked from the homepage navigation.
- A shared visual system that keeps the site coherent while allowing section-level variation.

## Technology Stack

### Framework

- SvelteKit.

### Styling

- Pure CSS.
- Use SvelteKit and Svelte component structure to combine:
  - global CSS for shared tokens, resets, layout primitives, and reusable patterns
  - component-scoped CSS for section-specific presentation and local overrides

### Data Source Strategy

- Resume data remains the canonical source of truth.
- Homepage content is derived from curated and transformed resume data.
- Resume page content is derived more directly from the resume dataset.

## Implementation Principles

- Keep the homepage editorial and compact, not resume-like.
- Keep the resume page structured and information-dense, but still readable.
- Use readable labels in homepage-facing content instead of raw IDs.
- Preserve internal references in source data, but convert them into presentation-oriented values in the implemented UI.
- Use component boundaries to keep each major section isolated in markup and scoped styling.

## Route Structure

- `/`
  - Homepage.
- `/resume`
  - Resume / CV page.
- `/projects`
  - Dedicated projects archive page.

## Shared Layout and Styling Strategy

### Global CSS Responsibilities

- CSS reset and base typography.
- Color tokens.
- Spacing scale.
- Grid and container rules.
- Shared chip styles.
- Shared button and link styles.
- Shared section spacing.
- Shared logo/icon sizing rules.
- Shared competency marker rules.

### Component-Scoped CSS Responsibilities

- Homepage navbar styling.
- Homepage hero layout and local motion.
- Experience entry layout.
- Project card layout.
- Education section layout.
- Skills section grid and chip behavior.
- Closing contact block layout.
- Resume page section-specific formatting.

## Homepage Implementation

### Homepage Navigation Model

- Brand: `Filipe Vilela` -> `/`
- Navigation:
  - `Projects` -> `/projects`
  - `Resume` -> `/resume`
  - `Contact` -> `/#contact`
- Primary CTA:
  - `Contact` -> `/#contact`

### Homepage Section Order

- Top of Homepage
- About Me
- Experience
- Projects
- Education
- Skills and Languages
- Closing Contact Block

## Homepage Content Structure

### Top of Homepage

#### Navbar

- Brand: `Filipe Vilela`
- Brand link: `/`
- Descriptor: none
- Navigation:
  - `Projects` -> `/projects`
  - `Resume` -> `/resume`
  - `Contact` -> `/#contact`
- Primary CTA:
  - `Contact` -> `/#contact`

#### Hero Section

- Intro line:
  - `Hello, I’m @fpvilela.`
  - `@fpvilela` links to `#about-me`
- Role line:
  - `Full-stack Developer.`
- Motion:
  - role line remains static for now
- Supporting paragraph:
  - `I build practical digital solutions across web applications, workflow automation, and API integrations.`
- Primary CTA:
  - `View projects` -> `/projects`
- Secondary CTA:
  - `Resume` -> `/resume`
- Proof items:
  - `Web systems.`
  - `Workflow automation.`
  - `API integrations.`

### About Me

- Section heading:
  - `About Me`
- Intro paragraph:
  - `I am a Full-stack developer passionate about technology and focused on creating practical digital solutions that solve real operational problems. My work encompasses web systems, workflow, automation, and API integrations.`
- Secondary paragraph:
  - `I like turning requirements into structured implementations, from interface and back-end logic to deployment, documentation, and process automation.`
- Highlights:
  - `Web systems and internal tools.`
  - `Workflow automation and integrations.`
- Ask me block:
  - Label:
    - `Ask me`

### Experience

Each experience item should preserve the existing role-first hierarchy while presenting secondary layers in readable form.

Structure for each experience item:

- Experience title
- Company name
- Company reference
- Company logo
- Employment period
- Short description
- Related roles shown as readable role labels
- Related projects shown as readable project names linking to project anchors when relevant

Entries:

#### Full-stack Developer

- Company name: `ROSH Tecnologia`
- Company reference: `#rosh`
- Company logo: asset placeholder
- Employment period: `03/2026 - 05/2026`
- Short description:
  - `Developed business websites and web systems spanning requirements analysis, front-end implementation, back-end logic, deployment, and WordPress delivery.`
- Related roles:
  - `Full-stack Developer`
  - `Front-end Developer`
  - `Systems Analyst`
  - `Deployment Specialist`
  - `WordPress Developer`
- Related projects:
  - `Connecta Moveis` -> `#connecta-moveis-website`
  - `Traje Fino` -> `#traje-fino-website`
  - `Track Day Landing Page` -> `#track-day-wordpress`

#### n8n Developer

- Company name: `Woont.co`
- Company reference: `#woont`
- Company logo: asset placeholder
- Employment period: `12/2025 - 02/2026`
- Short description:
  - `Built automation and conversational systems with n8n, AI services, APIs, and WhatsApp-based workflows for legal and real estate operational use cases.`
- Related roles:
  - `Workflow Automation Developer`
  - `AI Automation Developer`
  - `Chatbot Developer`
  - `API Integration Specialist`
- Related projects:
  - `Legal Automation` -> `#legal-automation`
  - `Real Estate Multi-Agent System` -> `#real-estate-multi-agent`

#### Personal Projects & Technical Learning

- Company name: `Personal Initiatives and Projects`
- Company reference: `#personal-projects`
- Company logo: asset placeholder
- Employment period: `10/2024 - Present`
- Short description:
  - `Developed personal projects focused on full-stack development, automation, integrations, and technical communication while expanding practical experience across products and learning initiatives.`
- Related roles:
  - `Full-stack Developer`
  - `Front-end Developer`
  - `Workflow Automation Developer`
  - `API Integration Specialist`
- Related projects:
  - `Communit Hub` -> `#communit-hub`
  - `Alerts to WhatsApp Automation` -> `#google-alerts-whatsapp-content-automation`
  - `YouTube Programming Channel` -> `#youtube-channel`

#### Back-end Developer

- Company name: `Seu Visto Certo`
- Company reference: `#vistocerto`
- Company logo: asset placeholder
- Employment period: `12/2023 - 11/2025`
- Short description:
  - `Developed backend automations, document processing workflows, CRM support routines, and technical documentation to improve legal and sales operations.`
- Related roles:
  - `Back-end Developer`
  - `Workflow Automation Developer`
  - `API Integration Specialist`
  - `Document Automation Developer`
  - `CRM Administrator`
  - `Sales Operations Specialist`
  - `CRM Trainer`
  - `Technical Documentation Specialist`
- Related projects:
  - `OneDrive PDF Extractor` -> `#onedrive-pdf-data-extractor`
  - `Sales Info System` -> `#sales-information-management-system`
  - `Lead-to-Deal System` -> `#lead-to-deal-automation`
  - `Pipedrive CRM Docs` -> `#pipedrive-crm-learnig-documentation`

#### Front-end Developer

- Company name: `Vzion Corporation`
- Company reference: `#vzion`
- Company logo: asset placeholder
- Employment period: `01/2023 - 06/2023`
- Short description:
  - `Implemented responsive front-end interfaces for a real estate web platform, covering property browsing and core user-facing pages.`
- Related roles:
  - `Front-end Developer`
- Related projects:
  - `Vilela Properties` -> `#vilela-properties`

### Projects

The homepage should show only the selected featured subset, not the full project archive.

Featured homepage projects:

- `Connecta Moveis`
- `Communit Hub`
- `Real Estate Multi-Agent System`
- `Legal Automation`

Each project item should include:

- Project title
- Project reference
- Year
- Summary
- Bullet points
- Optional links
- Skills shown as readable labels

### Education

This section follows a two-part structure inspired by the chosen homepage direction.

#### Education

- Period or graduation: `2021`
- Institution:
  - `Planalto University Center of the Federal District (Centro Universitario Planalto do Distrito Federal - UNIPLAN)`
- Institution link:
  - `https://www.uniplandf.edu.br/`
- Degree title:
  - `Bachelor in Systems Analysis and Development`
- Supporting note:
  - `Undergraduate degree focused on software, systems, and development foundations.`
- Location:
  - `Brasilia, DF, Brazil`

#### Courses and Certificates

- `CSS - The Complete Guide`
  - Status: `Completed`
  - Provider: `Udemy`
- `JavaScript - The Complete Guide (Beginner + Advanced)`
  - Status: `Completed`
  - Provider: `Udemy`
- `Svelte Tutorial`
  - Status: `Completed`
  - Provider: `Svelte`

### Skills and Languages

This section should show the full skill inventory in grouped form.

Rules:

- Do not show `since-year` on the homepage.
- Show competency through a lightweight marker per skill.
- Show one shared competency legend for the section.
- Use optional logos only for recognizable tools and technologies.
- Keep abstract, operational, or professional skills text-only.

Competency legend:

- `○ Beginner`
- `● Experienced`
- `◆ Advanced`
- `■ Expert`

Skill groups:

- `Development`
- `Database`
- `Automation and Platforms`
- `Integrations`
- `AI and Chatbots`
- `DevOps and Tools`
- `Applied Skills`

Languages subsection:

- `Portuguese: native`
- `English: intermediate`

### Closing Contact Block

This section should follow a hybrid contact direction:

- the lightweight closing rhythm of `santifer.io`
- the explicit labeled contact-action treatment of `zalt.me/contact`

Structure:

- Section heading
- Closing statement
- Contact actions with:
  - label
  - visible value
  - target

Current content:

- Heading:
  - `Let’s connect`
- Closing statement:
  - `Available for web development, automation, and collaboration opportunities.`
- Contact actions:
  - `Email`
    - Value: `fpvilela.dev@gmail.com`
    - Target: `mailto:fpvilela.dev@gmail.com`
  - `LinkedIn`
    - Value: `/in/fpvilela`
    - Target: `https://www.linkedin.com/in/fpvilela/`
  - `GitHub`
    - Value: `github.com/fpvilela`
    - Target: `https://github.com/fpvilela`

## Resume Page Implementation

The resume page should follow the structure already defined in the resume skeleton and derive directly from the resume dataset with minimal editorial compression.

### Resume Page Sections

- Contact Information
- Professional Summary
- Work Experience
- Projects
- Roles
- Skills
- Education
- Publications
- Teachings / Lectures
- Languages
- Companies

### Resume Page Behavior

- Include a download / print control.
- Preserve the denser, reference-oriented character of the resume.
- Keep internal reference fields where they help explain relationships across companies, roles, projects, and skills.

## Projects Page Implementation

The dedicated `/projects` page should hold the full project archive.

Rules:

- The homepage remains curated.
- The projects page contains the broader complete project list.
- Project detail structure should remain consistent with the data shape already used in the homepage and resume contexts.

## Component Planning

### Shared Components

- `SiteHeader`
- `SectionHeading`
- `ActionButton`
- `TagChip`
- `CompetencyLegend`
- `ContactAction`
- `ProjectSkillList`

### Homepage Components

- `HomeNavbar`
- `HomeHero`
- `AboutSection`
- `ExperienceSection`
- `ExperienceEntry`
- `FeaturedProjectsSection`
- `FeaturedProjectCard`
- `EducationSection`
- `SkillsSection`
- `ClosingContactSection`

### Resume Components

- `ResumeHeader`
- `ResumeContactSection`
- `ResumeSummarySection`
- `ResumeExperienceSection`
- `ResumeProjectsSection`
- `ResumeRolesSection`
- `ResumeSkillsSection`
- `ResumeEducationSection`
- `ResumeLanguagesSection`

## Styling Rules for Skills Section

- Use compact chips rather than long descriptive rows.
- Keep competency words out of each item.
- Use one shared legend for the section.
- Keep professional and abstract skills text-only.
- Use logos only where recognition value is strong.
- Ensure the section remains readable on mobile through a one-column stack or responsive wrapped groups.

## Content Mapping Rules

- Homepage content should be derived from the resume dataset, but transformed into concise homepage-oriented copy.
- Resume page content should remain close to the dataset structure.
- Homepage project and skill displays should use readable labels rather than raw IDs.
- Experience-related project links on the homepage may point to homepage project anchors where relevant.

## Implementation Notes

- Keep content in English in the specification and implementation layer.
- Prefer reusable data transformation helpers rather than duplicating display logic in page components.
- Keep CSS architecture simple:
  - global tokens and shared utilities in global styles
  - component-specific styling inside each Svelte component

## Immediate Implementation Readiness

The project now has enough defined structure to begin implementation of:

- homepage layout
- resume page layout
- shared style system
- curated homepage sections
- grouped skills presentation
- labeled contact closing block