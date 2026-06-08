SmartLens — Project Retrospective
Project: SmartLens — AI-Powered SME Financial Intelligence Dashboard  
Project Manager: Maxine Mutasa  
Date: May–June 2026  
Duration: 4 weeks  
Format: Solo project retrospective
---
1. Project Summary
SmartLens was a 4-week self-managed project to design and deliver an AI-powered Power BI dashboard for Zimbabwean SMEs. The project was completed on schedule, with all 8 planned deliverables delivered including a published Power BI dashboard, a simulated financial dataset, a full PM artifact suite, and an AI insight layer powered by the Claude API.
---
2. What Went Well ✅
Full PM process followed from day one  
Starting with a project charter before writing a single line of code forced clarity on scope, stakeholders, and success criteria early. This prevented scope creep and kept the project focused throughout all 4 weeks.
Data preparation applied real learning  
Using Microsoft Excel to simulate and clean the dataset directly applied skills from the Microsoft Power BI Data Analyst Professional Certificate. The process of structuring data correctly for Power BI import reinforced concepts around data types, null handling, and table relationships.
AI integration exceeded expectations  
The Claude AI API integration on Page 4 worked on the first successful attempt and produced genuinely useful, contextually accurate insights from the financial data. This was the most technically ambitious part of the project and became its strongest differentiator.
PM artifacts added real credibility  
Having a project charter, scope document, Gantt chart, risk register, and stakeholder personas gave the project structure and professionalism that a typical developer portfolio piece lacks. The artifacts tell the story of how the project was managed, not just what was built.
Hyperlocal relevance made the project stand out  
Anchoring the project in the Zimbabwean SME context — using local currency, realistic Harare-based business patterns, ZESA electricity tariffs, and Zimbabwe's construction season — made the problem statement authentic and differentiated the project from generic tutorial-based portfolio pieces.
---
3. What Could Have Gone Better ⚠️
Expense simulation logic had a flaw  
The Python script used to simulate the dataset generated expense totals higher than intended due to how multi-payment transactions were calculated. This resulted in total expenses ($265,542) exceeding total revenue ($253,100), producing a negative gross profit. While this created an interesting and realistic financial stress scenario, it was not the original intention and was only discovered after the data was loaded into Power BI.
Lesson: Always validate simulated data against expected ranges before importing into any BI tool. A simple summary check (total revenue vs total expenses) should have been run immediately after generation.
Power BI forecasting required a workaround  
The built-in Power BI forecast feature only works with continuous date fields, not text-based month names. This required changing the X-axis on the cash flow chart from Month Name to Date, which affected the visual presentation. More time should have been allocated to understanding Power BI's forecasting constraints before the build phase.
Lesson: Research tool-specific constraints during the planning phase, not during the build.
Publishing required an organisational email  
Power BI Service requires a work or school email for publishing, which was not anticipated in the project plan. This added an unplanned step of setting up a Microsoft 365 developer account, consuming time that was not budgeted.
Lesson: Validate tool access requirements (accounts, licensing, permissions) during Week 1 planning, not at the point of delivery.
Python environment setup was time-consuming  
Configuring Python for Power BI visuals required installing multiple libraries (matplotlib, pandas, anthropic) that were not pre-installed. Each missing library only surfaced as an error at runtime, creating an inefficient debug loop.
Lesson: For Python-dependent deliverables, set up and test the environment at the start of the build phase, not when the visual is ready to run.
---
4. Key Learnings 💡
Project management disciplines are not bureaucracy — they are insurance  
Every time the project felt pressured for time, having a clear scope document and Gantt chart made it easy to decide what to prioritise and what to defer. The risk register identified the scope creep risk in Week 1 — and that risk nearly materialised twice during the build phase.
Data quality is the foundation of every BI project  
No amount of DAX sophistication or AI integration fixes bad data. The expense simulation flaw demonstrated that data preparation is not a checkbox step — it requires validation, sanity checking, and iteration.
AI as a feature changes what a dashboard can do  
Integrating an LLM into the dashboard transformed it from a reporting tool into an advisory tool. The AI insights page answers the question "so what?" — which is ultimately what every business stakeholder wants to know. This is a pattern worth applying to future data projects.
Hyperlocal context is a competitive advantage  
Building for a specific, underserved market (Zimbabwean SMEs) made every design decision more intentional. The problem was real, the data was grounded, and the insights were relevant. Generic portfolio projects feel like exercises; contextualised ones feel like solutions.
---
5. What I Would Do Differently
Decision	What I'd change
Dataset simulation	Validate totals immediately after generation before importing
Tool research	Research Power BI Service licensing requirements in Week 1
Python setup	Install and test all Python dependencies at the start of Week 3
Forecast visual	Plan for continuous date axis from the start rather than retrofitting
Timeline	Add a dedicated half-day QA/testing step before the publishing milestone
---
6. Success Against Original Criteria
Success Criterion	Achieved?
All 8 deliverables completed within 4 weeks	✅ Yes
Power BI dashboard published and accessible	✅ Yes
AI insight layer generates meaningful summaries	✅ Yes
Full PM artifact suite documented	✅ Yes
Project added to GitHub with detailed README	✅ Yes
Post-project retrospective completed	✅ Yes (this document)
---
7. Final Reflection
SmartLens achieved everything it set out to do. More importantly, it demonstrated that data analytics and project management are not separate disciplines — the best data projects are managed well, and the best PM portfolios include real, measurable deliverables.
The negative profit margin in the dataset, while unintended, ended up creating a more compelling and realistic use case. A business under financial stress needs financial intelligence more urgently than a profitable one — which is exactly the argument for SmartLens's existence.
This project has strengthened my confidence in both Power BI and end-to-end project delivery, and has given me a tangible, documented case study to present to employers in data analytics and project management roles.
---
Prepared by Maxine Mutasa | May–June 2026
