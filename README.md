# Awesome-Data-Labeling-Quality-Control-Systems

# Top Data Labeling Quality Control Systems Ecosystem

**Curated List of SaaS Products & Open-Source GitHub Projects**  
*Focused on Inter-Annotator Agreement, Label Validation & Automated Quality Assurance*  
**Last updated: March 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Data Labeling Quality Control**. These tools provide statistical layers validating large-scale automated data labeling outputs—computing inter-annotator agreement (IAA), detecting label errors, and ensuring training data integrity before it reaches production models.

**Examples** include Scale AI, Labelbox, Encord, Supervisely, V7 Labs, SuperAnnotate, Dataloop, Kili Technology, Snorkel Flow, and Centaur Labs (the category leaders).

**Open-source emphasis**: This section is heavily expanded with every major active project for self-hosting, IAA computation, and open annotation quality assurance—ideal for ML engineers, data teams, and developers seeking transparent, vendor-independent label validation.

Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [SaaS/Hosted Platforms](#saas-hosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

- **[Scale AI](https://scale.com/)**  
  Enterprise data labeling with managed workforce of 240,000+ labelers worldwide. Features **Scale Donovan** for government/defense and **Scale GenAI** for RLHF and prompt curation, including work on OpenAI o1 and GPT-4 training . Pricing is not public; per-box rates range from $0.05 to $60+/hour depending on domain and QC tier .

- **[Labelbox](https://labelbox.com/)**  
  Enterprise self-service plus managed labeling platform. Three modes: **Self-service** (your team labels, from $25/seat/month), **Boost** (Labelbox supplies labelers), and **Foundry** (foundation models do first pass, humans review) . Features **SAM 2 integration for auto-masking** with reports of 5–10x annotator productivity. Free tier: 5,000 data rows, 3 users .

- **[Encord](https://encord.com/)**  
  Annotation plus active learning for medical imaging and multimodal data. Features **native DICOM/NIfTI** (preserving pixel spacing, HU values, series metadata), **Encord Active** for active learning routing low-confidence samples to labelers first, and multimodal support (image, video, DICOM, document, audio) . Medical-domain compliance: HIPAA, ISO 13485, FDA validation .

- **[V7 Labs](https://www.v7labs.com/)**  
  Three product lines: **V7 Darwin** (general CV annotation), **V7 Go** (document automation/extraction), **V7 Medical** (DICOM, HIPAA, FDA 510(k) friendly) . Features **model-assisted annotation** with proprietary SAM-like model plus Grounding DINO—one click, one box, or text prompt produces instant labels .

- **[Supervisely](https://supervisely.com/)**  
  Computer vision platform with advanced video and 3D point cloud labeling. Features tracking-by-detection, pretrained 3D models for LiDAR, and 2D-to-3D annotation transfer.

- **[SuperAnnotate](https://www.superannotate.com/)**  
  Platform supporting full lifecycle of AI data development. Provides annotation for images, video, text, audio, and documents with AI-assisted labeling, quality assurance workflows, and Python SDK/REST API .

- **[Dataloop](https://dataloop.ai/)**  
  Data labeling and annotation platform (acquired by Dell). Features automation, quality assurance, and multimodal data support .

- **[Kili Technology](https://kili-technology.com/)**  
  Training data platform with annotation, quality control, and active learning. SDK available on GitHub (kili-technology/kili-python-sdk) with 231 stars .

- **[Snorkel Flow](https://snorkel.ai/)**  
  Enterprise data development platform built on the open-source Snorkel library. Supports programmatic labeling, data curation, model training, and evaluation. The open-source Snorkel library (Apache-2.0) enables weak supervision with labeling functions, LabelModel, and slicing.

- **[Centaur Labs](https://centaurlabs.com/)**  
  Crowdsourced medical data labeling with expert network. Focuses on medical imaging annotation with quality control through consensus.

## Open-Source GitHub Projects

- **[Label Studio](https://github.com/HumanSignal/label-studio)**  
  The most flexible open-source data labeling tool (Apache-2.0) supporting text, vision, audio, and time-series data . **20,000+ GitHub stars**. Features custom XML UI templates, ML backend integrations, and webhook integrations. **The foundation for most open-source annotation workflows.**

- **[CVAT (Computer Vision Annotation Tool)](https://github.com/cvat-ai/cvat)**  
  High-performance browser-based video and image annotation (MIT) with AI tracking . **14,000+ GitHub stars**. Industry-standard for detection and segmentation annotation. Features automated labeling with models, interpolation between keyframes, and quality assurance workflows.

- **[iaa-od](https://pypi.org/project/iaa-od/)**  
  Comprehensive **Inter-Annotator Agreement analysis suite for Object Detection** tasks (PyPI) . Computes **Krippendorff's Alpha** (with agglomerative clustering for units), **Rater Vitality** (each annotator's contribution to global agreement), **Scale Complexity** (ambiguity across categories), **L-Score** (localization agreement from bounding box positions), **C-Score** (categorization agreement from intersecting boxes), and **Count/Size Granularity** (grouping vs. instance annotation behavior) . Includes visualization module and Jupyter notebooks. **The most comprehensive open-source IAA toolkit for object detection.**

- **[knowlyr-datalabel](https://pypi.org/project/knowlyr-datalabel/)**  
  Offline-first, zero-dependency annotation platform generating standalone HTML interfaces (PyPI, v0.3.0) . Features **5 annotation types** (rating, single-choice, multi-choice, text, ranking), dark mode, undo support, statistics panel, and large dataset support (1000+ tasks with pagination/search). **Multi-annotator merge with IAA computation** (Cohen's/Fleiss' Kappa, Krippendorff's Alpha). **LLM-powered pre-labeling, quality analysis, and guideline generation** via Kimi/Moonshot, OpenAI, or Anthropic. **MCP support** (11 tools, 6 resources, 3 prompts) for Claude Desktop/Code integration. **The most feature-complete lightweight open-source annotation quality tool.**

- **[Potato](https://github.com/davidjurgens/potato)**  
  Portable annotation framework with **20+ annotation types**, AI-assisted labeling, quality control, crowdsourcing support, and **agent trace evaluation** . **YAML-driven philosophy** with **12-phase human-LLM collaboration workflow**. Unlike LangSmith/Labelbox/Braintrust which collect human judgements as scores, Potato **documents reliability statistics over those judgements** . **The most explicit open-source IAA-focused annotation platform.**

- **[Argilla](https://github.com/argilla-io/argilla)**  
  Human-in-the-loop annotation specifically tailored for **LLM prompt-response evaluation and RLHF feedback** . Purpose-built for preference data with HuggingFace integration. **The standard open-source tool for LLM evaluation data curation** .

- **[bonepick](https://pypi.org/project/bonepick/)**  
  CLI tool for **annotation agreement comparison** between datasets (PyPI, v0.4.0) . Computes **Cohen's Kappa** (with interpretation scale: slight/fair/moderate/substantial/almost perfect), agreement rate, confusion matrix, and disagreement examples. Supports **ordinal labels** with Weighted Kappa (quadratic), MAE, RMSE, Pearson Correlation, and difference histogram. Compares human vs. human, human vs. LLM, or across annotation rounds .

- **[quallmer.app](https://cran.r-project.org/web/packages/quallmer.app/)**  
  R package providing an **interactive Shiny app for manual coding, LLM output validation, and IAA computation** (CRAN) . Three modes: **blind manual coding**, **LLM output validation**, and **agreement calculation**. Computes **Krippendorff's alpha, Cohen's kappa, Fleiss' kappa, ICC, and percent agreement** for nominal, ordinal, interval, and ratio data. Also computes **gold-standard validation metrics** (accuracy, precision, recall, F1) .

- **[cleanlab](https://github.com/cleanlab/cleanlab)**  
  Data-centric AI library for **finding label errors** and training robust classifiers. **The standard open-source tool for automated label error detection**—identifies mislabeled examples in datasets before training.

- **[Cleanlab Studio](https://cleanlab.ai/studio/)**  
  Client interface for Cleanlab Studio (open-source client, commercial platform). Detects label errors, outliers, and data issues at scale .

- **[Xtreme1](https://github.com/xtreme1-io/xtreme1)**  
  All-in-one data labeling and annotation platform for multimodal data (Apache-2.0, LF AI & Data Foundation project) . Supports **3D LiDAR point cloud, image, and LLM** (RLHF beta). Features data management and quality monitoring, **finding labeling errors and fixing them**, model results visualization for evaluation, and image data curation (MobileNetV3 & openTSNE) . **The first open-source data labeling project hosted in LF AI & Data Foundation** .

- **[Toloka crowd-kit](https://github.com/Toloka/crowd-kit)**  
  Python tools for **controlling quality of labeled data** (Apache-2.0) . **215 GitHub stars**. Provides the Python tools you already know for quality control in crowdsourced annotations.

- **[EffiARA](https://pypi.org/project/effiara/)**  
  Framework for **efficient annotation and reliability assessment** (PyPI) . Features **SampleDistributor** for calculating optimal sample distribution across annotators, **data generator** for synthetic test data, and **annotator reliability module** computing individual annotator reliability metrics from inter- and intra-annotator agreement . Published in arXiv:2410.14515.

### Additional Strong Open-Source Options

- **[doccano](https://github.com/doccano/doccano)** — Open-source text annotation tool (MIT) supporting text classification, sequence labeling, and sequence-to-sequence tasks .
- **[Prodigy](https://prodi.gy/)** — Scriptable, active learning annotation tool by spaCy creators. **60% annotation reduction** with active learning, air-gapped deployment . **Note**: Commercial license required.
- **[Universal Data Tool](https://github.com/UniversalDataTool/universal-data-tool)** — Web/desktop app for editing and annotating images, text, audio, and documents (MIT) .
- **[VGG Image Annotator (VIA)](https://www.robots.ox.ac.uk/~vgg/software/via/)** — Standalone image annotator packaged as single HTML file (<400 KB) running in any modern browser (BSD-2) .
- **[Pigeon](https://github.com/agermanidis/pigeon)** — Simple Jupyter widget for quick dataset annotation (Apache-2.0) .
- Community **n8n** workflows for annotation quality alerting and IAA report routing.

**Frameworks for building custom systems**: Combine **Label Studio** or **CVAT** for annotation with **iaa-od** or **knowlyr-datalabel** for IAA computation, **cleanlab** for automated label error detection, **quallmer.app** for gold-standard validation, and **PostgreSQL** for persistence—creating a fully self-hosted, enterprise-grade data labeling quality control platform.

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- Data labeling quality control systems handling training data must comply with data protection regulations (GDPR, CCPA, etc.) and ensure annotation workforce agreements are in place.
- **IAA is not a single metric.** Cohen's Kappa works for two annotators on nominal data. Fleiss' Kappa extends to multiple annotators. Krippendorff's Alpha handles missing data and multiple annotators across any measurement level . **Choose the metric matching your annotation setup**—using the wrong one produces misleading quality scores.
- **IAA measures agreement, not correctness.** Two annotators can agree on the wrong label. Gold-standard validation (accuracy, precision, recall, F1 against known-correct labels) is needed to assess absolute quality .
- **Automated label error detection is essential at scale.** Manual review of millions of labels is infeasible. Cleanlab identifies mislabeled examples statistically . iaa-od detects localization vs. categorization disagreements separately—revealing whether annotators disagree on *where* objects are or *what* they are .
- **Self-hosted open-source solutions require proper security hardening, annotation workforce management, and ongoing maintenance.** Training data is a strategic asset—access controls and versioning are essential.

---

**Made for ML engineers, data quality analysts, annotation managers, and developers building transparent label validation solutions.**  
Let's make Data Labeling Quality Control more open, data-driven, and statistically rigorous.
