# Contributing to AVSOPS Organizations Data

Thank you for helping keep veteran service organization data accurate and up-to-date. Every correction helps a veteran find the resources they need.

## Option 1: Report an update or error (easiest)

No technical skills needed. Just fill out a form:

- **[Update an existing organization](../../issues/new?template=update-organization.yml)** — changed address, phone, website, etc.
- **[Add a new organization](../../issues/new?template=add-organization.yml)** — a post or chapter not yet listed
- **[Report incorrect data](../../issues/new?template=report-error.yml)** — something is wrong

We'll review your submission and update the data.

## Option 2: Edit a CSV directly on GitHub

If you're comfortable with spreadsheets:

1. Navigate to the CSV file you want to edit (e.g., `vfw/local-posts.csv`)
2. Click the **pencil icon** (Edit this file) in the top right
3. Find the row for the organization you want to update
4. Make your changes
5. Click **Propose changes** at the bottom
6. Click **Create pull request**

GitHub will create a pull request that we'll review and merge.

## Option 3: Fork and submit a pull request

For bulk updates or programmatic changes:

1. Fork this repository
2. Clone your fork locally
3. Edit the CSV files
4. Commit and push your changes
5. Open a pull request against `main`

## Data guidelines

- **Don't change the column headers** — these are used by our import system
- **State codes** should be 2-letter abbreviations (e.g., `IN`, `CA`, `TX`)
- **geo_tag** format is `{state}_{fips}` (e.g., `in_18097`, `ca_06067`)
- **Boolean fields** (like `hall_rental`, `legion_riders`) should be `true`, `false`, or empty
- **URLs** should include `https://` or `http://`
- **Sort order**: rows are sorted by state, then post number — try to maintain this

## Who can contribute?

Anyone! We especially welcome updates from:

- **Post commanders and adjutants** updating their own listings
- **State DVA staff** with statewide data
- **County Veteran Service Officers** with local knowledge
- **Veterans and family members** who notice outdated info
- **Researchers** working with veteran service data

## Questions?

Open an issue or email ed@avsops.com.
