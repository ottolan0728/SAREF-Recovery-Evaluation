# SAREF-Recovery-Evaluation

Reproducibility repository for:

**State-Aware Recovery Evaluation for Tool-Using Artificial Intelligence Agents: Matched Failure States and Minimum Effective Intervention**

Author: Chun-Jan Tseng  
Affiliation: Department of Data Science, Soochow University, Taipei, Taiwan  
ORCID: https://orcid.org/0000-0003-1611-4259

## Purpose

This repository contains redistributable derived data and evaluation artifacts supporting the SAREF study. It is intended to make the reported recovery comparisons auditable without redistributing benchmark assets that remain subject to the upstream InterCode terms.

## Public contents

### derived_data
- `condition_level_results.csv`
- `fixed_strategy_summary.csv`
- `propagation_summary.csv`
- `action_set_ablation.csv`
- `leave_one_failure_class_out.csv`

### metadata
- `failure_recovery_taxonomy.csv`
- `task_registry_summary.csv`

### integrity
- `CLAIM_BOUNDARY.md`
- `R1A_CLOSURE_REPORT.md`
- `R1A_CLOSURE_MANIFEST.json`
- `audit_archive_hashes.csv`

### documentation
- `REPRODUCIBILITY_SCOPE.md`
- `MANUSCRIPT_ARTIFACT_MAP.md`

## Benchmark dependency

The study uses the public InterCode benchmark:
https://github.com/princeton-nlp/intercode

InterCode assets are not duplicated here when redistribution is restricted by upstream terms. Users should obtain the benchmark from its official repository and follow its licensing and setup instructions.

## Reproducibility boundary

The public package is intended to reproduce the reported derived analyses and manuscript display items from redistributable artifacts. It does not package every upstream benchmark asset or environment image.

The reported study uses 13 retained InterCode Bash tasks, 39 controlled failure episodes, and 117 matched recovery branches. The files in this repository are derived summaries of that frozen experiment. They should not be interpreted as a population sample of deployed AI-agent failures.

## Funding

This research was sponsored by the National Science and Technology Council (NSTC), Taiwan, under grant number NSTC 115-2222-E-031-002.

## Acknowledgment

The author acknowledges the National Center for High-Performance Computing for providing computational resources and facilities used in this research.
