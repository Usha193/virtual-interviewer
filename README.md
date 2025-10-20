
#  NLP-Based Virtual Interviewer
![Python](https://img.shields.io/badge/Python-3.8%2B-blue?logo=python)
![NLP](https://img.shields.io/badge/NLP-Semantic%20Similarity%20%7C%20ASAG-orange)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)
![License](https://img.shields.io/badge/License-MIT-lightgrey)

###  Vignan’s Lara Institute of Technology & Science  
**Authors:**  
Usha Sree Palleboyina, Bhagya Sri Panduri, Bhavya Sri Macharla  
**Guide:** Mr. Ch. Yadavendra Kumar, M.Tech  

---

##  Overview
The **NLP-Based Virtual Interviewer** is an intelligent, **voice-interactive interview simulation system** built using **Natural Language Processing (NLP)**.  
It allows users to practice interviews virtually, get automated feedback, and improve their communication and conceptual skills — without needing a human interviewer.

The system:
- Conducts **mock interviews** via voice interaction.
- Converts **speech to text** using an AI speech engine.
- Evaluates answers using **cosine similarity** and **sentence embeddings (CNN-based)**.
- Provides **scores and feedback** instantly.

---

## Motivation
During the pandemic, interviews moved online — but many candidates lacked real practice or timely evaluation.  
This project was designed to:
- Provide a **realistic interview environment** for beginners.  
- Automatically **evaluate descriptive answers** using NLP.  
- Help users **identify knowledge gaps** and improve before real interviews.

---

##  System Architecture
### Core Modules
1. **Speech-to-Text Conversion**
   - Converts interviewee’s spoken answers into text using APIs like IBM Watson or Google Speech API.
2. **Preprocessing**
   - Tokenization  
   - Stop-word removal  
   - Word stemming/lemmatization  
3. **Similarity Evaluation**
   - Calculates **semantic similarity** between user and model answers.  
   - Uses **cosine similarity** and **CNN-based sentence embeddings**.
4. **Scoring**
   - Generates final percentage-based score.  
   - Provides feedback for each question.

---

##  Key Techniques
| Technique | Purpose |
|------------|----------|
| **ASAG (Automated Short Answer Grading)** | Grades descriptive text answers using NLP |
| **Cosine Similarity** | Measures semantic closeness between user and model answers |
| **CNN-based Embeddings** | Improves contextual sentence similarity |
| **Speech Recognition** | Captures and converts spoken responses |

---

## Scoring Logic
| Cosine Similarity | Evaluation | Result |
|--------------------|-------------|---------|
| ≥ 0.5 | High similarity | Correct |
| 0.2–0.49 | Medium similarity | Needs improvement |
| < 0.2 | Low similarity | Incorrect |

Final score = Average of all individual question scores.

---

##  Tech Stack
- **Language:** Python  
- **Libraries:**  
  - `NLTK`, `spaCy` – NLP preprocessing  
  - `scikit-learn` – cosine similarity  
  - `TensorFlow` / `PyTorch` – CNN modeling  
  - `SpeechRecognition`, `pyaudio` – voice input  
- **APIs:** IBM Watson Voice Bot / Google Speech-to-Text  

---

##  Installation & Usage

### Clone the repository
```bash
git clone https://github.com/<your-username>/nlp-virtual-interviewer.git
cd nlp-virtual-interviewer
