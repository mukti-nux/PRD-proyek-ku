# PRD: School Profile Web Service

### TL;DR

Many Indonesian schools lack a modern, credible, and easily managed online presence, limiting their ability to attract new students and communicate effectively with the public. The School Profile Web Service solves this by providing a fully managed, dynamic website featuring a Super Admin dashboard, Supabase backend, and visually appealing Glassmorphism UI. Targeted at Indonesian schools, this service streamlines enrollment (PPDB), enhances reputation, and reduces admin workload.

---

## Goals

### Business Goals

* Increase digital credibility and visibility of client schools by 50% over previous web presence.
* Drive conversions for PPDB (new student enrollment) with Google Form integration, targeting at least 15% click-through from homepage visitors.
* Reduce admin update cycles to under 30 minutes through a centralized content management dashboard.
* Improve organic SEO traffic by 30% in six months through blog/article publishing.
* Enable scalable, multi-school deployment with easy Supabase configuration.

### User Goals

* Allow prospective students and parents to easily explore the school’s profile, teachers, achievements, gallery, events, FAQ, and registration pathways.
* Empower admins to manage all website content, sections, and branding from the Super Admin Dashboard without coding assistance.
* Provide visitors with quick communication pathways (WhatsApp, contact info) and clear CTAs for enrollment.
* Deliver a seamless, great-looking experience on all devices, especially mobile.

### Non-Goals

* This is not a Learning Management System (LMS); it will not offer coursework or grade/report modules.
* Not a student performance/grade portal—no handling of academic data beyond basic profile and achievements.
* Will not include real-time chat support or helpdesk ticketing systems.

---

## User Stories

**Persona 1: Prospective Student/Parent**

* As a prospective parent, I want to view a comprehensive school profile so that I can assess the school’s credibility and fit for my child.
* As a student, I want to browse teacher profiles so that I can get to know the educators.
* As a parent, I want to view the gallery and events so I can see school activities and atmosphere.
* As a student, I want to consult the FAQ so that I can quickly find answers without contacting the school.
* As a parent, I want to register my child easily via the PPDB Google Form so that the admissions process is streamlined.

**Persona 2: School Admin (Super Admin)**

* As an admin, I want to update the school’s vision, mission, and achievements so the site always reflects our strengths.
* As an admin, I want to add, edit, and delete teacher profiles and alumni information for transparency.
* As an admin, I want to rearrange homepage sections dynamically to highlight seasonal content (e.g., PPDB banners during enrollment).
* As an admin, I want to configure global settings (school name, colors, contact info) in one secure dashboard.
* As an admin, I want to input Supabase credentials for quick deployment or migration between schools.

**Persona 3: Casual Visitor**

* As a visitor, I want to read blog articles so I can stay informed about the school and education topics.
* As a visitor, I want to find contact info and location easily to get in touch or visit.
* As a visitor, I want a seamless media experience in the multimedia gallery without slowdowns or awkward layouts.

---

## Functional Requirements

* **Public-Facing Pages (Priority: High)**

  * **School Profile:** Display vision, mission, history, achievements, and alumni—build credibility.
  * **Teacher Database:** List all teachers with relevant bios, photo, and subjects.
  * **Multimedia Gallery:** Photo and video documentation of school activities; supports multiple formats.
  * **Blog / Articles:** CMS-driven publishing of educational content and news with SEO meta features.
  * **School Events:** Calendar or list view of upcoming/past events and agendas.
  * **FAQ:** Accordion or tabbed interface for frequently asked questions.
  * **Contact & Location:** School address, Google Maps embed, WhatsApp integration, phone/email info.
  * **PPDB (Google Form):** Embedded registration form for new students.
  * **Announcement Banner:** Dismissible or persistent banner for urgent/important updates.
  * **Call-to-Action (CTA):** Prominent buttons for “Register Now” and other key actions.

* **Admin Panel (Priority: High)**

  * **Super Admin Dashboard:** Secure login with CRUD operations for all public-facing content.
  * **Dynamic Homepage:** Admin can reorder, hide, or emphasize sections via drag-and-drop or toggles.
  * **Content Management:** Centralized data storage via Supabase; all edits reflected in real time.
  * **Global Settings:** Configure school name/logo, theme colors, contact info, and more.
  * **Supabase Integration:** Allow admin to enter/change Supabase URL and anonymous key for backend connection.

* **Platform & Infrastructure (Priority: Medium)**

  * **Analytics Tracking:** Monitor site visitor behavior, section performance, CTA engagement.
  * **Responsive Design:** Fully mobile-first and cross-device optimized.
  * **Glassmorphism UI:** Cards, galleries, and banners use blur/transparency styling for elegant UX.
  * **Vite Frontend Engine:** Guaranteed fast build, hot reload on changes, optimized deploy-ready bundle.

---

## User Experience

**Entry Point & First-Time User Experience**

* User lands on the Dynamic Homepage, greeted by a visually distinct Announcement Banner and hero CTA (“Register Now”).
* New visitors see concise school highlights; regular visitors benefit from fast load and persistent navigation.
* No explicit onboarding, but key site areas labeled clearly; floating WhatsApp button provides instant help.

**Core Experience**

* **Step 1:** User browses homepage, reviews banners/CTAs and selects an area of interest (e.g., School Profile).
  * Instant transitions; no page reloads unless necessary.
  * Section cards use Glassmorphism, with clear icons/titles.
* **Step 2:** User navigates to Teachers Database, Events, Gallery, or FAQ via menu.
  * Gallery/media use lazy-load and responsive design for mobile.
  * Event and FAQ content is collapsible/expandable—minimizes clutter.
* **Step 3:** User explores Blog/Articles for news/updates.
  * Article pages optimized for SEO with meta tags.
* **Step 4:** User views Contact & Location section. Google Maps and WhatsApp integration appear.
  * Map is touch-optimized; WhatsApp button floats for direct communication.
* **Step 5:** Ready to register, user clicks “Register Now” CTA.
  * Redirect to/iframe of Google Form; auto-scroll if needed for mobile view.
  * Smooth transition away/back to main site.
* **Step 6:** For admin users, login via Super Admin Dashboard.
  * Intuitive sidebar/menu.
  * Edit/add/remove any content (including homepage ordering).
  * See live previews of global setting changes.
  * Enter Supabase URL and anonymous key for backend integration.

**Advanced Features & Edge Cases**

* Admin can toggle Announcement Banner visibility; banners can expire by date.
* Drag-and-drop homepage section ordering with instant preview.
* Multischool deployment: site logic supports fast swapping of Supabase credentials.
* Error handling: user-friendly messages for failed content loads, “Contact support” prompts for fatal errors.
* Gallery gracefully degrades on slow networks; displays thumbnails while media loads.

**UI/UX Highlights**

* Glassmorphism everywhere: soft shadows, blur, and semi-transparent overlays, especially for gallery cards and banners.
* Color contrast accessible by default; admin can select colors in Global Settings previewing with contrast ratios.
* Sticky/floating WhatsApp button on every page for easy parent contact.
* Layout adjusts for all screen sizes—grid breaks into single column on mobile.
* Font sizes, button tap areas, and navigation adhere to accessibility standards.

---

## Narrative

In the heart of an Indonesian city, a school principal recognizes the urgency of improving the school’s digital identity to stay competitive. Her website is a static, outmoded brochure that requires developer intervention for every small update, leaving it outdated by the time prospective parents visit. Frustrated by this bottleneck, she opts for the School Profile Web Service.

Within days, her administrator logs into the intuitive Super Admin Dashboard and updates the school’s vision, mission, and current achievements. They add bios and photos for all teaching staff, building transparency and pride. New galleries from recent school events—sports day, science fair, and graduation—are uploaded in minutes using drag-and-drop features. The admin posts an engaging blog entry about the school’s win at a national science competition, drawing attention from parents and community members searching the web.

As PPDB (new student registration) season begins, the admin activates a prominent Announcement Banner and places a bright “Register Now” call-to-action above the homepage fold. Parents, searching for the best options for their children, discover the school’s new site via Google. They quickly find answers in the FAQ, review credentials and facilities through compelling media, and—convinced—click the CTA to register seamlessly through the integrated Google Form. The school’s standing rises, enrollment increases, and staff are empowered with a truly modern, easy-to-manage digital platform.

---

## Success Metrics

| Success Metric | Target/How Measured |
| --- | --- |
| PPDB Google Form click-through rate | ≥ 15% of homepage visitors (analytics event) |
| Avg. session duration | ≥ 2 minutes (Google Analytics) |
| FAQ engagement rate (accordion opens) | 20% reduction in WhatsApp inquiries |
| PPDB inquiries/registrations YoY | Tracked month-on-month increase |
| Admin content update cycle | < 30 min per cycle (admin logs/feedback survey) |
| SEO organic traffic | +30% in 6 months (Google Search Console) |
| Page load time (mobile) | < 2s, Lighthouse score ≥85 |
| Site uptime | 99.5% quarterly (monitoring platform) |
| Supabase query response | < 300ms (backend monitoring/metrics) |

### Tracking Plan

* CTA “Register Now” button clicks
* Page views per section (Profile, Events, Gallery, FAQ, Blog)
* Gallery photo/video views
* Blog article reads
* WhatsApp button clicks
* FAQ accordion opens/closes
* PPDB form redirect submissions
* Admin login and all CRUD actions

---

## Technical Considerations

### Technical Needs

* **Frontend:** Vite-powered (React or vanilla JS), implements Glassmorphism components and mobile-first layouts.
* **Backend:** Supabase (PostgreSQL) for data; Supabase Storage for photos/videos.
* **Dynamic Routing:** For blog, events, gallery, and content items.
* **Form Integration:** Google Form embedded for PPDB.
* **Maps Integration:** Google Maps embed in contact page.

### Integration Points

* **Supabase:** As central content DB and media store.
* **Google Forms:** For PPDB registration.
* **WhatsApp Business API:** For direct messaging.
* **Google Maps:** Embedded for easy navigation.
* **Analytics:** Google Analytics, Plausible, or similar for tracking and insights.

### Data Storage & Privacy

* Content and user-uploaded media live in Supabase tables/buckets.
* Access via anonymous key (read-only); admin (write/protected) via Row-Level Security (RLS).
* No sensitive student/parent PII stored in platform.
* Only contact inquiries (if any) stored temporarily, then purged per policy.

### Scalability & Performance

* Vite ensures initial page loads <2s; assets delivered via CDN.
* Supabase scales with database and storage growth.
* Mobile-first approach ensures performance even on low bandwidth.
* Browser caching and prefetch for popular sections/articles.

### Potential Challenges

* Exposed Supabase anonymous key—risk minimized via strict RLS on all tables.
* Google Form (PPDB) iFrame responsive design for small screens.
* Drag-and-drop homepage section (admin UI) requires careful design for accessibility and error prevention.
* Handling large media galleries without performance drop.

---

## Milestones & Sequencing

### Project Estimate

* **Medium (3–4 weeks)**

### Team Size & Composition

* **Lean, small team (2–3 people):**
  * 1 Frontend developer (Vite, Glassmorphism UI, dynamic routing)
  * 1 Fullstack/backend (Supabase schema, admin endpoints)
  * 1 Designer (Glassmorphism tokens/components)

### Suggested Phases

**Phase 1: Foundation (Week 1)**

* Key Deliverables: Supabase schema setup (Engineer), Global Settings module (Engineer), Super Admin Dashboard scaffold (Engineer), Vite project initialization (Engineer), Glassmorphism design system (Designer).
* Dependencies: Identification of initial Supabase tables, design tokens, initial admin UX flows.

**Phase 2: Public Pages (Week 2)**

* Key Deliverables: School Profile, Teacher Database, Multimedia Gallery, Blog/Articles, Events, FAQ, Contact & Location sections (Frontend Developer & Designer), PPDB Google Form embed (Engineer).
* Dependencies: Approved designs, finalized Supabase schemas.

**Phase 3: Admin & Dynamic Features (Week 3)**

* Key Deliverables: CRUD for all content areas, homepage section reordering, Announcement Banner management, CTA management, analytics event logging (Frontend & Backend).
* Dependencies: Completed public pages, working Supabase data flows.

**Phase 4: QA & Launch (Week 4)**

* Key Deliverables: Cross-device responsive testing, Lighthouse audits, RLS policy checks (Engineer), content seeding, initial documentation, deployment (Team).
* Dependencies: All core features completed, QA gates passed.

---
