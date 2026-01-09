**Peoject Title**: Safety Testing of Large Language Models (LLMs) in Low Resource Languages: A Case Study on Swahili
## Phase 0: Preparation, Scoping and MVP (Week 1)
**Goal**: Minimize the rework
### Final Scope and MVP
* Swahili only (no extra languages)
* Evaluation only (no fine-tuning)
* Automated and human evaluation
* Small but representative dataset

### Ethics and documentation
* Prepare annotation guidelines (Safe / Borderline / Unsafe).
* Draft content warning text.
* Prepare Microsoft Forms structure.

## Phase 1: Dataset Creation (Weeks 1 - 2)
**Goal**: Project structure and dataset created.
### Create a clean data repository

### Create a pilot dataset
* 50 - 100 English SafetyPrompts translated to Swahili
* 50 native Swahili samples (AfriHate + Mwitiderrick)
* Test translation quality
* Test classifiers
* Debug pipeline early
### Implement Translation pipeline
* Implement forward translation using NLLB and mBART
* Save both original and translated text
* Perform manual inspection.

## Phase 2: Automated Safety Pipeline (Weeks 2 - 3)
**Goal**: Get a working system early.
* Implement baseline toxicity scoring
* Start with one classifier (XLM-R Large Toxicity from HuggingFace)
* Implement refusal detection.

## Phase 3: LLMs Evaluation (Weeks 3 - 4)
**Goal**: Generate responses safely and consistently.
* Log
    * Prompt ID
	* Prompt type (harmful / neutral / sensitive)
	* Model name
	* Raw output

## Phase 4: Human Evaluation (Weeks 4 - 5)
**Goal**: Add cultural grounding.
### Sample Annotation subset
### Launch Microsoft Form
* Track Each item:
    * Prompt
    * Model response
    * Rating (Safe / Borderline / Unsafe)

### Measure agreement
* Implement:
    * Inter-annotator agreement
	* Human vs model disagreement logging

## Phase 5: Analysis & Benchmarking (Weeks 5 - 6)
**Goal**: Turn results into a benchmark.
### Compute metrics
* Implement:
	* Toxicity distributions
	* Refusal rate per category
	* False positives / false negatives
	* Human to model agreement (Spearman ρ)

### Error analysis
* Manually analyse:
	* Swahili idioms misclassified as toxic
	* Harmful prompts not refused
	* Over censorship cases

## Phase 6: Packaging & Reporting (Final Weeks)
**Goal**: Make project reusable and defensible.
### Deliverables
* Prepare:
	* Clean Swahili safety dataset (CSV/JSON)
	* Evaluation scripts
	* Clear limitations section

### Tie back to hypotheses
* Explicitly answer the following hypothesis:
	* H1: Did Swahili show worse safety?
	* H2: Did safety prompting help?
	* H3: What patterns emerged?