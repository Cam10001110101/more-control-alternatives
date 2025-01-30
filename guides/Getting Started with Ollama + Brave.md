# Getting Started with Ollama + Brave

This is a quick-start guide for leveraging Ollama's local AI capabilities with Brave browser while maintaining control over your data and privacy.

## Target Audience 

- **AI Newcomers**: Those taking their first steps beyond ChatGPT into the broader AI ecosystem
- **DeepSeek Users**: Current users of chat.deepseek.com and/or DeepSeek mobile apps
- **Privacy-Conscious Users**: Those interested in DeepSeek models but seeking more control over their data
- **Cost-conscious users going deeper**: Those interested in running AI models locally on their own hardware


## Prerequisites

1. **Install Ollama**
   * Follow our [Ollama Installation Guide](.\ollama-installation.md) for your platform
   * Verify Ollama is running on your system

2. **Install Brave Browser**
   * Download and install from [brave.com](https://brave.com)

## Setting Up Brave with Ollama

1. **Install the DeepSeek Model**
   ```bash
   ollama pull deepseek-r1:14b
   ```

2. **Open Brave Settings**
   * Click the menu icon (☰) in the top-right corner
   * Select "Settings"
   * Click on "Leo"
   ![Brave Leo Settings](System_Files/Image_Imports/Pasted%20image%2020250128133816.png)

3. **Configure Model**
   * Scroll to the bottom and click "Add new model" with the following settings:
     ```
     Label: DeepSeekR1_14b
     Model request name: deepseek-r1:14b
     Server Endpoint: http://localhost:11434/v1/chat/completions
     ```
   * Click "Save"

## Verifying Your Setup

1. **Test the Connection**
   * Click the Leo icon in Brave
   * Select your configured DeepSeek model
   * Try a simple test prompt like "Hello, how are you?"

2. **Troubleshooting**
   * If Leo can't connect, verify Ollama is running:
     ```bash
     ollama list
     ```
   * Check that the model is installed:
     ```bash
     ollama list
     ```
   * Verify the server endpoint is accessible:
     ```bash
     curl http://localhost:11434/v1/chat/completions
     ```

## Privacy Benefits

By running Ollama locally:
- All AI interactions stay on your machine
- No data leaves your control
- Complete privacy for sensitive queries
- No dependency on external services
- Full control over model usage and data

## Next Steps

* Experiment with different models available through Ollama
* Explore Leo's features in Brave
* Try more complex prompts and use cases
* Consider setting up multiple models for different purposes

## Additional Resources

* [Ollama Model Library](https://ollama.com/library)
* [Brave Leo Documentation](https://brave.com/leo/)


---

*Last updated: January 30, 2025*