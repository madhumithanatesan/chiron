
CHIRON - A Safe & Ethical Conversational Agent for Mental Health Support

Team - AI Enthusiasts
Members: Sumanth Sudha, Sana Ambreen, Priyadarshini Balasubramanian, Madhumitha Natesan, Mohammad Mahmud

Problem Statement

Create a mental health support chatbot using an open-source or hosted LLM that provides empathetic, ethically safe responses.

Chiron AI is a Dialogflow CX based conversational system designed to provide empathetic, safe, and ethically grounded support for mental health conversations.  Built using Playbooks, Vertex AI, and Google Cloud Speech, the agent delivers human like, responsible, and context aware interactions without hallucinations.

Overview

Unlike conventional LLM chatbots, Chiron AI is built around trust, safety, and factual grounding.  The agent is designed to:
Offer empathetic guidance and emotional support.  Stay grounded in verified mental health documentation and support resources . Maintain ethical standards (no medical advice, crisis redirection, privacy-safe). Integrate speech recognition for a natural, voice-based conversation. Use Vertex AI for controlled generative responses with safety filters.

Features

All LLM outputs are grounded in curated knowledge sources and verified documentation.  Sensitive or crisis-related topics automatically redirect to trusted helplines. Real-time speech recognition using Google Cloud Speech-to-Text. Optional voice output via Text-to-Speech for accessibility.  Uses sentiment analysis and contextual grounding to adjust tone and support level.  Each conversation path is modular, reusable, and designed with Dialogflow CX Playbooks.  Reduces hallucination risk through controlled prompt structures and parameterized contexts.  No personal data storage.  Conforms to ethical AI and mental health communication standards. 

System Architecture

User (Voice/Text) ↓ Speech-to-Text (Dialogflow Audio Input) ↓ Dialogflow CX Agent Playbooks (Welcome, Mood Assessment, Crisis, Supportive, Self-Help, Group Suggestion, Out-of-Scope, Closure) Tools (Empathetic Response Generator, Sentiment Analyzer, Hallucination Guard, Conversation Memory Manager) Random Therapy Event Generator (inline simulation) ↓ Text-to-Speech Output → User
Integrated Tools Empathetic Response Generator - Generates warm, context-aware replies using LLMs. Sentiment or Emotion Analyzer - Detects user mood and emotional intensity. Hallucination Guard - Validates LLM output for factuality, ethics, and safety. Conversation Memory Manager - Tracks prior interactions to prevent repeated prompts.

Playbook Summary Welcome & Disclaimer - Greets user, shows disclaimer, starts conversation. Mood Assessment - Detects emotional tone and routes flow. Crisis Support - Handles suicidal or distress signals safely. Supportive Conversation - Offers empathetic, reflective dialogue. Self-Help & Education - Shares wellness tips and random therapy events. Support Group Suggestion - Lists simulated group or therapy sessions. Out-of-Scope - Politely declines unsafe or medical requests. Closure - Ends with reassurance and optional upcoming event.

Speech Integration

Enable in Dialogflow CX (Manage → Integrations → Web Demo → Enable Audio Input & Output)
Input: AUDIO_ENCODING_LINEAR_16, 16kHz
Output: OUTPUT_AUDIO_ENCODING_MP3
Voice: en-US-Wavenet-E (calm tone)
Add microphone handling with Web Speech API or browser recorder.
Use outputAudioConfig in detectIntent API for spoken responses.

Example Interaction User: "I've been feeling anxious and can't sleep." Bot: I’m really sorry you’re feeling this way. It sounds like you’ve been feeling anxious and it’s affecting your sleep that can be really tough. You’re not alone in this. Would you like me to share a few simple grounding or relaxation techniques that might help right now? If your anxiety is making things too hard or you feel overwhelmed, I can also connect you to free mental health resources.

Deployment Steps

- Deploy tools as Cloud Run or Cloud Function endpoints.
- Paste endpoint URLs in Dialogflow CX under Tools → OpenAPI Schema → Servers → Base URL.
- Enable Service Account Auth for secure communication.
- Integrate front-end (web demo or API).
- Test text and voice interactions thoroughly.

Results
- Chiron's mythology inspired the healing concept into an AI empathy framework, a unique symbolic foundation that merges mythic archetypes with modern AI ethics.
- Designed multiple custom tools, Empathetic Response Generator, Hallucination Guard, Conversation Memory Manager  all extending Dialogflow CX beyond standard use.
- Combined emotional intelligence, ethical AI design, and speech-based human interaction into one unified flow.
- Demonstrates creative fusion of LLM empathy modeling + therapeutic UX principles, rarely explored together.
- Addresses a critical real-world challenge — providing scalable, safe mental-health support.
- Aligns with WHO and APA recommendations on AI-assisted emotional wellbeing (non-diagnostic support, crisis routing, accessibility).
- Speech integration increases inclusivity for users who prefer talking over typing, expanding accessibility.
- Ethical safeguards (Hallucination Guard + disclaimers) make it a viable community-support companion rather than a risky chatbot.
- Built with Dialogflow CX playbooks, LLM OpenAPI tools, and speech input/output pipeline — a sophisticated, multi-layer architecture.
- Modular tool system: each custom API (Empathetic Generator, Sentiment Analyzer, Hallucination Guard, Memory Manager) enhances logic, validation, and context flow.
- Designed for real-time, ethical content filtering — aligning LLM output with safety constraints dynamically.
- Demonstrated technical maturity: cloud-deployable APIs, consistent schema, speech integration, and responsive design alignment with therapeutic color theory.

Future Enhancement
- Add multilingual empathy models.
- Connect real wellness-event APIs.
- Integrate with wearables for mood tracking.
- Deploy as a Progressive Web App (PWA).
