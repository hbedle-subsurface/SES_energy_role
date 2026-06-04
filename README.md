# What's Your Energy Role?

Developed by [Dr. Heather Bedle](mailto:hbedle@ou.edu)  
Sustainable Energy Systems Certificate Program  
University of Oklahoma — [ou.edu/mcee/ses](https://ou.edu/mcee/ses)

**[Launch the quiz](https://hbedle-subsurface.github.io/SES_energy_role/)**

---

## The short version

Five questions. Five possible results. Zero prerequisites required.

This is a personality quiz — in the tradition of magazine quizzes and internet rabbit holes — but every result comes with a genuine explanation of what the SES Certificate offers someone in that discipline, why the energy transition needs that kind of thinking, and what a realistic career path looks like. The recruitment pitch is real. The personality profiles are also real, if you think about it.

---

## Why this exists

The SES Certificate is open to every major at OU. The challenge is that most non-STEM students assume it isn't for them — because the words "sustainable energy systems" read as an engineering program.

This quiz was built to close that perception gap. It meets students where they are (a phone, a poster QR code, a moment of curiosity) and reflects their own instincts back to them as a legitimate energy future. A political science student who wants to understand regulatory frameworks is not an edge case. A journalism student who wants to cover the energy transition is not a secondary audience. This quiz treats both as the target.

---

## The five roles

- **The Problem Solver** — wants to understand how things work from the inside out; drawn to the technical and modeling dimensions of energy; atmospheric science, engineering, geology, physics, math, CS, environmental science
- **The Storyteller** — translates complexity into public understanding; journalism, PR, English, history, philosophy, film, creative writing, rhetoric
- **The Deal Maker** — makes the economics real; business, finance, accounting, economics, supply chain, entrepreneurship
- **The Rule Writer** — understands that governance is the structural challenge; pre-law, political science, public administration, international studies, history, philosophy, Native American studies
- **The Justice Lens** — keeps the human dimension in the room; sociology, public health, fine arts, education, social work, psychology, anthropology, religious studies, women's & gender studies

Each result includes a personality description written for that specific archetype, a "fits well with" major pill strip, a tailored explanation of what SES offers that student, a scholarship callout, and two neighboring role cards.

---

## Who it's for

Any OU undergraduate — but designed especially to reach students in the humanities, social sciences, journalism, business, pre-law, fine arts, and education who would not otherwise see themselves in the SES program.

Useful for:

- Poster and flyer QR codes across campus
- Advisor and faculty one-pagers ("send your students here")
- Instagram and social media link-in-bio
- Tabling and recruitment events
- Classroom visits in non-STEM departments

---

## How to deploy

This is a single self-contained `index.html` file. No build step, no dependencies, no server required.

1. Fork or clone this repo
2. Enable GitHub Pages under **Settings → Pages → Deploy from branch → main**
3. The quiz will be live at `https://[your-username].github.io/[repo-name]/`

That's it.

---

## How to edit content

All quiz content lives in two clearly labeled JavaScript objects at the top of the `<script>` block in `index.html`. You do not need to touch any layout or styling code to update copy, scores, or result text.

**`QUESTIONS`** — the five quiz questions, each with:
- `eyebrow` — small label above the question (e.g. "Scenario 2")
- `text` — the question itself
- `sub` — optional subtext below the question
- `options[]` — array of answer objects, each with `text` and `scores`

**`RESULTS`** — the five result cards, each with:
- `title` / `badge` / `tagline` — hero copy
- `majors` — comma-separated string of majors, rendered as pill tags
- `description` — the personality read, written for that archetype
- `program` — why SES fits this student specifically
- `scholarship` — scholarship callout copy
- `neighbors[]` — two adjacent result roles with a short note each

Scores use weighted point values across five categories (`stem`, `comm`, `biz`, `policy`, `equity`). Each answer option can award points to one or more categories. The highest total at the end determines the result.

---

## The scholarship callout

Every result card surfaces the undergraduate scholarship program: up to $1,000, paid incrementally at four milestones ($250 each), no GPA minimum, any major, 20 awards available for 2026–27.

Questions to [SES@ou.edu](mailto:SES@ou.edu).

---

## License

[Creative Commons Attribution ShareAlike 4.0 International (CC BY-SA 4.0)](https://creativecommons.org/licenses/by-sa/4.0/)

Free to share and adapt with attribution and the same license on derivatives.
