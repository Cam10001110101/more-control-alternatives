## Introduction

In the rapidly evolving landscape of AI technology, finding the right balance between performance and privacy can be challenging. This guide introduces you to Groq's high-performance inference platform, offering enhanced data privacy compared to closed-source providers and those with varying business models and motivations.

## Who Is This Guide For?

This guide is perfect for:

- **AI Newcomers**: Those taking their first steps beyond ChatGPT into the broader AI ecosystem
- **DeepSeek Users**: Current users of chat.deepseek.com and/or DeepSeek mobile apps
- **Privacy-Conscious Users**: Those interested in DeepSeek models but seeking more control over their data

This guide is not for:
- Employing rogue technology in a business environment or in any unauthorized manner.

## Quick Setup Guide

### Prerequisites

Before getting started, you'll need to:

1. Create a Groq account at [console.groq.com/login](https://console.groq.com/login)
2. Generate an API key at [console.groq.com/keys](https://console.groq.com/keys)

> 🔒 **Security Note**: Treat your API key like a password - keep it secure and never share it publicly.

## Three Ways to Access Groq

### 1. Zero Setup: Web Interface

The fastest way to get started is through Groq's web interface:

1. Visit [chat.groq.com](https://chat.groq.com/)  
2. Select **"Deepseek-R1-Distil-Llama-70b"** from the model dropdown in the top right corner  
![Groq + Brave Integration Banner](./Images/Pasted%20image%2020250128131548.png)  

### 2. Quick Setup: Brave Browser Integration

For a balance of ease and privacy, follow these steps:

1. Generate your Groq API key at [console.groq.com/keys](https://console.groq.com/keys)
2. Install [Brave Browser](https://brave.com/)
3. Access Leo settings:
   
   ![Brave Leo Settings](./Images/Pasted%20image%2020250128133816.png)

4. Configure your model:
   - Click "Add new model"
   - Use these settings:

     ```
     Label: [Your chosen name]
     Model request name: deepseek-r1-distill-llama-70b
     Server Endpoint: https://api.groq.com/openai/v1/chat/completions
     API Key: [Your Groq API key]
     ```
 
   ![Model Configuration](./Images/Pasted%20image%2020250128154807.png)

### 3. Advanced Setup: Open WebUI

For users seeking maximum customization, check out the [Open WebUI project on GitHub](https://github.com/open-webui/open-webui).


---

*Last updated: January 28, 2025*
