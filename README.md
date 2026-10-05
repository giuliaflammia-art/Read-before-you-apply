<!-- This is the markdown template for the final project of the Building AI course, 
created by Reaktor Innovations and University of Helsinki. 
Copy the template, paste it to your GitHub README and edit! -->

# Read Before You Apply

*From job application to informed decision*

Building AI course project

## Summary

An AI system that helps candidates analyze job ads more clearly and transparently, organizing information, identifying gaps and ambiguities, and suggesting aspects to explore so they can make an informed decision and understand where it is worth investing their time.

## Background

Job searching has become an activity that requires a significant amount of time and energy from candidates. Even before applying, candidates need to analyze and interpret numerous job ads, understand whether they have the required skills and whether their profile is a good fit for the role, look for additional information about the company, and, in many cases, complete forms, tests, and various other steps in the application process. For people looking for work, this activity can be repeated across numerous applications, making the evaluation of opportunities a significant part of the job search process.

This investment of time is made even more difficult by the fact that job ads do not always provide sufficiently clear and complete information. Salary or contract type may not be specified; responsibilities may be described in generic terms or cover very different professional areas without clarifying which one is the main focus; essential and preferred requirements may not be clearly distinguished. Information about the organization of work and the selection process is also often missing or lacking in detail, while some formulations may be ambiguous.

Candidates therefore have to invest time in evaluating an opportunity without necessarily having a sufficiently clear picture of the role, its conditions, and what to expect during the selection process. This creates an information asymmetry: the company has information about the role and the process that the candidate may not always be able to know before applying.

The idea also comes from the experience of job searching and from observing how much time and energy candidates may have to invest in evaluating opportunities and going through application processes.

The problem, therefore, is not only about finding a job opportunity, but also about being able to **understand where it is worth investing one's time**. An AI-based system could help reduce this asymmetry by organizing the information contained in job ads, highlighting what is not specified or what may be ambiguous, and helping candidates identify which aspects to explore further and which questions to ask the company before deciding how to proceed.


## How is it used?

### Use and context

The system is designed for **people looking for work**, particularly candidates who have to evaluate many opportunities and may have difficulty quickly understanding whether a job ad contains sufficient and relevant information.

It can be used before deciding how much time and energy to invest in an application.

The process follows four stages:

- **Read:** the candidate enters the text of the job ad.
- **Understand:** the system organizes the information provided and highlights any ambiguities or missing information.
- **Question:** the system suggests which aspects may be worth exploring further and which questions to ask the company.
- **Decide:** the candidate uses this information to independently assess whether and how to proceed.

The goal is not to replace the candidate's decision, but to **put them in a position to make a more informed decision**.

### People affected

The people directly affected by the project are therefore **job seekers**, especially those who have to deal with a long and demanding job search, analyze numerous job ads, and make decisions based on information that is often incomplete or unclear.


## Data sources and AI methods

### Input

The system uses the **text of the job ad** as its main input. Through Natural Language Processing (NLP), the text is transformed into structured information.

### Information extracted

The system identifies, when present:

| Category | Examples |
|---|---|
| Role | Content Specialist |
| Responsibilities | SEO, content creation, analytics |
| Requirements | skills and qualifications |
| Experience | 3–5 years |
| Contract | full-time, temporary, etc. |
| Salary | if specified |
| Work arrangement | remote, hybrid, on-site |

The system also identifies missing information, ambiguous wording, and elements that require further investigation, turning them, when possible, into questions to ask the company.

### AI techniques

The project uses **Natural Language Processing (NLP)** techniques and mainly combines two operations:

- **Classification:** recognizing what type of information a part of the text contains.
- **Information extraction:** extracting the specific information contained in that part.

For example:

> “3–5 years of SEO experience required”

can be classified as a **requirement**, while the extracted information is **3–5 years** and **SEO**.

### Training data

Training would require a dataset of **labeled job ads**, divided between data used for training and data used to evaluate the system's performance on ads that were not seen during training.

The project would require a dataset from a public source or an existing dataset. **The choice of source and the relevant terms of use would need to be defined before implementation.**

### Model

Given the need to interpret linguistic context, the project could use a **neural network for NLP based on a transformer architecture**, which the course presents as particularly suitable for natural language processing tasks.

### Evaluation

Evaluation should not consider only the overall percentage of correct classifications, but also **the nature and importance of the errors**. For example, incorrectly interpreting the type of contract can have different consequences from making an error concerning a secondary requirement.

## Challenges

### Understanding context

Natural language can be ambiguous, and the system may incorrectly interpret the meaning of a sentence when context is important. For example, *“SEO experience is required”* and *“SEO experience is not required”* contain similar words, but have opposite meanings.

### Classification and extraction errors

The system may make errors when classifying or extracting information from a job ad. However, not all errors have the same relevance: an error concerning the type of contract may be more important than an error concerning a secondary requirement.

### Quality of training data

The results depend on the quality and variety of the data used for training. A dataset that is not sufficiently representative could make the system less effective when analyzing certain types of job ads.

### Missing information

The system can identify that a piece of information is not present in the job ad, but it cannot automatically know why it is missing.

For example:

> **“The salary is not specified in the job ad.”**

should not become:

> **“The company does not want to disclose the salary.”**

This distinction is essential to prevent the system from turning an absence of information into an interpretation that is not supported by the data.

### The candidate remains the decision-maker

The system should not determine whether an offer is good or bad, or whether the candidate should apply. Its role is to provide clearer and more structured information that allows the candidate to make an informed decision independently.

### Assessing the scope of a role

The system can highlight when a job ad includes responsibilities belonging to different professional areas, but it cannot automatically determine that a company is asking for “too much.” Making such an assessment would require comparing the job ad with external data about the job market, which represents a possible future development of the project.

These limitations also have an ethical dimension: the system should always distinguish between information contained in the job ad and interpretations, avoiding presenting as facts conclusions that cannot be supported by the data.

## What next?

The project could be further developed in several directions:

- **Public information about the company:** integrate publicly available online sources to provide candidates with additional information about the company, always distinguishing between information provided by the company and information from other sources.
- **Experiences of people who have worked at the company:** collect structured and concrete experiences relating, for example, to the selection process, tests, response times, and the actual responsibilities of the role, while avoiding turning the system into a review aggregator.
- **Comparison with the job market:** compare the job ad with similar ads to provide context about the skills required and the scope of different roles, without turning the comparison into a judgment of the offer.
- **Larger and more representative datasets:** improve the system through larger and more diverse datasets in order to reduce the limitations related to the quality and representativeness of the training data.

Developing these extensions would require skills in software development, NLP, data management and evaluation, as well as collaboration with people with expertise in recruitment and the job market. 


## Acknowledgments

Building AI, Elements of AI 
