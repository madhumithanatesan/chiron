CHIRON — A Safe & Ethical Conversational Agent for Mental Health Support

Chiron AI is a Dialogflow CX based conversational system designed to provide empathetic, safe, and ethically grounded support for mental health conversations.  
Built using Playbooks, Vertex AI, and Google Cloud Speech, the agent delivers human like, responsible, and context aware interactions without hallucinations.

Overview

Unlike conventional LLM chatbots, Chiron AI is built around trust, safety, and factual grounding.  
The agent is designed to:

Offer empathetic guidance and emotional support.  
Stay grounded in verified mental health documentation and support resources .
Maintain ethical standards (no medical advice, crisis redirection, privacy-safe). 
Integrate speech recognition for a natural, voice-based conversation.
Use Vertex AI for controlled generative responses with safety filters. 

Features

All LLM outputs are grounded in curated knowledge sources and verified documentation.  
Sensitive or crisis-related topics automatically redirect to trusted helplines.
Real-time speech recognition using Google Cloud Speech-to-Text. 
Optional voice output via Text-to-Speech for accessibility.  
Uses sentiment analysis and contextual grounding to adjust tone and support level.  
Each conversation path is modular, reusable, and designed with Dialogflow CX Playbooks.  
Reduces hallucination risk through controlled prompt structures and parameterized contexts.  
No personal data storage.  
Conforms to ethical AI and mental health communication standards.  

System Architecture

User (Voice/Text)
↓
Speech-to-Text (Dialogflow Audio Input)
↓
Dialogflow CX Agent
 Playbooks (Welcome, Mood Assessment, Crisis, Supportive, Self-Help, Group Suggestion, Out-of-Scope, Closure)
 Tools (Empathetic Response Generator, Sentiment Analyzer, Hallucination Guard, Conversation Memory Manager)
 Random Therapy Event Generator (inline simulation)
↓
Text-to-Speech Output → User

Integrated Tools
Empathetic Response Generator - Generates warm, context-aware replies using LLMs.
Sentiment or Emotion Analyzer - Detects user mood and emotional intensity.
Hallucination Guard - Validates LLM output for factuality, ethics, and safety.
Conversation Memory Manager - Tracks prior interactions to prevent repeated prompts.

Playbook Summary
Welcome & Disclaimer - Greets user, shows disclaimer, starts conversation.
Mood Assessment - Detects emotional tone and routes flow.
Crisis Support - Handles suicidal or distress signals safely.
Supportive Conversation - Offers empathetic, reflective dialogue.
Self-Help & Education - Shares wellness tips and random therapy events.
Support Group Suggestion - Lists simulated group or therapy sessions.
Out-of-Scope - Politely declines unsafe or medical requests.
Closure - Ends with reassurance and optional upcoming event.

Speech Integration
1. Enable in Dialogflow CX (Manage → Integrations → Web Demo → Enable Audio Input & Output)
   - Input: AUDIO_ENCODING_LINEAR_16, 16kHz
   - Output: OUTPUT_AUDIO_ENCODING_MP3
   - Voice: en-US-Wavenet-E (calm tone)
2. Add microphone handling with Web Speech API or browser recorder.
3. Use outputAudioConfig in detectIntent API for spoken responses.

Example Interaction
User: "I've been feeling anxious and can't sleep."
Bot: I’m really sorry you’re feeling this way. It sounds like you’ve been feeling anxious and it’s affecting your sleep that can be really tough. You’re not alone in this.
Would you like me to share a few simple grounding or relaxation techniques that might help right now?
If your anxiety is making things too hard or you feel overwhelmed, I can also connect you to free mental health resources.
 
Deployment Steps
1. Deploy tools as Cloud Run or Cloud Function endpoints.
2. Paste endpoint URLs in Dialogflow CX under Tools → OpenAPI Schema → Servers → Base URL.
3. Enable Service Account Auth for secure communication.
4. Integrate front-end (web demo or API).
5. Test text and voice interactions thoroughly.

Future Enhancements
- Add multilingual empathy models.
- Connect real wellness-event APIs.
- Integrate with wearables for mood tracking.
- Deploy as a Progressive Web App (PWA).

Author
Sumanth Sudha, Sana Ambreen, Priyadarshini Balasubramanian, Madhumitha Natesan, Mohammad Mahmud
