---
title: "AI/ML/GenAI on AWS"
date: 2025-07-09
weight: 1
chapter: false
pre: " <b> 4.1. </b> "
---

{{% notice warning %}}
⚠️ **Note:** The information below is for reference purposes only. Please **do not copy it verbatim** into your report, including this warning.
{{% /notice %}}

# Summary Report: "AI/ML/GenAI on AWS Workshop"

### Event Information

**Event Name:** AI/ML/GenAI on AWS Workshop  
**Date:** Saturday, November 15, 2025  
**Time:** 8:30 AM – 12:00 PM  
**Location:** AWS Vietnam Office  
**Duration:** 3.5 hours

---

### Workshop Overview

This hands-on workshop provided a comprehensive introduction to AWS's artificial intelligence and machine learning services, with a special focus on Generative AI using Amazon Bedrock. The session combined theory with practical demonstrations, helping participants understand how to build AI-powered applications on AWS.

---

### Key Topics Covered

#### 1. AWS AI Services

The workshop introduced six core AWS AI services that solve common business problems:

**Amazon Rekognition** – Computer Vision
- Analyze images and videos automatically
- Detect faces and compare them
- Identify objects, scenes, and activities
- Filter inappropriate content

**Amazon Polly** – Text-to-Speech
- Convert written text into natural speech
- Choose from various voices and languages
- Create voice-enabled applications

**Amazon Transcribe** – Speech-to-Text
- Convert audio to text automatically
- Works in real-time or batch mode
- Supports multiple languages

**Amazon Comprehend** – Natural Language Processing
- Analyze text to understand sentiment
- Extract key information (names, places, dates)
- Detect the language used

**Amazon Translate** – Language Translation
- Translate text between languages using AI
- Handle real-time or large batches
- Use custom vocabulary for specific industries

**Amazon Lex** – Conversational AI
- Build chatbots for customer service
- Create voice assistants
- Connect with other AWS services easily

#### 2. Generative AI with Amazon Bedrock

**What is Amazon Bedrock?**
Amazon Bedrock is AWS's platform for building applications with foundation models (large AI models) without managing infrastructure.

**Foundation Models Comparison**

| Model | Strengths | Best For |
|-------|-----------|----------|
| **Claude** | Strong reasoning, safety | Complex tasks, content creation |
| **Llama** | Open-source, customizable | Custom solutions, cost-sensitive |
| **Titan** | AWS-native, reliable | General AWS integration |

**Prompt Engineering Basics**

Learning how to write effective prompts to get better AI responses:

- **Clear instructions**: Be specific about what you want
- **Chain-of-Thought**: Ask the AI to explain its reasoning step-by-step
- **Few-shot learning**: Give examples of the output you want

Example:
```
Bad prompt: "Write about cats"
Good prompt: "Write a 200-word article about cat behavior for pet owners, focusing on why cats knock things over"
```

**Retrieval-Augmented Generation (RAG)**

RAG helps AI models use your own data to generate more accurate answers:

1. Store your documents in a knowledge base
2. When a user asks a question, find relevant documents
3. Send both the question and documents to the AI
4. Get an accurate, context-aware answer

**Bedrock Agents**

Create AI agents that can:
- Break down complex tasks into steps
- Use tools and APIs to accomplish tasks
- Make decisions based on information

**Guardrails**

Protect your AI applications with:
- Content filtering (block harmful content)
- Topic restrictions (stay on approved topics)
- Sensitive information masking (hide personal data)

#### 3. Live Demo

The highlight was building a **Generative AI chatbot** using Amazon Bedrock:

- Connected to a foundation model (Claude)
- Added a knowledge base with company documents
- Implemented guardrails for safety
- Tested real conversations

---

### What I Learned

#### Understanding AWS AI Services

Before the workshop, I wasn't sure which AWS service to use for different AI tasks. Now I know:
- Use **Rekognition** for analyzing images/videos
- Use **Polly** to add voice to applications
- Use **Comprehend** to understand customer feedback
- Use **Bedrock** for custom AI applications

#### Practical Prompt Engineering

Learning prompt engineering was eye-opening. Small changes in how you ask questions can dramatically improve AI responses. The Chain-of-Thought technique is particularly useful for complex problems.

#### RAG Architecture Benefits

Understanding RAG showed me how to make AI applications that:
- Use company-specific information
- Stay up-to-date without retraining
- Give more accurate and relevant answers

#### Building Safe AI Applications

The guardrails session taught me the importance of:
- Preventing harmful content generation
- Protecting user privacy
- Keeping AI responses on-topic

---

### Skills Gained

After this workshop, I can now:

✅ Choose the right AWS AI service for different use cases  
✅ Compare foundation models and select appropriate ones  
✅ Write effective prompts for better AI responses  
✅ Understand RAG architecture and when to use it  
✅ Build a basic Generative AI chatbot with Bedrock  
✅ Implement safety measures using Guardrails  

---

### How I'll Apply This

#### Short-term Applications
- Experiment with different foundation models on Bedrock
- Practice prompt engineering techniques
- Build a simple chatbot prototype for testing

#### Long-term Goals
- Propose an AI-powered feature for our current project
- Implement RAG for a knowledge base search system
- Integrate AWS AI services into existing applications

---

### Event Experience

The workshop was well-organized and beginner-friendly. The speakers explained complex concepts clearly and the hands-on demo made everything practical. Having 3.5 hours was perfect—enough time to cover important topics without feeling rushed.

The AWS Vietnam office provided a great learning environment with good facilities and networking opportunities with other participants interested in AI/ML.

#### What I Liked
- Hands-on approach with live demos
- Clear comparison of different AI services
- Practical examples from real projects
- Access to workshop materials for future reference

#### Event Photos
*Add your event photos here*

---

### Resources Provided

- AWS AI Services documentation links
- Bedrock getting started guide
- Prompt engineering cheat sheet
- RAG implementation examples
- Sample code from the chatbot demo

---

### Conclusion

This workshop gave me a solid foundation in AWS AI/ML services and Generative AI. The combination of service overview, prompt engineering, RAG architecture, and hands-on demos provided both breadth and depth of knowledge.

I'm excited to explore these tools further and find ways to integrate AI capabilities into my projects. The workshop demonstrated that building AI applications on AWS is more accessible than I thought.

---

*For more information about AWS AI services, visit: [AWS AI Services](https://aws.amazon.com/ai/)*
