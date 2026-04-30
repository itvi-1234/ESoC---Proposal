<p align="center">
  <img src="https://raw.githubusercontent.com/sktime/sktime/main/docs/source/images/sktime-logo-no-text.png" height="80" alt="sktime"/>
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
  <img src="gcos_logo.svg" height="80" alt="GC.OS"/>
</p>

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

| Field | Detail |
|---|---|
| **Name** | Sumit Goyal |
| **GitHub** | [itvi-1234](https://github.com/itvi-1234) |
| **Email** | Sumit.goyal.cse@gmail.com |
| **Contact** | +91 9460357477 |
| **LinkedIn** | [Sumit Goyal](https://linkedin.com/in/itvi-1234) |
| **TimeZone** | IST (GMT+05:30) |

---

## 2. Academic Background

My name is Sumit Goyal, and I am a third-year B.Tech student in Computer Science and Engineering at IIIT Kota.

I am interested in software development and enjoy building real-world projects. I have experience working with C++, Python, Docker, Kubernetes and web technologies, and I am also exploring AI/ML and automation.

I have worked on multiple projects where I built systems to automate tasks and process data efficiently and developed tools that helped reduce manual work and improve data handling. I have also gained practical exposure through several learning and competitive experiences — I completed an internship at MediaTechTemple, was selected for the Amazon ML Summer School'25, was a finalist at the Smart India Hackathon (SIH), and won the OpenAI × NextWave Buildathon (Rajasthan Regionals).

---

## 3. Development Experience & Projects

I have worked on several projects and internships focused on solving real-world problems through automation and intelligent systems.

---

### 🏢 Backend & Automation Intern — MediaTechTemple

During my internship at MediaTechTemple, I worked on reducing manual effort involved in collecting news and government job updates. The team previously gathered this information manually from newspapers and recruitment portals. I automated this workflow by building data extraction pipelines using Python, Selenium, and Chromium.

- Built a news aggregation system and a government jobs collector
- Significantly reduced repetitive manual work while improving reliability
- First onsite experience — worked closely with a team, received mentor feedback, and improved solutions iteratively

---

### 🎓 Amazon ML Summer School '25

Selected for the Amazon ML Summer School, ranking among the **top 3,000 out of 60,000+** candidates across India. Learned the fundamentals of machine learning, deep learning, and neural networks directly from Amazon researchers.

---

### 🌾 AgriVision AI — Smart India Hackathon Finalist

[AgriVision AI](https://frontend-taupe-rho-64.vercel.app/) is a full-stack precision agriculture platform built during the Smart India Hackathon Finals.

- Uses CNN, LSTM, YOLO, and hyperspectral imaging to detect crop diseases and stress in real time
- Processes live IoT sensor streams (soil NPK, NDVI, weather) — directly relevant to sensor-based AI
- This experience is what drives my interest in agricultural AI systems

---

### 💬 WhatsApp Business AI Agent

Built a [WhatsApp Business AI Agent](https://github.com/itvi-1234/whatsapp-ai-agent) that handles large volumes of customer chats automatically using AI and automation pipelines.

---

Through these experiences, I have gained hands-on experience with Python, C++, React, Flask, Selenium, and AI/ML tools, while actively contributing to open-source projects using Git.

*(Resume: [Link to Resume])*

---

## 4. Open Source Contributions

I actively contribute to open-source projects across different domains — from Kubernetes tooling to data science libraries.

---

### ☸️ CNCF Kubernetes — Headlamp

[Headlamp](https://headlamp.dev/) is a CNCF project providing a Kubernetes dashboard. I contributed several improvements to the frontend and backend of this tool.

- Fixed a TypeScript type issue causing runtime errors in the version display
- Added user-friendly toast notifications for failed port-forward operations
- Removed legacy Webpack fallback code that was creating unnecessary bundle overhead
- Added resource allocation summaries on the Node Details page
- Improved error messages shown when cluster actions fail

**→ [All merged PRs](https://github.com/kubernetes-sigs/headlamp/pulls?q=is%3Apr+author%3Aitvi-1234+is%3Aclosed)** — 13 closed PRs, all approved

---

### 🔷 JSON Schema Studio — ioflux-org

[JSON Schema Studio](https://github.com/ioflux-org/studio-json-schema) is an open-source visual editor for JSON Schemas. I contributed multiple fixes and features to improve how schemas are visualized.

- Fixed a bug where schemas with only a `type` keyword were showing the wrong node color
- Fixed cyclic `$ref` schema back-edge color alignment for clearer graph rendering
- Added edge highlighting when a node is clicked, making it easier to trace relationships
- Fixed a `processAST` bug that was causing graph rendering to fail in certain schema structures
- Implemented bidirectional interaction using AST and JSON pointer for better navigation
- Added navbar icons to fullscreen mode for improved usability
- Added SEO meta tags for better search indexing and social sharing

**→ [All merged PRs](https://github.com/ioflux-org/studio-json-schema/pulls?q=is%3Apr+author%3Aitvi-1234+is%3Aclosed)** — 13 closed PRs, all approved

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

---

## 7. Pipeline Overview

```
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
         └─────────────────────────────┘
```

---

## 8. Code Examples

### Example 1 — The Detection Pipeline

**What it does:** Connects data cleaning, feature extraction, and the AI model into one chain.
**Why we need it:** Instead of running separate scripts, a single pipeline processes incoming sensor data automatically and consistently.

```python
from sktime.detection.compose import DetectorPipeline

pipeline = DetectorPipeline(steps=[
    ("clean_data", RobustScaler()),
    ("find_patterns", WindowSummarizer(lag_feature={"mean": [50]})),
    ("ai_detector", SubLOF(n_neighbors=20, novelty=True)),
])

# Train on normal field data only
pipeline.fit(normal_tractor_data)

# Run on live data to spot the rock
danger_scores = pipeline.predict_scores(live_field_data)
```

---

### Example 2 — Advance Detection Time Metric

**What it does:** Measures how many milliseconds before the actual event our AI gave the warning.
**Why we need it:** Standard metrics only say "right" or "wrong". For this project, a warning that comes *after* the blade breaks is useless. We need to reward *early* detection.

```python
class AdvanceDetectionTime:
    def calculate_score(self, actual_event_time, predicted_event_time):
        # How many ms of warning did we give?
        warning_time = actual_event_time - predicted_event_time
        return warning_time
```

---

### Example 3 — Auto-Tuning the Best Settings

**What it does:** Automatically tests different AI sensitivity levels and picks the one that catches the most events with the fewest false alarms.
**Why we need it:** Guessing the right AI settings by hand is not reliable. This tool ensures the manufacturer always ships the most accurate and safest model.

```python
from sktime.detection.compose import AutoTunedDetector

tuner = AutoTunedDetector(
    estimator=SubLOF(),
    param_grid={"sensitivity": [0.01, 0.05, 0.1]},
)

tuner.fit(training_data)
print("Best setting:", tuner.best_params_)
```

---

## 9. Timeline — May 25 to August 25

| Phase | Dates | Goal |
|---|---|---|
| **Phase 1 — Setup** | May 25 – Jun 10 | Understand the dataset, set up the environment, map out data formats, plan the implementation with mentors |
| **Phase 2 — Features** | Jun 11 – Jun 25 | Build the feature extraction tools (RMS, Kurtosis, FFT energy bands) |
| **Phase 3 — Metrics** | Jun 26 – Jul 10 | Implement TPR, FPR, and Advance Detection Time as proper sktime metrics |
| **Phase 4 — Benchmark** *(Midterm)* | Jul 11 – Jul 25 | Build the `DetectionBenchmark` tool; submit midterm evaluation |
| **Phase 5 — Auto-Tuning** | Jul 26 – Aug 10 | Build `AutoTunedDetector` with automatic cross-validation |
| **Phase 6 — Explainability** | Aug 11 – Aug 25 | Add SHAP to show *which sensor* triggered the alert; finalize docs and PRs |

---

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
