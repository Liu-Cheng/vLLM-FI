# vLLM-FI

LaTeX source for **vLLM-FI: A Fault Injection Framework for Reliability Evaluation of LLM Inference**, a manuscript being prepared for submission to *IEEE Transactions on Computer-Aided Design of Integrated Circuits and Systems (TCAD)*.

**Authors:** Jie Ren, Zizhen Liu, Songwei Pei, Cheng Liu, Huawei Li, and Shangguang Wang.
**Corresponding authors:** Songwei Pei and Cheng Liu.

## Overview

vLLM-FI integrates runtime fault injection and reliability evaluation into vLLM. It models memory, computation, and communication faults, supports distributed and quantized LLM inference, and uses GPU-resident bit-flip operators to reduce injection overhead. Integration with `lm-evaluation-harness` enables evaluation across downstream tasks and inference configurations.

The paper evaluates injection consistency, runtime efficiency, and the effects of fault models, quantization, and model parallelism on LLM reliability. Under the evaluated settings, vLLM-FI achieves a 1.81–2.41× end-to-end speedup over MRFI. With the inference runtime held fixed, its CUDA injection backend achieves up to a 5.22× speedup in total experiment runtime over an MRFI-style CPU-mediated backend.

## Manuscript and collaboration

This repository contains the manuscript and figures and is synchronized with Overleaf. Keep `main.tex` as the Overleaf main document and use pdfLaTeX. Edit individual chapters in `sections/`; bibliography entries are in `sample.bib`, and the Figure 1 float is in `figures/architecture.tex`.

To compile locally, run `latexmk -pdf main.tex` from the repository root. Coordinate GitHub/Overleaf synchronization with other authors to avoid concurrent edits to the same files.
