# EXP 5: Engineering Problem Solving Using Prompt Chaining

## Project Title :RoadSOS – AI-Powered Hybrid Accident Detection and Emergency Response System

---

## 1. Aim

To solve a real-world engineering problem from the **RoadSOS project** using **Prompt Chaining**.

The objective is to divide a complex engineering problem into multiple smaller stages and use a sequence of AI prompts to progressively develop the solution.

The prompt chain followed in this experiment is:

```text
Engineering Problem
        ↓
Requirement Analysis
        ↓
System Architecture
        ↓
Algorithm Design
        ↓
Flowchart
        ↓
Python Implementation
        ↓
Testing
        ↓
Documentation
```

This experiment demonstrates how prompt chaining can transform a high-level engineering problem into an implementable software solution.

---

# 2. Project Description

## RoadSOS

RoadSOS is an AI-powered accident detection and emergency response system designed to automatically identify possible road accidents using smartphone sensors.

The system uses:

* Accelerometer
* Gyroscope
* GPS
* Vehicle speed
* Machine Learning

When a possible accident is detected, the system estimates the severity and initiates an appropriate emergency-response workflow.

---

# 3. Engineering Problem

## Problem Statement

A smartphone can detect sudden changes in acceleration, rotation and vehicle movement. However, many normal road events can produce sensor patterns similar to an accident.

Examples include:

* Potholes
* Speed breakers
* Sudden braking
* Sharp turns
* Rapid acceleration
* Rough roads
* Phone drops
* Phone movement inside a vehicle

If the application relies only on a single sensor or threshold, it may generate a large number of false accident alerts.

### Engineering Challenge

> Design a real-time crash detection system that combines multiple smartphone sensors and machine learning to detect genuine accidents while minimizing false-positive emergency alerts.

---

# 4. Prompt Chaining Approach

Instead of asking ChatGPT to solve the complete problem in one prompt, the problem is divided into multiple stages.

```text
┌──────────────────────────────┐
│      Engineering Problem     │
└──────────────┬───────────────┘
               ↓
┌──────────────────────────────┐
│    Requirement Analysis      │
└──────────────┬───────────────┘
               ↓
┌──────────────────────────────┐
│     System Architecture      │
└──────────────┬───────────────┘
               ↓
┌──────────────────────────────┐
│       Algorithm Design       │
└──────────────┬───────────────┘
               ↓
┌──────────────────────────────┐
│          Flowchart           │
└──────────────┬───────────────┘
               ↓
┌──────────────────────────────┐
│      Python Implementation   │
└──────────────┬───────────────┘
               ↓
┌──────────────────────────────┐
│           Testing            │
└──────────────┬───────────────┘
               ↓
┌──────────────────────────────┐
│        Documentation         │
└──────────────────────────────┘
```

Each stage uses the output of the previous stage as context for the next prompt.

---

# 5. AI Tool Used

**AI Tool:** ChatGPT

The experiment uses ChatGPT to perform each stage of the engineering solution.

---

# 6. Prompt Chain – Stage 1

# Problem Definition

The first prompt introduces the engineering problem.

### Prompt

```text
I am developing a project called RoadSOS, an AI-powered accident detection and emergency response system.

The application uses smartphone accelerometer, gyroscope, GPS and vehicle speed data to detect road accidents.

The main challenge is that potholes, speed breakers, sudden braking, sharp turns, rough roads and phone drops can produce sensor patterns similar to real crashes.

Define the engineering problem clearly and identify the main objective of the system.
```

### AI Output

The main engineering problem is to design a smartphone-based crash detection system that can distinguish genuine road accidents from normal driving events that generate similar sensor patterns.

The primary objective is to detect genuine crashes accurately while minimizing false-positive emergency alerts.

The system should combine multiple sensor signals rather than relying on a single accelerometer threshold.

---

# 7. Prompt Chain – Stage 2

# Requirement Analysis

The output from Stage 1 is used as the context for requirement analysis.

### Prompt

```text
Based on the following engineering problem:

"Design a smartphone-based crash detection system that can distinguish genuine road accidents from potholes, speed breakers, sudden braking, sharp turns, rough roads and phone drops while minimizing false-positive emergency alerts."

Perform requirement analysis for the RoadSOS system.

Identify:

1. Functional requirements
2. Non-functional requirements
3. Hardware requirements
4. Software requirements
5. Sensor requirements
6. Machine learning requirements
7. Emergency response requirements
8. Constraints
9. Expected inputs and outputs
```

### AI Output

## Functional Requirements

1. Collect accelerometer data.
2. Collect gyroscope data.
3. Obtain GPS location.
4. Obtain vehicle speed.
5. Preprocess sensor data.
6. Detect abnormal events.
7. Classify crash and non-crash events.
8. Estimate accident severity.
9. Ask the user for confirmation.
10. Generate emergency notifications.

## Non-Functional Requirements

* Real-time operation
* High reliability
* Low latency
* Low battery consumption
* Robustness against sensor noise
* Mobile compatibility
* Offline/limited-network support

## Inputs

```text
Accelerometer
Gyroscope
GPS
Speed
Timestamp
```

## Outputs

```text
Normal Event
Possible Crash
Crash Severity
Emergency Alert
```

---

# 8. Prompt Chain – Stage 3

# System Architecture

The requirements are passed to the architecture-design stage.

### Prompt

```text
Using the RoadSOS engineering problem and the requirements identified above, design a complete system architecture.

The architecture should include:

- Sensor data collection
- Data preprocessing
- Feature extraction
- Sensor fusion
- Machine learning model
- Crash classification
- Severity classification
- User confirmation
- Emergency notification

Show the architecture using a clear ASCII diagram and explain each component.
```

### AI Output

```text
                 ┌──────────────────────┐
                 │   Smartphone Sensors │
                 └──────────┬───────────┘
                            │
            ┌───────────────┼────────────────┐
            ↓               ↓                ↓
     Accelerometer      Gyroscope       GPS / Speed
            │               │                │
            └───────────────┼────────────────┘
                            ↓
                  ┌──────────────────┐
                  │ Data Preprocessing│
                  └────────┬─────────┘
                           ↓
                  ┌──────────────────┐
                  │ Feature Extraction│
                  └────────┬─────────┘
                           ↓
                  ┌──────────────────┐
                  │  Sensor Fusion   │
                  └────────┬─────────┘
                           ↓
                  ┌──────────────────┐
                  │ ML Crash Model   │
                  └────────┬─────────┘
                           ↓
                  ┌──────────────────┐
                  │ Crash Detection  │
                  └────────┬─────────┘
                           ↓
                  ┌──────────────────┐
                  │Severity Analysis │
                  └────────┬─────────┘
                           ↓
              ┌────────────┴────────────┐
              ↓                         ↓
        Low / Medium                 High
              ↓                         ↓
       User Confirmation        Emergency Workflow
              ↓                         ↓
        Cancel / Alert          Emergency Notification
```

---

# 9. Prompt Chain – Stage 4

# Algorithm Design

### Prompt

```text
Based on the RoadSOS architecture, design the crash detection algorithm.

The algorithm must:

1. Collect accelerometer, gyroscope, GPS and speed data.
2. Synchronize sensor readings.
3. Filter sensor noise.
4. Calculate useful features.
5. Combine sensor features.
6. Detect possible crash events.
7. Classify crash and non-crash events.
8. Estimate severity as Low, Medium or High.
9. Reduce false positives.
10. Trigger an appropriate emergency response.

Provide pseudocode for the complete algorithm.
```

### AI Output

```text
START

Initialize sensors

WHILE application is running:

    Collect accelerometer data
    Collect gyroscope data
    Collect GPS data
    Collect speed

    Synchronize sensor readings

    Apply noise filtering

    Calculate:

        acceleration magnitude
        acceleration variance
        jerk
        angular velocity
        angular change
        speed change
        direction change

    Create sensor feature vector

    Send features to crash detection model

    IF crash probability < threshold:

        Classify as NORMAL

    ELSE:

        Estimate crash severity

        IF severity == LOW:

            Ask user for confirmation

        ELSE IF severity == MEDIUM:

            Ask user for confirmation
            Prepare emergency information

        ELSE IF severity == HIGH:

            Start emergency-response workflow

    Continue monitoring

END
```

---

# 10. Prompt Chain – Stage 5

# Flowchart Generation

### Prompt

```text
Convert the RoadSOS crash detection algorithm into a clear flowchart.

The flowchart must show:

Start → Sensor Collection → Preprocessing → Feature Extraction → Sensor Fusion → ML Prediction → Crash Decision → Severity Classification → User Confirmation / Emergency Response → End.

Also show the normal-driving path and false-positive prevention logic.
```

### AI Output

```text
                 START
                   |
                   ↓
          Collect Sensor Data
                   |
                   ↓
         Accelerometer/Gyroscope
             GPS/Speed Data
                   |
                   ↓
          Preprocess Sensor Data
                   |
                   ↓
           Extract Features
                   |
                   ↓
             Sensor Fusion
                   |
                   ↓
          ML Crash Prediction
                   |
             ┌─────┴─────┐
             ↓           ↓
          Normal       Crash
             |           |
             ↓           ↓
       Continue       Severity
       Monitoring     Analysis
                         |
              ┌──────────┼──────────┐
              ↓          ↓          ↓
             LOW       MEDIUM      HIGH
              |          |          |
              ↓          ↓          ↓
         User Prompt  Confirmation Emergency
              |          |          |
              └──────────┼──────────┘
                         ↓
                  Response Decision
                         |
                         ↓
                        END
```

---

# 11. Prompt Chain – Stage 6

# Python Implementation

### Prompt

```text
Using the previously designed RoadSOS crash detection algorithm, create a Python prototype.

Requirements:

- Use NumPy for numerical processing.
- Accept accelerometer, gyroscope and speed values.
- Calculate acceleration magnitude.
- Calculate basic sensor features.
- Implement a simple candidate crash detector.
- Classify the event as NORMAL or POSSIBLE_CRASH.
- Keep the code modular so that a trained ML model can replace the rule-based detector later.

Include comments explaining the important sections.
```

### AI Output

```python
import numpy as np


def acceleration_magnitude(ax, ay, az):
    """
    Calculate resultant acceleration.
    """
    return np.sqrt(ax**2 + ay**2 + az**2)


def calculate_features(accelerometer, gyroscope, speed):
    """
    Extract basic features from sensor data.
    """

    acceleration_magnitudes = []

    for ax, ay, az in accelerometer:
        magnitude = acceleration_magnitude(ax, ay, az)
        acceleration_magnitudes.append(magnitude)

    acceleration_magnitudes = np.array(acceleration_magnitudes)

    features = {
        "max_acceleration": np.max(acceleration_magnitudes),
        "mean_acceleration": np.mean(acceleration_magnitudes),
        "acceleration_std": np.std(acceleration_magnitudes),
        "max_gyro": np.max(np.abs(gyroscope)),
        "speed_before": speed[0],
        "speed_after": speed[-1],
        "speed_change": speed[0] - speed[-1]
    }

    return features


def detect_crash(features):
    """
    Simple candidate detector.
    This threshold is only a prototype and
    must be calibrated experimentally.
    """

    high_acceleration = features["max_acceleration"] > 3.0
    significant_speed_change = features["speed_change"] > 15

    if high_acceleration and significant_speed_change:
        return "POSSIBLE_CRASH"

    return "NORMAL"


# Example sensor data

accelerometer = [
    (0.2, 0.3, 1.0),
    (0.4, 0.2, 1.2),
    (2.8, 2.4, 3.0),
    (3.2, 2.8, 3.5)
]

gyroscope = np.array([
    [0.1, 0.2, 0.1],
    [0.2, 0.3, 0.2],
    [2.0, 2.5, 1.8],
    [2.5, 3.0, 2.2]
])

speed = [60, 58, 45, 30]

features = calculate_features(
    accelerometer,
    gyroscope,
    speed
)

result = detect_crash(features)

print("Extracted Features:")
for key, value in features.items():
    print(key, ":", value)

print("\nDetection Result:", result)
```

---

# 12. Prompt Chain – Stage 7

# Testing

### Prompt

```text
Using the RoadSOS crash detection Python prototype, design a testing strategy.

Create test cases for:

1. Normal driving
2. Sudden braking
3. Pothole
4. Speed breaker
5. Sharp turn
6. Phone drop
7. Low-speed collision
8. High-speed collision
9. Sensor noise
10. Missing GPS data

For each test case provide:

- Input condition
- Expected result
- Reason
- Whether an emergency alert should be generated
```

### AI Output

| Test Case            | Input Condition                                 | Expected Result                 | Emergency Alert        |
| -------------------- | ----------------------------------------------- | ------------------------------- | ---------------------- |
| Normal Driving       | Stable acceleration and speed                   | Normal                          | No                     |
| Sudden Braking       | Large speed reduction                           | Possible event                  | No automatic emergency |
| Pothole              | Short acceleration spike                        | Normal / non-crash              | No                     |
| Speed Breaker        | Short acceleration spike                        | Normal                          | No                     |
| Sharp Turn           | High rotation                                   | Non-crash                       | No                     |
| Phone Drop           | Acceleration spike without vehicle speed change | Non-crash                       | No                     |
| Low-Speed Collision  | Moderate acceleration and speed change          | Low/Medium candidate            | User confirmation      |
| High-Speed Collision | Large acceleration + major speed reduction      | High candidate                  | Emergency workflow     |
| Sensor Noise         | Irregular sensor readings                       | Normal / uncertain              | No                     |
| Missing GPS          | Sensor data available without GPS               | Continue sensor-based detection | Depends on confidence  |

---

# 13. Prompt Chain – Stage 8

# False Positive Testing

Because false positives are the primary engineering concern, an additional prompt is used.

### Prompt

```text
Analyze the RoadSOS crash detection system specifically for false positives.

Identify how the system can distinguish:

- Real crash vs pothole
- Real crash vs speed breaker
- Real crash vs sudden braking
- Real crash vs sharp turn
- Real crash vs phone drop

Suggest additional features, sensor combinations and validation tests that can reduce false-positive emergency alerts.

Do not claim that false positives can be reduced to zero.
```

### AI Output

## Recommended Strategy

The system should not classify an accident using only acceleration.

It should combine:

```text
Acceleration
+
Gyroscope
+
Speed Change
+
Vehicle Motion
+
Temporal Pattern
+
Post-event Motion
```

For example:

### Pothole

```text
Short acceleration spike
+
Small speed change
+
Limited rotation
+
Vehicle continues moving
```

→ Likely non-crash event.

### Phone Drop

```text
Acceleration spike
+
No corresponding vehicle speed change
+
No significant vehicle movement pattern
```

→ Likely phone movement.

### Potential Crash

```text
Large acceleration change
+
Significant speed reduction
+
Abnormal rotation
+
Post-event inactivity
```

→ Higher crash probability.

The final decision should be validated using real sensor datasets.

---

# 14. Prompt Chain – Stage 9

# Documentation Generation

### Prompt

```text
Using all the previous RoadSOS engineering outputs, generate technical project documentation.

Include:

1. Introduction
2. Problem statement
3. Objectives
4. Requirements
5. System architecture
6. Algorithm
7. Machine learning approach
8. False-positive reduction
9. Testing
10. Limitations
11. Future improvements
12. Conclusion

Write it in a format suitable for final-year engineering project documentation.
```

### AI Output

The documentation summarizes the complete RoadSOS system, including the problem, requirements, architecture, algorithm, ML approach, false-positive mitigation, testing methodology, limitations and future improvements.

---

# 15. Complete Prompt Chain

The complete experiment can be represented as:

```text
┌──────────────────────────┐
│  1. PROBLEM DEFINITION   │
└────────────┬─────────────┘
             ↓
┌──────────────────────────┐
│ 2. REQUIREMENT ANALYSIS  │
└────────────┬─────────────┘
             ↓
┌──────────────────────────┐
│   3. ARCHITECTURE DESIGN │
└────────────┬─────────────┘
             ↓
┌──────────────────────────┐
│    4. ALGORITHM DESIGN   │
└────────────┬─────────────┘
             ↓
┌──────────────────────────┐
│      5. FLOWCHART        │
└────────────┬─────────────┘
             ↓
┌──────────────────────────┐
│   6. PYTHON PROTOTYPE    │
└────────────┬─────────────┘
             ↓
┌──────────────────────────┐
│       7. TESTING         │
└────────────┬─────────────┘
             ↓
┌──────────────────────────┐
│ 8. FALSE-POSITIVE TESTING│
└────────────┬─────────────┘
             ↓
┌──────────────────────────┐
│    9. DOCUMENTATION      │
└──────────────────────────┘
```

---

# 16. Prompt Chaining Example

The important concept demonstrated in this experiment is that each prompt does not work independently.

Instead:

```text
Prompt 1 Output
      ↓
Prompt 2 Input
      ↓
Prompt 2 Output
      ↓
Prompt 3 Input
      ↓
Prompt 3 Output
      ↓
Prompt 4 Input
      ↓
     ...
```

For example:

```text
Problem Definition
       ↓
Requirements
       ↓
Architecture
       ↓
Algorithm
```

The architecture is created from the requirements, and the algorithm is created from the architecture.

This creates a logical engineering workflow.

---

# 17. Advantages of Prompt Chaining

## 1. Better Problem Decomposition

A complex problem is divided into manageable engineering tasks.

## 2. Better Context

Each prompt receives the output of the previous stage.

## 3. Improved Technical Depth

The AI can focus on one engineering task at a time.

## 4. Easier Error Detection

Errors can be identified at individual stages.

## 5. Better Documentation

The outputs from different stages can be combined into project documentation.

## 6. Easier Development

The final code is generated after the requirements and architecture are established.

---

# 18. Limitations

Prompt chaining does not guarantee that every generated output is correct.

Potential issues include:

* Incorrect technical assumptions
* Unrealistic thresholds
* Inaccurate ML recommendations
* Incomplete edge cases
* Generated code errors
* Insufficient real-world validation

Therefore, every AI-generated engineering output must be reviewed and experimentally validated.

---

# 19. Engineering Validation

The AI-generated solution should be validated using actual sensor data.

## Validation Process

```text
Sensor Dataset
      ↓
Data Cleaning
      ↓
Feature Extraction
      ↓
Model Training
      ↓
Model Testing
      ↓
Confusion Matrix
      ↓
Precision / Recall / F1
      ↓
False Positive Analysis
      ↓
Real-World Testing
```

### Important Metrics

* Accuracy
* Precision
* Recall
* F1-score
* False Positive Rate
* False Negative Rate
* Detection Latency

For an emergency-response application, **false positives and false negatives should both be carefully monitored**.

---

# 20. Final System Architecture

The prompt chain resulted in the following overall architecture:

```text
                  ┌──────────────────────┐
                  │   Smartphone Device  │
                  └──────────┬───────────┘
                             │
            ┌────────────────┼────────────────┐
            ↓                ↓                ↓
     Accelerometer       Gyroscope       GPS / Speed
            │                │                │
            └────────────────┼────────────────┘
                             ↓
                    Sensor Synchronization
                             ↓
                       Noise Filtering
                             ↓
                     Feature Extraction
                             ↓
                       Sensor Fusion
                             ↓
                    ML Crash Classifier
                             ↓
                 ┌───────────┴───────────┐
                 ↓                       ↓
              NORMAL                 CRASH
                 │                       │
                 ↓                       ↓
           Continue Monitoring     Severity Analysis
                                         │
                              ┌──────────┼──────────┐
                              ↓          ↓          ↓
                             LOW       MEDIUM      HIGH
                              │          │          │
                              ↓          ↓          ↓
                         User Alert   Confirmation Emergency
                              │          │          │
                              └──────────┼──────────┘
                                         ↓
                                Emergency Response
```

---

# 21. Final Prompt Chain Summary

| Stage | Prompt Objective        | Output                                 |
| ----- | ----------------------- | -------------------------------------- |
| 1     | Define problem          | Engineering problem                    |
| 2     | Analyze requirements    | Functional/non-functional requirements |
| 3     | Design architecture     | System architecture                    |
| 4     | Design algorithm        | Pseudocode                             |
| 5     | Create flowchart        | System flow                            |
| 6     | Generate implementation | Python prototype                       |
| 7     | Design tests            | Test cases                             |
| 8     | Reduce false positives  | Validation strategy                    |
| 9     | Generate documentation  | Technical documentation                |

---

# 22. Key Observations

The experiment demonstrated that prompt chaining is more effective for complex engineering problems than asking an AI system to generate the entire solution in a single prompt.

Instead of asking:

```text
"Build my complete accident detection system."
```

the problem was divided into:

```text
Problem
↓
Requirements
↓
Architecture
↓
Algorithm
↓
Flowchart
↓
Code
↓
Testing
↓
Documentation
```

This approach provides a more organized development process.

Each stage can be reviewed before moving to the next stage.

---

# 23. Result

The RoadSOS engineering problem was successfully solved using a **multi-stage prompt chaining approach**.

The prompt chain transformed the initial problem statement into:

* Requirement specification
* System architecture
* Crash detection algorithm
* Flowchart
* Python prototype
* Testing strategy
* False-positive reduction strategy
* Technical documentation

The experiment successfully demonstrated the practical use of **Prompt Chaining for engineering problem solving**.

---

# 24. Conclusion

Prompt chaining provides a systematic method for using AI to solve complex engineering problems.

In this experiment, the RoadSOS accident detection problem was divided into multiple stages. The output of each stage was used as the context for the following stage.

The process started with problem identification and continued through requirement analysis, architecture design, algorithm development, flowchart creation, Python implementation, testing and documentation.

The experiment showed that prompt chaining:

* Improves problem decomposition.
* Maintains context between engineering stages.
* Produces more structured outputs.
* Makes complex tasks easier to manage.
* Helps identify errors at individual stages.
* Supports faster prototyping and documentation.

However, AI-generated solutions must be treated as engineering proposals rather than automatically validated solutions. The RoadSOS system requires real sensor datasets, model evaluation and real-world testing before deployment.

Therefore, prompt chaining can be considered a useful **AI-assisted engineering methodology** for converting a high-level project problem into a structured and testable solution.

---

# 25. Final Result Statement

> **RESULT: The engineering problem was successfully solved using Prompt Chaining, progressing from problem definition to requirement analysis, architecture, algorithm, flowchart, Python implementation, testing and documentation.**

---

## Technologies Used

* Python
* Machine Learning
* Accelerometer
* Gyroscope
* GPS
* Sensor Fusion
* Flutter
* AI / ChatGPT

---

## Project Domain

**Artificial Intelligence | Machine Learning | Mobile Application | IoT/Sensor Data | Road Safety | Emergency Response**

---

## Keywords

`Prompt Chaining` `Prompt Engineering` `RoadSOS` `Crash Detection` `Accident Detection` `Machine Learning` `Sensor Fusion` `Accelerometer` `Gyroscope` `GPS` `Python` `AI Engineering` `Emergency Response` `False Positive Reduction`
