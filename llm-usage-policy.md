# Large Language Models usage policy

## Introduction
---
In this article, we would like to discuss the use of third-party language models for conducting research, developing projects and writing code.

This topic has been addressed in the context of running implementation projects as well as the **educational** role the research club plays for its members.

According to [AGH Guidelines on the responsible use of artificial intelligence](https://www.agh.edu.pl/home/ckim/aktualnosci_i_wydarzenia/2025/0204/Wytyczne_GenAI_dla_AGH.pdf)
we have decided to provide a brief overview of how the guidelines have been applied to the activities of the research society. We are also expanding these standards to bring them into line with both academic research and modern market requirements.

## Research Projects
---
Such projects in research societies have two objectives: to advance a particular field of science or to create a useful tool, and in every case  to provide opportunities for team members to develop their skills in that field.

It is important to not forget about dynamic situation in IT which enables the automation and improvement of work using the available tools.

For this reason, generative artificial intelligence should be approached in such a way as to strike a balance between completing the project as a finished piece of work and gaining experience in developing new solutions and acquiring subject-specific knowledge.
## Doing research
---
LLMs may be used as auxiliary tools for literature mapping, brainstorming, summarizing long publications, and proofreading scientific text. However, AI-generated summaries must not replace the direct analysis of primary scientific literature. Members are strictly prohibited from relying on LLMs for factual verification or citation generation, as these models are prone to hallucinations. Every reference, mathematical formula, and clinical claim must be manually verified against peer-reviewed sources.
## Writing Code 
---
### Main code
Main code refers to the core architecture, machine learning model definitions, training pipelines, and critical diagnostic algorithms of a project. The use of LLMs for generating main code should be strictly limited to structural templates or architectural inspiration. The final implementation must be fully understood, manually verified, and tested by the developer. Copying complex logic or custom loss functions directly from LLMs without deep technical validation is prohibited.
### Auxiliary code
Auxiliary code includes data preprocessing scripts, visualization utilities (e.g., generating plots), configuration files, deployment setups, and automated unit tests. Members are encouraged to use LLMs to automate the generation of these routine components to maximize development speed. However, the resulting scripts must still undergo standard validation to ensure they do not introduce silent bugs into the data pipeline.
### Code Completion 
The use of real-time code completion tools (such as GitHub Copilot or IDE-integrated autocomplete extensions) is permitted during active development. These tools serve to accelerate syntax writing and boilerplate implementation. Developers must remain highly critical of inline suggestions, as autocomplete systems can frequently introduce subtle logical errors and domain knowledge.
## Code Revives
---
The code written as part of solutions is a crucial component of the project, enabling us to obtain and interpret the results that are published in our work. For this reason, it is important not to overlook the need to ensure the quality of the code.
### Code written by human
When reviving human-authored code, developers must first run automated checking tools or LLMs to instantly eliminate syntax typos and minor formatting errors. Following this initial automated pass, a thorough manual review is required to verify core algorithmic correctness and detect any basic logical flaws before modifying the codebase.

### Code written with gen-ai support
Code generated using artificial intelligence requires rigorous verification due to the specialist domain knowledge involved in our research. As with code written by humans, developers should first use automated tools or large language models (LLMs) to correct obvious typos. It is then necessary to carry out a thorough manual verification to ensure that the complex scientific logic is correct and free from subtle algorithmic errors.
### Testing
Testing is the standard method for maintaining high code quality and software reliability. Developers must integrate comprehensive test suites into their projects to ensure functional stability between different versions and safely prevent regressions during future updates.

## Processing project data 
---
No third parties should have access to patient data stored by the research club that has not been published by the issuing center, or without the clear written consent of the institution from which the project originates. It is therefore prohibited to send data processed within the research club to LLMs, even if these LLMs have processed the data automatically and free of charge.

An exception is made for language models installed locally or as part of a collaboration with large computing centers, such as Cyfronet AGH. However, it must be ensured that data is transmitted using secure protocols and stored in appropriate formats. In all cases, regardless of the situation, data should be anonymized before being sent or stored.


