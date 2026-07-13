---
title: "Candidates Scheduled with Unavailable Interviewers"
url: "https://status.ashbyhq.com/incidents/ns6917dzn3wx"
date: "2026-03-24"
feed_url: "https://status.ashbyhq.com/history.atom"
---
Mar 24 , 15:00 UTC Resolved - Candidates may have scheduled with unavailable interviewers during the following time periods: * Mar 24, 8:21AM - 9:52AM PDT * Mar 25, 9:52AM - Mar 27, 5:34AM PDT At the scheduled time, the interviewer may already have had a meeting. This happened because we shipped a bug that incorrectly calculated or displayed the interviewer’s availability. This bug affected the following scheduling features: * Manual scheduling * Direct booking links * Advanced scheduling We will be posting a post-mortem about how this happened and what we’re doing to prevent this issue in the
