# FarmPlay
### Gamified Digital Platform to Encourage Sustainable Farming Practices

**Project stage:** Idea and proposal  
**Project type:** Proposed mobile-friendly web application  
**Purpose:** Encourage farmers to adopt sustainable farming practices through missions, progress tracking, points, community participation, and recognition.

> **Current status:** This repository contains project documentation, proposed architecture, sample data, and planned test cases. The working application, live database, authentication, and integrations have **not yet been implemented**.

## Problem
Farmers may face barriers to adopting sustainable practices, including limited access to practical guidance, difficulty tracking progress, and a lack of engaging ways to learn from peers. FarmPlay proposes a simple, gamified platform that makes sustainable actions easier to discover, practise, and track.

## Proposed solution
FarmPlay will offer:
- **Personalised missions:** Suggested actions based on a farmer's crop, location, and farm size.
- **Progress tracking:** A record of completed missions and earned points.
- **Sustainability score:** An indicative score based on defined mission rules.
- **Community and leaderboard:** Optional peer sharing and recognition.
- **Rewards and recognition:** Badges or rewards for consistent participation.

The first prototype should focus on a small set of sample farmers and missions. Recommendations should be treated as general educational prompts, not a replacement for local agricultural experts.

## Proposed technology stack
- **Frontend:** HTML, CSS, JavaScript
- **Sample data for the first prototype:** Local JSON files
- **Possible backend/database later:** Supabase (authentication and PostgreSQL database)
- **Version control and documentation:** GitHub

The stack is a proposal and may change after the team validates the prototype requirements.

## Repository structure
```text
FarmPlay/
├── README.md
├── TECHNICAL_DESIGN.md
├── TEST_CASES.md
├── LICENSE
└── sample_data/
    ├── farmers.json
    └── missions.json
```

## Setup instructions

### A. View the project documentation
1. Open this repository on GitHub.
2. Read `TECHNICAL_DESIGN.md` for the proposed architecture.
3. Read `TEST_CASES.md` for planned validation scenarios.
4. Open the JSON files in `sample_data/` to review example data.

### B. Check the sample JSON data locally
1. Download or clone the repository.
2. Open the folder in a code editor such as Visual Studio Code.
3. Open `sample_data/farmers.json` and `sample_data/missions.json`.
4. Validate the JSON using your editor or a JSON validator.

No package installation, database, or API key is required to read the documentation and sample data. **There is no runnable application in this repository yet**, so there are no application start commands at this stage.

### C. Future application setup (planned)
When the app and Supabase integration are implemented:
1. Install the tools required by the selected frontend setup.
2. Create a Supabase project only if the team decides to use Supabase.
3. Add the required environment variables to a local `.env` file.
4. Run the application using the commands documented after the app scaffold exists.

Do not copy example variable names into a working application until the corresponding integration has been implemented.

## Environment variables
**Currently required:** None.

If Supabase is adopted in a later implementation, the frontend may need these public project settings:

```env
VITE_SUPABASE_URL=
VITE_SUPABASE_ANON_KEY=
```

These are **future placeholders**, not currently used by this documentation-only repository. Use only a Supabase publishable/anon key intended for client-side use, with appropriate Row Level Security (RLS) policies. **Never put a Supabase service-role key, database password, or other secret in frontend code or commit secrets to GitHub.** A `.env` file should be excluded from version control.

## How the proposed platform works
1. A farmer opens the platform.
2. The farmer views relevant sustainable farming missions.
3. The farmer completes an action and submits it for recording or review.
4. The system records completion and awards points according to defined rules.
5. The dashboard updates progress and the indicative sustainability score.
6. The farmer may compare progress or share learning with the community.

Mission completion and scoring will need clear rules and, where appropriate, verification to reduce false claims.

## Sample data
The `sample_data/` directory contains fictional farmer profiles and example missions for design and testing. The records are illustrative, not real farmer information or agronomic recommendations.

## Testing
Planned scenarios are listed in [`TEST_CASES.md`](TEST_CASES.md). They are test plans, not evidence that a working application has passed tests.

## License
This project is proposed to use the MIT License. See [`LICENSE`](LICENSE). Replace the copyright holder placeholder with the team's chosen name before publishing.

## Roadmap
- [ ] Confirm user needs with farmers and mentors.
- [ ] Create a basic responsive dashboard.
- [ ] Display missions from sample JSON data.
- [ ] Implement mission completion and points in the prototype.
- [ ] Test scoring and invalid inputs.
- [ ] Evaluate whether a backend and authentication are needed.
- [ ] Consider Supabase integration and privacy/security requirements.
- [ ] Pilot the prototype with feedback before making impact claims.

## Project principle
FarmPlay aims to encourage sustainable farming through accessible, practical, and engaging learning. Any impact claims should be based on measured results rather than points alone.
