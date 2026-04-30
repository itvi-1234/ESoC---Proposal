<div align="center">
  <img src="sktime.png" height="80" alt="sktime logo">
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
  <img src="gcos.png" height="80" alt="GC.OS logo">
</div>

<h1 align="center">ESoC 2026 — Project Proposal</h1>
<h3 align="center">Embedded AI for Predictive Sensor Systems in Agriculture 4.0</h3>

<p align="center">
  <strong>Applicant:</strong> Sumit Goyal &nbsp;|&nbsp;
  <strong>GitHub:</strong> <a href="https://github.com/itvi-1234">itvi-1234</a> &nbsp;|&nbsp;
  <strong>Email:</strong> Sumit.goyal.cse@gmail.com<br/>
  <strong>Institute:</strong> IIIT Kota &nbsp;|&nbsp; B.Tech CSE (3rd Year) &nbsp;|&nbsp; <strong>Timezone:</strong> IST (UTC+5:30)
</p>

---

## 1. Basic Information

<div align="center">

| Field | Detail |
|---|---|
| **Name** | Sumit Goyal |
| **GitHub** | [itvi-1234](https://github.com/itvi-1234) |
| **Email** | Sumit.goyal.cse@gmail.com |
| **Contact** | +91 9460357477 |
| **LinkedIn** | [Sumit Goyal](https://linkedin.com/in/itvi-1234) |
| **TimeZone** | IST (GMT+05:30) |

</div>

---

## 2. Academic Background

My name is Sumit Goyal, and I am a third-year B.Tech student in Computer Science and Engineering at IIIT Kota.

I am interested in software development and enjoy building real-world projects. I have experience working with C++, Python, Docker, Kubernetes and web technologies, and I am also exploring AI/ML and automation.

I have worked on multiple projects where I built systems to automate tasks and process data efficiently and developed tools that helped reduce manual work and improve data handling. I have also gained practical exposure through several learning and competitive experiences — I completed an internship at MediaTechTemple, was selected for the Amazon ML Summer School'25, was a finalist at the Smart India Hackathon (SIH), and won the OpenAI × NextWave Buildathon (Rajasthan Regionals).

---

## 3. Development Experience & Projects

I have worked on several projects and internships focused on solving real-world problems through automation and intelligent systems.



### -> Backend & Automation Intern — MediaTechTemple

During my internship at MediaTechTemple, I worked on reducing manual effort involved in collecting news and government job updates. The team previously gathered this information manually from newspapers and recruitment portals. I automated this workflow by building data extraction pipelines using Python, Selenium, and Chromium.

- Built a news aggregation system and a government jobs collector
- Significantly reduced repetitive manual work while improving reliability
- First onsite experience — worked closely with a team, received mentor feedback, and improved solutions iteratively


### -> Amazon ML Summer School '25

Selected for the Amazon ML Summer School, ranking among the **top 3,000 out of 60,000+** candidates across India. Learned the fundamentals of machine learning, deep learning, and neural networks directly from Amazon researchers.


### -> AgriVision AI — Smart India Hackathon Finalist

[AgriVision AI](https://frontend-taupe-rho-64.vercel.app/) is a full-stack precision agriculture platform built during the Smart India Hackathon Finals.

- Uses CNN, LSTM, YOLO, and hyperspectral imaging to detect crop diseases and stress in real time
- Processes live IoT sensor streams (soil NPK, NDVI, weather) — directly relevant to sensor-based AI
- This experience is what drives my interest in agricultural AI systems


### -> WhatsApp Business AI Agent

Built a [WhatsApp Business AI Agent](https://github.com/itvi-1234/whatsapp-ai-agent) that handles large volumes of customer chats automatically using AI and automation pipelines.


Through these experiences, I have gained hands-on experience with Python, C++, React, Flask, Selenium, and AI/ML tools, while actively contributing to open-source projects using Git.

*(Resume: [[Link to Resume](https://drive.google.com/file/d/1fXJrerC43ye37Ah3Air-tqLyje1yRMHH/view?usp=sharing)])*

---

## 4. Open Source Contributions

I actively contribute to open-source projects across different domains — from Kubernetes tooling to data science libraries.

---

### ☸️ CNCF Kubernetes — Headlamp

[Headlamp](https://headlamp.dev/) is a CNCF project providing a Kubernetes dashboard. I contributed several improvements to the frontend and backend of this tool.

- Added resource allocation summaries on the Node Details page
- Improved error messages shown when cluster actions fail
- Fixed a TypeScript type issue causing runtime errors in the version display
- Added user-friendly toast notifications for failed port-forward operations
- Removed legacy Webpack fallback code that was creating unnecessary bundle overhead


**→ [All merged PRs](https://github.com/kubernetes-sigs/headlamp/pulls?q=is%3Apr+author%3Aitvi-1234+is%3Aclosed)** — 14 Merged PRs, all approved

Additionally, I have contributed to the official **Headlamp Kyverno Plugin**, implementing strict type-safety and refining the CEL Policy UI components.
**→ [Kyverno Plugin PRs](https://github.com/headlamp-k8s/plugins/pulls?q=is%3Apr+author%3Aitvi-1234+is%3Aclosed)**

---

### 🔷 JSON Schema Studio — ioflux-org

[JSON Schema Studio](https://github.com/ioflux-org/studio-json-schema) is an open-source visual editor for JSON Schemas. I contributed multiple fixes and features to improve how schemas are visualized.

- Added stable E2e testing in the repository.
- Fixed cyclic `$ref` schema back-edge color alignment for clearer graph rendering
- Fixed a bug where schemas with only a `type` keyword were showing the wrong node color
- Added edge highlighting when a node is clicked, making it easier to trace relationships
- Fixed a `processAST` bug that was causing graph rendering to fail in certain schema structures
- Implemented bidirectional interaction using AST and JSON pointer for better navigation
- Added navbar icons to fullscreen mode for improved usability
- Added SEO meta tags for better search indexing and social sharing

**→ [All merged PRs](https://github.com/ioflux-org/studio-json-schema/pulls?q=is%3Apr+author%3Aitvi-1234+is%3Aclosed)** — 10 Merged PRs, all approved

---

### 📊 sktime — Time Series Analysis

To prepare for this project, I have already contributed bug fixes directly to `sktime`'s detection module:

- **SubLOF Multivariate Fix:** The model was silently ignoring all sensor channels except the first one during prediction. This was a critical bug for any multivariate (multi-sensor) use case.
- **DetectorPipeline Error Fix:** An invalid pipeline configuration would fail silently instead of raising an error. Fixed the missing `raise` keyword so errors surface properly.
- **STRAY Refactor:** The STRAY anomaly detection algorithm was classified as a "Transformer" instead of a "Detector", making it invisible to benchmarking tools. Rewrote it to fit the correct base class.

**→ [PR: fix-sublof-pipeline-bugs](https://github.com/itvi-1234/sktime/pull/new/fix-sublof-pipeline-bugs)**
**→ [PR: refactor-stray-detector](https://github.com/itvi-1234/sktime/pull/new/refactor-stray-detector)**

---

## 5. Project Overview

Imagine a large tractor farming a field. If a rock gets pulled into the machine, it can destroy the blades in milliseconds — costing thousands of dollars in repairs and downtime.

The sponsor has collected data from **1000+ real-world foreign object events**, captured using three types of sensors attached to the machine:

- 🔊 **Acoustics** — the sound the rock makes on impact
- 📳 **Vibration** — the physical shock through the machinery
- ⚙️ **Mechanics** — changes in torque and pressure in the drivetrain

The challenge is not just to *detect* the event — it is to detect it **as early as possible**, so the machine can stop the blade before damage occurs. Even a 200ms warning matters.

This project will build that detection system using `sktime`, and also create the tools to measure and benchmark how good each algorithm actually is.

---

## 6. How We Will Build It

We will build a step-by-step pipeline using `sktime`:

1. **Clean the Data** — Real-world sensors sometimes drop readings. We fill in the gaps and scale the numbers so vibration and acoustic data can be compared fairly.
2. **Find Patterns** — Raw waveforms are hard for AI to read. We summarize the data every few milliseconds (e.g., how spiky is the vibration? how loud is the sound?) to extract meaningful features.
3. **Detect Anomalies** — We train the AI on data from normal, safe operation. When a rock enters, the pattern looks different, and the AI flags it.
4. **Measure Success** — We build custom tools to measure: Did we catch it? How many false alarms? How many milliseconds of warning did we give?
5. **Compare Models** — We build a benchmarking tool to run different algorithms side by side and find the best one.
6. **Explain the Results (SHAP)** — We will integrate Explainable AI tools like SHAP so the system doesn't just trigger an alarm, but actually tells the engineers *which specific sensor* (e.g., vibration vs. mechanics) detected the rock.

---

## 7. Pipeline Overview


```text
               Tractor Sensors (Vibration + Acoustics + Mechanics)
                                       │
                                       ▼
                        ┌─────────────────────────────┐
                        │  Step 1 — Data Cleaning     │
                        │  Fill missing values        │
                        │  Scale sensor channels      │
                        └──────────────┬──────────────┘
                                       │
                                       ▼
                        ┌─────────────────────────────┐
                        │  Step 2 — Feature Extraction│
                        │  Rolling window summaries   │
                        │  (RMS, Kurtosis, FFT bands) │
                        └──────────────┬──────────────┘
                                       │
                                       ▼
                        ┌─────────────────────────────┐
                        │  Step 3 — Detection Model   │
                        │  Trained on "normal" data   │
                        │  SubLOF / STRAY / HMM       │
                        └──────────────┬──────────────┘
                                       │
                                       ▼
                        ┌─────────────────────────────┐
                        │  Step 4 — Evaluation        │
                        │  TPR · FPR                  │
                        │  Advance Detection Time     │
                        └──────────────┬──────────────┘
                                       │
                                       ▼
                        ┌─────────────────────────────┐
                        │  Step 5 — Benchmarking      │
                        │  Compare all models         │
                        │  Auto-tune best settings    │
                        └──────────────┬──────────────┘
                                       │
                                       ▼
                        ┌─────────────────────────────┐
                        │  Step 6 — Explainability    │
                        │  SHAP values                │
                        │  Sensor-level attribution   │
                        └─────────────────────────────┘
```

---

## 8. Proposed Implementation

Here is how the core pieces of this project will be built using `sktime`. These are not just illustrations — they reflect the actual design decisions I plan to implement.

---

### 1 — Feature Extraction from Raw Sensor Data

**What it does:** Converts raw millisecond-level vibration and acoustic readings into structured summaries (features) that an AI model can actually work with.
**Why it matters:** Raw waveforms are noisy and hard to compare. By computing things like the "spikiness" (Kurtosis) or average energy (RMS) of each rolling 50ms window, we give the AI a much cleaner signal to learn from.

```python
from sktime.transformations.series.summarize import WindowSummarizer
from sktime.transformations.compose import FeatureUnion

# Summarize each 50ms window with useful statistics
time_domain_features = WindowSummarizer(
    lag_feature={
        "mean":     [{"window_length": 50}],   # average level
        "var":      [{"window_length": 50}],   # how much it fluctuates
        "kurt":     [{"window_length": 50}],   # how "spiky" the signal is
    },
    n_jobs=-1,
)

# Custom class (to be built) — computes frequency-band energy using FFT
freq_domain_features = SensorFFTFeatureExtractor(n_bands=8)

# Merge both into one feature vector per window
full_features = FeatureUnion(transformer_list=[
    ("time", time_domain_features),
    ("freq", freq_domain_features),
])
```

---

### 2 — Full Detection Pipeline

**What it does:** Chains data cleaning, feature extraction, and the detection model into a single object that can be trained and deployed end-to-end.
**Why it matters:** A proper pipeline ensures every piece of incoming sensor data is processed in exactly the same way every time — no manual steps, no inconsistencies.

```python
from sktime.detection.compose import DetectorPipeline
from sktime.transformations.series.adapt import TabularToSeriesAdaptor
from sklearn.preprocessing import RobustScaler
from sktime.detection.lof import SubLOF

pipeline = DetectorPipeline(steps=[
    # Step 1: Scale each sensor channel so they're comparable
    ("scaler",   TabularToSeriesAdaptor(RobustScaler())),

    # Step 2: Extract features from rolling windows
    ("features", full_features),

    # Step 3: Detect anomalies using multivariate LOF
    #         novelty=True means it was trained on "normal" data only
    ("detector", SubLOF(n_neighbors=20, window_size=50, novelty=True)),
])

# Train only on normal field operation data
pipeline.fit(X_normal_operation)

# Score the full field recording — higher = more anomalous
scores = pipeline.predict_scores(X_live_field)

# Get the actual event intervals detected
events = pipeline.predict(X_live_field)
```

---

### 3 — Advance Detection Time Metric

**What it does:** Measures how many milliseconds *before* the actual impact our model issued the warning.
**Why it matters:** Standard AI metrics just say "right" or "wrong". In this project, a correct detection that arrives 5ms *after* impact is worthless. This metric captures the safety value of early detection.

```python
import numpy as np
from sktime.performance_metrics.detection import BaseDetectionMetric

class AdvanceDetectionTime(BaseDetectionMetric):
    """
    For each true event, finds the earliest prediction within a
    tolerance window and measures how far ahead it came.
    A higher score means we warned the operator earlier.
    """

    def __init__(self, margin_ms=200):
        self.margin_ms = margin_ms  # look-back window in ms

    def _evaluate(self, y_true, y_pred, X=None):
        advance_times = []

        for true_onset in y_true["ilocs"]:
            # Find any predictions within the tolerance window before the event
            early_preds = y_pred["ilocs"][
                (y_pred["ilocs"] >= true_onset - self.margin_ms) &
                (y_pred["ilocs"] <  true_onset)
            ]
            if len(early_preds) > 0:
                # Best case: earliest prediction we made
                advance_times.append(true_onset - early_preds.min())

        return np.mean(advance_times) if advance_times else 0.0

# Usage
metric = AdvanceDetectionTime(margin_ms=200)
score = metric(y_true_events, y_predicted_events)
print(f"Average advance warning: {score:.1f} ms")
```

---

### 4 — Model Benchmarking

**What it does:** Runs multiple detection algorithms on the same dataset and produces a comparison table of their performance scores.
**Why it matters:** There is no single "best" anomaly detector for all data. The benchmarking tool lets us rapidly evaluate SubLOF, STRAY, HMM, and Isolation Forest on the sponsor's real dataset and pick the winner objectively.

```python
from sktime.benchmarking.detection import DetectionBenchmark  # to be built
from sktime.performance_metrics.detection import WindowedF1Score, DetectionTPR

benchmark = DetectionBenchmark(
    estimators=[
        ("SubLOF",          pipeline_sublof),
        ("STRAY",           pipeline_stray),
        ("IsolationForest", pipeline_iforest),
    ],
    metrics=[
        WindowedF1Score(margin=10),
        DetectionTPR(),
        AdvanceDetectionTime(margin_ms=200),
    ],
    cv=TimeSeriesSplit(n_splits=3),
)

results = benchmark.run(X_field_data, y_true_events)
print(results.summary())
# ┌────────────────┬─────────┬─────────┬──────────────────────┐
# │ Model          │ F1      │ TPR     │ Advance Time (ms)    │
# ├────────────────┼─────────┼─────────┼──────────────────────┤
# │ SubLOF         │ 0.87    │ 0.91    │ 143 ms               │
# │ STRAY          │ 0.81    │ 0.85    │ 112 ms               │
# │ IsolationForest│ 0.74    │ 0.79    │  88 ms               │
# └────────────────┴─────────┴─────────┴──────────────────────┘
```

---

### 5 — Auto-Tuning the Best Settings

**What it does:** Automatically searches different sensitivity values for the detector and picks the setting that gets the best score using time-series cross-validation.
**Why it matters:** The right sensitivity threshold varies by field conditions and machinery type. Instead of guessing, this tool finds the optimal setting automatically and reproducibly.

```python
from sktime.detection.compose import AutoTunedDetector  # to be built
from sklearn.model_selection import TimeSeriesSplit

tuner = AutoTunedDetector(
    estimator=SubLOF(n_neighbors=20, novelty=True),
    param_grid={
        "estimator__contamination": [0.01, 0.05, 0.1, 0.2],
        "estimator__n_neighbors":   [10, 20, 30],
    },
    scoring=AdvanceDetectionTime(margin_ms=200),
    cv=TimeSeriesSplit(n_splits=3),
    n_jobs=-1,
)

tuner.fit(X_train, y_train)
print("Best parameters:", tuner.best_params_)
# Best parameters: {'contamination': 0.05, 'n_neighbors': 20}

# The best model, ready to use
best_model = tuner.best_estimator_
```

---

### 6 — SHAP Explainability (Stretch Goal)

**What it does:** After the model detects an event, SHAP tells us exactly which sensor channel (vibration, acoustics, or mechanics) was responsible for triggering the alarm.
**Why it matters:** Trust is critical in safety systems. An engineer needs to know *why* the alarm went off, not just that it did. SHAP provides that sensor-level explanation.

```python
import shap
import pandas as pd

# Wrap the detector's scoring function for SHAP
def score_fn(X_array):
    X_df = pd.DataFrame(X_array, columns=feature_names)
    return pipeline.predict_scores(X_df).values

explainer = shap.KernelExplainer(
    model=score_fn,
    data=shap.sample(X_normal_features, 100),  # background = "normal" data
)

# Explain what triggered an anomaly in a specific event window
shap_values = explainer.shap_values(X_event_window)

# Output: which sensor contributed most to the anomaly score
# Acoustics_RMS:         +0.62  ← loudest contributor
# Vibration_Kurtosis:    +0.31
# Mechanics_Pressure:    +0.07
shap.summary_plot(shap_values, X_event_window, feature_names=feature_names)
```
---

## 9. Timeline — May 25 to August 25

The project runs for 3 months across 6 phases. Each phase maps directly to one of the implementation sections above.

| Phase | Dates | Work | Deliverable |
|---|---|---|---|
| **Phase 1 — Community Bonding & Setup** | May 25 – Jun 7 | Understand the sponsor dataset schema, discuss data format with mentors, set up the local dev environment, write initial design docs | Dev environment ready, data exploration notebook, alignment with mentor on API design |
| **Phase 2 — Feature Extraction** | Jun 8 – Jun 21 | Build `SensorFFTFeatureExtractor`, integrate with `WindowSummarizer` + `FeatureUnion`, write tests | Merged PR: feature extraction transformer with full test coverage |
| **Phase 3 — Evaluation Metrics** | Jun 22 – Jul 5 | Implement `DetectionTPR`, `DetectionFPR`, and `AdvanceDetectionTime` as proper `sktime` metric classes | Merged PR: 3 new detection metrics with docs and examples |
| **Phase 4 — Benchmarking** *(Midterm)* | Jul 6 – Jul 19 | Build `DetectionBenchmark`, wire up all algorithms and metrics, run on sponsor data | Merged PR: `DetectionBenchmark` class; midterm evaluation submitted |
| **Phase 5 — Auto-Tuning** | Jul 20 – Aug 2 | Build `AutoTunedDetector` with `TimeSeriesSplit` cross-validation and `best_params_` output | Merged PR: `AutoTunedDetector` with tests |
| **Phase 6 — Explainability & Wrap-up** | Aug 3 – Aug 25 | SHAP integration, final documentation, `examples/benchmarking_detection.ipynb` notebook, PR cleanup | Stretch goal PR (SHAP); tutorial notebook; all PRs finalized and ready for review |

> **Note:** I plan to open draft PRs early and work iteratively so mentors can review progress throughout.



## 10. Availability

I have no other commitments this summer. I can dedicate **30–35 hours per week** to this project and am comfortable with daily GitHub updates and weekly mentor calls.

---

## 11. Why Me?

1. **I know the domain.** AgriVision AI processes live agricultural sensor data — the same type of problem, just applied to tractor safety.
2. **I am already in the code.** I submitted and fixed real bugs in `sktime`'s detection module before writing this proposal.
3. **I have contributed at scale.** 13 closed PRs in CNCF Headlamp, 13 in JSON Schema Studio — I know how to contribute consistently in large open-source projects.
4. **I build end-to-end.** I don't just write models — I build complete pipelines, from raw sensor input to dashboard alerts, as shown by AgriVision.
5. **I write clearly.** I believe documentation is as important as the code itself.

---

*Submitted for ESoC 2026 · sktime × GC.OS × European Agricultural Machinery Manufacturer*
