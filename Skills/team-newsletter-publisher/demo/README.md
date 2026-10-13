# Team Newsletter Publisher — Demo Content

Example output for the [team-newsletter-publisher](../) skill. This folder is for humans browsing GitHub. Do not upload `demo/` to SharePoint Skills.

## What's included

- `sample-files/Team-Newsletter-October-2026-EXAMPLE.html` — the bundled template filled with **fictional example content** (Contoso, "Jordan Example", placeholder hero image)
- `sample-files/Team-Newsletter-October-2026-EXAMPLE.pdf` — the same page printed to PDF

## Setup

1. Open the HTML in a browser to see the finished design.
2. Install the inner package `team-newsletter-publisher/team-newsletter-publisher/` into **Agent Assets → Skills**.
3. Create a Word newsletter from your Team Newsletter template (fields such as IssueMonth, FeaturedTitle, News1_Title …, see `field-mapping.md`) and save it in a document library.
4. Select the .docx and ask Copilot: *"publish the team newsletter"*.

## What to expect

The skill writes `Team-Newsletter-<Month>-<Year>.html` and/or `.pdf` next to the Word file, matching this sample's layout with your content. Empty fields are hidden and sections renumbered.
