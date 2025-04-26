# AI Resume Expert: Builder & Analyzer Prompts
**Version:** 1.2 (Reflects latest `Resume_Analysis_Expert_Prompt`)

<!-- ![Banner Image](assets/banner.png) -->

[![Version](https://img.shields.io/badge/version-1.0.0-blue)](https://github.com/zx0r/LinkedIn-AI-Prompts)
[![License](https://img.shields.io/badge/license-MIT-green)](LICENSE)
[![ATS Score](https://img.shields.io/badge/ATS_Score-100%2F100-brightgreen)](README.md#ats-optimisation-score)
![LinkedIn](https://img.shields.io/badge/-LinkedIn-blue?logo=linkedin) 
![Greenhouse](https://img.shields.io/badge/-Greenhouse-23D49B)
![Workday](https://img.shields.io/badge/-Workday-2D5DF5)

## Project Description

This project provides two sophisticated prompt templates designed to interact with a Large Language Model (LLM) acting as an **Expert Career Advisor**. The advisor specializes in **Artificial Intelligence (AI), Natural Language Processing (NLP), and Machine Learning (ML)** roles, possesses deep knowledge of modern **Applicant Tracking Systems (ATS)**, and understands **Talent Acquisition** strategies within the tech industry.

The core goal is to leverage this expert AI persona to:
1.  Provide actionable recommendations for **improving and optimizing** an existing resume (`Resume_Builder_Expert_Prompt`).
2.  Conduct a **comprehensive analysis and assessment** of an existing resume's effectiveness (`Resume_Analysis_Expert_Prompt`).

Both prompts are specifically tailored for candidates targeting technical roles in the competitive AI/ML/NLP space.

## Core Concepts & Features

*   **Expert AI Persona:** The AI adopts the role of a seasoned career advisor with specific expertise in AI/ML/NLP hiring, ATS intricacies, and recruiter behavior.
*   **Domain Focus:** Specifically designed for resumes targeting AI, Machine Learning, and Natural Language Processing positions.
*   **Advanced ATS Knowledge:** The prompts instruct the AI to consider various ATS parsing mechanisms:
    *   Keyword Matching (Frequency, Relevance)
    *   Semantic Similarity (Vector Embeddings like Word2Vec/GloVe, Transformer models like BERT/SBERT/SESA)
    *   Transformer-based Ranking (Contextual understanding like LinkedIn's LiGR)
    *   Fairness Considerations
*   **Recruiter Behavior Insights:** The analysis incorporates factors like recruiter skim-reading patterns, profile completeness, click-through rates (CTR), the impact of action verbs, and the importance of quantification.
*   **Actionable Feedback:** Both prompts aim to provide specific, concrete feedback that the user can directly implement.
*   **Context-Aware Analysis:** The quality and specificity of the feedback significantly increase when target job roles and descriptions are provided.

## Prompts Overview

This project includes two distinct prompt templates:

1.  **`Resume_Builder_Expert_Prompt`:**
    *   **Goal:** To analyze an existing resume and provide highly specific, actionable **recommendations for improvement and rewriting**.
    *   **Output:** Focuses on suggesting *how* to enhance different sections (Summary, Skills, Experience, Projects, Education) with rewritten examples, keyword suggestions, and quantification advice, all tailored for AI/ML/NLP roles and ATS optimization.

2.  **`Resume_Analysis_Expert_Prompt`:**
    *   **Goal:** To perform a comprehensive, deep-level **analysis and assessment** of the resume's current state and effectiveness.
    *   **Output:** Provides a structured report including overall assessment, detailed analysis of each section (including skills inventory and proficiency estimation), identification of strengths and weaknesses, ATS optimization checks (with score), course/certification recommendations, an overall resume score, and *conditional analyses* comparing the resume against a specific target role or job description if provided.

```bash
You are an experienced resume analyst with deep knowledge of industry standards, job requirements, and ATS (Applicant Tracking System) optimization practices.
Your task is to provide a **comprehensive and detailed analysis** of the provided resume, identifying both strengths and areas for improvement.

Structure your response as follows:
[Provide a detailed evaluation of the resume’s quality, structure, and formatting. Highlight key issues (e.g., formatting errors, lack of organization), and suggest potential improvements.]
[Analyze the candidate's career trajectory, professional summary, and career goals. Explain how clearly their career progression is presented and whether it aligns with their stated objectives.]

Skills Evaluation:
- Current Skills: [List all skills demonstrated in the resume, categorized by type (technical skills, soft skills, domain-specific knowledge, programming languages, tools, etc.).]
- Skill Proficiency: [Assess the level of expertise in key skills based on how they are presented.]
- Missing Skills: [Identify important skills that are missing for the target role. Explain why each is important.]

Experience:
[Analyze the experience section for clarity, impact, and relevance. Focus on action verbs, quantifiable achievements, and how well the experience aligns with the candidate's target role. Suggest improvements.]

Education:
[Review the education section, including the relevance of degrees, certifications, and any missing educational elements that could strengthen the profile.]

Key Strengths:
[List 5-7 specific strengths of the resume, explaining why they are effective and how they contribute to the overall impact of the document.]

Areas for Improvement and Violations:
[List 5-7 specific issues or violations (e.g., formatting problems, vague descriptions, lack of quantifiable data). Provide clear recommendations for improvement.]

ATS (Applicant Tracking System) Optimization Evaluation:
- ATS Score: XX/100
- Issues Identified: [Point out formatting issues, missing keywords, or any other factors that may affect ATS performance.]
- Recommendations: [Suggest changes in keywords, section structure, and other adjustments to enhance ATS performance.]

Recommended Courses and Certifications:
[Suggest 5-7 specific courses or certifications that would enhance the candidate's profile, with brief explanations of why each would be valuable.]

Final Resume Score:
Resume Score: XX/100
- 85–100: Excellent resume (ready to send with minor adjustments)
- 75–84: Good resume (requires moderate improvements)
- 60–74: Average resume (requires significant improvements)
- <60: Poor resume (needs complete overhaul)

Resume for analysis:
{resume_text}
```

## Persona Details

The AI acts as an **Expert Career Advisor & Resume Strategist** with:
*   Specialization in AI/NLP/ML recruitment.
*   Experience in Talent Acquisition for top tech companies.
*   Technical understanding of modern ATS (keyword, semantic, transformer-based).
*   Awareness of recruiter metrics and behaviors (search ranking factors, CTR, quantification value).

## Input Variables

Both prompts utilize the following input variables:

*   `resume_text` (**Required**): The full plain text content of the candidate's resume.
*   `target_job_role` / `job_role` (**Optional, Highly Recommended**): The specific job title the candidate is targeting (e.g., "Machine Learning Engineer", "NLP Scientist").
*   `target_job_description` / `job_description` (**Optional, Highly Recommended**): The full text of a specific job description the candidate is interested in.

**Note:** Providing the optional variables significantly enhances the specificity and accuracy of the AI's feedback, especially regarding keyword alignment, skill gaps, and ATS performance for a particular target.

## How to Use

1.  **Choose the Right Prompt:**
    *   Use `Resume_Builder_Expert_Prompt` when you want specific guidance on *how to rewrite and improve* your resume sections.
    *   Use `Resume_Analysis_Expert_Prompt` when you want a detailed *assessment* of your resume's current strengths, weaknesses, ATS compatibility, and alignment with specific roles/jobs.
2.  **Prepare Inputs:**
    *   Extract the **plain text** from your resume. Avoid submitting formatted text directly from PDF/DOCX if possible, as formatting can interfere with analysis. Focus on the content.
    *   Identify a specific `target_job_role` if you have one.
    *   Copy the full text of a relevant `target_job_description` if available.
3.  **Execute the Prompt:** Provide the inputs to the chosen prompt template within your LLM interface.
4.  **Review the Output:** Carefully read the AI's analysis and recommendations.
5.  **Implement & Iterate:**
    *   Apply the actionable suggestions to improve your resume.
    *   Consider using the `Resume_Analysis_Expert_Prompt` after making changes suggested by the `Resume_Builder_Expert_Prompt` to assess the improvements.
6.  **Verify:** Always use your own judgment and verify the technical accuracy of suggestions. The AI provides expert *guidance*, but the candidate is the final owner of the resume content.
7.  **Leverage Context:** Remember that providing the `target_job_role` and `target_job_description` unlocks the most powerful and tailored feedback, especially the conditional analysis sections in `Resume_Analysis_Expert_Prompt`.

## Key Differences Between Prompts

| Feature                  | `Resume_Builder_Expert_Prompt`  | `Resume_Analysis_Expert_Prompt`           |
| :----------------------- | :-------------------------------------- | :---------------------------------------------- |
| **Primary Goal**         | Improvement & Rewriting Guidance        | Comprehensive Analysis & Assessment             |
| **Output Focus**         | Actionable "how-to" suggestions, examples | Structured report, scores, detailed breakdown   |
| **Key Sections**         | Recommendations per resume section      | Assessment, Skills Inventory, Strengths/Weaknesses, ATS Score, Resume Score, Conditional Analyses |
| **Scoring**              | Estimated ATS Score                     | Estimated ATS Score, Overall Resume Score       |
| **Conditional Analysis** | No (implicit use of context)            | Yes (explicit sections for Role/JD match)       |
| **Use Case**             | Actively improving/editing the resume   | Diagnosing current state, checking alignment |

## Technical Foundations

The effectiveness of these prompts relies on the LLM's ability to understand and apply concepts related to:
*   Natural Language Processing (for analyzing resume and job description text)
*   Information Retrieval (simulating keyword and semantic search)
*   Machine Learning Concepts (understanding the domain)
*   Simulated Reasoning (adopting the persona and applying recruitment knowledge)

#### Features

- **Prompt Templates**: Predefined prompts tailored for various industries and roles.
- **Interactive Mode**: Step-by-step guidance to input your information seamlessly.
- **ATS Optimization**: Ensures resumes are formatted and keyword-optimized for ATS compatibility.
- **Platform Alignment**: Tailors resumes to meet the standards of platforms like LinkedIn.

#### Getting Started

When crafting prompts for Large Language Models (LLMs) to generate or update resumes, both explicit variable specification and interactive input methods have their distinct advantages. The choice between them depends on the desired level of control, user engagement, and the complexity of the task.

**Explicit Variable Specification:**

By clearly defining variables such as [Target Role], [Target Industry], and [Current Resume] within the prompt, you provide the LLM with structured and comprehensive context. This approach ensures that the model understands the specific requirements upfront, leading to more accurate and tailored responses. Explicit prompts reduce ambiguity, allowing the model to focus on generating content that aligns closely with the provided parameters. This method is particularly effective when the input data is complete and well-defined.​

**Interactive, Step-by-Step Input:**

Engaging in a dynamic dialogue with the LLM, where information is gathered iteratively, can enhance the depth and relevance of the generated resume. This method, known as interactive or progressive prompting, allows for real-time clarification and refinement of details. It is especially beneficial when dealing with complex scenarios or when the initial information is incomplete. By breaking down the task into manageable steps, the model can address each aspect thoroughly, leading to a more personalized and accurate output. This approach mirrors the concept of "Chain-of-Thought Prompting," where complex problems are divided into logical steps, facilitating better reasoning and coherence in responses. ​

**Combining Both Approaches:**

Integrating explicit variable specification with interactive input can leverage the strengths of both methods. Starting with a structured prompt to establish the foundational context, followed by interactive exchanges to refine and elaborate on specific details, can result in a highly customized and effective resume. This hybrid approach ensures that the LLM has a clear understanding of the core requirements while remaining flexible to adapt to additional information or changes provided during the interaction.​

**Conclusion:**

Both explicit variable specification and interactive input methods are suitable for creating or updating resumes using LLMs. The optimal choice depends on the specific use case:​

- Use explicit variables when you have all necessary information upfront and seek a straightforward, structured output.​
- Opt for interactive input when details are evolving, require clarification, or when a more personalized approach is desired.​

By understanding and applying these prompting techniques, you can effectively guide LLMs to produce resumes that are well-aligned with targeted roles and industries.​

---

LinkedIn profiles are structured to mirror traditional CV sections, facilitating a comprehensive presentation of professional qualifications. The primary LinkedIn sections and their CV counterparts are:

1. **Introduction Section**:
   - **LinkedIn**: This top section includes your Name, Profile Photo, Background Photo, Headline, Current Position, Education, Location, Industry, and Contact Info.
   - **CV Equivalent**: Contact Information

2. **About Section**:
   - **LinkedIn**: A summary that provides an overview of your professional background, skills, and career objectives.
   - **CV Equivalent**: Personal Statement or Summary

3. **Experience Section**:
   - **LinkedIn**: Detailed descriptions of your work history, including job titles, company names, durations, and key responsibilities or achievements.
   - **CV Equivalent**: Professional Experience

4. **Education Section**:
   - **LinkedIn**: Information about your academic background, degrees earned, institutions attended, and years of study.
   - **CV Equivalent**: Academic History

5. **Skills Section**:
   - **LinkedIn**: A list of your professional skills, which can be endorsed by connections to validate your expertise.
   - **CV Equivalent**: Key Skills and Qualifications

6. **Licenses & Certifications**:
   - **LinkedIn**: Details of any professional certifications or licenses you've obtained.
   - **CV Equivalent**: Professional Certifications

7. **Projects**:
   - **LinkedIn**: Descriptions of significant projects you've worked on, highlighting your role and the outcomes.
   - **CV Equivalent**: Projects

8. **Publications**:
   - **LinkedIn**: Citations or links to articles, research papers, or books you've authored or contributed to.
   - **CV Equivalent**: Publications

9. **Honors & Awards**:
   - **LinkedIn**: Recognition or awards received for professional achievements.
   - **CV Equivalent**: Industry Awards

10. **Volunteer Experience**:
    - **LinkedIn**: Information about unpaid work or community service roles you've undertaken.
    - **CV Equivalent**: Volunteering Experience

11. **Languages**:
    - **LinkedIn**: Languages you are proficient in.
    - **CV Equivalent**: Languages

12. **Organizations**:
    - **LinkedIn**: Professional associations or groups you are a member of.
    - **CV Equivalent**: Professional Affiliations

By aligning these sections appropriately, you can ensure consistency between your LinkedIn profile and your CV, presenting a cohesive and professional image to potential employers.

---

##### Recommended Layout (Clean ATS-Friendly Style):
```bash
[Full Name] | Location | Phone | Email | GitHub | LinkedIn

⚡ Professional Summary
- Short and impactful 3–4 line summary tailored to the target job.

🛠️ Skills
- Bullet-list or categorized by technical domain (e.g., Languages, Tools, Infrastructure).

💼 Experience
Company Name – Role
Date Range
- Impact-oriented bullet points with metrics, tools used, and outcomes.

📁 Projects (for AI/Tech Roles)
- Title | Tools Used
- 1–2 bullets on what you did, tech stack, and value.

🎓 Education
Degree or Field – Institution
Dates | Relevant coursework or certifications (if recent).

🏅 Certifications / Languages / Achievements (Optional)
```
---

**Summary**
##### 🧠 1. AI / Prompt Engineering / LLMs
Infrastructure-first engineer skilled in Unix systems, automation, and AI tooling. Translates abstract concepts into scalable LLM pipelines using structured thinking, rapid prototyping, and prompt-driven iteration.

##### 💸 2. FinTech / Platform Engineering / DevOps
Systems engineer with deep Unix/Linux expertise and a focus on secure, high-availability infrastructure. Converts technical complexity into scalable solutions through disciplined execution, planning, and quantifiable outcomes.

##### 🚀 3. Startup / Generalist / Tech Stack Flexibility
Agile infrastructure engineer blending Unix mastery with cross-platform customization and self-directed problem solving. Delivers efficient, scalable systems through rapid prototyping and structured analysis.

💼 **Happy offers for your dream job**
