# Smart Fitness Recommender System 🧠💪  
*A Personalized Workout Recommendation Model Using Machine Learning*

This project develops a **Smart Fitness Recommendation Engine** that suggests **personalized workout routines** based on the user’s physical profile and fitness goals.  
The goal is to help individuals **train smarter, not harder**, by aligning workouts with their body needs.

---

## 🎯 Key Idea

Instead of assigning generic workout plans, this system learns from real fitness behavior patterns and suggests **exercise schedules optimized for:**

| Input Variable | Description |
|---|---|
| **Gender** | Biological sex category |
| **Fitness Goal** | Muscle Gain / Fat Burn |
| **BMI Category** | Underweight / Normal / Overweight |

The output is an **exercise schedule** such as:
- Strength Training + Cardio Mix  
- HIIT Sessions  
- Light Resistance + Yoga  
- etc.

---

## 🧠 Model Architecture

- **Algorithm:** Random Forest Classifier  
- **Dataset Size:** ~65,000 records  
- **Task:** Multi-class classification  
- **Purpose:** Predict the most suitable *Exercise Schedule*  
- **Integration Target:** On-device inference in Flutter (TFLite compatible)

---

## 📊 Dataset Insights & Exploratory Analysis

### Distribution of Fitness Goals
<img width="570" height="432" alt="1" src="https://github.com/user-attachments/assets/b3caca77-a28a-4bf4-9944-54144f428b49" />

### BMI vs Goal Relationship
<img width="611" height="472" alt="2" src="https://github.com/user-attachments/assets/7ad359af-62f9-48b3-83e4-0066b40c1e0b" />

### Confusion Matrix (Model Evaluation)
<img width="444" height="378" alt="4" src="https://github.com/user-attachments/assets/b8a37cc8-988e-4618-88c1-0a75307bcafd" />

### Feature Importance
<img width="736" height="402" alt="3" src="https://github.com/user-attachments/assets/addda088-d02f-43b4-b7ba-2d16370b90ca" />

---

## 🚀 Model Performance

| Metric | Score |
|---|---|
| **Accuracy** | **100%** ✅ |
| Precision | 1.00 |
| Recall | 1.00 |
| F1-Score | 1.00 |

> The dataset is highly structured and the relationship between BMI + Goal and Exercise Schedule is strong, producing a near-perfect model.

---

## 📦 Exported Files (for Flutter App AI Integration)

| File | Purpose |
|---|---|
| `fitness_recommender.pkl` | Trained ML model |
| `scaler.pkl` | Normalization scaler |
| `label_encoders.pkl` | Encoding mappings |

Next Step:  
Convert `.pkl` → `.onnx` → `.tflite` for **on-device AI** with TensorFlow Lite.

---

## 🔧 Project Roadmap

- [x] Data Cleaning & Preprocessing  
- [x] Model Training & Evaluation  
- [x] Feature Importance & Interpretation  
- [ ] Export Model to TFLite  
- [ ] Integrate with Flutter App UI  
- [ ] On-device inference optimization  
- [ ] Adaptive workout progress learning (v2)

---

## 🧩 Example Flutter Integration Idea
The model will be used to generate **dynamic workout recommendations** inside the app:

```dart
final recommendation = aiModel.predict({
  "gender": "male",
  "goal": "muscle_gain",
  "bmi_category": "normal_weight"
});
