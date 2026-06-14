# Ashby GraphQL Schema

## Overview

This conceptual GraphQL schema represents the Ashby all-in-one recruiting and ATS platform API surface. Ashby exposes a JSON-RPC-style REST API at `https://api.ashbyhq.com/` using HTTP Basic authentication with an API key. This schema captures the logical types, relationships, and operations available across candidates, applications, jobs, openings, offers, interviews, hiring teams, surveys, custom fields, and webhooks.

Reference: https://developers.ashbyhq.com/reference

## Schema Source

Derived from Ashby REST API reference documentation. Ashby does not publish a native GraphQL endpoint; this schema is a conceptual translation of the REST surface into GraphQL type definitions for integration mapping and tooling purposes.

## Core Domain Types

### Recruiting Pipeline

- **Job** — A recruiting concept representing a role to fill, with title, department, employment type, status, and lifecycle dates.
- **JobDetails** — Extended job metadata including team assignments, compensation range, and custom field values.
- **JobStatus** — Enum of job lifecycle states: Draft, Open, Paused, Closed, Filled.
- **JobType** — Enum of employment types: FullTime, PartTime, Contract, Temporary, Intern.
- **JobLocation** — Location associated with a job, referencing the location dictionary.
- **JobDepartment** — Department association for a job, referencing the department dictionary.
- **JobOpening** — A headcount slot (requisition line) associated with a job. Multiple openings per job allow parallel-hire tracking.
- **JobOpeningDetails** — Extended opening metadata including target start date, compensation, and custom fields.
- **JobOpeningStatus** — Enum: Open, Filled, Closed, OnHold.
- **JobPost** — A candidate-facing job posting (the public advertisement for a job).
- **JobPostDetails** — Extended posting content including description HTML, apply URL, and careers page configuration.

### Candidates

- **Candidate** — A person in the talent database with name, contact details, social handles, and demographics.
- **CandidateDetails** — Extended candidate record including tags, custom fields, linked applications, and notes.
- **CandidateEmail** — An email address associated with a candidate (primary or secondary).
- **CandidatePhone** — A phone number associated with a candidate.
- **CandidateSource** — The attribution source (job board, referral, sourced, agency) for how a candidate entered the system.

### Applications

- **Application** — A candidate's submission against a specific job, progressing through pipeline stages.
- **ApplicationDetails** — Extended application record including stage history, archive reason, offer reference, and custom fields.
- **ApplicationStatus** — Enum: Active, Archived, Hired, Converted.
- **ApplicationStage** — The current or historical stage of an application within a pipeline.

### Pipeline Stages

- **Stage** — A named step in a hiring pipeline (Recruiter Screen, Technical Interview, Offer, etc.).
- **StageDetails** — Extended stage metadata including order, form definitions, and interview definitions attached.
- **StageType** — Enum: PreScreen, Screen, Assessment, Interview, Offer, Hired.
- **StageMilestone** — A significant pipeline milestone marker (e.g., Active, Offer, Hired) used for reporting.

### Org Structure

- **Department** — An organizational department used to scope jobs and reporting.
- **DepartmentDetails** — Extended department record including parent department, child departments, and headcount.
- **Team** — A sub-unit within a department for finer-grained org structure.
- **User** — An Ashby platform user (recruiter, hiring manager, coordinator, interviewer, or admin).
- **UserDetails** — Extended user record including role assignments, active jobs, and contact info.
- **UserRole** — Enum: OrgAdmin, Recruiter, HiringManager, Interviewer, Coordinator, Sourcer.

### Notes and Activity

- **Note** — A free-text note attached to a candidate or application.
- **NoteDetails** — Extended note record including author, timestamps, and visibility settings.
- **NoteType** — Enum: General, InterviewPrep, ClientFeedback, Internal.
- **Activity** — An audit log event on a candidate or application (stage change, email sent, note added).
- **ActivityType** — Enum: StageChange, EmailSent, NoteAdded, OfferCreated, FeedbackSubmitted, WebhookFired.

### Email and Communication

- **Email** — An email message sent to or from a candidate via the Ashby platform.
- **EmailDetails** — Extended email record including body, attachments, and delivery status.
- **EmailThread** — A threaded conversation grouping related email messages with a candidate.

### Interviews

- **Interview** — An interview definition configured for a job stage (type, duration, interviewers).
- **InterviewDetails** — Extended interview definition with form definitions and instructions.
- **InterviewType** — Enum: Phone, Video, Onsite, Technical, Panel, HiringManager, Cultural.
- **InterviewFeedback** — Scorecard feedback submitted by an interviewer for a candidate interview event.
- **InterviewFeedbackRating** — Enum: StrongNo, No, Mixed, Yes, StrongYes.
- **InterviewSchedule** — A day-of itinerary linking a candidate to a set of time-slotted interview events.

### Offers

- **Offer** — A compensation offer extended to a candidate, with approval workflow and version history.
- **OfferDetails** — Extended offer record including compensation breakdown, equity, start date, and custom fields.
- **OfferStatus** — Enum: Draft, PendingApproval, Approved, Extended, Accepted, Rejected, Rescinded.
- **OfferTemplate** — A reusable offer template defining compensation structure and approval chains.

### Custom Fields and Forms

- **CustomField** — A tenant-defined metadata field attached to candidates, applications, openings, or other resources.
- **CustomFieldType** — Enum: Text, LongText, Number, Boolean, Date, Select, MultiSelect, User, Candidate.
- **Form** — A structured data-collection form (feedback, application, survey).
- **FormField** — A single question or input within a form, with type, label, and options.

### Sourcing

- **Source** — A candidate sourcing channel (e.g., LinkedIn, Indeed, Employee Referral).
- **SourceType** — Enum: JobBoard, Referral, Sourced, Agency, Direct, Other.

### Reporting

- **ReportingField** — A field used in Ashby Analytics reports and dashboards (pipeline metrics, source analytics, EEO).
- **Scorecard** — An aggregated interview scorecard summarizing all feedback for a candidate-application pair.
- **ScorecardRating** — Enum: StrongNo, No, Mixed, Yes, StrongYes.

### Webhooks and Platform

- **Webhook** — A subscription to Ashby platform events delivered to an external endpoint.
- **WebhookEvent** — Enum: CandidateHired, ApplicationCreated, ApplicationStageChange, ApplicationArchived, OfferCreated, OfferApproved, OfferAccepted, InterviewScheduleCreated, SurveySubmitted, JobOpened, JobClosed.
- **APIKey** — An API credential used for HTTP Basic authentication to the Ashby API.
- **Token** — An authentication token or session context for API access.

### Search

- **SearchQuery** — Input parameters for searching candidates, applications, or jobs.
- **SearchResults** — Paginated result set from a search operation.

## GraphQL Operations

### Queries

- `job(id: ID!): Job`
- `jobs(status: JobStatus, departmentId: ID, limit: Int, cursor: String): JobConnection`
- `jobOpening(id: ID!): JobOpening`
- `jobOpenings(jobId: ID, status: JobOpeningStatus, limit: Int, cursor: String): JobOpeningConnection`
- `jobPost(id: ID!): JobPost`
- `jobPosts(jobId: ID, limit: Int, cursor: String): JobPostConnection`
- `candidate(id: ID!): Candidate`
- `candidates(email: String, name: String, limit: Int, cursor: String): CandidateConnection`
- `application(id: ID!): Application`
- `applications(candidateId: ID, jobId: ID, status: ApplicationStatus, limit: Int, cursor: String): ApplicationConnection`
- `stage(id: ID!): Stage`
- `stages(jobId: ID!): [Stage]`
- `department(id: ID!): Department`
- `departments(limit: Int, cursor: String): DepartmentConnection`
- `user(id: ID!): User`
- `users(role: UserRole, limit: Int, cursor: String): UserConnection`
- `interview(id: ID!): Interview`
- `interviews(jobId: ID, stageId: ID): [Interview]`
- `interviewSchedule(id: ID!): InterviewSchedule`
- `interviewFeedback(id: ID!): InterviewFeedback`
- `offer(id: ID!): Offer`
- `offers(applicationId: ID, status: OfferStatus, limit: Int, cursor: String): OfferConnection`
- `customField(id: ID!): CustomField`
- `customFields(objectType: String, limit: Int, cursor: String): CustomFieldConnection`
- `source(id: ID!): Source`
- `sources(limit: Int, cursor: String): SourceConnection`
- `scorecard(applicationId: ID!): Scorecard`
- `webhook(id: ID!): Webhook`
- `webhooks: [Webhook]`
- `searchCandidates(query: SearchQuery!): SearchResults`
- `searchApplications(query: SearchQuery!): SearchResults`
- `searchJobs(query: SearchQuery!): SearchResults`

### Mutations

- `createCandidate(input: CreateCandidateInput!): Candidate`
- `updateCandidate(id: ID!, input: UpdateCandidateInput!): Candidate`
- `createApplication(input: CreateApplicationInput!): Application`
- `updateApplication(id: ID!, input: UpdateApplicationInput!): Application`
- `moveApplicationToStage(applicationId: ID!, stageId: ID!): Application`
- `archiveApplication(applicationId: ID!, archiveReasonId: ID!): Application`
- `reactivateApplication(applicationId: ID!): Application`
- `createNote(input: CreateNoteInput!): Note`
- `createOffer(input: CreateOfferInput!): Offer`
- `updateOffer(id: ID!, input: UpdateOfferInput!): Offer`
- `createInterviewSchedule(input: CreateInterviewScheduleInput!): InterviewSchedule`
- `submitInterviewFeedback(input: SubmitInterviewFeedbackInput!): InterviewFeedback`
- `createWebhook(input: CreateWebhookInput!): Webhook`
- `deleteWebhook(id: ID!): Boolean`

## Authentication

Ashby uses HTTP Basic authentication. The API key is passed as the username with an empty password. All requests target `https://api.ashbyhq.com/`.

## Pagination

List operations use cursor-based pagination with `limit` (default 100, max 500) and `cursor` (opaque string for the next page). Responses include `moreDataAvailable` and `nextCursor` fields.

## Rate Limits

Ashby enforces rate limits per API key. Refer to https://developers.ashbyhq.com/ for current limits.
