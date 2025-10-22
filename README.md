Empathetic Mental Health Support Chatbot (Dialogflow CX + LLM + Speech Integration)
 
Overview
--------
This project implements a mental-health support chatbot that offers empathetic, ethically safe, and context-aware conversations using Dialogflow CX integrated with Large Language Models (LLMs). The chatbot helps users express emotions safely, offers supportive guidance, and provides verified self-help or therapy resources while respecting privacy, accuracy, and mental-health ethics.
 
It uses Dialogflow CX Playbooks, LLM tools, memory managers, hallucination guards, and speech integration for accessibility.
 
Project Goals
-------------
- Provide a safe digital space for users to share emotions.
- Deliver empathetic responses grounded in psychological best practices.
- Prevent unsafe, speculative, or repeated interactions.
- Maintain factual accuracy and data privacy.
- Support voice input and output for accessibility.
 
System Architecture
-------------------
User (Voice/Text)
↓
Speech-to-Text (Dialogflow Audio Input)
↓
Dialogflow CX Agent
├── Playbooks (Welcome, Mood Assessment, Crisis, Supportive, Self-Help, Group Suggestion, Out-of-Scope, Closure)
├── Tools (Empathetic Response Generator, Sentiment Analyzer, Hallucination Guard, Conversation Memory Manager)
└── Random Therapy Event Generator (inline simulation)
↓
Text-to-Speech Output → User
 
Integrated Tools
----------------
Empathetic Response Generator - Generates warm, context-aware replies using LLMs.
Sentiment or Emotion Analyzer - Detects user mood and emotional intensity.
Hallucination Guard - Validates LLM output for factuality, ethics, and safety.
Conversation Memory Manager - Tracks prior interactions to prevent repeated prompts.
 
Playbook Summary
----------------
Welcome & Disclaimer - Greets user, shows disclaimer, starts conversation.
Mood Assessment - Detects emotional tone and routes flow.
Crisis Support - Handles suicidal or distress signals safely.
Supportive Conversation - Offers empathetic, reflective dialogue.
Self-Help & Education - Shares wellness tips and random therapy events.
Support Group Suggestion - Lists simulated group or therapy sessions.
Out-of-Scope - Politely declines unsafe or medical requests.
Closure - Ends with reassurance and optional upcoming event.
 
Speech Integration
------------------
1. Enable in Dialogflow CX (Manage → Integrations → Web Demo → Enable Audio Input & Output)
   - Input: AUDIO_ENCODING_LINEAR_16, 16kHz
   - Output: OUTPUT_AUDIO_ENCODING_MP3
   - Voice: en-US-Wavenet-E (calm tone)
2. Add microphone handling with Web Speech API or browser recorder.
3. Use outputAudioConfig in detectIntent API for spoken responses.
 
Example Interaction
-------------------
User: "I've been feeling anxious and can't sleep."
Bot: "That sounds really exhausting. It’s okay to feel that way—you’re not alone. There’s a free Evening Mindfulness Circle tomorrow at 7 PM CST if you’d like to try guided relaxation."
 
Ethical & Safety Design
-----------------------
- No medical diagnosis or prescriptions.
- Crisis detection triggers emergency helpline responses.
- Hallucination Guard ensures factual, non-speculative content.
- Memory Manager avoids repetitive questioning.
- Data privacy: anonymized logs, no personal identifiers stored.
 
Deployment Steps
----------------
1. Deploy tools as Cloud Run or Cloud Function endpoints.
2. Paste endpoint URLs in Dialogflow CX under Tools → OpenAPI Schema → Servers → Base URL.
3. Enable Service Account Auth for secure communication.
4. Integrate front-end (web demo or API).
5. Test text and voice interactions thoroughly.
 
Future Enhancements
-------------------
- Add multilingual empathy models.
- Connect real wellness-event APIs.
- Integrate with wearables for mood tracking.
- Deploy as a Progressive Web App (PWA).
