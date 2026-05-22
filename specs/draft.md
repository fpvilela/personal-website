# Current Draft

## Planning Rationale

### Site Direction

- The site follows an interactive resume direction because the project content is built around professional history, projects, skills, education, and contact information, not around selling services in a commercial portfolio format.
- `Home` is the main page because the goal is to concentrate the professional narrative in one guided experience, while `Projects` and `Resume` work as supporting pages.

### Site Pages

- `Home` exists to present the main narrative of the professional journey.
- `Projects` exists because `resume/projects.yaml` already contains a broad and heterogeneous set of projects that would make `Home` too long if everything were shown there.
- `Resume` exists as a separate page because it should remain directly accessible as a formal and practical destination instead of being diluted inside `Home`.

### Navigation

- The main `Navbar` was kept concise with `Home`, `Projects`, `Resume`, and `Contact` because these are the clearest global destinations.
- An auxiliary vertical navigation bar was added only to `Home` because the page now contains several sections and benefits from internal navigation without overloading the main `Navbar`.

### Hero

- `Hero` was kept because every main reference uses a strong introductory area to establish identity, positioning, and the first actions of the experience.
- The three CTAs were chosen to reflect the actual goals of the site:
  - `View Projects` for proof of work.
  - `View Resume` for direct access to the formal resume page.
  - AI conversation for the interactive resume experience.
- The AI CTA was defined as a resume assistant because the goal is not to add a generic chatbot, but a feature that helps visitors explore the professional profile.

### About Me

- `About Me` became a dedicated section right after `Hero` because the site needs a transition between the introduction and the denser professional sections.
- Keeping it separate from `Hero` makes the page architecture clearer and prevents the first screen from carrying too much responsibility at once.

### Experiences

- `Experiences` became the core section of `Home` because the whole site structure depends on it.
- It is the section that connects companies, roles, and projects through the relations already defined in `resume/experiences.yaml`.
- The vertical timeline format was chosen because it matches the chronological nature of the content and aligns well with references such as `brittanychiang.com`, `harshvora.dev`, and `codebyluis.dev`.
- Each item uses the experience title itself, not the company name, because this matches the actual structure of `resume/experiences.yaml` and better reflects the intended reading of the professional journey.

### Roles

- `Roles` became a dedicated section because `resume/roles.yaml` already defines roles as reusable entities with their own descriptions.
- Centralizing role descriptions in a separate section prevents `Experiences` from becoming too long or repetitive.
- This keeps the timeline scannable while still preserving role depth elsewhere in the page.

### Companies

- `Companies` became a dedicated section because companies need to remain navigable as related entities from `Experiences`.
- Without a dedicated section, companies could still appear inside `Experiences`, but they would lose internal navigability as part of the interactive resume logic.
- This decision was made more for structural coherence than for content density alone.

### Projects

- `Projects` became a section in `Home` because projects are the clearest proof of execution for the journey shown in `Experiences`.
- Only selected projects will appear in `Home` because the project inventory in `resume/projects.yaml` is too large and varied to fit the main page without harming readability.
- The dedicated `Projects` page will contain the full list so the site can balance narrative focus and content depth.
- Skills attached to projects will behave as labels or filters because sending users from the `Projects` page back to the `Skills` section in `Home` would create unnecessary context switching.

### Skills

- `Skills` became a dedicated section because it consolidates the technical profile after the visitor has already seen experiences, roles, and projects.
- Showing the competency level for each skill makes sense because `resume/skills.yaml` and `resume/competencies.yaml` already provide that structure.
- A single legend for competency levels was preferred over repeating full explanations for every skill because it is clearer, more professional, and easier to scan.

### Education And Courses

- `Education` became a main section because formal education still plays a validating role in the profile, even with lower volume than experience or projects.
- `Courses` did not become a standalone main section because the current amount of course content is small and better treated as complementary to education.
- This follows the logic seen in references that combine education and certifications or adjacent learning credentials inside the same broader area.

### Contact

- `Contact` became the final section of `Home` because the references support contact as a closing section rather than as a central narrative block.
- It remains a real section, not just a footer detail, because it still needs visibility and deliberate structure.
- Its internal grouping was defined as direct contact and professional presence because the available data in `resume/contact.yaml` naturally splits that way.

## Current `Home` Structure

1. `Hero`
2. `About Me`
3. `Experiences`
4. `Roles`
5. `Companies`
6. `Projects`
7. `Skills`
8. `Education`
9. `Contact`

## Not Addressed Yet

- `Companies` structure.
