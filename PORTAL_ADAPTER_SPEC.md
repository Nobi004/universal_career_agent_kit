# Portal Adapter Specification

## Principle

Do not build one brittle browser script that assumes every job portal works the same way. Use a common candidate model and separate platform adapters.

## Adapter capabilities

Each adapter should declare:
- `platform_id`
- `supports_profile_read`
- `supports_profile_write`
- `supports_job_search`
- `supports_application_submission`
- `supports_application_status_read`
- `auth_method`
- `permitted_automation_method`
- `rate_limit`
- `terms_reviewed_at`
- `known_constraints`

Implement only capabilities supported by the platform and its terms. Prefer official APIs or supported integrations. Browser interaction may be used only where permitted and stable.

## Profile field mapping

Map canonical fields to each platform:
- name
- headline/title
- location
- work authorization / eligible countries
- remote preference
- summary/about
- employment history
- education
- skills
- projects/portfolio
- publications
- languages
- salary expectation
- availability
- links/contact

A platform's field may combine or split canonical fields. Preserve provenance and never silently change the underlying fact.

## Platform behavior

- Read the platform's current field limits and validation rules before writing.
- Store a snapshot of the old profile.
- Generate a field-level diff.
- Ask approval before publishing.
- Verify saved values by re-reading the profile.
- Log failures and partial saves.
- Never store passwords or session cookies in project files.
- Do not defeat bot detection or access controls.

## Job source normalization

Treat sources such as We Work Remotely, HiringCafe, Wellfound, YC startup listings, Remotive, Remote OK, company career pages, and Bangladesh-specific job boards as discovery sources, not as proof of eligibility or vacancy validity.

For every listing, independently inspect:
- whether Bangladesh is eligible
- whether “remote” means worldwide or restricted-country remote
- whether hiring is employee, contractor, EOR, or freelance
- whether timezone overlap is required
- whether the employer is real
- whether the vacancy is still open
- whether the application link leads to the employer or a trusted ATS

Do not assume a listing aggregator has current or complete data. Deduplicate by employer + normalized title + canonical URL + location.

## Manual fallback

If an adapter is unsupported, blocked, or unreliable, produce a ready-to-paste profile/application package and precise manual steps. Do not claim the profile was updated or application submitted unless confirmed.
