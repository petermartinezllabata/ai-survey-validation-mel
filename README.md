# AI-assisted Survey Validation for Multi-country Data Collection

## Overview

Large-scale surveys used in international and governance contexts often suffer from inconsistencies in question design, unclear definitions, and limited comparability across countries. These issues directly affect data quality, statistical analysis, and policy relevance.

This project explores how Large Language Models (LLMs) can support the systematic review of survey instruments (e.g. XLSForms), identifying design flaws before deployment and improving the reliability and usability of collected data.

---

## Objective

To develop a lightweight, AI-assisted workflow that evaluates survey questions and flags issues related to:

- Measurement validity  
- Statistical reliability  
- Cross-country comparability  
- Analytical usability  
- Conceptual clarity  

---

## Approach

The system uses structured prompts to simulate expert-level review of survey questions.

### Input
- Survey questions extracted from XLSForms  
- Metadata and questionnaire structure  

### Process
- Prompt-based evaluation using an LLM  
- Assessment across predefined methodological dimensions:
  - Clarity and precision  
  - Measurement quality  
  - Conceptual validity  
  - Structure  
  - Response design  
  - Comparability  
  - Analytical usability  

### Output
- Structured JSON containing:
  - Identified issues  
  - Severity levels  
  - Explanations  
  - Suggested improvements  

---

## Example

### Input (survey question)

> Does the data on police provided in this questionnaire cover the entire geographical territory of your country?

### Output (simplified)

```json
{
  "dimension": "Comparability",
  "severity": "medium",
  "explanation": "Different interpretations of territorial coverage may affect comparability.",
  "suggested_fix": "Provide a standardized definition."
}
