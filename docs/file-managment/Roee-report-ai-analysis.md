# **Project Contribution Report**

## **Role & Context**

Role: Project Coordinator & Team Member

Project: Teacher Portal – File Management System

Team Size: 4 Members

## **1\. Project Coordination & Planning**

I acted as a coordinator to help organize our work and keep track of our goals.

* **Requirements Definition:** I took responsibility for creating the initial **Product Requirements Document (PRD)** to give the team a clear, defined starting point.  
* **Task Organization:** Assisted in breaking down the project into manageable tasks and tracking progress.  
* **Scheduling:** Helped adjust our weekly plans to fit the changing availability of team members.

## **2\. Technical Implementation & Integration**

My primary technical focus was on infrastructure and tying the application parts together.

* **Component Integration:** I was responsible for the actual integration of the frontend system. I took the individual components (File-browser, File-card, File-icon) and implemented them into the main src/app/teacher/file-management/page.tsx, ensuring they functioned correctly as a cohesive unit.  
* **Firebase Setup:** Handled the backend configuration for Firebase to ensure the database and authentication services were ready for the team to use.  
* **GitHub Management:** Set up and maintained the GitHub Projects board to help us visualize our workflow.  
* **Code Support:** Provided code reviews to help refine the logic and style across the project.

## **3\. Documentation & Structure**

I established the project's foundation to facilitate asynchronous work.

* **File Structure:** Created the open-spec directory and established the folder hierarchy.  
* **Architecture:** Wrote the Architecture.md file to outline how our system components interact.  
* **Maintenance:** Kept the project documentation organized and accessible.

## **4\. Navigating Team Challenges**

Our team faced significant scheduling conflicts this semester, and I did my best to keep the project moving forward despite these constraints.

* **Shared Challenges:** We navigated this project during a complex period. One team member (Avinoam) was on reserve duty (Miluim) for most of the semester, and another (Tamar) was in the advanced stages of pregnancy.  
* **Personal Circumstances:** I was also managing a family emergency involving the birth of my first child and a difficult postpartum recovery.  
* **Outcome:** Despite these limited hours and personal obligations, we supported each other and managed to deliver a functional project.

**\[Prompts I used attached in the next page\]**

**Prompts that I inserted to LLMs along the way:**

I am documenting the system design for our file management module. Generate a template for an Architecture.md file that effectively outlines the data flow between the frontend components and the Firebase backend.

I need to integrate three existing components (File-browser, File-card, File-icon) into src/app/teacher/file-management/page.tsx. Suggest a clean layout structure and component hierarchy to ensure the page remains readable and maintainable.

Review this logic for fetching the file list from Firebase. Identify potential edge cases where the data might fail to load, and suggest how to implement a graceful fallback UI for the user.

PRD creation prompts:

This is combination of few examples prompts/conversations we had we some models like Gemini, Claude, etc. \-\> so we combine the main input-output into one sum-up file:  
————  
\# PRD Generation Assistant for Course Submission  
You are an expert Product Manager helping a student team create a professional PRD (Product Requirements Document) that meets the collaborative repository standards for their course project.  
\#\# Your Task  
Generate a complete, submission-ready PRD based on the team's project information. The output must comply with the PM's collaborative workflow requirements and be ready for PR submission to the master repository.  
\#\# Input You'll Receive  
1\. \*\*Course Project Description\*\* \- Overall project context and requirements  
2\. \*\*PM's Collaborative PRD Guidelines\*\* \- The workflow, structure, and quality standards  
3\. \*\*Team's Project Information\*\* \- Your feature/project details in whatever format you have (notes, files, descriptions)  
\#\# Required Outputs  
Generate these four deliverables:  
\#\#\# 1\. \`Drafts/\[your\_feature\_name\]\_draft.md\`  
The main PRD document containing:  
\*\*Required Metadata Block:\*\*  
\`\`\`markdown  
\#\# Status: DRAFT  
\#\# Owner: \[Your Team Name/PM Name\]  
\#\# Last Updated: \[Date\]  
\`\`\`  
\*\*Required Sections:\*\*  
\- \*\*Problem Statement\*\*: Clear description of the problem being solved  
\- \*\*Target Users\*\*: Who benefits from this feature  
\- \*\*Solution Overview\*\*: High-level description of the solution  
\- \*\*Detailed Requirements\*\*: Numbered list of specific, testable requirements  
\- \*\*User Stories\*\*: Format: "As a \[user\], I want \[goal\] so that \[benefit\]" with acceptance criteria  
\- \*\*Success Metrics\*\*: Quantifiable measures (e.g., "reduce load time to \< 2s", "80% user adoption")  
\- \*\*Technical Constraints\*\*: API limits, performance requirements, dependencies  
\- \*\*Out of Scope\*\*: What this PRD explicitly does NOT include  
\#\#\# 2\. Glossary Entries (\`glossary.md\` additions)  
List all new terms with definitions:  
\`\`\`markdown  
\- \*\*\[Term\]\*\*: \[Clear, concise definition\]  
\`\`\`  
Include:  
\- Product-specific terminology  
\- Technical jargon  
\- Acronyms  
\- Domain concepts  
\#\#\# 3\. Content Extracts for Perspective Files  
\*\*For \`userStories.md\`:\*\*  
\- High-level user goals and outcomes (2-3 sentences each)  
\*\*For \`system.md\`:\*\*  
\- API endpoints/requirements  
\- Architecture components  
\- Infrastructure needs  
\- Technical specifications  
\*\*For \`dataModel.md\`:\*\*  
\- New entities/tables  
\- Required fields with types  
\- Relationships between entities  
\- Data constraints  
\#\# Quality Standards to Follow  
1\. \*\*Specificity\*\*: Use quantifiable metrics  
\- ❌ "fast response time"  
\- ✅ "API latency \< 200ms at p95"  
2\. \*\*Testability\*\*: Every requirement must be verifiable  
\- Include acceptance criteria  
\- Define "done" clearly  
3\. \*\*Terminology Consistency\*\*: Use the same term throughout, define in glossary  
4\. \*\*Complete User Stories\*\*:  
\- Clear actor, goal, and benefit  
\- Specific acceptance criteria  
\- Measurable outcomes  
5\. \*\*Proper Structure\*\*: Follow markdown best practices with clear heading hierarchy  
\#\# Output Format  
Provide the complete PRD draft first, then the supporting materials:  
\`\`\`markdown  
\# \[Feature Name\] \- PRD Draft  
\#\# Status: DRAFT  
\#\# Owner: \[Team Name\]  
\#\# Last Updated: \[Date\]  
\#\# Problem Statement  
\[2-3 paragraphs\]  
\#\# Target Users  
\[User segments\]  
\#\# Solution Overview  
\[High-level approach\]  
\#\# Detailed Requirements  
1\. \[Requirement with specific acceptance criteria\]  
2\. \[Requirement with specific acceptance criteria\]  
...  
\#\# User Stories  
\#\#\# Story 1: \[Title\]  
\*\*As a\*\* \[user type\]  
\*\*I want\*\* \[goal\]  
\*\*So that\*\* \[benefit\]  
\*\*Acceptance Criteria:\*\*  
\- \[ \] \[Specific, testable criterion\]  
\- \[ \] \[Specific, testable criterion\]  
\#\# Success Metrics  
\- \[Quantifiable metric with target\]  
\- \[Quantifiable metric with target\]  
\#\# Technical Requirements  
\[API specs, performance requirements, constraints\]  
\#\# Data Requirements  
\[Entities, fields, relationships needed\]  
\#\# Out of Scope  
\- \[Explicitly excluded items\]  
\#\# Dependencies  
\[Other features, systems, or teams this depends on\]  
\---  
\# Glossary Entries to Add  
\- \*\*\[Term 1\]\*\*: \[Definition\]  
\- \*\*\[Term 2\]\*\*: \[Definition\]  
\---  
\# Content for Perspective Files  
\#\# userStories.md Extract  
\[User-facing summaries\]  
\#\# system.md Extract  
\[Technical/architectural content\]  
\#\# dataModel.md Extract  
\[Data schema content\]  
\`\`\`  
\---  
\#\# Now Generate My PRD  
\*\*Course Project Description:\*\*  
in the attached file.  
\*\*Project Information:\*\*  
in the attached file  
\*\*PM's Guidelines for the general collaborate PRD:\*\*  
\[what is a good workflow to create and maintain a structured PRD folder with multiple product managers collaborating over a shared GitHub repo. I want to store all files in MD. I want to use LLM agents to help enforce consistency and collaborative review with PRs. I want to maintain modular MD files for draft ideas, a live consolidated 'prd.md' master file, a userStories.md perspective, a system perspective, and a data model perspective. I want to actively maintain a glossary.md file to enforce consistent terminology. I want to use GitHub actions to enforce the workflow.  
That is an excellent, advanced workflow design. Leveraging Markdown for content modularity and GitHub for automation (Actions and LLM agents) creates a robust, scalable system for collaborative PRD maintenance.  
I will outline the recommended folder structure, the collaborative workflow, and the enforcement mechanisms, and then provide drafts for the core files: a README.md (to document the process), the master prd.md, and the critical glossary.md.  
Here is the setup for your structured PRD folder and workflow:  
I. Repository Structure  
Your folder structure needs to be logical and immediately understandable to new collaborators.  
/PRD\_Repo  
├── .github/  
│ └── workflows/  
│ ├── prd\_linter.yml (For Markdown/Style checks)  
│ └── consistency\_agent.yml (For LLM review)  
├── Drafts/  
│ ├── feature\_x\_draft.md (Drafts are feature-specific, temporary, and granular)  
│ └── feature\_y\_draft.md  
├── prd.md (The CONSOLIDATED master document \- Read-only source of truth)  
├── userStories.md (Perspective 1: User focus)  
├── system.md (Perspective 2: Technical/API focus)  
├── dataModel.md (Perspective 3: Data focus)  
├── glossary.md (The single source of truth for terminology)  
└── README.md (Documents the entire workflow and folder structure)  
II. Collaborative Workflow: The PR Cycle  
The core principle here is that no changes are made directly to the primary .md files on the main branch. Everything must go through a Pull Request (PR).  
Start a Draft: A PM creates a new feature branch (e.g., feature/onboarding-v2). They start documenting the idea in a new file within the Drafts/ folder (e.g., Drafts/onboarding\_v2\_draft.md).  
Initial PR (Draft Review): The PM opens a PR from their feature branch to the main branch. This initial PR contains only the new file in the Drafts/ folder. This is for early conceptual review by stakeholders.  
Integration (The Key Step): Once the draft is approved, the PM manually or semi-automatically moves the final content from the draft into the relevant master files.  
Content goes into prd.md.  
New terms are added to glossary.md.  
User-facing summaries go into userStories.md.  
System/API requirements go into system.md.  
Changes to entities/fields go into dataModel.md.  
The temporary draft file can then be deleted or moved to an Archive/ folder.  
Final PR Submission: The feature branch now contains the integrated, consistent changes across all core files. The PM pushes these integrated changes.  
Automated Enforcement: GitHub Actions are triggered on the PR (see Section III).  
Collaborative Review: Human PMs review the PR. The LLM Agent's review comments act as an aid, highlighting consistency gaps and terminology issues.  
Merge: The PR is only merged once human and automated checks pass, ensuring the main branch is always a high-quality source of truth.  
III. Enforcement with GitHub Actions & LLM Agents  
The workflow enforcement relies on two main GitHub Action pipelines:  
Action Pipeline Enforcement Mechanism LLM Agent Role  
prd\_linter.yml Uses standard Markdown linting tools (e.g., markdownlint) to enforce style, maximum line length, heading structure, and required metadata blocks (e.g., STATUS:, OWNER:) in prd.md. None (Focus on structural/syntax consistency)  
consistency\_agent.yml This action calls your internal LLM agent (via an API) to perform advanced semantic checks against the PR changes. 1\. Glossary Check: Scan changes to prd.md. If a term is used that is not present in glossary.md, or if an existing term is used with a definition inconsistent with glossary.md, the agent adds a comment to the PR requesting clarification or an update to glossary.md. 2\. Perspective Consistency: Check if changes in prd.md are logically supported by corresponding updates in userStories.md, system.md, and dataModel.md. 3\. Clarity/Ambiguity: Critique the writing for common ambiguities, lack of quantification (e.g., "fast" vs. "latency \< 200ms"), or vague user stories.  
I'll now provide the essential files you requested, starting with the documentation for the team.  
This robust workflow enforces collaboration through the PR requirement, consistency through the shared perspectives and the glossary.md file, and automation via the LLM agents and GitHub Actions.  
Let me know if you would like me to draft the content for one of the perspective files (userStories.md, system.md, or dataModel.md) to see how they reference the master PRD\!  
PRD Repository Structure and Workflow  
Product Requirements Document (PRD) Repository  
This repository serves as the single source of truth for all product requirements, collaboratively maintained by the Product Management team. We use a structured, modular Markdown approach enforced by Pull Requests and automated LLM agents to ensure consistency and quality.  
1\. Directory Structure Overview  
Folder/File Purpose Update Method  
prd.md Master PRD. The consolidated, detailed source of all requirements. This is the primary reference. PR only. Updated by integrating approved drafts.  
Drafts/ Contains in-progress, feature-specific documentation before integration. PMs create new files here for every new feature.  
userStories.md A high-level view summarizing the primary user goals and outcomes derived from prd.md. PR only. Must be consistent with prd.md.  
system.md The technical perspective, documenting architectural requirements, API definitions, and infrastructure needs. PR only. Must be consistent with prd.md.  
dataModel.md Details on required data changes, entity relationships, and necessary fields. PR only. Must be consistent with prd.md.  
glossary.md Critical. Defines all official product, business, and technical terminology. PR only. Must be updated any time a new term is introduced or an existing term's definition changes.  
2\. The Collaborative Workflow (PR Flow)  
All updates, no matter how small, MUST follow this process:  
Branch: Create a new feature branch (git checkout \-b feature/my-new-feature).  
Draft: Create a new document in Drafts/ (e.g., Drafts/my\_feature\_draft.md). Write requirements, scope, and goals.  
Integrate: Once the draft is finalized and approved by stakeholders (often via an initial review PR), integrate the content into the main files:  
Update prd.md  
CRITICAL: Update glossary.md with any new or changed terminology.  
Update userStories.md, system.md, and dataModel.md as necessary.  
Final PR: Push all changes to your feature branch and open a Pull Request targeting main.  
3\. Automated Enforcement (GitHub Actions & LLM Agent)  
When a PR is opened, two pipelines automatically run:  
A. PRD Linter (prd\_linter.yml)  
This runs markdownlint to check structural elements:  
Enforces correct heading levels.  
Ensures required metadata fields (e.g., \#\# Status: \[DRAFT/LIVE\], \#\# Owner: \[PM Name\]) are present in prd.md.  
B. Consistency Agent (consistency\_agent.yml)  
This LLM-driven agent performs semantic analysis:  
Terminology Enforcement: The agent compares new terms in the PR (especially in prd.md) against glossary.md. It will comment on the PR if a new term is used but not defined, or if an existing term is used inconsistently.  
Cross-Document Check: The agent verifies that key requirements introduced in prd.md have corresponding summary information or links in the perspective files (userStories.md, system.md, dataModel.md).  
The PR cannot be merged until the LLM Agent confirms all terminology and cross-document consistency checks have passed.\]  
Generate a complete, submission-ready PRD following all the requirements above.  
Here is the complete, submission-ready PRD based on your project files and collaborative guidelines.  
Markdown  
\# CourseLLM Platform (V1) \- PRD Draft  
\#\# Status: DRAFT  
\#\# Owner: CourseLLM Team  
\#\# Last Updated: 2025-11-08  
\#\# Problem Statement  
\[cite\_start\]In modern computer science (CS) departments, there is a disconnect between the rapid advancement of AI tools and the core goals of education\[cite: 5\]. \[cite\_start\]Teachers are concerned that students may use AI as a "shortcut" to complete assignments, bypassing the learning process and failing to master the material.  
Conversely, students are eager to use modern tools. \[cite\_start\]They want enhanced, faster, and more personalized access to their course material to learn better and deeper. The current challenge is the lack of a tool that bridges this gap—one that uses AI to facilitate genuine understanding rather than just providing answers.  
\#\# Target Users  
\* \[cite\_start\]\*\*Students:\*\* Students taking courses in the CIS Faculty @BGU\[cite: 15\].  
\* \[cite\_start\]\*\*Teachers:\*\* Teachers of courses at the CIS Faculty @BGU\[cite: 15\].  
\#\# Solution Overview  
\[cite\_start\]This project, "CourseLLM," is an AI-powered learning enhancement platform specifically for the CS department\[cite: 5\]. \[cite\_start\]It does \*\*not\*\* create new course content or replace existing AI tools\[cite: 9, 10\]. \[cite\_start\]Instead, it \*\*enhances the learning experience\*\* around existing material\[cite: 10\].  
For students, it provides:  
\* \[cite\_start\]A \*\*Socratic chatbot\*\* scoped strictly to their course materials\[cite: 18, 33\].  
\* \[cite\_start\]Personalized quiz and exercise generation to master content.  
\* \[cite\_start\]Assistance with platform-specific tasks like debugging and tool installation.  
\* \[cite\_start\]Motivational context on why material is important.  
For teachers, it provides:  
\* \[cite\_start\]A "content-aware" system where they can upload course notes, slides, and exercises\[cite: 25, 39\].  
\* \[cite\_start\]Tools to generate "LLM-resilient" assignments that test true understanding.  
\* \[cite\_start\]A dashboard to monitor student progress along predefined "learning trajectories"\[cite: 25, 26\].  
\#\# Detailed Requirements  
1\.  \[cite\_start\]\*\*Teacher Content Ingestion:\*\* The system must allow teachers to upload course-related files, including notes, documents, exams, slides, exercises, and quizzes.  
    \* \*\*Acceptance Criteria:\*\*  
        \* \[cite\_start\]\[ \] Uploaded content is indexed to support a Retrieval-Augmented Generation (RAG) approach.  
        \* \[cite\_start\]\[ \] The system performs a consistency review of the uploaded materials\[cite: 40\].  
2\.  \[cite\_start\]\*\*Chatbot Scope Enforcement:\*\* The student-facing chatbot must be strictly restricted to the content of the indexed course material\[cite: 31\].  
    \* \*\*Acceptance Criteria:\*\*  
        \* \[cite\_start\]\[ \] The system must identify and filter out questions not related to the course material\[cite: 31\].  
3\.  \[cite\_start\]\*\*Socratic Learning Interaction:\*\* The chatbot must \*\*not\*\* provide direct answers to student questions\[cite: 34\].  
    \* \*\*Acceptance Criteria:\*\*  
        \* \[cite\_start\]\[ \] The chatbot must be programmed to provide a Socratic learning experience\[cite: 33\].  
        \* \[cite\_start\]\[ \] Before answering, the chatbot must first check for student misconceptions, analyze their intentions, and check their perspectives\[cite: 34\].  
4\.  \[cite\_start\]\*\*Student Personalization:\*\* The chatbot's answers and guidance must be adjusted to the current knowledge level of the student as recorded in the system.  
5\.  \[cite\_start\]\*\*Personalized Quiz Generation:\*\* The system must be able to generate personalized quizzes, exams, and exercises for students.  
    \* \*\*Acceptance Criteria:\*\*  
        \* \[cite\_start\]\[ \] Generated quizzes are designed to verify that the student has mastered the content.  
        \* \[cite\_start\]\[ \] The system can check that the tasks are performed correctly\[cite: 23\].  
6\.  \[cite\_start\]\*\*Student Progress Monitoring:\*\* The system must actively monitor and track student progress\[cite: 35\].  
    \* \*\*Acceptance Criteria:\*\*  
        \* \[cite\_start\]\[ \] The system must log what skills and content the student has acquired.  
        \* \[cite\_start\]\[ \] Progress must be tracked against predefined "learning trajectories" set by the teacher.  
7\.  \[cite\_start\]\*\*Teacher Assignment Generation:\*\* The system must assist teachers in preparing assignments (quizzes, exams).  
    \* \*\*Acceptance Criteria:\*\*  
        \* \[cite\_start\]\[ \] The system must help create assignments that are "LLM resilient".  
        \* \[cite\_start\]\[ \] The system must verify that generated assignments correspond to the taught material and are of appropriate complexity.  
8\.  \[cite\_start\]\*\*Logging for Metrics:\*\* The product must produce activity logs that can be analyzed to quantitatively measure value and success.  
\#\# User Stories  
\#\#\# Story 1: Student Socratic Chat  
\*\*As a\*\* Student  
\*\*I want\*\* to ask questions about my course notes in a Socratic way  
\[cite\_start\]\*\*So that\*\* I can identify my own misconceptions and learn the material deeply, not just get the answer\[cite: 13, 33, 34\].  
\*\*Acceptance Criteria:\*\*  
\* \[cite\_start\]\[ \] When I ask "What is the answer to HW1, Q3?", the chatbot refuses and instead asks me what I've tried so far or what part of the problem I find confusing\[cite: 34\].  
\* \[cite\_start\]\[ \] The chatbot's hints are based on my current tracked progress (e.g., if I've mastered "loops" but not "recursion").  
\* \[cite\_start\]\[ \] All questions I ask and topics I discuss are logged against my "learning trajectory"\[cite: 37, 56\].  
\#\#\# Story 2: Teacher Creates Resilient Quiz  
\*\*As a\*\* Teacher  
\*\*I want\*\* to create an assignment that is "LLM resilient"  
\[cite\_start\]\*\*So that\*\* I can be confident students are learning the material and not just using AI to get the answers\[cite: 12, 27\].  
\*\*Acceptance Criteria:\*\*  
\* \[cite\_start\]\[ \] I can access a tool to help me generate assignment questions.  
\* \[cite\_start\]\[ \] The system verifies the generated questions correspond to the material I taught by cross-referencing my uploaded content.  
\* \[ \] The system provides a "resilience score" (e.g., 1-10) indicating how easily a standard LLM could answer the question, allowing me to refine it.  
\#\# Success Metrics  
\* \*\*Student Adoption:\*\* 70% of students in a target course use the chatbot at least once per week.  
\* \[cite\_start\]\*\*Learning Efficacy (Student):\*\* 80% of students who use the personalized quiz feature  show a 15% improvement in scores on subsequent "mastery" checks.  
\* \[cite\_start\]\*\*Teacher Engagement:\*\* 90% of teachers in the pilot program upload their course materials for at least one course.  
\* \[cite\_start\]\*\*Socratic Interaction Rate:\*\* \> 60% of chatbot sessions are classified as "Socratic" (i.e., the bot asks more clarifying questions than it gives direct answers), as measured by activity logs\[cite: 33, 34, 56\].  
\#\# Technical Requirements  
\* \[cite\_start\]The system must use a Retrieval-Augmented Generation (RAG) approach, indexing course material to ground the chatbot's responses.  
\* \[cite\_start\]All user interactions, chatbot queries, and progress updates must be logged to a database for analysis and metric calculation.  
\* \[cite\_start\]The system must support file uploads for various formats (e.g., PDF, .md, .txt, .pptx).  
\* \[cite\_start\]The system must maintain a persistent profile for each student to track their knowledge level  \[cite\_start\]and progress.  
\#\# Data Requirements  
\* \[cite\_start\]\*\*StudentProfile:\*\* \`student\_id\`, \`current\_level\_map\` (JSONB) , \`trajectory\_progress\` (JSONB).  
\* \[cite\_start\]\*\*CourseMaterial:\*\* \`course\_id\`, \`document\_id\`, \`content\_vector\`, \`source\_file\_name\`.  
\* \[cite\_start\]\*\*LearningTrajectory:\*\* \`trajectory\_id\`, \`course\_id\`, \`topic\_name\`, \`dependencies\`.  
\* \[cite\_start\]\*\*InteractionLog:\*\* \`session\_id\`, \`student\_id\`, \`timestamp\`, \`query\_text\`, \`response\_text\`, \`is\_socratic\` (boolean).  
\#\# Out of Scope  
\* \[cite\_start\]Creating new, original course material\[cite: 9\].  
\* \[cite\_start\]Replacing existing university platforms or general-purpose chatbots (like NotebookLM)\[cite: 10\].  
\* \[cite\_start\]A fully automated grading system for all assignment types\[cite: 28\].  
\* \[cite\_start\]Advanced, foolproof cheating detection (the initial feature is "LLM-resilient" assignment creation, not post-submission detection)\[cite: 27, 29\].  
\#\# Dependencies  
\* \[cite\_start\]Access to the CS Department's official course list and materials to target\[cite: 5, 15\].  
\* Access to student enrollment lists to create \`StudentProfile\` accounts.  
Glossary Entries to Add

*   
  Learning Trajectories: A predefined sequence of topics and skills, ordered by dependency, that a student must master.  
*   
  LLM Resilient: A quality of an assignment (quiz, exam) indicating it is designed to be difficult to solve correctly using a standard Large Language Model, thereby requiring genuine understanding from the student.  
* RAG (Retrieval-Augmented Generation): The technical approach of indexing course material to support a chatbot, which retrieves relevant content first before generating an answer. This ensures answers are grounded in the provided documents.  
* Socratic Learning Experience: An interaction style for the chatbot where it avoids direct answers. Instead, it guides the student by checking for misconceptions, analyzing intentions, and asking probing questions.

Content for Perspective Files  
userStories.md Extract

* Student Perspective: Students need a way to interact with their course material 24/7 in a personalized way that challenges them to think, rather than just providing answers. They want to know why they are learning something and get help with practical tasks like debugging code. The goal is to use AI to learn "better, deeper, faster".  
*   
  Teacher Perspective: Teachers need confidence that AI tools are enhancing, not hindering, learning. They require tools to help them create better, "LLM-resilient" assignments and monitor which students are falling behind on specific "learning trajectories".

system.md Extract

*   
  Architecture: The core architecture relies on a RAG (Retrieval-Augmented Generation) model.  
* API Endpoints:  
  *   
    POST /upload/{course\_id}: Allows teachers to upload course files (PDFs, slides, notes). The backend will trigger an indexing job.  
  * POST /chat/{course\_id}: Student chat interface. Requires student\_id in the request body to retrieve their profile and current\_level.  
  *   
    GET /progress/{student\_id}: Retrieves the student's current position on all "learning trajectories".  
  *   
    POST /generate\_quiz/{course\_id}: Generates a personalized quiz for the requesting student.  
*   
  Infrastructure: Requires a vector database to store indexed content embeddings for the RAG system.  
*   
  Logging: All chat interactions must be logged with metadata (student\_id, timestamp, trajectory\_tags) to enable quantitative analysis of student progress and product value.

dataModel.md Extract

* Entities:  
  * StudentProfile: Stores student-specific data. Fields: student\_id (PK), course\_list, current\_level\_map (JSONB, e.g., {"topic\_a": "mastered", "topic\_b": "struggling"}) , trajectory\_progress (JSON).  
  * CourseMaterial: Stores indexed content. Fields: content\_id (PK), course\_id (FK), source\_document, content\_chunk (text), content\_vector (embedding).  
  * LearningTrajectory: Defines the course structure. Fields: trajectory\_id (PK), course\_id (FK), topic\_name, dependencies (e.g., list of topic\_ids).  
  * InteractionLog: Logs all chat sessions. Fields: log\_id (PK), session\_id, student\_id (FK), timestamp, query\_text, response\_text, is\_socratic\_flag (boolean).

"""  
Glossary Entries to Add  
Learning Trajectories: A predefined sequence of topics and skills, ordered by dependency, that a student must master.  
LLM Resilient: A quality of an assignment (quiz, exam) indicating it is designed to be difficult to solve correctly using a standard Large Language Model, thereby requiring genuine understanding from the student.  
RAG (Retrieval-Augmented Generation): The technical approach of indexing course material to support a chatbot, which retrieves relevant content first before generating an answer. This ensures answers are grounded in the provided documents.  
Socratic Learning Experience: An interaction style for the chatbot where it avoids direct answers. Instead, it guides the student by checking for misconceptions, analyzing intentions, and asking probing questions.  
"""  
is this part and the following parts ate part of the prd?  
because it is separate.  
what should i submit?  
Your final answer should only by what i finally submit.  
Here is the content you need to submit.  
Based on your team's workflow, your submission is a Pull Request (PR) that modifies multiple files. The content for each file is below.  
File 1: Drafts/CourseLLM\_V1\_draft.md (New File)  
Markdown  
\# CourseLLM Platform (V1) \- PRD Draft  
\#\# Status: DRAFT  
\#\# Owner: CourseLLM Team  
\#\# Last Updated: 2025-11-08  
\#\# Problem Statement  
In modern computer science (CS) departments, there is a disconnect between the rapid advancement of AI tools and the core goals of education. \[cite\_start\]Teachers are concerned that students may use AI as a "shortcut" to complete assignments, bypassing the learning process and failing to master the material\[cite: 94\].  
Conversely, students are eager to use modern tools. \[cite\_start\]They want enhanced, faster, and more personalized access to their course material to learn better and deeper\[cite: 95\]. The current challenge is the lack of a tool that bridges this gap—one that uses AI to facilitate genuine understanding rather than just providing answers.  
\#\# Target Users  
\* \[cite\_start\]\*\*Students:\*\* Students taking courses in the CIS Faculty @BGU\[cite: 97\].  
\* \[cite\_start\]\*\*Teachers:\*\* Teachers of courses at the CIS Faculty @BGU\[cite: 97\].  
\#\# Solution Overview  
\[cite\_start\]This project, "CourseLLM," is an AI-powered learning enhancement platform specifically for the CS department\[cite: 87, 89, 90\]. \[cite\_start\]It does \*\*not\*\* create new course content or replace existing AI tools\[cite: 91\]. \[cite\_start\]Instead, it \*\*enhances the learning experience\*\* around existing material\[cite: 92\].  
For students, it provides:  
\* \[cite\_start\]A \*\*Socratic chatbot\*\* scoped strictly to their course materials\[cite: 100, 113, 115\].  
\* \[cite\_start\]Personalized quiz and exercise generation to master content\[cite: 104\].  
\* \[cite\_start\]Assistance with platform-specific tasks like debugging and tool installation\[cite: 102\].  
\* \[cite\_start\]Motivational context on why material is important\[cite: 103\].  
For teachers, it provides:  
\* \[cite\_start\]A "content-aware" system where they can upload course notes, slides, and exercises\[cite: 107, 121\].  
\* \[cite\_start\]Tools to generate "LLM-resilient" assignments that test true understanding\[cite: 109\].  
\* \[cite\_start\]A dashboard to monitor student progress along predefined "learning trajectories"\[cite: 107, 108\].  
\#\# Detailed Requirements  
1\.  \[cite\_start\]\*\*Teacher Content Ingestion:\*\* The system must allow teachers to upload course-related files, including notes, documents, exams, slides, exercises, and quizzes\[cite: 121\].  
    \* \*\*Acceptance Criteria:\*\*  
        \* \[cite\_start\]\[ \] Uploaded content is indexed to support a Retrieval-Augmented Generation (RAG) approach\[cite: 123\].  
        \* \[cite\_start\]\[ \] The system performs a consistency review of the uploaded materials\[cite: 122\].  
2\.  \[cite\_start\]\*\*Chatbot Scope Enforcement:\*\* The student-facing chatbot must be strictly restricted to the content of the indexed course material\[cite: 113\].  
    \* \*\*Acceptance Criteria:\*\*  
        \* \[cite\_start\]\[ \] The system must identify and filter out questions not related to the course material\[cite: 113\].  
3\.  \[cite\_start\]\*\*Socratic Learning Interaction:\*\* The chatbot must \*\*not\*\* provide direct answers to student questions\[cite: 116\].  
    \* \*\*Acceptance Criteria:\*\*  
        \* \[cite\_start\]\[ \] The chatbot must be programmed to provide a Socratic learning experience\[cite: 115\].  
        \* \[cite\_start\]\[ \] Before answering, the chatbot must first check for student misconceptions, analyze their intentions, and check their perspectives\[cite: 116\].  
4\.  \[cite\_start\]\*\*Student Personalization:\*\* The chatbot's answers and guidance must be adjusted to the current knowledge level of the student as recorded in the system\[cite: 114\].  
5\.  \[cite\_start\]\*\*Personalized Quiz Generation:\*\* The system must be able to generate personalized quizzes, exams, and exercises for students\[cite: 104\].  
    \* \*\*Acceptance Criteria:\*\*  
        \* \[cite\_start\]\[ \] Generated quizzes are designed to verify that the student has mastered the content\[cite: 104\].  
        \* \[cite\_start\]\[ \] The system can check that the tasks are performed correctly\[cite: 105\].  
6\.  \[cite\_start\]\*\*Student Progress Monitoring:\*\* The system must actively monitor and track student progress\[cite: 117\].  
    \* \*\*Acceptance Criteria:\*\*  
        \* \[cite\_start\]\[ \] The system must log what skills and content the student has acquired\[cite: 119\].  
        \* \[cite\_start\]\[ \] Progress must be tracked against predefined "learning trajectories" set by the teacher\[cite: 108, 119\].  
7\.  \[cite\_start\]\*\*Teacher Assignment Generation:\*\* The system must assist teachers in preparing assignments (quizzes, exams)\[cite: 109\].  
    \* \*\*Acceptance Criteria:\*\*  
        \* \[cite\_start\]\[ \] The system must help create assignments that are "LLM resilient"\[cite: 109\].  
        \* \[cite\_start\]\[ \] The system must verify that generated assignments correspond to the taught material and are of appropriate complexity\[cite: 109\].  
8\.  \[cite\_start\]\*\*Logging for Metrics:\*\* The product must produce activity logs that can be analyzed to quantitatively measure value and success\[cite: 15\].  
\#\# User Stories  
\#\#\# Story 1: Student Socratic Chat  
\*\*As a\*\* Student  
\[cite\_start\]\*\*I want\*\* to ask questions about my course notes in a Socratic way \[cite: 100, 115\]  
\[cite\_start\]\*\*So that\*\* I can identify my own misconceptions and learn the material deeply, not just get the answer\[cite: 95, 116\].  
\*\*Acceptance Criteria:\*\*  
\* \[cite\_start\]\[ \] When I ask "What is the answer to HW1, Q3?", the chatbot refuses \[cite: 116\] \[cite\_start\]and instead asks me what I've tried so far or what part of the problem I find confusing\[cite: 116\].  
\* \[cite\_start\]\[ \] The chatbot's hints are based on my current tracked progress (e.g., if I've mastered "loops" but not "recursion")\[cite: 114\].  
\* \[cite\_start\]\[ \] All questions I ask and topics I discuss are logged against my "learning trajectory"\[cite: 117, 119\].  
\#\#\# Story 2: Teacher Creates Resilient Quiz  
\*\*As a\*\* Teacher  
\[cite\_start\]\*\*I want\*\* to create an assignment that is "LLM resilient" \[cite: 109\]  
\[cite\_start\]\*\*So that\*\* I can be confident students are learning the material and not just using AI to get the answers\[cite: 94, 109\].  
\*\*Acceptance Criteria:\*\*  
\* \[cite\_start\]\[ \] I can access a tool to help me generate assignment questions\[cite: 109\].  
\* \[cite\_start\]\[ \] The system verifies the generated questions correspond to the material I taught by cross-referencing my uploaded content\[cite: 109, 121\].  
\* \[ \] The system provides a "resilience score" (e.g., 1-10) indicating how easily a standard LLM could answer the question, allowing me to refine it.  
\#\# Success Metrics  
\* \*\*Student Adoption:\*\* 70% of students in a target course use the chatbot at least once per week.  
\* \[cite\_start\]\*\*Learning Efficacy (Student):\*\* 80% of students who use the personalized quiz feature show a 15% improvement in scores on subsequent "mastery" checks\[cite: 14, 104\].  
\* \[cite\_start\]\*\*Teacher Engagement:\*\* 90% of teachers in the pilot program upload their course materials for at least one course\[cite: 90, 107\].  
\* \[cite\_start\]\*\*Socratic Interaction Rate:\*\* \> 60% of chatbot sessions are classified as "Socratic" (i.e., the bot asks more clarifying questions than it gives direct answers), as measured by activity logs\[cite: 15, 115\].  
\#\# Technical Requirements  
\* \[cite\_start\]The system must use a Retrieval-Augmented Generation (RAG) approach, indexing course material to ground the chatbot's responses\[cite: 123\].  
\* \[cite\_start\]All user interactions, chatbot queries, and progress updates must be logged to a database for analysis and metric calculation\[cite: 15, 117\].  
\* \[cite\_start\]The system must support file uploads for various formats (e.g., PDF, .md, .txt, .pptx)\[cite: 121\].  
\* \[cite\_start\]The system must maintain a persistent profile for each student to track their knowledge level and progress\[cite: 114, 118\].  
\#\# Data Requirements  
\* \[cite\_start\]\*\*StudentProfile:\*\* \`student\_id\`, \`current\_level\_map\` (JSONB) \[cite: 114, 118\]\[cite\_start\], \`trajectory\_progress\` (JSONB)\[cite: 119\].  
\* \[cite\_start\]\*\*CourseMaterial:\*\* \`course\_id\`, \`document\_id\`, \`content\_vector\` \[cite: 123\]\[cite\_start\], \`source\_file\_name\`\[cite: 121\].  
\* \[cite\_start\]\*\*LearningTrajectory:\*\* \`trajectory\_id\`, \`course\_id\`, \`topic\_name\`, \`dependencies\`\[cite: 108\].  
\* \[cite\_start\]\*\*InteractionLog:\*\* \`session\_id\`, \`student\_id\`, \`timestamp\`, \`query\_text\`, \`response\_text\`, \`is\_socratic\` (boolean)\[cite: 15, 115\].  
\#\# Out of Scope  
\* \[cite\_start\]Creating new, original course material\[cite: 91\].  
\* \[cite\_start\]Replacing existing university platforms or general-purpose chatbots (like NotebookLM)\[cite: 91\].  
\* \[cite\_start\]A fully automated grading system for all assignment types\[cite: 110\].  
\* \[cite\_start\]Advanced, foolproof cheating detection \[cite: 111\] (the initial feature is "LLM-resilient" assignment creation, not post-submission detection).  
\#\# Dependencies  
\* Access to the CS Department's official course list and materials to target.  
\* Access to student enrollment lists to create \`StudentProfile\` accounts.  
File 2: glossary.md (Additions)  
Markdown  
\- \[cite\_start\]\*\*Learning Trajectories\*\*: A predefined sequence of topics and skills, ordered by dependency, that a student must master\[cite: 108\].  
\- \[cite\_start\]\*\*LLM Resilient\*\*: A quality of an assignment (quiz, exam) indicating it is designed to be difficult to solve correctly using a standard Large Language Model, thereby requiring genuine understanding from the student\[cite: 109\].  
\- \[cite\_start\]\*\*RAG (Retrieval-Augmented Generation)\*\*: The technical approach of indexing course material to support a chatbot, which retrieves relevant content first before generating an answer\[cite: 123\]. This ensures answers are grounded in the provided documents.  
\- \[cite\_start\]\*\*Socratic Learning Experience\*\*: An interaction style for the chatbot where it avoids direct answers\[cite: 116\]. \[cite\_start\]Instead, it guides the student by checking for misconceptions, analyzing intentions, and asking probing questions\[cite: 115, 116\].  
File 3: userStories.md (Additions)  
Markdown  
\#\#\# CourseLLM V1  
\* \[cite\_start\]\*\*Student Perspective:\*\* Students need a way to interact with their course material 24/7 in a personalized way that challenges them to think, rather than just providing answers\[cite: 95, 100, 115\]. \[cite\_start\]They want to know \*why\* they are learning something \[cite: 103\] \[cite\_start\]and get help with practical tasks like debugging code\[cite: 102\]. \[cite\_start\]The goal is to use AI to learn "better, deeper, faster"\[cite: 95\].  
\* \[cite\_start\]\*\*Teacher Perspective:\*\* Teachers need confidence that AI tools are enhancing, not hindering, learning\[cite: 94\]. \[cite\_start\]They require tools to help them create better, "LLM-resilient" assignments \[cite: 109\] \[cite\_start\]and monitor which students are falling behind on specific "learning trajectories"\[cite: 107, 108\].  
File 4: system.md (Additions)  
Markdown  
\#\#\# CourseLLM V1  
\* \[cite\_start\]\*\*Architecture:\*\* The core architecture relies on a \*\*RAG (Retrieval-Augmented Generation)\*\* model\[cite: 123\].  
\* \*\*API Endpoints:\*\*  
    \* \[cite\_start\]\`POST /upload/{course\_id}\`: Allows teachers to upload course files (PDFs, slides, notes)\[cite: 121\]. \[cite\_start\]The backend will trigger an indexing job\[cite: 123\].  
    \* \[cite\_start\]\`POST /chat/{course\_id}\`: Student chat interface\[cite: 100\]. \[cite\_start\]Requires \`student\_id\` in the request body to retrieve their profile and \`current\_level\`\[cite: 114\].  
    \* \[cite\_start\]\`GET /progress/{student\_id}\`: Retrieves the student's current position on all "learning trajectories"\[cite: 117, 119\].  
    \* \[cite\_start\]\`POST /generate\_quiz/{course\_id}\`: Generates a personalized quiz for the requesting student\[cite: 104\].  
\* \[cite\_start\]\*\*Infrastructure:\*\* Requires a vector database to store indexed content embeddings for the RAG system\[cite: 123\].  
\* \[cite\_start\]\*\*Logging:\*\* All chat interactions must be logged with metadata (student\_id, timestamp, trajectory\_tags) to enable quantitative analysis of student progress and product value\[cite: 15, 117\].  
File 5: dataModel.md (Additions)  
Markdown  
\#\#\# CourseLLM V1  
\* \*\*Entities:\*\*  
    \* \`StudentProfile\`: Stores student-specific data. \[cite\_start\]Fields: \`student\_id\` (PK), \`course\_list\`, \`current\_level\_map\` (JSONB, e.g., {"topic\_a": "mastered", "topic\_b": "struggling"}) \[cite: 114, 118\]\[cite\_start\], \`trajectory\_progress\` (JSON)\[cite: 119\].  
    \* \`CourseMaterial\`: Stores indexed content. \[cite\_start\]Fields: \`content\_id\` (PK), \`course\_id\` (FK), \`source\_document\` \[cite: 121\]\[cite\_start\], \`content\_chunk\` (text), \`content\_vector\` (embedding)\[cite: 123\].  
    \* \`LearningTrajectory\`: Defines the course structure. \[cite\_start\]Fields: \`trajectory\_id\` (PK), \`course\_id\` (FK), \`topic\_name\`, \`dependencies\` (e.g., list of topic\_ids)\[cite: 108\].  
    \* \`InteractionLog\`: Logs all chat sessions. \[cite\_start\]Fields: \`log\_id\` (PK), \`session\_id\`, \`student\_id\` (FK), \`timestamp\`, \`query\_text\`, \`response\_text\`, \`is\_socratic\_flag\` (boolean)\[cite: 15, 115\].  
make the filed more detailed with clean .md format  
Here is the more detailed, submission-ready content for each of the five files, formatted in clean Markdown.  
File 1: Drafts/CourseLLM\_V1\_draft.md (New File)  
Markdown  
\# CourseLLM Platform (V1) \- PRD Draft  
\#\# Status: DRAFT  
\#\# Owner: CourseLLM Team  
\#\# Last Updated: 2025-11-08  
\---  
\#\# 1\. Problem Statement  
\[cite\_start\]In modern computer science (CS) departments, there is a disconnect between the rapid advancement of AI tools and the core goals of education\[cite: 94\]. \[cite\_start\]Teachers are concerned that students may use AI as a "shortcut" to complete assignments, bypassing the learning process and failing to master the material\[cite: 94\]. \[cite\_start\]This creates an environment of mistrust and forces educators to spend time creating "LLM resilient" assignments rather than focusing on teaching\[cite: 109\].  
\[cite\_start\]Conversely, students are eager to use modern tools\[cite: 95\]. \[cite\_start\]They want enhanced, faster, and more personalized access to their course material to learn "better, deeper, faster"\[cite: 95\]. The current challenge is the lack of a tool that bridges this gap—one that uses AI to facilitate genuine understanding rather than just providing answers.  
\#\# 2\. Target Users  
\#\#\# User Personas  
\* \*\*Persona 1: The Student ("Alex")\*\*  
    \* \*\*Role:\*\* 2nd-year CS student.  
    \* \*\*Goals:\*\* Wants to understand complex topics (like algorithms or data structures) thoroughly, not just pass the exam. Gets stuck on debugging and setup issues.  
    \* \*\*Frustrations:\*\* Finds it hard to get personalized help outside of office hours. Worries about falling behind. Feels standard AI chatbots just give the answer without teaching.  
\* \*\*Persona 2: The Teacher ("Dr. Chen")\*\*  
    \* \*\*Role:\*\* Tenured Professor in the CIS Faculty.  
    \* \[cite\_start\]\*\*Goals:\*\* Wants to ensure students are \*actually\* learning the material\[cite: 94\]. Wants to monitor class progress to identify topics that are poorly understood.  
    \* \[cite\_start\]\*\*Frustrations:\*\* Spends too much time grading and creating cheat-proof assignments\[cite: 109, 110\]. Worries that AI is eroding critical thinking skills.  
\#\# 3\. Solution Overview  
This project, "CourseLLM," is an AI-powered learning enhancement platform specifically for the CS department. \[cite\_start\]It does \*\*not\*\* create new course content or replace existing AI tools\[cite: 91\]. \[cite\_start\]Instead, it \*\*enhances the learning experience\*\* around existing material provided by the teacher\[cite: 91, 107\].  
For students, it provides:  
\* \[cite\_start\]A \*\*Socratic chatbot\*\* scoped strictly to their course materials, which guides them to answers instead of providing them directly\[cite: 115, 116\].  
\* \[cite\_start\]Personalized quiz and exercise generation to master content\[cite: 104\].  
\* \[cite\_start\]Assistance with platform-specific tasks like debugging and tool installation\[cite: 102\].  
\* \[cite\_start\]Motivational context on \*why\* the material is important\[cite: 103\].  
For teachers, it provides:  
\* \[cite\_start\]A "content-aware" system where they can upload course notes, slides, and exercises to create a trusted knowledge base\[cite: 121\].  
\* \[cite\_start\]Tools to generate "LLM-resilient" assignments that test true understanding\[cite: 109\].  
\* \[cite\_start\]A dashboard to monitor student progress along predefined "learning trajectories"\[cite: 107, 108\].  
\#\# 4\. Detailed Requirements  
\#\#\# REQ-1.0: Teacher Content Ingestion  
Teachers must be able to upload their course materials to define the knowledge base for the chatbot.  
\* \*\*1.1:\*\* The system must provide an interface for teachers to upload files (PDF, .md, .pptx, .txt).  
\* \[cite\_start\]\*\*1.2:\*\* All uploaded content must be processed, chunked, and indexed into a vector database to support a RAG approach\[cite: 123\].  
\* \[cite\_start\]\*\*1.3:\*\* The system must perform a basic consistency review (e.g., flag new terms not found in other documents)\[cite: 122\].  
\*\*Acceptance Criteria (1.2):\*\*  
\* \*\*Given\*\* a teacher uploads a 50-page PDF of lecture notes  
\* \*\*When\*\* the processing is complete (within 5 minutes)  
\* \*\*Then\*\* a student asking a question relevant to that PDF receives a grounded response.  
\#\#\# REQ-2.0: Socratic Chatbot  
The student-facing chatbot must function as a Socratic tutor, not an answer key.  
\* \[cite\_start\]\*\*2.1:\*\* The chatbot's knowledge must be strictly restricted to the course material uploaded by the teacher\[cite: 113\].  
\* \[cite\_start\]\*\*2.2:\*\* The system must identify and filter out questions not related to the course material\[cite: 113\].  
\* \[cite\_start\]\*\*2.3:\*\* The chatbot must \*\*not\*\* provide direct answers to "what is the answer" or "write the code for me" questions\[cite: 116\].  
\* \[cite\_start\]\*\*2.4:\*\* The chatbot interaction model must first check for student misconceptions, analyze their intentions, and ask guiding questions before providing hints\[cite: 116\].  
\*\*Acceptance Criteria (2.3 & 2.4):\*\*  
\* \*\*Given\*\* a student asks, "What is the solution to problem 3?"  
\* \*\*When\*\* the bot responds  
\* \*\*Then\*\* the response is a question, such as "Great question\! What have you tried so far?" or "What part of the problem statement do you think is most important?"  
\#\#\# REQ-3.0: Student Personalization  
The system must adapt to the individual student's knowledge level.  
\* \[cite\_start\]\*\*3.1:\*\* The system must maintain a \*\*Student Profile\*\* that tracks progress on "learning trajectories"\[cite: 119\].  
\* \[cite\_start\]\*\*3.2:\*\* The chatbot's answers and guidance must be adjusted based on the student's recorded knowledge level (e.g., "It looks like you haven't mastered 'recursion' yet, let's review that first.")\[cite: 114\].  
\#\#\# REQ-4.0: Personalized Quiz Generation  
The system must be able to generate on-demand practice materials for students.  
\* \*\*4.1:\*\* Students must be able to request a personalized quiz on a specific topic.  
\* \[cite\_start\]\*\*4.2:\*\* Generated quizzes must be based \*only\* on the indexed course material\[cite: 104\].  
\* \[cite\_start\]\*\*4.3:\*\* The system must be able to check the student's answers for correctness and update their Student Profile\[cite: 105, 118\].  
\#\#\# REQ-5.0: Teacher Assignment Generation  
\[cite\_start\]The system must assist teachers in creating effective, "LLM-resilient" assignments\[cite: 109\].  
\* \*\*5.1:\*\* Teachers must have an interface to generate draft questions (quiz, exam, homework) based on selected topics.  
\* \[cite\_start\]\*\*5.2:\*\* The system must verify that generated questions correspond to the taught material and are of appropriate complexity\[cite: 109\].  
\* \*\*5.3:\*\* The system must provide a "resilience score" or analysis for generated questions.  
\#\#\# REQ-6.0: System Logging  
The product must produce activity logs to measure success and value.  
\* \*\*6.1:\*\* All chat interactions must be logged with metadata (student\_id, session\_id, topic\_tags).  
\* \*\*6.2:\*\* All quiz generation and completion events must be logged.  
\* \[cite\_start\]\*\*6.3:\*\* Logs must be anonymized and analyzable to compute success metrics\[cite: 15\].  
\#\# 5\. User Stories  
\#\#\# Story 1: Student Gets "Unstuck"  
\* \*\*As a\*\* Student  
\* \*\*I want\*\* to ask the chatbot why my sorting algorithm isn't working at 2 AM  
\* \*\*So that\*\* I can get a hint and continue learning, instead of being blocked until office hours.  
\*\*Acceptance Criteria:\*\*  
\* \[ \] I can paste my code snippet into the chat.  
\* \[ \] The bot recognizes it's related to "sorting algorithms" from Week 4's lecture.  
\* \[ \] The bot does \*not\* fix the code for me.  
\* \[ \] The bot \*does\* ask me, "What do you think is happening on line 5?" or "Have you considered the base case for your recursion?"  
\#\#\# Story 2: Teacher Creates a Resilient Quiz  
\* \*\*As a\*\* Teacher  
\* \*\*I want\*\* to generate a 5-question quiz on "Data Structures"  
\* \[cite\_start\]\*\*So that\*\* I can test my students' understanding with questions that can't be easily answered by a generic LLM\[cite: 109\].  
\*\*Acceptance Criteria:\*\*  
\* \[ \] I can select the topic "Data Structures" and "Week 5 Slides" as the source.  
\* \[ \] The system generates 5 draft questions.  
\* \[ \] Each question has a "Resilience Score" (e.g., "High: Requires applying concepts from the lecture slides") or ("Low: Simple definition lookup").  
\* \[ \] I can edit and save the questions to create the final quiz.  
\#\#\# Story 3: Student Checks Understanding  
\* \*\*As a\*\* Student  
\* \*\*I want\*\* to take a practice quiz on "Python Dictionaries"  
\* \[cite\_start\]\*\*So that\*\* I can verify I have mastered the content before the midterm\[cite: 104\].  
\*\*Acceptance Criteria:\*\*  
\* \[ \] I can ask the bot, "Generate a 3-question quiz on Python Dictionaries."  
\* \[ \] The bot generates questions based on the course's "Intro to Python" notes.  
\* \[cite\_start\]\[ \] After I answer, the bot tells me which I got right/wrong and updates my "Learning Trajectory" progress\[cite: 105, 119\].  
\#\# 6\. Success Metrics  
| Metric | Description | Target (V1) |  
| \--- | \--- | \--- |  
| \*\*Student Adoption\*\* | % of students in a pilot course who use the chatbot at least once per week. | \> 70% |  
| \*\*Socratic Interaction Rate\*\*| % of chatbot sessions where the bot asks more questions than it provides direct answers. | \> 60% |  
| \*\*Teacher Engagement\*\* | % of teachers in the pilot who upload \>80% of their course materials. | \> 90% |  
| \*\*Mastery Improvement\*\* | % of students who use the personalized quiz feature and show a \>15% score improvement on a subsequent graded assignment for that topic. | \> 50% |  
| \*\*Content Relevance\*\* | % of chatbot answers that are flagged by students as "Not relevant to my course". | \< 5% |  
\#\# 7\. Technical Requirements  
\* \[cite\_start\]\*\*RAG Pipeline:\*\* The system must use a Retrieval-Augmented Generation (RAG) approach\[cite: 123\]. This involves a vector database (e.g., Pinecone, Chroma) and an LLM (e.g., Gemini).  
\* \[cite\_start\]\*\*Logging:\*\* All user interactions (queries, responses, quiz attempts) must be logged to a production database (e.g., BigQuery, PostgreSQL) for metrics analysis\[cite: 15\].  
\* \*\*Authentication:\*\* The system must securely authenticate users (Students, Teachers) against the university's identity system (e.g., OAuth, SAML).  
\* \*\*Privacy:\*\* Student data (progress, queries) must be handled with strict confidentiality and must not be visible to other students.  
\#\# 8\. Data Requirements  
(See \`dataModel.md\` for full schema)  
\* \*\*StudentProfile:\*\* Must store student's current knowledge level and progress.  
\* \*\*CourseMaterial:\*\* Must store indexed content chunks and vectors.  
\* \*\*LearningTrajectory:\*\* Must store the teacher-defined course structure.  
\* \*\*InteractionLog:\*\* Must store all chat and quiz events for analysis.  
\#\# 9\. Out of Scope  
\* \[cite\_start\]Creating new, original course material\[cite: 91\].  
\* \[cite\_start\]Replacing existing university platforms (like Moodle) or general-purpose chatbots (like NotebookLM)\[cite: 91\].  
\* \[cite\_start\]A fully automated grading system for \*all\* assignment types (e.g., free-form essays)\[cite: 110\].  
\* \[cite\_start\]Advanced, foolproof cheating detection\[cite: 111\]. The feature is "LLM-resilient" \*generation\*, not \*detection\*.  
\* Direct student-to-student interaction.  
\#\# 10\. Dependencies  
\* Access to the CS Department's official course list and materials.  
\* Integration with the university's authentication system for student/teacher rosters.  
File 2: glossary.md (Additions)  
Markdown  
\- \*\*Content Index\*\*: The processed, vectorized knowledge base created from the teacher's-uploaded course materials. This is the "ground truth" for the RAG system.  
\- \[cite\_start\]\*\*Learning Trajectories\*\*: A predefined sequence of topics and skills, ordered by dependency, that a student must master\[cite: 108\]. Defined by the teacher.  
\- \[cite\_start\]\*\*LLM Resilient\*\*: A quality of an assignment (quiz, exam) indicating it is designed to be difficult to solve correctly using a standard Large Language Model, thereby requiring genuine understanding from the student\[cite: 109\].  
\- \[cite\_start\]\*\*RAG (Retrieval-Augmented Generation)\*\*: The technical approach of indexing course material to support a chatbot\[cite: 123\]. The system \*retrieves\* relevant content first before \*generating\* an answer, ensuring it is grounded in the provided documents.  
\- \[cite\_start\]\*\*Socratic Interaction Rate\*\*: A success metric that measures the percentage of chatbot sessions where the bot guides the student with questions rather than providing direct answers\[cite: 115, 116\].  
\- \[cite\_start\]\*\*Socratic Learning Experience\*\*: An interaction style for the chatbot where it avoids direct answers\[cite: 115\]. \[cite\_start\]Instead, it guides the student by checking for misconceptions, analyzing intentions, and asking probing questions\[cite: 116\].  
\- \[cite\_start\]\*\*Student Profile\*\*: A persistent data record for each student, tracking their current knowledge level, skills acquired, and progress on learning trajectories\[cite: 114, 119\].  
File 3: userStories.md (Additions)  
Markdown  
\#\#\# CourseLLM V1  
\#\#\#\# High-Level User Goals (Epics)  
\* \*\*Goal: Student Learning Enhancement\*\*  
    \* \[cite\_start\]\*\*Description:\*\* Students want to use the platform to gain a deeper understanding of their course material in a personalized, on-demand way\[cite: 95\]. \[cite\_start\]This includes getting "unstuck" on problems, practicing for exams, and understanding \*why\* topics are important\[cite: 103, 104\].  
    \* \*\*Related PRD:\*\* \`CourseLLM\_V1\_draft.md\` (Sections 4.2, 4.4)  
\* \*\*Goal: Teacher Content Control\*\*  
    \* \[cite\_start\]\*\*Description:\*\* Teachers need to define the "single source of truth" for their course\[cite: 107\]. \[cite\_start\]This involves uploading all their materials and trusting that the platform will \*only\* use this content to interact with students\[cite: 121, 113\].  
    \* \*\*Related PRD:\*\* \`CourseLLM\_V1\_draft.md\` (Section 4.1)  
\* \*\*Goal: Academic Integrity Assurance\*\*  
    \* \[cite\_start\]\*\*Description:\*\* Teachers need tools that help them assess genuine student knowledge in the age of AI\[cite: 94\]. \[cite\_start\]This includes generating "LLM-resilient" assignments and monitoring student progress to identify gaps in understanding\[cite: 107, 109\].  
    \* \*\*Related PRD:\*\* \`CourseLLM\_V1\_draft.md\` (Section 4.5)  
\* \*\*Goal: Personalized Learning Path\*\*  
    \* \[cite\_start\]\*\*Description:\*\* The platform must adapt to each student's individual knowledge level, providing simpler explanations for beginners and more complex challenges for advanced students, all guided by the teacher's "Learning Trajectories"\[cite: 114, 119\].  
    \* \*\*Related PRD:\*\* \`CourseLLM\_V1\_draft.md\` (Section 4.3)  
File 4: system.md (Additions)  
Markdown  
\#\#\# CourseLLM V1  
\#\#\#\# Architecture Overview  
\[cite\_start\]The system is a 3-tier web application built on a \*\*Retrieval-Augmented Generation (RAG)\*\* architecture\[cite: 123\].  
1\.  \*\*Frontend:\*\* A responsive web client for student and teacher dashboards.  
2\.  \*\*Backend:\*\* A set of microservices (e.g., \`auth-service\`, \`chat-service\`, \`content-service\`) to handle business logic.  
3\.  \*\*Data Tier:\*\* Includes a primary relational DB (e.g., PostgreSQL) for user data and a Vector DB (e.g., Chroma) for the Content Index.  
\#\#\#\# RAG Data Flow (Chat)  
1\.  A student sends a query via the \`chat-service\`.  
2\.  The \`chat-service\` retrieves the \`student\_id\` and \`course\_id\`.  
3\.  The query is sent to the \`content-service\`, which converts the query to an embedding.  
4\.  The \`content-service\` queries the Vector DB to find the most relevant "chunks" of text from the teacher's-uploaded materials.  
5\.  The original query, relevant chunks, and chat history are passed to the LLM.  
6\.  \[cite\_start\]A "meta-prompt" instructs the LLM to act as a Socratic tutor \[cite: 115\]\[cite\_start\], use \*only\* the provided chunks \[cite: 113\]\[cite\_start\], and personalize the response based on the student's profile\[cite: 114\].  
7\.  The final, grounded response is sent to the student.  
8\.  \[cite\_start\]The entire interaction is logged asynchronously to the \`InteractionLog\` table\[cite: 15\].  
\#\#\#\# API Endpoints  
\* \`POST /api/v1/course/{course\_id}/upload\`  
    \* \*\*Role:\*\* Teacher  
    \* \*\*Action:\*\* Uploads course files. Triggers an asynchronous indexing job.  
\* \`POST /api/v1/chat/{course\_id}\`  
    \* \*\*Role:\*\* Student  
    \* \*\*Action:\*\* Sends a chat message. Request body includes \`query\` and \`session\_id\`. The \`student\_id\` is derived from the auth token.  
\* \`GET /api/v1/progress/{course\_id}\`  
    \* \*\*Role:\*\* Student (sees their own), Teacher (sees class aggregate)  
    \* \[cite\_start\]\*\*Action:\*\* Retrieves progress on Learning Trajectories\[cite: 107, 119\].  
\* \`POST /api/v1/quiz/generate\`  
    \* \*\*Role:\*\* Student  
    \* \*\*Action:\*\* Generates a personalized quiz. Body includes \`course\_id\`, \`topic\`, \`num\_questions\`.  
\* \`POST /api/v1/assignment/generate\`  
    \* \*\*Role:\*\* Teacher  
    \* \[cite\_start\]\*\*Action:\*\* Generates draft "LLM-resilient" questions\[cite: 109\].  
\#\#\#\# Infrastructure  
\* \[cite\_start\]\*\*Vector Database:\*\* Required for storing embeddings from course materials\[cite: 123\].  
\* \*\*Relational Database:\*\* Required for all structured data (users, profiles, logs).  
\* \*\*LLM Provider:\*\* API access to a powerful LLM (e.g., Google Gemini).  
\* \[cite\_start\]\*\*Logging System:\*\* A scalable logging/analytics platform (e.g., BigQuery, ELK stack) is required to compute metrics\[cite: 15\].  
File 5: dataModel.md (Additions)  
Markdown  
\#\#\# CourseLLM V1  
This file details the required data entities for the CourseLLM platform.  
\#\#\#\# Table: \`StudentProfile\`  
Stores student-specific data, including their knowledge state.  
| Field | Type | Constraints | Description |  
| \--- | \--- | \--- | \--- |  
| \`student\_id\` | \`VARCHAR(255)\` | Primary Key, FK to University Auth | Unique student identifier. |  
| \`course\_ids\` | \`ARRAY\[TEXT\]\` | Not Null | List of courses the student is enrolled in. |  
| \`knowledge\_map\` | \`JSONB\` | Not Null | \[cite\_start\]JSON object mapping topics to a mastery level (e.g., \`{"topic\_id\_1": "struggling", "topic\_id\_2": "mastered"}\`). \[cite: 114\] |  
| \`trajectory\_progress\`| \`JSONB\` | Not Null | \[cite\_start\]JSON object tracking progress on defined Learning Trajectories\[cite: 119\]. |  
\#\#\#\# Table: \`CourseMaterial\`  
Stores the indexed content chunks from teacher-uploaded files.  
| Field | Type | Constraints | Description |  
| \--- | \--- | \--- | \--- |  
| \`content\_id\` | \`UUID\` | Primary Key | Unique identifier for this content chunk. |  
| \`course\_id\` | \`VARCHAR(255)\` | Not Null, FK to Course | Identifies the course this content belongs to. |  
| \`source\_document\` | \`VARCHAR(1024)\` | | \[cite\_start\]The name of the original uploaded file (e.g., "lecture\_1.pdf"). \[cite: 121\] |  
| \`content\_chunk\` | \`TEXT\` | Not Null | The raw text chunk. |  
| \`content\_vector\` | \`VECTOR(...)\` | Not Null | \[cite\_start\]The embedding vector for this chunk\[cite: 123\]. |  
\#\#\#\# Table: \`LearningTrajectory\`  
Defines the teacher's desired learning path for a course.  
| Field | Type | Constraints | Description |  
| \--- | \--- | \--- | \--- |  
| \`trajectory\_id\` | \`UUID\` | Primary Key | Unique identifier for this trajectory. |  
| \`course\_id\` | \`VARCHAR(255)\` | Not Null, FK to Course | The course this trajectory belongs to. |  
| \`topic\_name\` | \`VARCHAR(255)\` | Not Null | The human-readable name of the topic (e.g., "Recursion"). |  
| \`dependencies\` | \`ARRAY\[UUID\]\` | | \[cite\_start\]List of other \`trajectory\_id\`s that must be mastered first\[cite: 108\]. |  
\#\#\#\# Table: \`InteractionLog\`  
Logs all chat sessions for analysis and metric calculation.  
| Field | Type | Constraints | Description |  
| \--- | \--- | \--- | \--- |  
| \`log\_id\` | \`BIGSERIAL\` | Primary Key | Unique log entry ID. |  
| \`session\_id\` | \`UUID\` | Not Null | Identifier for a single chat session. |  
| \`student\_id\` | \`VARCHAR(255)\` | Not Null, FK to StudentProfile | The student in the session. |  
| \`timestamp\` | \`TIMESTAMPTZ\` | Not Null | Time of the event. |  
| \`event\_type\` | \`VARCHAR(50)\` | | Type of event (e.g., 'query', 'response', 'quiz\_start'). |  
| \`query\_text\` | \`TEXT\` | | The student's raw query. |  
| \`response\_text\`| \`TEXT\` | | The bot's response. |  
| \`is\_socratic\_flag\` | \`BOOLEAN\` | | \[cite\_start\]True if the response was a guiding question, not a direct answer\[cite: 115\]. |  
| \`metadata\` | \`JSONB\` | | Extra data, e.g., retrieved context chunk IDs, relevance score. |  
I have a detailed PRD draft that follows a specific collaborative workflow structure. I need you to consolidate and restructure this into a cleaner, more concise format that fits our repository's master file structure.  
Please transform my draft into 5 separate clean files:

1. prd.md \- The master consolidated PRD with these sections:  
   * Status, Owner, Vision  
   * Objectives (MVP)  
   * Target Audience  
   * Problem & Motivation  
   * MVP Scope (organized by Student Features, Teacher Features, Governance)  
   * Non-Goals  
   * Success Metrics (use placeholder variables like X%, Y%, Z%)  
   * Assumptions & Constraints  
   * Release Plan (Sprint-based)  
   * Dependencies/Risks  
   * References  
2. glossary.md \- Simplified, concise term definitions (remove citation markers)  
3. dataModel.md \- Entity-focused with:  
   * Clear entity list with fields  
   * Relationships section showing connections between entities  
   * Use simple notation like "1..N" for relationships  
4. system.md \- Architecture-focused with:  
   * High-Level Architecture description  
   * Key APIs section with role and action for each endpoint  
   * Non-Functional Requirements  
   * Safety & Integrity considerations  
5. userStories.md \- Persona-based with:  
   * Clear Personas section  
   * Separate Student Stories and Teacher Stories  
   * Use "As a \[role\], I want to \[action\], so that I can \[benefit\]" format  
   * Add Acceptance Hints section at the end

Key transformations:

* Remove all citation markers \[cite\_start\] and \[cite: X\]  
* Simplify language while keeping all essential information  
* Convert detailed requirements into higher-level capability descriptions  
* Use bullet points more liberally in the master prd.md  
* Make the structure more scannable and digestible  
* Keep technical accuracy but reduce verbosity"

File 1: PRD/prd.md (Clean File)  
Markdown  
\# CourseLLM – Product Requirements Document (PRD)  
\#\# Status  
DRAFT (MVP \- 2025-11-08)  
\#\# Owner  
CourseLLM Project Team  
\#\# Vision  
To help Teachers and Students in a University CS Department better teach and better learn using AI.  
\#\# Objectives (MVP)  
\* \*\*Student Learning:\*\* Enable students in the CS Dept to use the product to learn the material of existing courses more effectively.  
\* \*\*Teacher Enablement:\*\* Enable teachers in the CS Dept to use the product to better teach existing courses.  
\* \*\*Enhancement, Not Replacement:\*\* The product enhances the learning experience around existing material; it does not create new material or replace existing AI tools.  
\#\# Target Audience  
\* \*\*Primary:\*\* Students taking Courses in the CIS Faculty @BGU.  
\* \*\*Secondary:\*\* Teachers of Courses at the CIS Faculty @BGU.  
\#\# Problem & Motivation  
\* \*\*Teacher Concern:\*\* Teachers worry that students may use AI technology as a shortcut to avoid learning, even if they can still fulfill course requirements.  
\* \*\*Student Desire:\*\* Students want enhanced, personalized, and faster access to course material to learn better and deeper.  
\#\# MVP Scope (Capabilities)  
\#\#\# 1\. Student Features  
\* \*\*Scoped Chatbot:\*\* A chatbot restricted to the specific course material.  
    \* Must provide a Socratic learning experience.  
    \* Must \*not\* answer questions directly; instead, it checks for misconceptions and analyzes intentions.  
    \* Answers must be adjusted to the student's current recorded level.  
\* \*\*Personalized Practice:\*\* Generate personalized quizzes, exams, and exercises to master content and verify understanding.  
\* \*\*Platform Assistance:\*\* Help students with course-related logistics, such as installing tools, debugging issues, and submitting assignments.  
\* \*\*Motivation:\*\* Provide context on \*why\* the material is important, beautiful, or relevant.  
\* \*\*Resource Access:\*\* Provide access to additional relevant resources (papers, videos, tutorials).  
\#\#\# 2\. Teacher Features  
\* \*\*Content Preparation:\*\* Allow teachers to upload, prepare, and review the consistency of course content (notes, slides, exams, etc.).  
\* \*\*Learning Trajectories:\*\* Enable teachers to prepare "learning trajectories" (a sequence of topics to be mastered).  
\* \*\*Assignment Generation:\*\* Assist teachers in preparing quizzes, assignments, and exams that are testable, correspond to the material, and are "LLM resilient".  
\* \*\*Progress Monitoring:\*\* Allow teachers to monitor student progress, tracking what skills and content have been acquired against the learning trajectories.  
\* \*\*Integrity Tools:\*\* Assist teachers with grading assignments and detecting cheating.  
\#\#\# 3\. Governance  
\* \*\*RAG Implementation:\*\* All content must be indexed to support a RAG (Retrieval-Augmented Generation) approach.  
\* \*\*Metrics & Logging:\*\* The product must produce logs of activity to monitor student progress and compute metrics that measure value.  
\#\# Non-Goals (MVP)  
\* The product will not create new course material.  
\* The product will not replace existing AI tools like NotebookLM or general-purpose chatbots.  
\#\# Success Metrics (MVP)  
\* \*\*Student Adoption:\*\* X% of students in a pilot course use the Socratic chatbot \> 3 times per week.  
\* \*\*Teacher Engagement:\*\* Y% of teachers in the pilot program successfully upload their course content and define at least one "learning trajectory."  
\* \*\*Learning Efficacy:\*\* Z% of students who use the personalized quiz feature show measurable improvement in knowledge mastery.  
\* \*\*Scope Adherence:\*\* \>99% of chatbot answers are successfully filtered to be within the scope of the course material.  
\#\# Assumptions & Constraints  
\* \*\*Content Source:\*\* Teachers must provide all course content (notes, slides, etc.) for the system to be effective.  
\* \*\*Chatbot Scope:\*\* The chatbot's scope \*must\* be strictly restricted to the provided course material.  
\* \*\*Learning Model:\*\* The chatbot must \*not\* answer questions directly and must adhere to a Socratic learning model.  
\#\# Release Plan (MVP)  
\* \*\*Sprint 1 (Wk 1-2):\*\* Ingestion pipeline (teachers upload content) and RAG indexing.  
\* \*\*Sprint 2 (Wk 3):\*\* Core Socratic chatbot (student-facing) with scope enforcement.  
\* \*\*Sprint 3 (Wk 4):\*\* Learning Trajectories and Student Progress Monitoring (v1).  
\* \*\*Sprint 4 (Wk 5):\*\* Personalized Quiz Generation (student) and Assignment Generation (teacher).  
\* \*\*Sprint 5 (Wk 6):\*\* Pilot launch with one CS course.  
\#\# Dependencies / Risks  
\* \*\*Risk:\*\* Poor quality or incomplete course materials uploaded by teachers will lead to a poor chatbot experience.  
\* \*\*Risk:\*\* The Socratic model may frustrate students who want a quick answer.  
\* \*\*Dependency:\*\* Requires a robust indexing and RAG system to ensure answers are grounded.  
\#\# References  
\* CourseLLM Project Brainstorm Notes (02 Nov 2025).  
\* PRD Workflow & Guidelines.  
File 2: PRD/glossary.md (Clean File)  
Markdown  
\# Glossary  
\- \*\*Learning Trajectories\*\*: A sequence of topics, ordered by dependency, that are to be mastered by the students.  
\- \*\*LLM Resilient\*\*: A quality of an assignment (quiz, exam) verifying that it is testable, corresponds to the material, and is designed to be difficult to solve correctly using a standard Large Language Model.  
\- \*\*RAG (Retrieval-Augmented Generation)\*\*: The technical approach of indexing the course material to support the chatbot, ensuring answers are grounded in provided documents.  
\- \*\*Socratic Learning Experience\*\*: An interaction style for the chatbot where it avoids answering questions directly. Instead, it guides the student by checking for misconceptions and analyzing the perspectives behind the student's questions.  
\- \*\*Student Progress Monitoring\*\*: The process of checking what a student knows and where they are lacking knowledge, and keeping track of acquired skills and content.  
File 3: PRD/dataModel.md (Clean File)  
Markdown  
\# Data Model (MVP)  
\#\# Entities  
\* \*\*Student\*\* (student\_id, name, enrolled\_course\_ids)  
\* \*\*Teacher\*\* (teacher\_id, name, course\_ids)  
\* \*\*Course\*\* (course\_id, teacher\_id, title, material\_ids, trajectory\_ids)  
\* \*\*CourseMaterial\*\* (material\_id, course\_id, source\_type \[notes, slides, exam, quiz\], original\_filename, status \[uploaded, indexed\])  
\* \*\*MaterialChunk\*\* (chunk\_id, material\_id, chunk\_text, text\_vector, metadata\_json)  
\* \*\*LearningTrajectory\*\* (trajectory\_id, course\_id, name, topic\_sequence\_json \[e.g., {"topic1": {"depends\_on": \[\]}}\])  
\* \*\*StudentProgress\*\* (progress\_id, student\_id, course\_id, knowledge\_level, acquired\_skills\_map, current\_trajectory\_node)  
\* \*\*Assignment\*\* (assignment\_id, course\_id, type \[quiz, exam\], is\_llm\_resilient\_flag, items\_json)  
\* \*\*ChatSession\*\* (session\_id, student\_id, course\_id, start\_time, end\_time)  
\* \*\*ChatLog\*\* (log\_id, session\_id, timestamp, query\_text, response\_text, is\_socratic, is\_off\_topic\_flag)  
\#\# Relationships  
\* \*\*Teacher\*\* 1..N \*\*Course\*\*  
\* \*\*Course\*\* 1..N \*\*Student\*\* (via enrollment, managed by \`Student.enrolled\_course\_ids\`)  
\* \*\*Course\*\* 1..N \*\*CourseMaterial\*\*  
\* \*\*CourseMaterial\*\* 1..N \*\*MaterialChunk\*\*  
\* \*\*Course\*\* 1..N \*\*LearningTrajectory\*\*  
\* \*\*Course\*\* 1..N \*\*Assignment\*\*  
\* \*\*Student\*\* 1..N \*\*StudentProgress\*\* (one per course)  
\* \*\*Student\*\* 1..N \*\*ChatSession\*\*  
\* \*\*ChatSession\*\* 1..N \*\*ChatLog\*\*  
File 4: PRD/system.md (Clean File)  
Markdown  
\# System Perspective  
\#\# High-Level Architecture (MVP)  
\* \*\*Ingestion Pipeline\*\*  
    \* Teachers upload course files (notes, documents, exams, slides, etc.).  
    \* System reviews material for consistency.  
    \* System indexes all material to support a RAG approach.  
\* \*\*Scoped RAG Chatbot\*\*  
    \* Queries are checked against course scope; non-related questions are filtered out.  
    \* A Socratic orchestrator prevents direct answers and probes for misconceptions.  
\* \*\*Personalization Engine\*\*  
    \* Retrieves \`StudentProgress\` to adjust the chatbot's answers to the student's current level.  
    \* Logs student skills and content acquisition back to the \`StudentProgress\` profile.  
\* \*\*Teacher Console\*\*  
    \* A dashboard for teachers to monitor student progress and define "learning trajectories".  
    \* An interface to generate "LLM resilient" assignments.  
\#\# Key APIs (Sketch)  
\* \`POST /api/course/{id}/upload\`  
    \* \*\*Role:\*\* Teacher  
    \* \*\*Action:\*\* Uploads course materials. Triggers indexing job.  
\* \`POST /api/course/{id}/chat\`  
    \* \*\*Role:\*\* Student  
    \* \*\*Action:\*\* Submits a query. System returns a Socratic response.  
\* \`GET /api/student/{id}/progress?course={id}\`  
    \* \*\*Role:\*\* Student (self), Teacher (all students)  
    \* \*\*Action:\*\* Retrieves current progress on learning trajectories.  
\* \`POST /api/course/{id}/quiz/generate\`  
    \* \*\*Role:\*\* Student  
    \* \*\*Action:\*\* Generates a personalized quiz.  
\* \`POST /api/course/{id}/assignment/generate\`  
    \* \*\*Role:\*\* Teacher  
    \* \*\*Action:\*\* Generates a draft, LLM-resilient assignment.  
\#\# Non-Functional Requirements  
\* \*\*Scope Enforcement:\*\* The system \*must\* filter out questions not related to the course.  
\* \*\*Socratic Adherence:\*\* The chatbot \*must not\* answer questions directly.  
\* \*\*Personalization:\*\* All Socratic responses \*must\* be adjusted based on the student's recorded knowledge level.  
\#\# Safety & Integrity  
\* \*\*Cheating Detection:\*\* The system must provide features to assist teachers in detecting cheating.  
\* \*\*Assignment Validation:\*\* All teacher-generated assignments must be verified as testable and corresponding to the taught material.  
File 5: PRD/userStories.md (Clean File)  
Markdown  
\# User Stories  
\#\# Personas  
\* \*\*Student:\*\* An enrolled student in a CS Faculty course at BGU.  
\* \*\*Teacher:\*\* A teacher or TA for a CS Faculty course at BGU.  
\#\# Student Stories  
\* \*\*As a Student, I want to\*\* chat about my course material, \*\*so that I can\*\* learn the material better and deeper.  
\* \*\*As a Student, I want to\*\* receive Socratic guidance instead of direct answers, \*\*so that I can\*\* identify my own misconceptions and learn to solve problems myself.  
\* \*\*As a Student, I want to\*\* generate personalized quizzes, \*\*so that I can\*\* verify that I have mastered the content.  
\* \*\*As a Student, I want to\*\* get help with installing tools and debugging issues, \*\*so that I can\*\* make using the course "platform" easier.  
\* \*\*As a Student, I want to\*\* ask "Why is this important?", \*\*so that I can\*\* feel motivated and understand the context of what I'm learning.  
\#\# Teacher Stories  
\* \*\*As a Teacher, I want to\*\* upload all my course files (notes, slides, exercises), \*\*so that I can\*\* ensure the chatbot's scope is strictly restricted to my material.  
\* \*\*As a Teacher, I want to\*\* prepare "learning trajectories", \*\*so that I can\*\* define the sequence of topics my students should master.  
\* \*\*As a Teacher, I want to\*\* generate "LLM resilient" assignments, \*\*so that I can\*\* trust that my students are learning the material without taking shortcuts.  
\* \*\*As a Teacher, I want to\*\* monitor student progress, \*\*so that I can\*\* check what skills they have acquired and where they are lacking knowledge.  
\* \*\*As a Teacher, I want\*\* help detecting cheating and grading assignments, \*\*so that I can\*\* focus more on teaching.  
\#\# Acceptance Hints (MVP)  
\* A student query that is off-topic (e.g., "What's the weather?") \*must\* be filtered and refused.  
\* A student query asking for a direct answer (e.g., "What is the answer to HW1 Q3?") \*must\* be refused, and the bot must respond with a Socratic question.  
\* A generated personalized quiz \*must\* be based on the student's current recorded knowledge level.  
\* A teacher \*must\* be able to upload a PDF and have its content be part of the chatbot's knowledge base.  
