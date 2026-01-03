# 🎶 Genre Classification and Chord Generation from Lyrics using LLMs

> ⚠️ **Notebook Rendering Notice**
>
> This Jupyter Notebook contains audio generation and interactive outputs (such as music playback). Due to GitHub’s rendering limitations, the notebook may appear as **“Invalid Notebook”** in the preview.
>
> 👉 **Recommended:** Please download the notebook and run it locally, or view the pre-rendered HTML version for the best experience.

---

## Description
This project explores the use of **Large Language Models (LLMs)** to analyze song lyrics for **genre classification**, **emotion detection**, and **chord progression generation**, effectively connecting **Natural Language Processing (NLP)** with music composition.

By extracting semantic and emotional context from lyrics, the system generates musically coherent chord progressions and renders them as playable audio, demonstrating how language understanding can guide creative music generation.

---

## Datasets
The project uses the following datasets for training, validation, and evaluation:

- Genius Lyrics Dataset  
  https://www.cs.cornell.edu/~arb/data/genius-expertise/

- Million Song Dataset  
  http://millionsongdataset.com/index.html

- Musixmatch Lyrics Dataset  
  http://millionsongdataset.com/musixmatch/

- Chordonomicon Dataset  
  https://huggingface.co/datasets/ailsntua/Chordonomicon

---

## 🧠 Project Overview
Using a combination of pre-trained and fine-tuned models, the project performs:

- 🎼 **Genre Classification** using BERT  
- 🎭 **Emotion Detection** using VADER sentiment analysis  
- 🎹 **Chord Generation** using a fine-tuned GPT-2 model  
- 📈 **Evaluation** using Falcon-7B (LLM-based) and human feedback  
- 🔉 **Audio Synthesis** from generated chord progressions  

---

## 📁 Dataset Summary

| Dataset | Description |
|-------|-------------|
| Lyrics Dataset | 273 cleaned song lyrics used for genre and emotion prediction |
| Musixmatch | Lyrics with emotional tags and metadata for validation |
| Million Song Dataset | Song metadata such as title, tempo, and release year |
| Chordonomicon | Real-world chord progressions used to fine-tune GPT-2 |

---

## 🔧 Tools & Libraries
- **Transformers (Hugging Face):** BERT, GPT-2  
- **VADER:** Sentiment analysis  
- **pretty_midi:** MIDI-to-WAV audio rendering  
- **Seaborn, Matplotlib:** Data visualization  
- **Falcon-7B:** LLM-based qualitative evaluation  
- **Scikit-learn:** Model utilities  

---

## ⚙️ Methodology

### Genre Classification
Lyrics are preprocessed and tokenized before being passed into a fine-tuned BERT model to classify songs into genres such as Pop, Rock, and Hip-hop. The predicted genre provides stylistic guidance for chord generation.

### Emotion Detection
VADER is used to assign sentiment polarity (Positive, Neutral, or Negative) to each lyric. The detected emotion influences harmonic choices, such as using minor chords for sad or negative lyrics.

### Chord Generation
GPT-2 is fine-tuned on chord sequences from the Chordonomicon dataset. The model is prompted with the lyrics, predicted genre, and detected emotion to generate chord progressions, which are post-processed to ensure valid formatting.

---

## 📊 Evaluation

### LLM-Based Evaluation
Falcon-7B evaluates the alignment between lyrics and generated chord progressions on a scale of 1–10. The model achieved an average score of **8/10**, highlighting strong emotional consistency and musical flow.

### Human Evaluation
Five human evaluators rated the generated audio on a scale of 1–5. The average score of **4.4/5** confirmed positive reception and alignment with the lyrical theme.

---

## 🔉 Output Example
- **Lyric Input:** “When the night falls and the stars light the sky.”
- **Generated Chords:**  
Bb F C Bb F C Bb F C Bb F C B

- **Audio Output:** Saved as `output_music.wav` and included in this repository.

---

## Results Summary

| Component | Model Used | Outcome |
|---------|------------|--------|
| Genre Classification | BERT | Accurate genre prediction |
| Emotion Detection | VADER | Clear sentiment labeling |
| Chord Generation | GPT-2 (fine-tuned) | Realistic, mood-aligned progressions |
| Evaluation | Falcon-7B + Human | Avg. 8/10 (LLM), 4.4/5 (Human) |

---

## Conclusion
This project demonstrates the potential of **LLMs in creative AI applications**, showing how lyrical meaning and emotion can be transformed into musically coherent chord progressions. By combining NLP, deep learning, and audio synthesis, the system highlights new possibilities for AI-assisted music composition.
