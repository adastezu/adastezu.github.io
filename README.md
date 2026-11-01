# Avinandan Das — academic website

A lightweight academic website inspired by the supplied reference screenshot: serif typography, purple links, a grey navigation bar, and a photograph to the right of the biography.

## View the downloaded website

Extract the ZIP and open `dist/index.html` in a browser. No installation is
needed. Keep the `dist/` folder and its contents together so that the pages can
find the stylesheet and photographs.

For a local server, run `python3 -m http.server 8000 --directory dist` from this
folder and visit `http://localhost:8000`.

## Editing

- `build.py` now has a contents list, numbered section headings, comments, and
  consistent indentation. Read `BUILD_GUIDE.md` for a detailed explanation.
- Edit the biography, photograph markup, and news in **section 4**,
  `HOME_CONTENT`. The homepage was previously written directly inside a
  `page('index', ...)` call.
- Edit `RESEARCH_OVERVIEW` at the start of **section 4** to update the research
  summary on the Home page. It contains the opening two
  paragraphs of the research statement and retains the earlier parameterized
  and exact graph algorithms work.
- Edit `PUBLICATIONS` in **section 5** to add or update papers. Each paper has
  named fields rather than one long tuple.
- Edit `CONFERENCE_TALKS` and `SEMINAR_TALKS` in **section 6.2** to add talks or
  recordings. Each entry has a `links` list; recording links appear beside the
  relevant presentation.
- Edit experience, teaching, and contact text in **section 7**.
- Run `python3 build.py` to regenerate the five HTML pages in `dist/`.
- Edit `dist/style.css` to change the appearance.
- The original photograph is in `dist/assets/avinandan-das.jpg`. It is displayed using CSS; the source image is unchanged.

The site uses no client-side JavaScript or third-party font, analytics, or framework dependencies. All navigation and email links work with plain HTML. The `dist/` directory can also be hosted on another static website provider.

Each build replaces the five generated HTML files. Make content changes in
`build.py` to retain them across builds. The script does not overwrite CSS or
assets. Rebuilding your local copy does not automatically publish it.

## Hosting elsewhere

Upload the contents of `dist/` to a static website host, with `index.html` at the
root. If the website address changes, update `ORIGIN` in section 2 of `build.py`
and rebuild to refresh social preview metadata. Only files in `dist/` are needed
by the host; Python runs on your computer when you generate those files.

## Content provenance

Content was checked on 22 October 2026 against the existing website, Aalto profile, the Distributed Algorithms group's publication list, and the linked papers:

- https://sites.google.com/view/avinandan/home
- https://sites.google.com/view/avinandan/publications
- https://www.aalto.fi/en/people/avinandan-das
- https://research.cs.aalto.fi/da/
- https://dblp.org/pid/182/1881.html

Teaching contributions and thesis details also use information supplied by the owner in conversation. The full thesis title was corrected on 30 October 2026 against the DBLP thesis record (https://dblp.org/rec/phd/hal/Das24) and the Inria PIRAT 2024 activity report (https://radar.inria.fr/rapportsactivite/RA2024/pirat/PIRAT-RA-2024.pdf). It is set once as `THESIS_TITLE` in section 2 of `build.py` and used on both Home and Experience pages. Paper links are attached directly to each publication. The source website's photo credit to Sayan Mukherjee is retained. This version contains no private administrative, application, financial, or personal-health information.

The original CV link was not included because it could not be verified as publicly accessible during preparation.

The research overview on the Home page uses the opening two
paragraphs of the research statement supplied by the owner on 31 October 2026.
It also mentions the earlier work in parameterized and exact graph algorithms.
All earlier publications remain listed on the Research page.

## Talk records

The Talks section was added on 31 October 2026. The owner confirmed the five
conference presentations, the IRIF and Aalto seminars, and the LaBRI streaming
certification talk. Their earlier statement identifies the PODC presentation as
*Is a LOCAL Algorithm Computable?*; the other coauthored brief announcement is
not listed as a personal presentation.

- IRIF lists four PhD/non-permanent-member seminar entries: 26 May 2021,
  2 June 2022, 7 April 2023, and 24 October 2024:
  https://www.irif.fr/seminaires/doctorants/index
- The Aalto/Helsinki CS Theory Seminar lists the talk on 12 February 2025:
  https://research.cs.aalto.fi/theory/seminar/seminar.html
- The official WG 2021 YouTube recording explicitly names Avinandan as the
  presenter: https://www.youtube.com/watch?v=bIQSN35Gixs
- IWOCA's programme and slides confirm the title and 10 June 2020 date:
  https://iwoca2020.labri.fr/program/
- PODC's programme lists the local computability brief announcement:
  https://icalppodcspaa2026.cs.rhul.ac.uk/program/

The LaBRI announcement supplied by the owner confirms 26 September 2025 and
the title *Semi-Streaming Algorithms for Graph Property Certification*. Only
the talk's title, date, and institution are used on the website. The owner's
IWOCA Google Drive recording link is pending; the public slides link is included.
