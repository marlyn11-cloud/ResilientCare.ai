<h1 align="center">ResilientCare.ai: Privacy-First Mental Wellness Companion</h1>

<p align="center">
  <strong>An AI-driven coach for academic stress and daily friction.</strong>
</p>

---

## Project Overview

**ResilientCare.ai** is an intelligent, browser-based wellness companion designed specifically to help students process academic stress, burnout, and daily friction. 

* **The User Problem:** Students frequently face "Daily Friction"—conflicts that aren't classified as mental crises but still require emotional regulation and processing. Many avoid digital wellness tools due to valid privacy concerns about sensitive emotional data being sent to cloud APIs.
* **The Solution:** ResilientCare provides immediate, empathetic support directly in the browser. By leveraging Client-Side Machine Learning (WebAssembly), it guarantees 100% user privacy, zero network latency, and a safe space to handle micro-conflicts without data exfiltration.

---

## Design Philosophy & UX Principles

* **Privacy as a UX :** In mental health applications, trust is the product. Operating completely offline ensures the user feels safe sharing vulnerable thoughts.
* **Designing for High Cognitive Load:** Users interacting with the app are likely in a state of stress or overwhelm. The interface uses strategic color theory, simplified navigation, and tactile interactions to reduce cognitive strain.
* **Clinical Safety over Generative Freedom:** Raw Large Language Models (LLMs) can hallucinate or offer dangerous advice. ResilientCare prioritizes deterministic safety, relying on a strict state-machine to guide users through clinically safe conversational pathways.

---

## Key Features & User Experience

* **"Hold to Vent" Interface:** A core UI component featuring a dynamic, CSS-animated orb. The tactile nature of "holding" to interact serves as a grounding technique during high-stress moments.
* **Psychological Theme Engine:** The UI adapts to the user's sensory needs, offering multiple psychological color profiles (Dark Mode, Cocoa Cupcake Pink, Calming Blue) to create a personalized, soothing environment.
* **Empathetic Routing & Resistance Detection:** The AI monitors for cognitive resistance (e.g., short replies like "idk" or "nothing"). Instead of forcing task productivity, the system dynamically shifts into "Empathetic Mode" to validate and ground the user.
* **Crisis Pattern Safety Net:** The app automatically detects severe emotional distress and immediately pauses the standard workflow to provide critical, real-world crisis resources (e.g., 988 Lifeline), ensuring user safety.
* **Interactive Insights Dashboard:** Using D3.js, the app visualizes local session data into interactive network graphs, clustering related emotional nodes (e.g., "Overwhelm" to "Deadline") to help users identify their triggers over time.

---

## Prototyping & Technology Stack

The architecture was specifically chosen to balance an intelligent conversational UI with absolute data privacy.

### Frontend & Visualizations
* **HTML, CSS, JavaScript**
* **D3.js:** Interactive emotional theme tracking and pattern recognition.
* **Web Storage API:** Local caching and session history.

### Local AI & Conversational Architecture
* **Transformers.js & WebAssembly (WASM):** In-browser inference engine running Hugging Face models (MobileBERT, DistilBERT).
* **Zero-Shot Classification & Sentiment Analysis:** Real-time evaluation of distress levels and intent categorization.
* **Context Routing & State Machine:** Deterministic conversational scripting paired with an EmotionLayer to match the user's distress tone.
* **RAG Pipeline:** Contextual integration to ensure conversational fluidity and prevent repetitive responses.

---

## UX Learnings & Takeaways

1. **Designing for HCI in Mental Health:** I learned that UI *is* UX in wellness apps. Building the "Hold to Vent" orb and dynamic psychological themes taught me how color theory and CSS animations directly mitigate user cognitive load.
2. **Deterministic AI Safety:** I realized that pure LLM text generation isn't always the right tool for vulnerable users. Engineering the resistance protocol taught me how to blend AI sentiment analysis with strict deterministic logic to build a safer, more reliable experience.
3. **Edge AI Constraints & Performance:** Moving ML inference to the browser required careful management of model quantization and memory. Delivering sub-30MB payloads for instant local caching taught me how to balance complex AI features with frontend performance.

---

## Designed and engineered by Marlyn Grullon
