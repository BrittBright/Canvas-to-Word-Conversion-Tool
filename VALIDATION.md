# Prototype validation

Validated against the instructor-authorized Canvas course export supplied for this project. Instructor content is not included in this application package.

- Parsed 99 supported items: 28 pages, 49 assignments, 1 discussion, 8 announcements, 3 quizzes, 9 external links, and 1 syllabus.
- Preserved 17 modules and recovered all 20 quiz questions from Canvas's full QTI files, rather than the empty Common Cartridge quiz shells.
- Generated 99 separate student Word documents and a ZIP with module folders, linked files, and a conversion report. The test produced 52 embedded image placements.
- Checked the generated Office XML for well-formedness, title preservation, image embedding, student answer-key exclusion, and extracted instructor answers. A multiple-answer question specifically verifies that negated QTI conditions are not treated as correct answers.
- Checked selection filters, module selection, focus retention, preview sanitization, one-item DOCX download, and full-course ZIP download in an independent DOM environment using the actual application bundles. Invalid exports and unsafe ZIP paths are rejected.
- Rendered and visually inspected representative Word outputs: the 22-image Google Drive guide, a syllabus assignment with a rubric table, and student/instructor versions of the AI quiz. Layout review led to fixes for percentage image widths, keeping quiz choices together, and keeping table rows together.

The DOM tests use Sharp for image decoding because the test environment lacks a usable local browser. Native browser canvas decoding and the live browser interface still require instructor testing. The private hosted site could not be tested through the cloud browser because it requires sign-in. These checks are not an accessibility certification; review Word's Accessibility Checker and the conversion notes before distribution.

Suggested instructor test: export one screenshot-heavy page, one assignment, one discussion, and one quiz; compare each Word file with Canvas, then try a module ZIP. Check question wording, answer choices, image readability/alt text, heading navigation, tables, and the conversion report.
