# Learning Designer — Demo Content

Sample files for the [learning-designer](../) skill. This folder is for humans browsing GitHub. Do not upload `demo/` to SharePoint Skills.

## What's included

- `sample-files/learning-request-brief-template.docx` — the Learning Request Brief Word template with `{Field}` placeholders, for creating the Structured Document Generation form
- `sample-files/sample-learning-request-brief-custom-skills-powerpoint.docx` — a filled sample brief for the topic "Custom Skills in PowerPoint"

## Setup

1. Upload `learning-request-brief-template.docx` to a SharePoint document library and create a Document generation form from it.
2. Install the inner package `learning-designer/learning-designer/` into **Agent Assets → Skills**.
3. Submit the form, or upload the filled sample brief to the library.
4. Optionally, add an image named exactly `learning-visual.png` (or `learning-visual.jpg`) in the same folder as the brief.
5. Select the brief and ask Copilot: *"build the learning dashboard from this brief"*.

## What to expect

The skill produces one self-contained HTML learning dashboard that follows the layout of `learning-designer/references/test-output-custom-skills.html` (the bundled reference for the same topic), with the content of your brief and up to 3 stages.

## Verification cases

- Use a non-PowerPoint topic, such as team onboarding. Confirm that headings, cards, checks, images and footer use only the new brief's content; no sample-topic text should remain.
- Supply only Stage 1, leaving the Stage 2 and Stage 3 sets blank. Expect Overview plus one stage tab, one path tile, and no navigation to missing stages. Repeat with two and three complete stages.
- Leave a required field blank, supply an incomplete stage, or supply Stage 3 without Stage 2. Expect a request to correct the brief, not an invented stage or a partially generated dashboard.
- Test tabs by mouse and arrow keys, next-step buttons, and flip cards by hover and keyboard focus. In the reference button quizzes, correct and incorrect choices should show topic-neutral feedback.
