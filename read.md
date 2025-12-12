The Sakshi Witness Loop: Entropy-Guided AI Architecture

Principal Investigator: Nirmal G. Parmar

Status: Proof of Concept Verified

Date: December 2025

🔬 Abstract

Current Large Language Models (LLMs) often "hallucinate" because they lack introspective access to their own uncertainty. This project introduces the Sakshi Witness Loop, a neuro-symbolic architecture that monitors the Shannon Entropy of the model's internal logits during inference.

When entropy exceeds a specific threshold (indicating confusion), a secondary "Witness" process injects a control token (e.g., [STATE: UNCERTAIN]) back into the context window. This recursive feedback loop forces the model to acknowledge its own uncertainty, significantly reducing hallucinations and enabling "System 2" thinking.

📊 Experimental Results

We conducted comparative tests using a GPT-2 base model.

Experiment

Prompt

Avg Entropy

Result

Control

"The sun rises in the..."

0.01 (Low)

Focused, Factual Output

Test

"The color of a square circle..."

5.53 (High)

Witness Intervention Triggered

Visualization

(Note: Entropy spikes indicate cognitive dissonance. The Sakshi mechanism detects these spikes before the model commits to a hallucination.)

🛠️ How to Run

This repository contains a Jupyter Notebook (Sakshi_Experiment.ipynb) that demonstrates the architecture.

Open the notebook in Google Colab or Jupyter.

Run the sakshi_generate function.

Observe the real-time entropy logs as the model generates text.

🧠 Core Algorithm

if entropy > threshold:
    inject_state("[STATE: CONFUSED]")
    re_evaluate_context()
else:
    generate_next_token()


📜 Citation

If you use this architecture in your research, please cite:

Parmar, N. G. (2025). The Sakshi Witness Loop: An Entropy-Guided Neuro-Symbolic Architecture for Self-Reflective Language Models.
[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.14915409.svg)](https://doi.org/10.5281/zenodo.14915409)
