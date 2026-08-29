# Wander AI Studio --- Project Handoff

## Purpose of this document

This document transfers the **Wander AI Studio** project from a ChatGPT
conversation held in Wander's institutional/school account to his
**personal ChatGPT account**, where development should continue.

**Important:** this is a personal project. It is **not an Escola Eleva
project** and is **not intended for Wander's school students**. It is
being developed independently for Wander's **private English students**.

The new ChatGPT/Codex conversation should treat this document as the
authoritative project handoff. Do not restart discovery from zero,
redesign the project without reason, or confuse it with Wander's
school/IPC/Language Arts work.

------------------------------------------------------------------------

# 1. The original problem

The project began with a simple problem:

Wander uses several AI platforms for different purposes and finds it
confusing and inefficient to move constantly among tools, materials,
apps, files, activities and student information.

The idea evolved into something much more useful than a dashboard of AI
links:

> Build one dynamic web application where Wander can manage his private
> students, their learning materials, activities, media, progress and
> AI-assisted content creation.

The goal is consolidation.

Wander has already built many individual educational apps and resources
with AI assistance. Instead of continuing to create disconnected apps,
he wants one persistent system that can contain and manage them.

------------------------------------------------------------------------

# 2. Product vision

**Wander AI Studio** should become a personal AI-powered learning
platform for Wander's private English students.

It should eventually provide:

-   one teacher/admin dashboard for Wander;
-   an individual dashboard for every student;
-   student profiles with level, books and learning materials;
-   persistent learning history;
-   lessons and learning resources;
-   video;
-   audio/listening activities;
-   interactive exercises;
-   tests generated or assembled inside the platform;
-   automatic correction where appropriate;
-   opportunities for students to correct mistakes and try again;
-   error reports for students;
-   more detailed performance/error reports for Wander;
-   progress tracking;
-   notifications to Wander when a student submits work;
-   email notifications;
-   management of students and materials;
-   reusable content and activities;
-   AI-assisted creation from inside the application;
-   the ability for the system to use the student's level, materials and
    history when helping Wander create something.

This is closer to a **personal AI-powered LMS / teaching studio** than a
conventional link dashboard.

------------------------------------------------------------------------

# 3. Core user roles

## Teacher / Administrator

Wander should have one central dashboard from which he can:

-   add, edit and deactivate students;
-   open any student's dashboard/profile;
-   assign books and materials;
-   see current units/topics;
-   create and assign activities;
-   upload or organize media;
-   review submissions;
-   see recurring errors;
-   see progress;
-   generate reports;
-   receive submission notifications;
-   create/adapt materials using AI;
-   manage the overall platform.

## Student

Each student should eventually have a private account/dashboard
containing only their own learning environment.

Possible areas:

-   My Course
-   Lessons
-   Videos
-   Listening
-   Reading
-   Practice
-   Tests
-   Corrections
-   Feedback
-   Progress

Students should not have access to other students' data.

------------------------------------------------------------------------

# 4. Learning cycle

A central product idea is:

``` text
Learn
  ↓
Practice
  ↓
Submit
  ↓
Analyze
  ↓
Understand errors
  ↓
Try again
  ↓
Personalized revision
  ↓
Progress
```

The application should eventually do more than record grades.

It should help identify patterns in student performance.

Example:

``` text
Student: Maria

Recurring issues

Past Simple
• irregular verb forms
• 7 errors in the last 4 activities

Listening
• understands gist well
• difficulty identifying numbers

Vocabulary
• travel vocabulary improving

Suggested next step
Short irregular-verbs revision before the next lesson
```

The student-facing feedback should be simpler and encouraging, while
Wander's teacher report can contain more pedagogical detail.

------------------------------------------------------------------------

# 5. Student memory

"Memory" should not depend only on ChatGPT conversation memory.

The application itself should maintain structured, persistent student
information in its database.

Examples:

-   name;
-   account;
-   age or age group where relevant;
-   English level;
-   course/book;
-   current unit;
-   topics studied;
-   assigned materials;
-   completed activities;
-   answers;
-   attempts;
-   errors;
-   feedback;
-   recurring difficulties;
-   strengths;
-   test results;
-   progress;
-   teacher notes;
-   AI-generated recommendations.

This structured history should later be usable as context for
AI-assisted creation.

------------------------------------------------------------------------

# 6. AI Creator vision

A major future feature is an AI creation area inside Wander's teacher
dashboard.

Example request:

> Create a 20-minute revision activity for João using Units 5 and 6 of
> his book. Focus on past simple and travel vocabulary. He has
> difficulty with irregular verbs.

The system should eventually be able to combine:

-   the student's profile;
-   English level;
-   assigned book/material;
-   current unit;
-   previous performance;
-   recurring errors;
-   Wander's request;

and produce an appropriate resource.

Potential creation types include:

-   lesson;
-   exercise;
-   homework;
-   revision;
-   quiz;
-   test;
-   listening activity;
-   reading activity;
-   vocabulary practice;
-   grammar practice;
-   visual review;
-   diagram;
-   image;
-   printable material.

This is a long-term feature. Do not attempt to build all of it in the
first sprint.

------------------------------------------------------------------------

# 7. Media and activity model

Lessons/materials may eventually contain blocks such as:

``` text
WATCH
Video

LISTEN
Audio + questions

READ
Text

PRACTICE
Interactive exercise

CREATE
Student production

TEST
Graded activity
```

Audio may come from legitimate uploaded material or newly produced
content.

AI can help create original listening scripts, questions, images,
diagrams and supporting resources.

Copyright must be respected. Commercial textbooks can inform course
structure and pedagogical context, but the application should not become
an unauthorized repository or reproduction system for copyrighted books.

------------------------------------------------------------------------

# 8. Current technical state

A public GitHub repository already exists:

https://github.com/wandermartins-prog/wander.ai.studio-

Current published prototype:

https://wandermartins-prog.github.io/wander.ai.studio-/

The project began as a simple static GitHub Pages prototype.

Known files created during the first development phase:

``` text
README.md
index.html
style.css
script.js
```

GitHub Pages was successfully activated.

The current prototype is only a foundation and should **not** be
mistaken for the final architecture.

Wander has now connected **Supabase to his GitHub account**.

He plans to connect **ChatGPT/Codex to GitHub from the desktop app using
his personal ChatGPT account**.

Development should continue from the personal account.

Before modifying the repository, Codex should inspect the actual current
repository state rather than assuming this handoff contains the latest
code.

------------------------------------------------------------------------

# 9. Initial architecture direction

The architecture discussed before migration was approximately:

``` text
Frontend
React

Hosting / web application
Vercel

Database + Authentication + Storage
Supabase

Source control
GitHub

AI
OpenAI API initially
Optional additional AI providers later

Email notifications
Potentially Resend or another appropriate transactional email service

Media
Supabase Storage and/or appropriate embedded media sources
```

This is an **architecture direction, not an irreversible decision**.

The new Codex session should inspect the existing repository and current
tooling before migration.

Do not introduce unnecessary frameworks or infrastructure merely because
they are fashionable.

The system requires a backend/server-side layer for secrets and AI API
calls. API keys must never be exposed in public client-side JavaScript.

------------------------------------------------------------------------

# 10. Why GitHub Pages alone is insufficient

The original prototype can remain useful as a historical starting point,
but the intended application requires capabilities such as:

-   authentication;
-   authorization;
-   private student data;
-   database access;
-   file storage;
-   submissions;
-   AI API calls;
-   server-side secrets;
-   email notifications.

Therefore, the production application cannot rely solely on static
GitHub Pages.

------------------------------------------------------------------------

# 11. Current conceptual information architecture

A useful high-level model is:

``` text
WANDER AI STUDIO
│
├── Teacher Dashboard
│   ├── Students
│   ├── Materials
│   ├── Assignments
│   ├── Reports
│   ├── Notifications
│   └── AI Creator
│
├── Student Dashboard
│   ├── My Course
│   ├── Lessons
│   ├── Videos
│   ├── Listening
│   ├── Exercises
│   ├── Tests
│   ├── Corrections
│   └── Progress
│
└── Intelligence Layer
    ├── Student history
    ├── Level
    ├── Books/materials
    ├── Activity generation
    ├── Error analysis
    ├── Revision suggestions
    └── Difficulty adaptation
```

This is conceptual. It does not require every item to be implemented
immediately.

------------------------------------------------------------------------

# 12. Development discipline

This point is extremely important.

During the original conversation, the project repeatedly expanded and
changed direction because new ideas were introduced before the current
stage was completed.

Wander explicitly requested a more stable process.

Follow these rules:

1.  Work one stage at a time.
2.  Finish the current stage before introducing a new architecture or
    major idea.
3.  Put good new ideas into a backlog instead of changing the current
    sprint.
4.  Do not repeatedly restart the application.
5.  Inspect existing work before replacing it.
6.  Prefer complete, testable increments.
7.  Clearly state which files will change before major implementation.
8.  Validate the result before moving to the next stage.
9.  Avoid overwhelming Wander with unnecessary development jargon.
10. Explain important technical decisions in accessible language.
11. Never silently expand the project into Wander's school/Eleva
    workflow.
12. Private students are the product's target users.

A useful task format is:

``` text
Objective
Expected result
Files/components affected
Implementation
Validation
```

Use this when useful, without turning every tiny change into
bureaucracy.

------------------------------------------------------------------------

# 13. Important scope correction

An earlier phase of the conversation incorrectly drifted toward Wander's
work at Escola Eleva, including IPC and Language Arts workflows.

That was a misunderstanding.

Those workflows may contain useful examples of Wander's teaching style,
but they are **not the product scope**.

The definitive scope is:

> Wander AI Studio is Wander's independent personal project for managing
> and teaching his private English students.

Do not treat this as an institutional Escola Eleva product.

Do not require school-wide adoption.

Do not design it around school approval processes.

------------------------------------------------------------------------

# 14. Multi-AI background

One motivation for the original idea was Wander's use of several AI
systems for different strengths.

Historically he has used tools such as:

-   ChatGPT;
-   Claude;
-   Gemini;
-   NotebookLM;
-   Grok;
-   Canva and other creation tools.

The application may eventually integrate or route work among external
tools/providers, but **multi-provider AI routing is backlog**, not a V1
requirement.

The immediate goal is to build a useful application, not an elaborate AI
orchestration layer.

------------------------------------------------------------------------

# 15. Visual creation opportunities

Modern ChatGPT capabilities may be useful for producing assets for the
platform, including:

-   avatars;
-   student-safe characters;
-   illustrations;
-   diagrams;
-   visual topic reviews;
-   vocabulary visuals;
-   grammar diagrams;
-   listening support imagery;
-   printable materials;
-   coloring resources for younger learners;
-   UI assets.

A future Visual Library may store reusable visual identities/styles.

However, visual-system development should not derail core platform
functionality.

------------------------------------------------------------------------

# 16. Questions still requiring Wander's decisions

Before freezing V1 requirements, resolve these product questions with
Wander:

### 1. Student scale

Approximately how many private students will normally be active at once?

Examples: 5, 10, 20, 50.

### 2. Age range

Are students mainly:

-   children;
-   teenagers;
-   adults;
-   or a mixture?

### 3. Current course books/materials

Which books and levels does Wander currently use?

A simple list is enough initially.

### 4. Authentication

Should each student have their own username/login?

The previous recommendation was yes.

### 5. Parent access

Should parents/guardians have their own accounts in V1, or should V1
include only Wander + student?

### 6. Automatic correction

Which activity types should V1 correct automatically?

Likely candidates:

-   multiple choice;
-   matching;
-   gap fill;
-   true/false;
-   short answer where appropriate.

Longer productions may require teacher/AI-assisted review.

### 7. Interface language

Should the student interface be:

-   English only;
-   bilingual;
-   configurable?

Should Wander's teacher interface be Portuguese, English or
configurable?

Resolve these before committing to the detailed V1 data model and
screens.

------------------------------------------------------------------------

# 17. Recommended immediate next step in the personal account

Do **not** begin by generating a large amount of code.

The first personal-account session should:

1.  Read this handoff completely.
2.  Inspect the current GitHub repository.
3.  Inspect the existing prototype and README.
4.  Confirm the Supabase/GitHub state that is actually accessible.
5.  Ask Wander only for the unresolved V1 decisions listed above.
6.  Produce a concise **V1 Product Blueprint**.
7.  Obtain Wander's approval of that blueprint.
8.  Freeze the V1 scope.
9.  Create a development backlog.
10. Begin implementation in small, working increments.

The first implementation sprint should establish the new application's
foundation, not attempt to build the entire AI LMS at once.

------------------------------------------------------------------------

# 18. Suggested V1 philosophy

V1 should prove the central workflow:

``` text
Wander creates student
        ↓
Student has private account/profile
        ↓
Wander assigns learning material/activity
        ↓
Student completes it
        ↓
Result is stored
        ↓
Student receives feedback
        ↓
Wander sees submission/result
```

If this works reliably, more sophisticated features can be layered onto
it.

Likely later phases include:

-   richer automatic correction;
-   retries;
-   error taxonomy;
-   personalized revision;
-   AI Creator;
-   listening generation;
-   advanced reports;
-   email automation;
-   visual library;
-   multi-AI integration.

Do not make all of these prerequisites for the first working release.

------------------------------------------------------------------------

# 19. Existing prototype history

The initial prototype had a simple home page with:

-   Wander AI Studio title;
-   quick action buttons;
-   Teaching links;
-   AI platform links;
-   Creation links.

The JavaScript contained placeholder modules such as:

-   Lesson Planner;
-   Assessment Builder;
-   Slides Studio;
-   Game Studio.

These were prototypes from the earlier "AI dashboard" concept.

They are not binding requirements.

When moving to the private-student platform, preserve useful code only
where appropriate. Do not preserve obsolete architecture merely for
sentimental reasons.

------------------------------------------------------------------------

# 20. Security and privacy principles

Because the platform will contain private-student information:

-   never expose service keys in frontend code;
-   use proper authentication;
-   enforce per-user access controls;
-   use Supabase Row Level Security or equivalent authorization;
-   minimize personally identifiable information;
-   collect only information needed for teaching;
-   separate teacher/admin permissions from student permissions;
-   protect uploaded files;
-   do not expose one student's data to another;
-   plan backups and data deletion;
-   treat AI provider data sharing deliberately rather than
    automatically sending entire student histories to external models.

These principles should be incorporated from the beginning rather than
bolted on after student data exists.

------------------------------------------------------------------------

# 21. Source of truth hierarchy

When information conflicts, use this priority:

1.  Wander's newest explicit instruction.
2.  Current approved V1 Product Blueprint.
3.  Current repository/code/database state.
4.  This handoff document.
5.  Earlier brainstorming.

Brainstorming is not a requirement.

------------------------------------------------------------------------

# 22. Final instruction to the receiving ChatGPT/Codex

Continue this project rather than restarting it.

First understand what exists.

Then resolve the seven outstanding V1 decisions.

Then produce and freeze the V1 Product Blueprint.

Only after that should implementation resume.

The project should remain:

**personal, independent, focused on Wander's private English students,
practical, persistent, multimedia-capable, AI-assisted and built
incrementally.**

The long-term aspiration is not merely to create another collection of
educational apps.

It is to create **one system Wander can actually live in as a private
teacher**.
