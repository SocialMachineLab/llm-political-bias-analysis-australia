# Whose Politics Do LLMs Represent? Uncovering Political Bias in LLMs’ Latent Space

## Files

- `./ProbeClassifier.py`: Code to replicate the results of probe for identifying party related Vectors in MLP.
- `./PersonMapping.py`: Code to replicate the results of mapping between personas and the identified party-related
value vectors.
- `./replicate_figures.ipynb`: Code to replicate the figures. 
- `.Data/DataSurveyProfiles/`: Data for persona profile
- `.Data/DataTraining/`: Data for trainig probe.
- `.Data/ScalingFactor/`: Scaling factor result to replicate the figures

## Performance of Probing Classifiers by Party and Model


| Party | Model | Accuracy | Brier Score | Precision | Recall | F1 Score |
|------|------|------|------|------|------|------|
| **Australian Greens** | gemma-7b | 0.502 | 0.235 | 0.240 | 0.833 | 0.372 |
|  | Gemma-7b-it | 0.502 | 0.236 | 0.240 | 0.833 | 0.372 |
|  | Llama2-7b | 0.510 | 0.236 | 0.232 | 0.765 | 0.356 |
|  | Llama2-7b-chat | 0.509 | 0.236 | 0.235 | 0.784 | 0.361 |
|  | Llama3.1-8b | 0.506 | 0.232 | 0.238 | 0.809 | 0.367 |
|  | Llama3.1-8b-inst | 0.504 | 0.235 | 0.237 | 0.811 | 0.367 |
|  | Llama3.2-3b | 0.502 | 0.233 | 0.240 | 0.833 | 0.372 |
|  | Llama3.2-3b-inst | 0.502 | 0.235 | 0.240 | 0.833 | 0.372 |
|  | Meta-llama3-8b | 0.504 | 0.234 | 0.238 | 0.817 | 0.368 |
|  | Meta-llama3-8b-inst | 0.504 | 0.233 | 0.237 | 0.811 | 0.367 |
|  | Mistral-7b-inst | 0.506 | 0.237 | 0.239 | 0.817 | 0.369 |
|  | Qwen2.5-7b | 0.510 | 0.237 | 0.235 | 0.781 | 0.361 |
|  | Qwen2.5-7b-inst | 0.516 | 0.234 | 0.234 | 0.760 | 0.358 |
| **Australian Labor Party** | gemma-7b | 0.607 | 0.246 | 0.371 | 0.475 | 0.417 |
|  | Gemma-7b-it | 0.601 | 0.248 | 0.364 | 0.468 | 0.409 |
|  | Llama2-7b | 0.591 | 0.250 | 0.343 | 0.421 | 0.378 |
|  | Llama2-7b-chat | 0.590 | 0.250 | 0.343 | 0.424 | 0.379 |
|  | Llama3.1-8b | 0.599 | 0.249 | 0.359 | 0.453 | 0.401 |
|  | Llama3.1-8b-inst | 0.595 | 0.249 | 0.349 | 0.426 | 0.383 |
|  | Llama3.2-3b | 0.601 | 0.248 | 0.365 | 0.473 | 0.412 |
|  | Llama3.2-3b-inst | 0.597 | 0.248 | 0.353 | 0.435 | 0.390 |
|  | Meta-llama3-8b | 0.598 | 0.250 | 0.361 | 0.465 | 0.406 |
|  | Meta-llama3-8b-inst | 0.601 | 0.247 | 0.365 | 0.471 | 0.411 |
|  | Mistral-7b-inst | 0.596 | 0.247 | 0.350 | 0.427 | 0.385 |
|  | Qwen2.5-7b | 0.595 | 0.250 | 0.349 | 0.427 | 0.384 |
|  | Qwen2.5-7b-inst | 0.595 | 0.249 | 0.347 | 0.419 | 0.380 |
| **Liberal Party of Australia** | gemma-7b | 0.610 | 0.246 | 0.380 | 0.491 | 0.428 |
|  | Gemma-7b-it | 0.606 | 0.248 | 0.370 | 0.463 | 0.412 |
|  | Llama2-7b | 0.584 | 0.251 | 0.359 | 0.506 | 0.420 |
|  | Llama2-7b-chat | 0.576 | 0.252 | 0.349 | 0.494 | 0.409 |
|  | Llama3.1-8b | 0.607 | 0.248 | 0.372 | 0.465 | 0.413 |
|  | Llama3.1-8b-inst | 0.603 | 0.248 | 0.372 | 0.483 | 0.420 |
|  | Llama3.2-3b | 0.606 | 0.247 | 0.373 | 0.478 | 0.419 |
|  | Llama3.2-3b-inst | 0.611 | 0.247 | 0.380 | 0.486 | 0.427 |
|  | Meta-llama3-8b | 0.604 | 0.248 | 0.371 | 0.475 | 0.417 |
|  | Meta-llama3-8b-inst | 0.606 | 0.247 | 0.373 | 0.472 | 0.416 |
|  | Mistral-7b-inst | 0.606 | 0.247 | 0.367 | 0.450 | 0.405 |
|  | Qwen2.5-7b | 0.583 | 0.251 | 0.355 | 0.489 | 0.411 |
|  | Qwen2.5-7b-inst | 0.589 | 0.251 | 0.353 | 0.457 | 0.398 |
| **National Party of Australia** | gemma-7b | 0.395 | 0.251 | 0.238 | 0.741 | 0.360 |
|  | Gemma-7b-it | 0.424 | 0.250 | 0.233 | 0.658 | 0.344 |
|  | Llama2-7b | 0.432 | 0.255 | 0.231 | 0.635 | 0.339 |
|  | Llama2-7b-chat | 0.434 | 0.253 | 0.222 | 0.584 | 0.321 |
|  | Llama3.1-8b | 0.415 | 0.252 | 0.224 | 0.631 | 0.331 |
|  | Llama3.1-8b-inst | 0.400 | 0.255 | 0.232 | 0.698 | 0.348 |
|  | Llama3.2-3b | 0.400 | 0.251 | 0.230 | 0.688 | 0.345 |
|  | Llama3.2-3b-inst | 0.402 | 0.253 | 0.238 | 0.728 | 0.358 |
|  | Meta-llama3-8b | 0.417 | 0.250 | 0.230 | 0.656 | 0.341 |
|  | Meta-llama3-8b-inst | 0.397 | 0.253 | 0.230 | 0.694 | 0.346 |
|  | Mistral-7b-inst | 0.408 | 0.254 | 0.224 | 0.643 | 0.333 |
|  | Qwen2.5-7b | 0.449 | 0.253 | 0.222 | 0.559 | 0.318 |
|  | Qwen2.5-7b-inst | 0.448 | 0.252 | 0.223 | 0.563 | 0.319 |

## Data Sources and Labeling Procedure for Probing Data Training

### (V-Party) dataset

For Varieties of Party Identity and Organization (V Party) Dataset, labels were generated from the coded survey responses in the dataset and the accompanying V-Party Codebook. For binary questions, responses coded as “Yes” were labeled “Agree,” while responses coded as “No” were labeled “Disagree.” For questions with multiple response options, the question text and the selected answer were combined to form a declarative statement representing the party’s position. These statements were labeled “Agree,” since they reflect a characteristic attributed to the party by the expert coders. The codebook was used to retrieve the exact question wording and the meaning of each response option, ensuring that the generated statement accurately reflected the coded variable. After constructing each statement, minor textual normalization was applied: the word “Australia” was inserted where relevant to provide geographical context.

### Manifesto Project dataset

Data from the Manifesto Project Dataset contain coded categories representing positive and negative references to policy themes within party manifestos. For labeling, the positive and negative scores associated with each category were combined into a single value. If the resulting value was greater than zero, the statement was labeled “Agree.” If the value was less than zero, it was labeled “Disagree.” A value equal to zero was treated as Neutral. This procedure converts the directional coding of manifesto statements into a standardized agreement label compatible with the other data sources.


### Roll-call votes (division records; party-level labels)

We use the Parliamentary Handbook of the Commonwealth of Australia API to obtain Roll-call vote data. This were obtained from parliamentary division records, where each division represents a formal recorded vote on a specific motion or bill. These records report the vote of each individual member of parliament (MP), voted “Ayes” or “Noes.”, each record already contains a party identifier (Party). Motion or bill were considered as statements and labeled as follows: Result = 0 (Ayes) was labeled “Agree” and Result = 1 (Noes) was labeled “Disagree.”
