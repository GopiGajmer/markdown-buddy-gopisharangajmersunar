**AI Assistance Declaration**: I used ChatGPT (GPT-5.6 Luna) on October 2, 2026 for drafting README content and Markdown formatting suggestions, and Claude for step-by-step guidance. Prompts used: listed below. I verified outputs using GitHub's Markdown preview, knitting the .Rmd in Posit Cloud, and comparing against the tidyverse README. All final calculations are done by myself. I am responsible for the accuracy and originality of this work.

# Appendix: AI Prompts and Key Responses

All prompts below were given to ChatGPT (GPT-5.6 Luna) on October 2, 2026.

## Step 1: Understanding README structure

### Prompt 1 (Seed)

**Prompt:** "Explain what sections a good GitHub README for an R data analysis project should include."

**Key response:** ChatGPT listed 16 sections with examples, from Project Title and Overview to Limitations, Future Improvements, and Author. It also gave a recommended order and said the most important sections are Overview, Dataset, Setup, How to Run, Analysis, Results, and Conclusion.

**What I did:** I read the answer and noticed that the code block in the Setup section was never closed. I also compared the list with a real tidyverse README.

### Prompt 2 (Refinement)

**Prompt:** "Revise the sections list so it's concise and uses Markdown headers and bullet formatting."

**Key response:** ChatGPT shortened the list into the same 16 sections, each with one or two short descriptions.

**What I did:** I used this shorter list as the basis for my own README outline.

### Prompt 3 (Critique/Validation)

**Prompt:** "Check the Markdown syntax for correctness and readability."

**Key response:** ChatGPT said the structure was correct and rewrote the outline using `#` for the title, `##` for sections, and `-` for bullets. It also listed what it checked, such as consistent capitalization and a simple heading hierarchy.

**What I did:** I noted that this check did not catch the unclosed code block from Prompt 1, so I could not rely on it alone.

## Step 2: Generating the README

### Prompt 4 (Seed)

**Prompt:** "Here's a summary of my R project: "Regional Sales Summary" is a small R project that generates a synthetic sales dataset (100 rows, 4 regions), calculates average sales per region, and creates a bar chart. Key script: analysis.R (documented in analysis.Rmd). Dependencies: R (4.x) and the ggplot2 package. All data is synthetic and created inside the script. No real data is used. Generate a professional README.md file using Markdown."

**Key response:** ChatGPT produced a full README with Overview, Objectives, Tools, Project Files, Dependencies, How to Run, Data, Analysis, Visualization, Results, Reproducibility, Limitations, and Author sections.

**What I did:** I noticed it listed `analysis.R` as a file, but my repository only contains `analysis.Rmd`.

### Prompt 5 (Refinement)

**Prompt:** "Add sections for Installation, Example Code, and License. Keep tone concise and professional."

**Key response:** ChatGPT added Installation, Example Code, and License sections and shortened the rest of the README.

**What I did:** I replaced its example code with the exact code from my own script, because its variable names (`Region`, `Sales`) did not match my `analysis.Rmd`.

### Prompt 6 (Critique/Validation)

**Prompt:** "Review the Markdown for syntax errors and suggest 2 improvements for clarity."

**Key response:** ChatGPT found no syntax errors. It suggested (1) clarifying the License section because it mentioned the MIT License without a LICENSE file, and (2) merging the overlapping Analysis, Results, and Visualization sections into one.

**What I did:** I applied both improvements. I reworded the License section to say the project is for educational purposes, and I merged the three sections into "Analysis & Results". I also updated the file list and "How to Run" steps to match my repository, then previewed the README on GitHub.

## Step 3: Documenting the R script with R Markdown

### Prompt 7 (Seed)

**Prompt:** "Here's my R script description: It creates synthetic sales data for 4 regions, calculates average sales per region, and plots a bar chart using ggplot2. Suggest Markdown formatting and code block examples."

**Key response:** ChatGPT suggested a Project Description, an Analysis Steps list, an Example Code section using an `r` code fence for syntax highlighting, and a Requirements section. It also left one code block unclosed in the Dependencies section.

**What I did:** I did not copy the example code because its variable names did not match my script. I kept my own code and noticed the unclosed code block.

### Prompt 8 (Refinement)

**Prompt:** "Add syntax highlighting and improve section organization (e.g., # Purpose, ## Inputs, ## Outputs)."

**Key response:** ChatGPT reorganized the document into Purpose, Inputs, Outputs, Requirements, Example Code, Project Structure, How to Run, Notes, and License sections, and used `r` code fences for syntax highlighting.

**What I did:** My `analysis.Rmd` already used Purpose, Inputs, Code, and Outputs headings. I compared it with ChatGPT's structure to confirm the organization was consistent.

### Prompt 9 (Critique/Validation)

**Prompt:** "Is the Markdown consistent with RMarkdown best practices?"

**Key response:** ChatGPT said the structure follows good Markdown practice for a README, but an `.Rmd` file also needs a YAML header and `{r}` code chunks instead of `r` code fences.

**What I did:** My `analysis.Rmd` already had a YAML header and an `{r}` code chunk. I confirmed this against ChatGPT's advice, then knitted the file in Posit Cloud and checked that the headings, code block, table, and chart all displayed correctly.
