# HackerOne Bug Bounty Reports Dataset

This repository contains the dataset for the paper:

> **From Reviewers' Lens: Understanding Bug Bounty Report Invalid Reasons with LLMs**
>
> Jiangrui Zheng, Yingming Zhou, Ali Abdullah Ahmad, Hanqing Yao, Xueqing Liu
>
> *Workshop on Secure and Safe AI Agents for Big Data Infrastructure*, 2025

## Overview

This dataset consists of publicly disclosed bug bounty reports collected from the [HackerOne](https://hackerone.com/) platform. It is designed to support research on understanding why bug bounty reports are marked as invalid, leveraging Large Language Models (LLMs) for automated analysis.

## Dataset Contents

### `json.zip` — Bug Bounty Reports

Contains **9,942 JSON files**, each representing a publicly disclosed HackerOne report. Each JSON file includes the following fields:

| Field | Description |
|-------|-------------|
| `title` | Title of the vulnerability report |
| `Reported on` | Submission date |
| `Reported by` | Reporter's username |
| `Reported to` | Target vendor/program |
| `Severity` | Severity rating (e.g., Medium, High, Critical) |
| `Weakness` | Vulnerability type (e.g., SSRF, XSS, SQL Injection) |
| `CVE ID` | Associated CVE identifier (if any) |
| `Bounty` | Bounty amount awarded |
| `summary` | Report summary |
| `timeline` | Full interaction timeline between reporter and triager |
| `status` | Final resolution status (e.g., Resolved, Informative, Not Applicable) |
| `stats_all_time` | Reporter's all-time statistics (Signal, Impact, Reputation) |
| `credits` | Reporter's credit information |

### `vendor_scope.zip` — Vendor Program Scope Information

Contains **313 CSV files** with in-scope asset definitions for various bug bounty programs, plus a mapping file:

- **`report_map.csv`** — Maps vendor names to their HackerOne team handles
- **Per-vendor CSVs** (e.g., `shopify.csv`, `adobe.csv`) — Each file lists the program's in-scope assets with fields including:
  - `identifier` — Asset identifier (URL, app name, etc.)
  - `asset_type` — Type of asset (URL, iOS app, Android app, etc.)
  - `instruction` — Scope instructions and notes
  - `eligible_for_bounty` — Whether the asset is eligible for bounty
  - `eligible_for_submission` — Whether submissions are accepted
  - `max_severity` — Maximum severity rating accepted


## Citation

If you use this dataset in your research, please cite our paper:

```bibtex
@inproceedings{zheng2025reviewers,
  title={From Reviewers' Lens: Understanding Bug Bounty Report Invalid Reasons with LLMs},
  author={Zheng, Jiangrui and Zhou, Yingming and Ahmad, Ali Abdullah and Yao, Hanqing and Liu, Xueqing},
  booktitle={Workshop on Secure and Safe AI Agents for Big Data Infrastructure},
  year={2025}
}
```

## License

This dataset is provided for research purposes. The original reports are publicly disclosed on HackerOne by their respective authors.
