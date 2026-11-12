# Verse

A static multi-page website for Verse, customisable software for university computing departments and software-related assignment submissions.

[Explore Verse](https://verse-coursework.wryhobby2.chatgpt.site) (private preview)

Serve `dist/` with any static web server. No installation or build step is required. For example, run `python -m http.server 5184 --directory dist`, then open http://localhost:5184. Google Fonts and Three.js 0.160.0 load from CDNs; all other code is inline in each HTML page. If WebGL2 is unavailable, the home page's optical canvas provides a 2D fallback.

## Pages

- `/` — original prism hero, coursework introduction and workspace perspectives
- `/product/` — assignment briefs, submissions and lecturer feedback
- `/how-it-works/` — course setup, hand-in and review workflow
- `/for-departments/` — computing departments and their academic requirements
- `/for-students/` — briefs, file or repository hand-in and feedback
- `/for-lecturers/` — contextual submission review, marks and feedback
- `/customisation/` — university identity, course formats and department rules
- `/faq/` — product, submission and preview questions

Compatibility entry points redirect to the current audience pages.

Directories contain real index.html files, so page refreshes and direct links work on static hosts. Navigation uses site-root paths, so serve the site at the root of its domain. No client-side router or fallback rewrite is required.

The glass prism responds to pointer movement and supports automatic motion, pause/resume, touch, and reduced-motion preferences. It stops rendering when it leaves the viewport. Every page includes an accessible workspace preview with Student, Lecturer and Department views.

The Department view changes university and department names, sample course, accepted submission format, deadline, late-work handling, mark total and group-submission fields. The Student view validates a matriculation number and a source file or repository URL, then generates a local submission preview with replacement history. The Lecturer view accepts a mark and feedback, which become visible in the Student view. Native tabs support arrow-key navigation; Escape closes the dialog.

This is a browser-only demonstration, not a production submission service. File contents are never read or uploaded: the preview uses only names and sizes. Repository links are displayed without fetching them. Student submission details and feedback live in page memory and are cleared on close; configuration resets on refresh. No browser storage, student accounts, backend, code execution or institutional integration is connected. The 10 MB limit is a preview validation rule.

Glass geometry and analytic environment are ported from Vercel's MIT-licensed vercel-labs/vgpu. The copyright and full permission notice are embedded in the HTML.
