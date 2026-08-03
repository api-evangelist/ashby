# Ashby (ashby)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Ashby is an all-in-one talent strategy platform combining ATS, sourcing, scheduling, and analytics. The Ashby API exposes candidates, applications, jobs, openings, offers, interviews, hiring teams, surveys, custom fields, and webhooks for recruiting operations teams.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/ashby/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/ashby/refs/heads/main/apis.yml)

## Tags

- HR
- ATS
- Recruiting
- Analytics
- Sourcing
- Scheduling

## Timestamps

- **Created:** 2026-05-08
- **Modified:** 2026-05-19

## APIs

### Ashby Candidates API

Create candidates from external sources, retrieve candidate profiles, manage candidate-level identifiers, social handles, demographics, tags, and custom fields. Candidates exist independently of any single application.

#### Tags

- Candidates
- People

#### Properties

- [Documentation](https://developers.ashbyhq.com/)
- [API Reference](https://developers.ashbyhq.com/reference)
- [OpenAPI](openapi/ashby-api-openapi.json) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/ashby-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/ashby-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Ashby Applications API

Submit applications against jobs, advance applications through stages, reject, archive, withdraw, and reactivate applications across the hiring pipeline.

#### Tags

- Applications
- Pipeline

#### Properties

- [Documentation](https://developers.ashbyhq.com/)
- [OpenAPI](openapi/ashby-api-openapi.json) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/ashby-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/ashby-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Ashby Jobs API

Manage jobs (the recruiting concept) — title, department, employment type, status, and lifecycle — separate from openings (headcount slots).

#### Tags

- Jobs
- Postings

#### Properties

- [Documentation](https://developers.ashbyhq.com/)
- [OpenAPI](openapi/ashby-api-openapi.json) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/ashby-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/ashby-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Ashby Openings API

Manage openings — the headcount slots associated with a job; multiple openings allow tracking parallel hires per requisition.

#### Tags

- Openings
- Headcount

#### Properties

- [Documentation](https://developers.ashbyhq.com/)
- [OpenAPI](openapi/ashby-api-openapi.json) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/ashby-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/ashby-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Ashby Job Postings API

Manage public job postings (the candidate-facing job ads) and the careers-page configuration including title, location, description, and apply URL.

#### Tags

- Job Postings
- Public

#### Properties

- [Documentation](https://developers.ashbyhq.com/)
- [OpenAPI](openapi/ashby-api-openapi.json) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/ashby-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/ashby-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Ashby Offers API

Generate offer drafts, route through approvals, and track offer versions, compensation, and acceptance status.

#### Tags

- Offers
- Approvals

#### Properties

- [Documentation](https://developers.ashbyhq.com/)
- [OpenAPI](openapi/ashby-api-openapi.json) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/ashby-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/ashby-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Ashby Interviews API

Read interview definitions configured per job stage and the per- candidate interview events generated as candidates progress.

#### Tags

- Interviews
- Stages

#### Properties

- [Documentation](https://developers.ashbyhq.com/)
- [OpenAPI](openapi/ashby-api-openapi.json) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/ashby-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/ashby-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Ashby Interview Schedules API

Create and manage interview schedules — the day-of itinerary linking candidates, interviewers, and time slots, including ad-hoc and template-driven schedules.

#### Tags

- Interview Schedules
- Scheduling

#### Properties

- [Documentation](https://developers.ashbyhq.com/)
- [OpenAPI](openapi/ashby-api-openapi.json) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/ashby-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/ashby-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Ashby Feedback API

Read interview feedback and scorecards submitted by interviewers, including ratings, free-text responses, and recommendation values.

#### Tags

- Feedback
- Scorecards

#### Properties

- [Documentation](https://developers.ashbyhq.com/)
- [OpenAPI](openapi/ashby-api-openapi.json) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/ashby-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/ashby-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [OpenAPI](openapi/ashby-assessments-partner-openapi.json) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/ashby-assessments-partner.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/ashby-assessments-partner.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Ashby Feedback Form Definitions API

Read the structured feedback form templates (questions, rating scales, recommendation values) configured for the tenant.

#### Tags

- Feedback Templates
- Forms

#### Properties

- [Documentation](https://developers.ashbyhq.com/)
- [OpenAPI](openapi/ashby-api-openapi.json) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/ashby-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/ashby-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [OpenAPI](openapi/ashby-assessments-partner-openapi.json) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/ashby-assessments-partner.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/ashby-assessments-partner.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Ashby Hiring Team API

Read the hiring-team assignments per job — recruiter, hiring manager, sourcer, coordinator, and interviewer roles.

#### Tags

- Hiring Team
- Roles

#### Properties

- [Documentation](https://developers.ashbyhq.com/)
- [OpenAPI](openapi/ashby-api-openapi.json) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/ashby-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/ashby-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Ashby Archive Reasons API

Read the configured archive reasons used when candidates are rejected, withdrawn, or hired.

#### Tags

- Archive Reasons
- Disposition

#### Properties

- [Documentation](https://developers.ashbyhq.com/)
- [OpenAPI](openapi/ashby-api-openapi.json) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/ashby-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/ashby-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Ashby Sources API

Read the source taxonomy (job board, referral, sourced, agency) attached to candidate applications for sourcing analytics.

#### Tags

- Sources
- Attribution

#### Properties

- [Documentation](https://developers.ashbyhq.com/)
- [OpenAPI](openapi/ashby-api-openapi.json) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/ashby-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/ashby-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Ashby Surveys API

Read survey responses (EEO, candidate experience) submitted alongside applications. PII-isolated for compliance reporting.

#### Tags

- Surveys
- EEO

#### Properties

- [Documentation](https://developers.ashbyhq.com/)
- [OpenAPI](openapi/ashby-api-openapi.json) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/ashby-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/ashby-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Ashby Locations API

Read the location dictionary used to tag jobs, postings, and candidate location preferences.

#### Tags

- Locations
- Offices

#### Properties

- [Documentation](https://developers.ashbyhq.com/)
- [OpenAPI](openapi/ashby-api-openapi.json) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/ashby-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/ashby-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Ashby Departments API

Read the department dictionary used to scope jobs, openings, and reporting.

#### Tags

- Departments
- Org Structure

#### Properties

- [Documentation](https://developers.ashbyhq.com/)
- [OpenAPI](openapi/ashby-api-openapi.json) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/ashby-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/ashby-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Ashby Custom Fields API

Read custom field definitions and values across candidates, applications, openings, and other resources for tenant-specific metadata and reporting.

#### Tags

- Custom Fields
- Metadata

#### Properties

- [Documentation](https://developers.ashbyhq.com/)
- [OpenAPI](openapi/ashby-api-openapi.json) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/ashby-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/ashby-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Ashby Users API

Read Ashby user accounts and their role assignments (Org Admin, Recruiter, Hiring Manager, Interviewer).

#### Tags

- Users
- Permissions

#### Properties

- [Documentation](https://developers.ashbyhq.com/)
- [OpenAPI](openapi/ashby-api-openapi.json) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/ashby-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/ashby-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Ashby Webhooks API

Subscribe to Ashby events (candidateHired, applicationStageChange, offerCreated, interviewScheduleCreated, surveySubmitted) and receive authenticated webhook deliveries.

#### Tags

- Webhooks
- Events

#### Properties

- [Documentation](https://developers.ashbyhq.com/docs/setting-up-webhooks)
- [OpenAPI](openapi/ashby-api-openapi.json) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/ashby-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/ashby-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Ashby Partner Job Feed

Dedicated partner job feed for distributing live postings to job boards and aggregators with consistent metadata.

#### Tags

- Job Feed
- Partners

#### Properties

- [Documentation](https://developers.ashbyhq.com/docs/dedicated-partner-job-feeds)
- [OpenAPI](openapi/ashby-api-openapi.json) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/ashby-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/ashby-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Ashby Careers Page API

Public read-only API for retrieving published jobs and posting content for embedding in custom careers pages.

#### Tags

- Careers Page
- Public

#### Properties

- [Documentation](https://developers.ashbyhq.com/docs/custom-careers-page)
- [OpenAPI](openapi/ashby-api-openapi.json) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/ashby-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/ashby-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [LinkedIn](https://www.linkedin.com/company/ashbyhq)
- [Website](https://www.ashbyhq.com/)
- [Documentation](https://developers.ashbyhq.com/)
- [API Reference](https://developers.ashbyhq.com/reference)
- [Pricing](https://www.ashbyhq.com/pricing)
- [Login](https://app.ashbyhq.com/login)
- [Status Page](https://status.ashbyhq.com/)
- [Blog](https://www.ashbyhq.com/blog)
- [Support](https://www.ashbyhq.com/support)
- [GitHub Organization](https://github.com/ashbyhq)
- [Privacy Policy](https://www.ashbyhq.com/privacy)
- [Terms of Service](https://www.ashbyhq.com/terms)
- [Authentication](https://developers.ashbyhq.com/docs/authentication)
- [Webhooks](https://developers.ashbyhq.com/docs/setting-up-webhooks)
- [Plans](plans/ashby-plans-pricing.yml)
- [Rate Limits](rate-limits/ashby-rate-limits.yml)
- [Fin Ops](finops/ashby-finops.yml)
- [Features](undefined)
- [Integrations](https://www.ashbyhq.com/integrations)
- [L L Ms Txt](https://developers.ashbyhq.com/llms.txt)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
