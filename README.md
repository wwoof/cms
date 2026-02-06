# Request for Proposals (RFP)

**Editorial CMS for National WWOOF Organizations**

**Published:** February 2026

**Proposal Deadline:** March 31, 2026

## 1. Project Overview

The Worldwide Opportunities on Organic Farms (WWOOF) is a non-governmental not-for-profit network of local organizations connecting visitors with organic farmers to foster educational and cultural exchange and build a global community mindful of ecological farming. More information is available at [wwoof.net](https://wwoof.net).

The **Federation of WWOOF Organizations** operates a shared technical platform, the **Common WWOOF Platform (CWP)**, which manages member listings, memberships, messaging, reviews, etc. for 25+ national organisations. Examples: [Canada](https://wwoof.ca), [France](https://wwoof.fr), [Korea](https://wwoof.kr).

Alongside the CWP, **national WWOOF organizations** need modern, public-facing editorial websites. These sites communicate values, share news and events, showcase coordinators, and provide an entry point for prospective members and volunteers.

Currently, national organizations use a variety of approaches (custom websites, WordPress, third-party tools), resulting in inconsistent quality, duplicated effort, and fragmented user experience. Examples: [Canada](https://org.wwoof.ca), [France](https://asso.wwoof.fr), [Italy](https://org.wwoof.it), [USA](https://impact.wwoofusa.org/), [Portugal](https://org.wwoof.pt).

We are seeking proposals to build a **shared editorial CMS** that can:

* Power up to 25+ national websites across multiple domains
* Support multilingual content per site
* Offer an easy-to-use editor experience for national coordinators
* Allow multi-site management, enabling super admins to deploy new websites or languages easily
* Expose content via APIs for potential reuse in the CWP (for exampple: showing events created in the CMS inside the CWP)

## 2. Objectives & Goals

The CMS should:

* Clearly represent each national organization and its people
* Fit both small and large organizations, from minimal content to complex editorial needs
* Align visually and structurally with the broader WWOOF ecosystem (see our [visual identity](https://drive.google.com/file/d/1fFN24M7fK2MSsHPYfEXoW7albiWhkpqZ/view?usp=sharing))
* Require minimal ongoing technical involvement from the Federation’s IT team
* Complement, not replace, the CWP — focusing solely on editorial content and public communication

## 3. Scope & Deliverables

### 3.1 MVP Features

The initial version should include:

* **Pages**: static and semi-static pages (About, Projects, Press, Contact, etc.)
* **Blog / News**: consistent structure (titles, text, images)
* **Events**: structured fields with listing pages
* **Content Blocks**: ~15–20 reusable blocks (text+image, calls to action, coordinator list via CWP API, featured hosts, social embeds, document downloads, etc.)
* **Multilingual Support**: per-site languages, with flexible translation workflow
* **Media Uploads**: image and document support for editors
* **Server-Side Rendering**: content must be indexable by search engines

### 3.2 Multi-Site Management

* Super admins must be able to **add/remove new sites** or new language versions easily
* Coordinators should ideally have access **only to their national site**
* Multi-site must be supported **out-of-the-box**, without relying on custom infrastructure

### 3.3 User Types & Access Levels

The CMS is intended to support a small, clearly defined set of user roles. These roles are described here to clarify expectations around access and permissions.

#### Super Admins (Federation)

* A very limited number of users (approximately 2–3 people)
* Employed by the Federation of WWOOF Organizations
* Responsibilities include:
  * Creating and removing sites (national sites and language variants)
  * Managing domains and basic site configuration (shared plugins, global settings, etc.)
  * Granting and revoking access to specific sites for other users
* Super admins require access across all sites

#### Editors / Coordinators (National Organizations)

* Employees or trusted volunteers of national WWOOF organizations
* Typically have access to **one national website only**
* May manage content in one or more languages for that site
* Responsible for:
  * Creating and editing pages, posts, and events
  * Managing editorial content using blocks
* Fine-grained role management is not required for the MVP; simplicity and clarity are preferred

#### Public Users (Visitors)

* No authentication
* Includes members of national organizations and the general public
* Can browse public content and submit information via public forms (e.g. contact forms)

### 3.4 Integrations

* Loose, read-only integration with CWP via APIs
* Optional integrations: newsletters (e.g., Brevo/Mailchimp), webinar tools (e.g., Calendly), donations (Stripe), social media embeds

### 3.4 Technical & Hosting Requirements

* Proposal should include **technology choice recommendations** (WordPress, Craft, Statamic, etc.)
* CMS should allow **self-hosting** on our servers (Kubernetes) or via a cloud provider, owned by the Federation
* Vendor may customize CMS admin interface minimally to simplify editor experience
* Content must be **exposable via APIs**, maintaining separation of content and presentation
* Maintenance plan option is encouraged but not required

### 3.5 Future Considerations (Out of Scope for MVP)

In the future, the CMS may support **limited, unauthenticated content submission** by public users, for example:

* Submitting a marketplace item (e.g. equipment for sale, job offer)
* One-time form-based submissions
* No user accounts
* No ability to edit content after submission
* All submissions require approval by an admin before publication

These features are **explicitly out of scope for the MVP**, but the proposed solution should not make them impossible to implement later.

## 4. Design & User Experience

* Strong emphasis on **mobile-first responsive design**
* [Visual identity](https://drive.google.com/file/d/1fFN24M7fK2MSsHPYfEXoW7albiWhkpqZ/view?usp=sharing) already defined; vendor should focus on:
  * Front-end design and presentation
  * Block design and page templates
  * Navigation consistency **between CMS sites and CWP**
* The existing [editorial website of **WWOOF France**](https://asso.wwoof.fr/) can be used as a reference and starting point for block design and page structures, in order to leverage prior design work and reduce unnecessary redesign efforts
* No need to redesign CMS admin interface beyond minimal usability improvements

## 5. Data Migration (Blog Posts)

Most existing editorial websites used by national WWOOF organizations are built with **WordPress**.

As part of this project, the Federation intends to provide a **limited migration path from WordPress**, with the following scope:

* **Only blog/news posts** will be migrated
* Pages and other content types are **out of scope**
* Migration is **best effort** and aims to preserve historical content, not exact visual fidelity

The selected vendor will be expected to provide a reusable script to migrate WordPress blog posts (text, images when possible, and basic metadata) into the new CMS, along with basic documentation.

## 6. Timeline

| Phase                       | Timeline         | Notes                                   |
| --------------------------- | ---------------- | --------------------------------------- |
| RFP Publication             | Feb 2026         | Public posting                          |
| Proposal Submission         | March 2026       | Deadline: March 31                      |
| Vendor Selection & Contract | April 2026       | Federation review and selection         |
| Design Phase                | May 2026         | UX/UI for front-end and block templates |
| Development                 | Summer–Fall 2026 | MVP build, testing, deployment          |
| Handover / Launch           | End 2026         | CMS live for national sites             |

Vendors may suggest alternative timelines if they believe adjustments are realistic.

## 7. Proposal Requirements

Proposals should include:

1. **Technical Approach**: CMS choice, architecture, multi-site support, API exposure, hosting plan
2. **Design Approach**: front-end templates, blocks, navigation strategy
3. **Project Plan**: phased timeline with milestones (design, development, testing, launch)
4. **Previous Projects**: examples of relevant CMS or web development experience, preferably including multi-site or multilingual projects
5. **Team Composition**: proposed roles and responsibilities (UX/UI, development)
6. **Cost Estimate**: development, optional maintenance, and hosting considerations
7. **Optional Maintenance Plan**: proposals for post-MVP support

## 8. Evaluation Criteria

Proposals will be evaluated on:

* Technical simplicity and maintainability
* Usability for coordinators (non-technical users)
* Cost and efficiency
* Quality of previous design and development work
* Ability to provide both front-end design and development in a single contract
* Proposed technology and hosting approach

## 9. Ownership & Post-Launch

* All intellectual property, code, and content produced for the CMS will belong to the Federation
* CMS must allow Federation IT team to take full ownership post-MVP
* Vendor must provide code in a **GitHub repository under the Federation’s organization**

## 10. Submission Instructions

* Proposals must be submitted [here](https://airtable.com/appPzDblrauasJbUp/pagpPoe9OuYFjsoye/form).
* Format: PDF or Markdown document, including all sections listed above
* Deadline: **March 31, 2026**

Questions about the RFP may be submitted via email to [dev@wwoof.net](mailto:dev@wwoof.net) until **March 15, 2026**.
