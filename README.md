# 🎵 AI Music Generation: LSTM vs Transformer

## 📄 Descrizione del Progetto
Questo repository ospita un confronto sperimentale tra due diverse architetture di Deep Learning applicate alla **generazione musicale algoritmica**:

1.  **LSTM (Long Short-Term Memory)**: Un approccio classico basato su reti ricorrenti.
2.  **Transformer**: Un approccio moderno basato sul meccanismo di attenzione (Categorical).

L'obiettivo è generare brani musicali (con un focus sullo stile Romantico/Classico) partendo da dataset MIDI e confrontare la coerenza e la qualità compositiva dei due modelli.

---

## 📂 Struttura del Repository

Il progetto è diviso in due notebook principali:

### 1. `Copia_di_LSTM_RomaticaV2.ipynb` (Approccio Classico)
* **Architettura:** LSTM (Recurrent Neural Network).
* **Funzionalità:**
    * Preprocessing dei file MIDI usando `music21`.
    * **EDA (Exploratory Data Analysis):** Visualizzazione della distribuzione di note e accordi tramite grafici a barre.
    * Training sequenziale per predire la nota successiva.
* **Librerie chiave:** `music21`, `pandas`, `matplotlib`, `tensorflow/keras`.

### 2. `Trasformer_CategoricoV3.ipynb` (Approccio Moderno)
* **Architettura:** Transformer (Attention-based).
* **Funzionalità:**
    * Tokenizzazione avanzata dei file MIDI usando `miditok` e `symusic`.
    * Modellazione del linguaggio applicata alla musica (Categorical).
    * **Generazione Audio:** Pipeline integrata per sintetizzare l'output direttamente in formato `.wav` usando `fluidsynth`.
* **Librerie chiave:** `miditok`, `symusic`, `torch`, `fluidsynth`.

---

## ⚙️ Installazione e Requisiti

Il codice è ottimizzato per essere eseguito su **Google Colab** (consigliato per l'accesso alla GPU), ma può essere eseguito in locale installando le seguenti dipendenze:

```bash
# Librerie base e Data Science
pip install numpy pandas matplotlib

# Gestione MIDI e Tokenizzazione
pip install music21
pip install miditok symusic

# Framework di Deep Learning (Installa quello necessario al notebook in uso)
pip install torch torchvision torchaudio --index-url [https://download.pytorch.org/whl/cu118](https://download.pytorch.org/whl/cu118)
pip install tensorflow

# Sintesi Audio (Richiesto per il notebook Transformer)
pip install fluidsynth-python
