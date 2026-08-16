# Model Answers: Research Methods and Information Systems Scenarios

This document provides self-contained model answers to Questions 1–10. The answers are written as academically appropriate examples; exact wording, variables, sample sizes, and statistical procedures may be adapted to a particular proposal or dataset.

---

# QUESTION 1: Digital Education and AI Tutoring

## a. Research problem

A suitable research problem is:

> **Despite the potential of AI-powered mobile tutoring to provide personalized mathematics support in rural secondary schools, there is insufficient local evidence on whether its use improves students' mathematics performance under conditions of limited teacher availability, unequal device access, intermittent connectivity, and differing levels of digital literacy.**

The problem is **researchable** because AI-platform usage and mathematics performance can be measured using system logs, tests, and questionnaires. It is **feasible** if the study is limited to selected schools, classes, or one academic term. It is **significant** because poor access to qualified mathematics teachers can affect educational achievement and AI tutoring may provide additional support. It is **contextually relevant** because rural schools may face infrastructure, affordability, language, device-sharing, and connectivity constraints that make findings from other settings difficult to generalize.

## b. Research objectives and questions

### Objectives
1. To determine the effect of using the AI-powered mobile tutoring platform on students' mathematics performance.
2. To examine the relationship between the frequency/intensity of AI tutoring use and mathematics achievement.
3. To investigate students' and teachers' perceptions of the usefulness, usability, and challenges of the AI tutoring platform.

### Research questions
1. What effect does use of the AI-powered mobile tutoring platform have on students' mathematics performance?
2. How do usage patterns and user perceptions relate to students' mathematics achievement?

## c. Hypotheses

For the main effectiveness test:

- **H₀:** There is no statistically significant difference in mathematics performance between students who use the AI tutoring platform and comparable students who do not use it.
- **H₁:** There is a statistically significant difference in mathematics performance between students who use the AI tutoring platform and comparable students who do not use it.

If a directional hypothesis is justified:

- **H₀:** Use of the AI tutoring platform does not significantly improve mathematics performance.
- **H₁:** Use of the AI tutoring platform significantly improves mathematics performance.

## d. Appropriate research approach

A **mixed-methods approach** is most appropriate. Quantitative data, such as pre-test and post-test scores, platform usage frequency, completion rates, and attendance, can estimate the magnitude of any performance change. Qualitative interviews or focus groups can explain why the platform was or was not effective and identify barriers such as connectivity, language, trust, digital literacy, or teacher support. Combining both forms of evidence provides stronger practical conclusions than either approach alone.

## e. Ethical issues

Because school students are a potentially vulnerable population, the study should obtain approval from the relevant ethics authority and education institutions. **Parental/guardian consent** and, where appropriate, **student assent** should be obtained. Participation should be voluntary and students should not be penalized for declining.

Academic and behavioral data should be collected only when necessary, using **data minimization**. Personally identifying information should be separated from research data or replaced with coded identifiers. Access should be restricted according to roles, and data should be encrypted during transmission and storage where feasible. Researchers should clearly state who can access the data, how long it will be retained, whether it will be shared, and how it will be securely deleted. Reports should present aggregated or anonymized findings. Particular care is needed because behavioral logs may reveal learning difficulties, habits, or patterns that could stigmatize students if misused.

## f. Context diagram and activity diagram

### Context diagram

```text
+----------------+        learning requests/results        +----------------------+
|    Students    | <-------------------------------------> |  AI Tutoring System  |
+----------------+                                         +----------------------+
                                                                    |
                 progress reports / administration                  |
                                                                    v
+----------------+ <------------------------------------------> +----------------+
| Teachers/School|          performance and usage data          | Administrators |
+----------------+                                               +----------------+
                                                                    |
                                                                    v
                                                            +----------------+
                                                            | AI/Content/Data|
                                                            | Services        |
                                                            +----------------+
```

### Activity diagram

```text
(Start)
   |
   v
[Student logs in]
   |
   v
[Select mathematics topic]
   |
   v
[Diagnostic assessment]
   |
   v
[AI analyzes current knowledge]
   |
   v
[Generate personalized lesson/exercises]
   |
   v
[Student answers]
   |
   +---- Incorrect ----> [Give hint/explanation] ----+
   |                                                 |
   +---- Correct ------------------------------------+
                                                     v
                                             [Update progress]
                                                     |
                                                     v
                                             [Store authorized data]
                                                     |
                                                     v
                                                   (End)
```

---

# QUESTION 2: Smart Traffic Management in Kigali

## a. Research problem and narrowing

A suitable research problem is:

> **Traffic congestion and road-safety risks in Kigali may be worsened by limited real-time coordination of traffic information. Although GPS, cameras, IoT sensors, and adaptive traffic lights could support intelligent traffic management, there is insufficient evidence on which data sources and predictive methods most effectively improve congestion prediction and signal decisions in selected Kigali traffic corridors.**

To make the investigation feasible, it should be narrowed to, for example, **three to five high-congestion corridors**, selected intersections, specific peak periods, and one or two measurable outcomes such as average travel time, queue length, delay, or congestion category. A pilot study over several weeks or months is more manageable than attempting to model the entire city.

## b. Primary and secondary data

**Primary data** are collected directly for the current study. Examples include:
- Traffic counts conducted by researchers.
- GPS traces voluntarily provided by sampled vehicles.
- Roadside sensor readings.
- Driver or commuter surveys.
- Interviews with traffic officers and transport planners.
- Direct observation of queues and signal waiting times.

**Secondary data** already exist and were originally collected for another purpose. Examples include:
- Historical traffic records.
- Road-network maps.
- Previous accident statistics.
- Published reports and academic studies.
- Weather records.
- Existing municipal transport datasets.

The main distinction is that primary data are collected specifically to answer the present research questions, whereas secondary data are reused from existing sources.

## c. Sampling strategy

A **multistage stratified sampling strategy** is suitable.

1. Stratify roads or intersections by characteristics such as congestion level, road type, district, or land-use intensity.
2. Randomly or purposively select representative sites from each stratum.
3. Stratify observations by time period, such as morning peak, midday, evening peak, and weekend.
4. For drivers or commuters, use systematic or stratified sampling where a valid sampling frame exists.

This approach improves representation because congestion differs by location and time. A simple sample from one road or one peak period could produce biased conclusions.

## d. Correlation, regression, and classification

**Correlation** can measure the strength and direction of association between variables such as traffic volume and average speed.

**Regression** can model a continuous outcome, for example:

\[
TravelTime = \beta_0 + \beta_1(TrafficVolume) + \beta_2(Weather) + \beta_3(TimeOfDay) + \epsilon
\]

The model can estimate how each predictor is associated with travel time while holding other variables constant.

**Classification** can predict categories such as *free flow*, *moderate congestion*, and *severe congestion*. Inputs may include vehicle count, average speed, occupancy, time, weather, incidents, and historical patterns. Classification performance can be assessed using accuracy, precision, recall, F1-score, and a confusion matrix.

## e. Ethical concerns

GPS and camera data can reveal sensitive movement patterns. Continuous surveillance may affect privacy and create risks of misuse or unauthorized monitoring. Vehicle identifiers and number plates can be personally identifiable when linked with other information.

Safeguards include collecting only necessary data, defining a clear legal basis and purpose, providing notices where required, limiting retention periods, pseudonymizing identifiers, controlling access, encrypting data, auditing access, and establishing procedures for breaches and third-party sharing. Data collected for traffic optimization should not be reused for unrelated purposes without appropriate authorization.

## f. Data-flow diagram and class diagram

### Level-0 data-flow diagram

```text
[GPS Devices] ----\
[Traffic Cameras] ---> (Traffic Data Collection) ---> (Data Processing)
[IoT Sensors] ----/                                      |
                                                          v
                                                  (Prediction Engine)
                                                          |
                                                          v
                                                   (Control Decisions)
                                                          |
                              +---------------------------+------------------+
                              v                           v                  v
                       [Traffic Lights]            [Traffic Dashboard] [Alerts]
```

### Class diagram

```text
+----------------+        +----------------+
| RoadSegment    |        | Sensor         |
|----------------|        |----------------|
| roadId         |1      *| sensorId       |
| name           |--------| location       |
| length         |        | status         |
+----------------+        +----------------+

+----------------+        +----------------+
| TrafficReading |        | Prediction     |
|----------------|        |----------------|
| readingId      |        | predictionId   |
| time           |        | congestionLevel|
| speed          |        | forecastTime   |
| volume         |        +----------------+
+----------------+                ^
        ^                         |
        |                         |
        +-------------------------+
                  used by
             +----------------+
             | TrafficController|
             |----------------|
             | controlId      |
             | optimizeSignal()|
             +----------------+
                    |
                    v
             +----------------+
             | TrafficLight   |
             |----------------|
             | lightId        |
             | state          |
             | changeTiming() |
             +----------------+
```

---

# QUESTION 3: AI-Based Smart Agriculture

## a. Research aim and objectives

### Aim
To evaluate whether an AI-based forecasting system using environmental, soil, satellite, and historical agricultural data can improve crop-yield prediction for smallholder farming contexts in Rwanda.

### Objectives
1. To compile and preprocess rainfall, temperature, soil, satellite-imagery, and historical crop-yield data.
2. To identify the environmental and agricultural variables most strongly associated with crop productivity.
3. To develop and train an AI-based crop-yield prediction model.
4. To compare the prediction accuracy of the AI model with an appropriate baseline forecasting method.

## b. Hypothesis

- **H₀:** The AI-based forecasting model does not significantly improve crop-yield prediction accuracy compared with the baseline model.
- **H₁:** The AI-based forecasting model significantly improves crop-yield prediction accuracy compared with the baseline model.

Accuracy may be operationalized using MAE, RMSE, or another pre-specified error measure.

## c. Inductive and deductive reasoning

**Inductive reasoning** moves from observations to broader patterns or propositions. Researchers could explore historical farm and environmental data, observe recurring relationships between rainfall, vegetation indicators, soil characteristics, and yields, and use those patterns to develop candidate predictors or hypotheses.

**Deductive reasoning** begins with a theory or hypothesis and tests it using data. For example, the researchers may hypothesize that combining multi-source environmental variables will reduce prediction error compared with a historical-average model. The hypothesis is then tested on training and independent test data.

Thus, induction is useful for discovering patterns, while deduction is useful for formally testing proposed relationships.

## d. Stratified sampling

Stratified sampling is justified because agricultural conditions are heterogeneous. The population can be divided into strata based on:
- Agro-ecological zones.
- Major crop types.
- Soil characteristics.
- Altitude or climatic conditions.

A sample is then selected from each relevant stratum. This increases the likelihood that important environmental diversity is represented and can improve generalizability compared with sampling only from easily accessible farms.

## e. Statistical techniques

**Correlation analysis** can identify variables associated with crop yield, although correlation does not establish causation.

**Regression analysis** can estimate the relationship between yield and multiple predictors, for example rainfall, temperature, soil properties, and vegetation indices. Regression coefficients can help assess the contribution of predictors under model assumptions.

**Principal Component Analysis (PCA)** can reduce a large set of correlated variables into fewer components that preserve substantial variation. PCA can reduce multicollinearity and simplify later modelling, although transformed components may be less directly interpretable.

## f. Flowchart and correlation diagram

### Flowchart

```text
(Start)
   |
[Collect rainfall, temperature, soil, imagery, yield data]
   |
[Clean and validate data]
   |
[Feature engineering/selection]
   |
[Split data: training, validation, test]
   |
[Train AI model]
   |
[Evaluate prediction accuracy]
   |
{Accuracy acceptable?}
   | Yes                     | No
   v                         v
[Deploy/Report]       [Tune model/features]
   |                         |
 (End) <---------------------+
```

### Correlation diagram

```text
Rainfall -----------\
Temperature ---------\
Soil properties ------> [Crop Yield]
Satellite indicators -/       ^
Historical records --/        |
                              |
                     Other factors/confounders
```

---

# QUESTION 4: Cybersecurity Awareness in SMEs

## a. Literature review, research gap, and theory

A literature review systematically examines previous studies on phishing, cybersecurity training, employee behavior, human error, and security incidents. It can identify what has already been established, such as whether training generally improves awareness, and what remains uncertain.

A research gap may be found if, for example, previous studies were conducted mainly in large organizations, measured only knowledge rather than actual behavior, or did not examine SMEs in the relevant context. The review can also establish a theoretical foundation using behavioral or technology-adoption theories, helping explain how training may influence knowledge and behavior.

## b. Research framework

```text
Cybersecurity Training
          |
          v
 Employee Knowledge
          |
          v
  Security Behavior
          |
          v
 Security Incidents

Possible controls: job role, prior experience, education, access privileges,
organization size, baseline security maturity.
```

Knowledge may act as a **mediating variable**: training may improve knowledge, which then influences behavior. Improved behavior may reduce the probability or frequency of incidents.

## c. Hypotheses

- **H₀:** The cybersecurity-awareness programme has no statistically significant effect on employee cybersecurity knowledge or security behavior.
- **H₁:** The cybersecurity-awareness programme has a statistically significant positive effect on employee cybersecurity knowledge or security behavior.

A separate incident hypothesis may be:

- **H₀:** The rate of security incidents does not differ before and after implementation of the programme.
- **H₁:** The rate of security incidents is lower after implementation of the programme.

## d. Chi-square, t-test, and ANOVA

**Chi-square** is appropriate for examining association between categorical variables, such as whether employees completed training (yes/no) and whether they correctly reported a simulated phishing message (yes/no), provided assumptions regarding expected frequencies are satisfied.

A **t-test** is appropriate for comparing the means of two groups, such as trained versus untrained employees. A paired t-test may compare the same employees' knowledge scores before and after training.

**ANOVA (F-test)** is appropriate for comparing means across three or more groups, such as employees receiving basic, intermediate, or intensive training. If ANOVA is significant, appropriate post-hoc tests can identify which groups differ.

## e. Ethical challenges and safeguards

Performance monitoring may create fear, stigma, or employment consequences. Employees may feel pressured to participate or may not understand how data from phishing simulations or security logs will be used.

Safeguards include informed participation where appropriate, clear purpose limitation, collecting only necessary variables, pseudonymizing research datasets, restricting access, reporting aggregated results, separating research findings from disciplinary processes where possible, and establishing retention and deletion schedules. Researchers should avoid deceptive testing unless ethically justified and approved, and should minimize unnecessary psychological or employment harm.

## f. Flowchart and ER diagram

### Flowchart

```text
(Start)
   |
[Assess baseline knowledge/behavior]
   |
[Deliver cybersecurity training]
   |
[Conduct assessment or simulation]
   |
[Collect authorized performance data]
   |
[Analyze knowledge and behavior]
   |
[Identify gaps]
   |
[Provide targeted improvement]
   |
 (End)
```

### Entity-relationship diagram

```text
[EMPLOYEE] 1 ----- participates in ----- * [TRAINING_SESSION]
    |
    | 1
    +------ completes ------ * [ASSESSMENT]
                                  |
                                  | may generate
                                  v
                             [SECURITY_EVENT]

EMPLOYEE(employee_id, role, ...)
TRAINING_SESSION(session_id, topic, date)
ASSESSMENT(assessment_id, score, result)
SECURITY_EVENT(event_id, type, date, severity)
```

---

# QUESTION 5: Digital Health and Community Health Workers

## a. Cross-sectional versus longitudinal design

A **cross-sectional design** measures variables at one point in time. It is useful for estimating current application use, adherence, or user perceptions, but it cannot directly show how outcomes change over time.

A **longitudinal design** follows the same patients, health workers, or facilities across multiple time points. It can measure changes in adherence and reporting after introduction of the application and is therefore generally more appropriate for evaluating an intervention over time. A longitudinal design requires more resources and must address participant loss and repeated measurements.

## b. Data sources and instruments

### Primary data
- Community health worker surveys.
- Patient interviews, where ethically appropriate.
- Direct observation.
- Application usability questionnaires.
- Prospectively collected adherence records.

Suitable instruments include structured questionnaires, interview guides, observation checklists, and validated adherence scales.

### Secondary data
- Existing patient records.
- Disease-surveillance databases.
- Historical treatment and appointment records.
- Application usage logs, if already routinely generated.

Data extraction forms and secure, authorized database queries can be used to collect secondary data.

## c. Data preparation

1. **Data cleaning:** remove duplicates, correct obvious data-entry errors, standardize dates and categories, and check ranges.
2. **Missing values:** quantify missingness and investigate its pattern. Depending on the mechanism and amount, use complete-case analysis, appropriate imputation, or explicit missing categories where justified. Missing values should not be replaced automatically without analysis.
3. **Normalization/scaling:** rescale variables when methods are sensitive to different measurement ranges, for example using min-max scaling or z-score standardization.
4. **Validation:** apply range, type, format, consistency, and cross-field checks. Compare a sample against source records where authorized.

All transformations should be documented and reproducible.

## d. Correlation and regression

Correlation can provide an initial estimate of association between application usage and patient adherence.

Regression can model adherence as an outcome while controlling for confounders. For example, a linear model may be used for a continuous adherence score, while logistic regression may be used when adherence is classified as adherent/non-adherent.

A simplified model is:

\[
Adherence = \beta_0 + \beta_1(AppUsage) + \beta_2(Age) + \beta_3(TravelDistance) + \cdots + \epsilon
\]

A statistically significant association does not by itself prove that application use causes improved adherence.

## e. Ethical framework

A comprehensive framework should include:

- **Informed consent:** explain the study purpose, data collected, risks, benefits, voluntary participation, and withdrawal procedures.
- **Confidentiality:** restrict information access to authorized personnel and apply role-based access controls.
- **Anonymization/pseudonymization:** remove or replace direct identifiers in research datasets; recognize that complete anonymization may be difficult.
- **Secure storage:** encrypt sensitive information, use secure authentication, maintain backups, and log access.
- **Data minimization and purpose limitation:** collect only data necessary for defined objectives and do not reuse it incompatibly.
- **Responsible use:** prohibit discrimination, stigmatization, unauthorized sharing, and inappropriate automated decisions.
- **Governance:** define accountability, retention periods, deletion procedures, breach response, ethics oversight, and compliance with applicable health and data-protection rules.

---

# QUESTION 6: Blockchain-Based Land Registration

## a. Research problem

A suitable research problem is:

> **Paper-based land-registration processes may experience delays, fragmented records, limited auditability, opportunities for unauthorized alteration, and difficulties in verifying transaction history. Although blockchain-based systems are proposed as a potential solution, there is insufficient context-specific evidence regarding whether such systems can improve registration efficiency, transparency, record integrity, and user trust without creating unacceptable legal, technical, privacy, or governance risks.**

The study can be narrowed to one jurisdiction, selected registration offices, a defined transaction type, or a prototype/pilot rather than evaluating nationwide implementation.

## b. Objectives and research questions

### Objectives
1. To assess inefficiencies and integrity risks in the existing land-registration process.
2. To evaluate the potential effect of blockchain adoption on processing time, transparency, and record verification.
3. To identify legal, technical, organizational, and user-related barriers to adoption.

### Research questions
1. How could a blockchain-based platform affect the efficiency, transparency, and integrity of land-registration processes?
2. What factors enable or constrain adoption of blockchain technology in land administration?

## c. Sequential hypothesis-testing process

1. Define the research question and measurable variables.
2. Formulate **H₀**, usually representing no effect or no difference.
3. Formulate **H₁**, representing the expected effect or difference.
4. Select an appropriate statistical test based on variable type, design, and assumptions.
5. Choose a significance level, commonly \(\alpha = 0.05\).
6. Collect and prepare the data.
7. Calculate the test statistic and p-value or confidence interval.
8. Compare the evidence with the decision criterion.
9. **Reject H₀** when evidence is sufficiently inconsistent with H₀; otherwise **fail to reject H₀**. Failure to reject is not proof that H₀ is true.
10. Interpret practical as well as statistical significance and report assumptions and limitations.

## d. Parametric and non-parametric tests

**Parametric tests** generally rely on assumptions about the distribution or parameters of the data. Examples include t-tests, ANOVA, and Pearson correlation. They are appropriate when measurement scales and assumptions such as independence and approximate distributional conditions are adequately satisfied.

**Non-parametric tests** make fewer distributional assumptions and are useful for ordinal data, highly skewed data, or small samples where parametric assumptions are not reasonable. Examples include Mann–Whitney U, Wilcoxon signed-rank, Kruskal–Wallis, Spearman correlation, and chi-square tests for categorical data.

The choice should be based on study design and diagnostics, not simply on sample size.

## e. Legal, ethical, IP, ownership, and jurisdictional issues

Land records involve property rights and therefore require clear legal recognition of digital records, electronic signatures, and system outputs. Privacy concerns arise if personal or ownership information is made unnecessarily visible. Immutable storage can conflict with correction, rectification, or retention requirements.

The study must clarify **who owns and controls the data**, who may write or validate records, and who is responsible for errors. Intellectual-property issues may concern software, smart-contract code, databases, and licensing. Jurisdictional questions arise if infrastructure, nodes, cloud providers, or users operate across borders. A blockchain design does not automatically solve governance problems; legal authority, dispute resolution, correction procedures, key management, and accountability must be defined.

---

# QUESTION 7: Multigranularity Deep Learning for LULC Classification

## a. Research problem

A suitable problem is:

> **Conventional single-scale deep-learning approaches to Land Use and Land Cover classification may fail to represent objects and spatial patterns that occur at different scales. Fine details may be lost in coarse representations, while broad contextual information may be insufficiently captured by fine-scale models. There is therefore a need to investigate whether a multigranularity deep-learning model can improve classification of heterogeneous LULC classes in Kigali compared with an appropriate single-scale baseline.**

## b. Objectives and research questions

### Objectives
1. To develop a multigranularity deep-learning model integrating fine-, medium-, and coarse-scale spatial features.
2. To evaluate its performance across built-up areas, agriculture, forests, wetlands, water bodies, and bare land.
3. To compare its performance with a conventional single-scale deep-learning classifier.

### Research questions
1. Does multigranularity feature integration improve LULC classification performance compared with a single-scale model?
2. Which LULC classes benefit most from multigranularity spatial representation?

## c. Variables

- **Independent variable:** classification approach or model architecture, particularly multigranularity versus single-scale representation.
- **Dependent variables:** classification performance measures such as accuracy, precision, recall, F1-score, and IoU.
- **Control variables:** satellite dataset, geographic extent, class definitions, training/test split, preprocessing, computational budget where possible, and evaluation procedure.
- **Possible confounding variables:** image resolution, acquisition season, cloud contamination, class imbalance, label quality, sensor differences, terrain, and unequal spatial distribution of classes.

## d. Hypotheses

- **H₀:** The multigranularity deep-learning model does not produce significantly better LULC classification performance than the conventional single-scale classifier.
- **H₁:** The multigranularity deep-learning model produces significantly better LULC classification performance than the conventional single-scale classifier.

The comparison should specify the metric and unit of statistical comparison, such as repeated experimental runs or matched image tiles.

## e. Performance measures

- **Accuracy:** proportion of correctly classified observations. Overall accuracy can be misleading when classes are imbalanced.
- **Precision:** \(TP/(TP+FP)\). It measures how many predicted positives are actually positive.
- **Recall:** \(TP/(TP+FN)\). It measures how many actual positives are correctly detected.
- **F1-score:** harmonic mean of precision and recall, useful when balancing both types of error.
- **Intersection over Union (IoU):** overlap between predicted and reference regions, commonly used for segmentation:
  \[
  IoU = \frac{TP}{TP+FP+FN}
  \]
- **Confusion matrix:** a table showing actual versus predicted classes, allowing examination of which classes are commonly confused.

Results should preferably be reported per class as well as overall.

---

# QUESTION 8: Smart City Waste Management

## a. Research problem

A suitable research problem is:

> **Conventional waste collection often relies on fixed schedules and limited real-time information, which may cause unnecessary collection trips, overflowing bins, inefficient vehicle routes, and uneven service quality. There is insufficient evidence on whether integrating IoT bin data, vehicle GPS information, mobile reporting, and predictive analytics can improve forecasting of waste-generation patterns and optimize collection operations in the selected urban context.**

The problem is important because inefficiency can increase costs, fuel use, environmental impacts, and public-health risks.

## b. Research aim, objectives, and questions

### Aim
To investigate whether an intelligent waste-management system can improve prediction of waste generation and optimization of collection operations.

### Objectives
1. To analyze current waste-generation and collection patterns.
2. To collect and integrate IoT bin, GPS, mobile-application, and operational data.
3. To develop a predictive model for waste generation or bin-fill status.
4. To evaluate whether data-driven scheduling can reduce overflow, travel distance, delay, or operational cost.

### Research questions
1. Which factors and data features most effectively predict waste-generation or bin-fill patterns?
2. To what extent can predictive analytics improve waste-collection scheduling compared with conventional fixed schedules?

## c. Data sources and instruments

### Primary data
- Bin sensor readings.
- Direct observation of overflow.
- GPS data from collection vehicles.
- Interviews or surveys of operators and residents.
- Field measurements of collected waste.

Instruments include IoT sensors, GPS devices, observation checklists, weighing equipment, questionnaires, and interview guides.

### Secondary data
- Historical collection records.
- Municipal waste statistics.
- Route maps.
- Population or land-use data.
- Weather records where relevant.

Database extraction tools and standardized data-collection forms can support secondary-data collection.

## d. Regression and classification

Regression can predict continuous outcomes such as kilograms of waste generated or estimated fill level. Predictors may include location, day of week, season, population density, previous collection, weather, and historical patterns.

Classification can predict categories such as *low*, *medium*, or *high* fill level, or whether a bin is likely to overflow before the next planned collection. Predicted priorities can then feed into route-optimization or scheduling algorithms. Models should be evaluated on data not used for training and compared with a baseline.

## e. Ethical and practical challenges

Location and household-related data may reveal routines, socioeconomic patterns, or service use. Municipal data may also contain commercially or operationally sensitive information.

Mitigations include collecting only necessary location precision, aggregating household data where possible, separating identities from analytics datasets, restricting access, securing devices and APIs, defining retention periods, and informing affected users about data practices. Practical challenges include sensor failure, network outages, vandalism, incomplete data, interoperability, maintenance costs, staff training, and unequal access to mobile applications.

---

# QUESTION 9: E-Learning and Student Performance

## a. Literature review and conceptual framework

A literature review can synthesize evidence on LMS engagement, self-regulated learning, digital access, academic achievement, and learning analytics. It can identify inconsistent findings, under-studied contexts, limitations of previous measures, or gaps in controlling for prior academic ability.

A conceptual framework could propose:

```text
LMS Engagement
(login frequency, time, submissions, discussion)
             |
             v
      Learning Processes
(self-regulation, participation, engagement)
             |
             v
   Academic Performance

Moderators: digital access, course type, year of study
Controls: prior performance, demographics, workload
```

The literature should justify each proposed relationship rather than treating all available variables as equally meaningful.

## b. Variables

- **Independent variable:** LMS engagement, operationalized using indicators such as logins, time on materials, submissions, and participation.
- **Dependent variable:** academic performance, such as examination score or final grade.
- **Mediating variable:** a mechanism through which engagement may influence performance, for example self-regulated learning or assignment completion.
- **Moderating variable:** a factor changing the strength or direction of the relationship, for example digital access, course type, or prior digital skills.
- **Control variables:** prior academic performance, study level, workload, attendance, or other justified baseline characteristics.

## c. Directional and non-directional hypotheses

### Directional
- **H₀:** Higher LMS engagement is not associated with higher academic performance.
- **H₁:** Higher LMS engagement is positively associated with higher academic performance.

### Non-directional
- **H₀:** There is no statistically significant relationship between LMS engagement and academic performance.
- **H₁:** There is a statistically significant relationship between LMS engagement and academic performance.

## d. Correlation and multiple regression

Correlation can summarize the direction and strength of association between individual LMS measures and performance.

Multiple regression can examine several predictors simultaneously:

\[
Performance = \beta_0 + \beta_1(Logins) + \beta_2(TimeSpent) + \beta_3(Submissions) + \beta_4(PriorPerformance) + \epsilon
\]

Regression helps estimate the association of each predictor while controlling for others. Researchers should check assumptions, multicollinearity, influential observations, and the validity of interpreting LMS “time spent” as genuine learning activity.

## e. Bias and confounding

Possible biases include:
- **Selection bias:** students who use the LMS more may already be more motivated.
- **Measurement bias:** login counts may not equal meaningful engagement.
- **Confounding:** prior ability, motivation, socioeconomic resources, internet access, and instructor quality may affect both LMS use and grades.
- **Reverse causality:** high-performing students may engage differently because they are already succeeding.

The design can reduce these problems by collecting baseline variables, using clearly defined measures, applying multivariable adjustment, using longitudinal data where possible, pre-specifying analyses, and avoiding causal claims unless the design supports them.

---

# QUESTION 10: AI-Based Healthcare Diagnosis

## a. Research problem

A suitable research problem is:

> **AI-assisted diagnostic systems may support earlier and more consistent disease identification by integrating symptoms, laboratory results, medical images, and clinical records. However, evidence is needed to determine whether the proposed system improves diagnostic accuracy, timeliness, or clinical decision support in the intended hospital context, and whether performance is equitable, explainable, safe, and acceptable to healthcare professionals.**

The research gap should be made specific, for example limited validation on local patient populations, inadequate comparison with clinicians or existing diagnostic procedures, insufficient evidence about particular disease groups, or lack of evaluation of bias and clinical workflow effects.

## b. Research objectives and questions

### Objectives
1. To develop or configure the AI diagnostic system using appropriately governed clinical data.
2. To evaluate diagnostic accuracy and other performance measures against a defined reference standard.
3. To compare diagnostic performance or decision support with existing clinical practice where ethically and methodologically appropriate.
4. To assess usability, explainability, fairness, and clinician acceptance.
5. To identify safety, ethical, and implementation risks.

### Research questions
1. How accurately does the AI diagnostic system identify the target disease conditions compared with an accepted reference standard?
2. How does AI-assisted decision support affect diagnostic performance, timeliness, and clinician acceptance?
3. Does performance differ meaningfully across relevant patient subgroups?

## c. Quantitative, qualitative, and mixed methods

**Quantitative research** uses numerical measurements and statistical analysis. It is appropriate for diagnostic sensitivity, specificity, AUROC, error rates, and time-to-decision.

**Qualitative research** examines experiences and meanings through interviews, observations, or open-ended responses. It is useful for understanding clinician trust, workflow fit, explainability, and perceived risks.

**Mixed methods** combines both. It is the strongest overall choice here because a healthcare diagnostic system must be evaluated not only for numerical accuracy but also for usability, safety, trust, and implementation context.

## d. Sampling, preprocessing, hypothesis testing, and model evaluation

**Sampling:** Define the target patient population and eligibility criteria. Use a representative or carefully justified sampling method, and ensure independent training, validation, and test sets. Prevent data leakage, especially when multiple records or images belong to the same patient.

**Preprocessing:** Check data quality, handle missingness appropriately, standardize formats, encode variables, normalize inputs when needed, and document transformations. Labels should be validated against an appropriate clinical reference standard.

**Hypothesis testing:** Pre-specify hypotheses, outcomes, comparison methods, significance levels, and subgroup analyses. For example, test whether AI-assisted diagnosis has higher sensitivity or accuracy than a baseline under a defined evaluation design.

**Model evaluation:** Use measures suitable for the task, such as sensitivity, specificity, precision, recall, F1-score, AUROC, calibration, and confusion matrices. Evaluate external validity where possible and report confidence intervals. Clinical usefulness should also be assessed; a high statistical score does not guarantee safe real-world benefit.

## e. Ethical implications

Key issues include:

- **Informed consent and lawful governance:** determine when consent is required and ensure data use is consistent with ethical approval and applicable rules.
- **Privacy and confidentiality:** minimize identifiable data, apply access controls, encryption, secure storage, and appropriate retention/deletion procedures.
- **Bias and fairness:** examine whether training data underrepresent certain populations and evaluate subgroup performance to reduce unequal harm.
- **Explainability:** provide clinicians with sufficiently understandable information about outputs, limitations, uncertainty, and appropriate use.
- **Accountability:** clearly define responsibility for data quality, model maintenance, clinical decisions, and adverse events. AI recommendations should not obscure professional accountability.
- **Potential harm:** false positives, false negatives, automation bias, delayed treatment, inappropriate trust, and cybersecurity failures must be assessed and mitigated.
- **Human oversight:** deployment should include clear escalation pathways and ensure that clinicians can question or override AI recommendations when clinically justified.
- **Monitoring:** model performance can change as patient populations, equipment, and clinical practices change; therefore, ongoing validation, auditing, incident reporting, and controlled updates are necessary.

---

# Concluding Note

Across all scenarios, a strong research design requires clear alignment among the **research problem, aim, objectives, questions, hypotheses, variables, data sources, sampling strategy, analytical methods, evaluation measures, and ethical safeguards**. Diagrams should be adapted to the exact system requirements, and statistical methods should be selected according to the type of data, study design, assumptions, and intended inference.





-----------
-----------

Research Methods & System Analysis — Key Takeaways

Big picture:
Problem → Objectives → Questions → Hypotheses → Approach → Sampling → Data Analysis → System Modelling

1. Research Problem
Key takeaway

A research problem explains:

What is wrong/unknown + why it matters + what needs to be investigated.

Remember

Current situation → Problem → Knowledge gap → Need for research

Template

Although [current situation], [problem] remains a challenge. While [technology/intervention] may address the problem, there is limited evidence about [what is unknown]. Therefore, research is needed to investigate [what you want to study].

Don't confuse
❌ Technology = not necessarily the research problem
✅ The problem/gap surrounding the technology = research problem
Example

Rural students have limited access to qualified mathematics teachers, and it is unclear whether AI tutoring improves their mathematics performance.

2. Research Objectives
Key takeaway

An objective says:

What the researcher intends to DO.

Usually begins with:

To determine
To examine
To assess
To investigate
To evaluate
To identify
To compare
To explore
Formula

To + action verb + variable/topic + context

Example

To determine the effect of AI tutoring on mathematics performance.

General vs specific objectives

General objective:

The overall purpose of the study.

Specific objectives:

Smaller measurable tasks used to achieve the general objective.

Golden rule

Each objective should be:

Clear
Specific
Measurable
Relevant to the research problem
Achievable
3. Research Questions
Key takeaway

A research question says:

What does the researcher want to find out?

The question should correspond directly to an objective.

Example

Objective:

To determine the effect of AI tutoring on mathematics performance.

Question:

What is the effect of AI tutoring on mathematics performance?

Common conversions
Objective	Research question
To determine the effect of X on Y	What is the effect of X on Y?
To examine relationship between X and Y	What is the relationship between X and Y?
To compare A and B	Is there a difference between A and B?
To assess the level of X	What is the level of X?
To identify factors influencing X	What factors influence X?
To explore perceptions of X	What are users' perceptions of X?
To determine whether X predicts Y	To what extent does X predict Y?
Key rule

Objective = statement.
Question = question.

4. Hypotheses
Key takeaway

A hypothesis is:

A testable prediction about a relationship, effect, difference, or prediction.

You normally derive it from your research question/objective.

Two main hypotheses

H₀ = Null hypothesis

No significant effect/relationship/difference.

H₁ = Alternative hypothesis

Significant effect/relationship/difference exists.

Example

Research question:

What is the effect of AI tutoring on mathematics performance?

H₀:

AI tutoring has no statistically significant effect on mathematics performance.

H₁:

AI tutoring has a statistically significant effect on mathematics performance.

Remember

H₀ = Nothing significant is happening.

H₁ = Something significant is happening.

5. Hypothesis Types
Effect

RQ:

What is the effect of X on Y?

H₀:

X has no significant effect on Y.

H₁:

X has a significant effect on Y.

Relationship

RQ:

What is the relationship between X and Y?

H₀:

There is no significant relationship between X and Y.

H₁:

There is a significant relationship between X and Y.

Difference

RQ:

Is there a difference between Group A and Group B?

H₀:

There is no significant difference.

H₁:

There is a significant difference.

Prediction

RQ:

To what extent does X predict Y?

H₀:

X does not significantly predict Y.

H₁:

X significantly predicts Y.

6. Research Approach
Key takeaway

Research approach asks:

What type of evidence do I need to answer my research problem?

There are three main approaches.

Quantitative

Numbers + measurement + statistics

Use when you want to:

Measure
Compare
Test relationships
Test effects
Predict
Test hypotheses
Think:

How much? How many? How strong? Does X affect Y?

Qualitative

Words + experiences + meanings

Use when you want to understand:

Experiences
Perceptions
Opinions
Feelings
Challenges
Motivations
Why/how something happens
Think:

Why? How? What do people experience?

Mixed Methods

Quantitative + qualitative

Use when you need both:

“Does it work?” + “Why/how does it work?”

Example

AI tutoring:

Pre/post-test → quantitative
Student interviews → qualitative
Both → mixed methods
7. Research Approach vs Research Design

Don't confuse these.

Research approach

How broadly will you investigate?

Quantitative
Qualitative
Mixed methods
Research design

What specific structure will you use?

Examples:

Experimental
Quasi-experimental
Correlational
Survey
Case study
Descriptive
Example

Approach: Quantitative
Design: Quasi-experimental

8. Sampling
Key takeaway

Sampling asks:

Who will participate, and how will I select them?

Important terms

Population

Everyone you want to study.

Sample

The smaller group you actually study.

Sampling strategy

The method used to select the sample.

9. Probability Sampling

Everyone has a known chance of selection.

Usually useful for quantitative research.

Simple Random

Everyone has an equal chance.

Think: random selection.

Systematic

Select every kth person.

Example:

Every 10th student.

Think: fixed interval.

Stratified

Divide population into groups and sample from each group.

Example:

Sample students from every year of study.

Think:

EVERY GROUP

Cluster

Divide into natural groups and select some groups.

Example:

Select 10 schools and study students within those schools.

Think:

SOME GROUPS

Multistage

Sampling occurs through several levels.

Example:

District → School → Student

Think:

Several stages

10. Non-Probability Sampling

Not everyone has a known/equal chance.

Purposive

Deliberately select people with relevant knowledge/experience.

Think:

Specific people

Example:

CHWs who have used a mobile health application.

Convenience

Select whoever is easiest to access.

Think:

Easy to reach

Snowball

Participants recommend other participants.

Think:

Participant → participant → participant

Quota

Recruit until predetermined subgroup numbers are reached.

Example:

50 males + 50 females.

11. Sampling Cheat Sheet
Situation	Strategy
Equal chance	Simple random
Every kth person	Systematic
People from every subgroup	Stratified
Select whole groups	Cluster
Several sampling levels	Multistage
Specific experience needed	Purposive
Easiest people to reach	Convenience
Participants recruit others	Snowball
Fill subgroup targets	Quota
Most important distinction

Stratified = sample FROM every group.

Cluster = select SOME groups.

12. Correlation
Key takeaway

Correlation asks:

Are X and Y related?

Example:

Is LMS engagement related to academic performance?

Correlation coefficient

Usually r.

Range:

-1 to +1

+1 = perfect positive relationship
0 = no linear relationship
-1 = perfect negative relationship
Remember

Correlation = CONNECTION

Very important

Correlation does not automatically mean causation.

If X and Y are correlated, it does not prove X caused Y.

13. Regression
Key takeaway

Regression asks:

Can X be used to predict Y?

Example:

Can LMS engagement predict examination performance?

Basic equation:

Y = b₀ + b₁X

Where:

Y = outcome
X = predictor
b₀ = intercept
b₁ = coefficient/slope
Remember

Regression = PREDICTION

14. Correlation vs Regression
Correlation	Regression
Relationship	Prediction
X ↔ Y	X → Y
Measures association	Models/predicts outcome
Uses correlation coefficient	Uses regression equation/coefficients
Memory

Correlation = Are they connected?

Regression = Can X predict Y?

15. Classification
Key takeaway

Classification predicts a:

CATEGORY / CLASS

Examples:

Disease / No disease
Phishing / Legitimate
Pass / Fail
Forest / Agriculture / Water
At-risk / Not at-risk
Remember

Classification = CATEGORY

Compare
Technique	Predicts
Regression	Number
Classification	Category

Example:

Crop yield = 3.5 tonnes → Regression

Crop type = Maize → Classification

16. Classification Algorithms

Common examples:

Decision Tree

Makes decisions through rules.

If attendance < 50% → At risk.

K-Nearest Neighbors (KNN)

Looks at similar/nearby examples and uses their classes.

Logistic Regression

Despite its name, it is often used for:

Classification, especially binary outcomes.

17. Classification Evaluation

A common tool is the confusion matrix.

	Actual Positive	Actual Negative
Predicted Positive	TP	FP
Predicted Negative	FN	TN
Remember
TP = correctly predicted positive
TN = correctly predicted negative
FP = false alarm
FN = missed positive

Important metrics:

Accuracy = overall correctness
Precision = correctness of positive predictions
Recall = how many actual positives were found
18. Context Diagram
Key takeaway

A context diagram shows:

Who/what interacts with the entire system?

It gives the big picture.

Example:

Student ───────→
               │
Teacher ───────→ AI TUTORING SYSTEM
               │
Admin ─────────→

Important

The system is normally treated as one single process.

Remember:

Context = SYSTEM + EXTERNAL INTERACTIONS

19. DFD

DFD = Data Flow Diagram

Key takeaway

A DFD shows:

How data moves through the system.

It can show:

External entities
Processes
Data stores
Data flows

Example:

Student
   ↓
Submit Question
   ↓
AI Processing
   ↓
Generate Answer
   ↓
Student

Remember

DFD = DATA FLOW

20. Context Diagram vs DFD
Context	DFD
High-level	More detailed
Whole system as one process	Multiple processes
External interactions	Data movement
Big picture	Internal data flow
Memory

Context = WHO interacts?

DFD = HOW DOES DATA MOVE?

21. Activity Diagram
Key takeaway

Shows:

Activities and their sequence/workflow.

Example:

START
  ↓
Login
  ↓
Select Topic
  ↓
Answer Question
  ↓
Correct?
 /    \
Yes    No
 ↓      ↓
Next   Hint
  \    /
    ↓
   END


Can show:

Start
Activities
Decisions
Loops
End
Remember

Activity = WORKFLOW

22. Flowchart
Key takeaway

A flowchart shows:

Procedural or algorithmic logic.

Example:

START
  ↓
Enter marks
  ↓
Marks ≥ 50?
 /       \
Yes       No
 ↓         ↓
PASS      FAIL
 \         /
    ↓
   END

Remember

Flowchart = ALGORITHM / LOGIC

23. Activity Diagram vs Flowchart

They are similar, but:

Activity diagram

Focuses on:

System/business workflow

Example:

Submit assignment → teacher reviews → grade recorded.

Flowchart

Focuses on:

Algorithm/procedure

Example:

Input marks → calculate average → if average ≥ 50 → pass.

Memory

Activity = WORK

Flowchart = LOGIC

24. Class Diagram
Key takeaway

A class diagram shows:

Classes/objects, their attributes, methods, and relationships.

Example:

+------------------+
|     Student      |
+------------------+
| studentID        |
| name             |
| email            |
+------------------+
| login()          |
| submitAnswer()   |
+------------------+


A class contains:

Class name
Attributes
Methods/operations
Remember

Class = SOFTWARE OBJECTS

25. ERD

ERD = Entity Relationship Diagram

Key takeaway

An ERD shows:

What data the database stores and how entities are related.

Example:

STUDENT
---------
StudentID PK
Name
Email

     |
     | enrolls
     ↓

COURSE
---------
CourseID PK
CourseName


Important concepts:

Entity
Attribute
Primary key
Foreign key
Relationship
Cardinality
Remember

ERD = DATABASE

26. Class Diagram vs ERD
Class Diagram	ERD
Software design	Database design
Classes	Entities
Attributes	Attributes
Methods	Usually no methods
Inheritance	Relationships/keys
Objects	Stored data
Memory

Class = how software objects behave

ERD = how database data is organized

27. Collaboration Diagram

Also commonly called a communication diagram.

Key takeaway

It shows:

Which objects communicate with each other and what messages they exchange.

Example:

Student
   |
1: login()
   ↓
Mobile App
   |
2: authenticate()
   ↓
Authentication Server
   |
3: verify()
   ↓
Database


The numbered messages are important.

Remember

Collaboration = OBJECT COMMUNICATION

28. All Diagram Types — One Table
| Diagram | Main question | Keyword |
|---|---|---|
| **Context Diagram** | Who interacts with the system? | **Interaction** |
| **DFD** | How does data move? | **Data** |
| **Activity Diagram** | What activities happen? | **Workflow** |
| **Flowchart** | What is the algorithm/logic? | **Logic** |
| **Class Diagram** | What software objects exist? | **Objects** |
| **ERD** | What data is stored? | **Database** |
| **Collaboration Diagram** | Which objects communicate? | **Communication** |


29. The Entire Topic in One Memory Map
```
RESEARCH
│
├── Research Problem
│     └── What is wrong/unknown?
│
├── Objectives
│     └── What will I DO?
│
├── Questions
│     └── What do I want to KNOW?
│
├── Hypotheses
│     └── What do I PREDICT?
│
├── Research Approach
│     ├── Quantitative → NUMBERS
│     ├── Qualitative → EXPERIENCES
│     └── Mixed → BOTH
│
├── Sampling
│     └── Who will I study?
│
└── Data Analysis
      ├── Correlation → RELATIONSHIP
      ├── Regression → PREDICTION
      └── Classification → CATEGORY
```
```
SYSTEM ANALYSIS
│
├── Context → INTERACTIONS
├── DFD → DATA FLOW
├── Activity → WORKFLOW
├── Flowchart → ALGORITHM
├── Class → OBJECTS
├── ERD → DATABASE
└── Collaboration → COMMUNICATION
```
30. The 20-second exam cheat sheet

--------------

If you're under exam pressure, remember these:
```
Research problem → What is wrong/unknown?

Objective → What will I do?

Question → What do I want to know?

Hypothesis → What do I predict?

Quantitative → Numbers.

Qualitative → Experiences/meaning.

Mixed → Numbers + experiences.

Sampling → Who do I select?

Correlation → Relationship.

Regression → Prediction.

Classification → Category.

Context diagram → External interactions.

DFD → Data movement.

Activity diagram → Workflow.

Flowchart → Algorithm/logic.

Class diagram → Software objects.

ERD → Database.

Collaboration diagram → Object communication.
```
The most important chain to memorize:
```
Problem → Objective → Question → Hypothesis → Approach → Sampling → Analysis
```
And for systems:

```
Context → Data → Process → Objects → Database → Communication
```

