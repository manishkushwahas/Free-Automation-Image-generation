# 🤖 Automation Image & Text Generation using n8n

**What is this project?**  
It’s a web automation system that unites **AI-powered text generation** and **AI-based image creation** inside **n8n**, a no-code automation platform.  
This project automatically creates **captions, hashtags, and images** from a single user input — transforming creativity into automation with intelligence and simplicity.

---

## 🎯 Purpose of this Project
**The purpose of this project** is to demonstrate how AI can automate the process of generating both **images and text** in a unified workflow using **n8n**.  
By connecting powerful APIs like **OpenAI**, **Stability AI**, and **Replicate**, this system delivers creative automation with minimal manual effort.

This project serves as a **creative automation assistant** ideal for:
- Social media managers  
- Digital marketers  
- Content creators  
- Businesses automating visual content production  

---

## 🧩 How It Works (Workflow Explanation)

1. **Webhook Node**  
   - Acts as the entry point for user input (keyword or phrase).  
   - Receives data from the HTML dashboard.

2. **AI Text Generation Node**  
   - Uses **OpenAI GPT** or similar models to create a descriptive caption or prompt based on input.

3. **AI Image Generation Node**  
   - Takes the generated text and produces an AI image using **Stability AI** or **Replicate API**.

4. **Hashtag Generator Node**  
   - Automatically extracts or generates hashtags related to the content for better engagement.

5. **Google Sheet / Drive Node**  
   - Stores the generated **image URL**, **caption**, and **hashtags** in Google Sheets or uploads the image to Google Drive.

6. **Response Node**  
   - Sends the final output (text + image + hashtags) back to the dashboard for display and download.

---

## 💻 Dashboard Overview
The **HTML dashboard** serves as the user interface for interacting with the n8n workflow.

- Left panel: Accepts user input (keywords or prompts).  
- Right panel: Displays AI-generated image, message, and hashtags.  
- JavaScript handles data exchange between the dashboard and n8n webhook using `fetch()` API.

---

## 🧠 What I Learned
- Designing **multi-node workflows** in n8n.  
- Integrating **AI APIs** for text and image generation.  
- Building a responsive **HTML5 + Bootstrap** front-end.  
- Managing **API keys**, **webhooks**, and **JSON data**.  
- Automating creative workflows end-to-end.

---

## 🧰 Requirements to Run
1. **n8n** installed locally or on the cloud  
2. **API keys** for OpenAI / Stability AI / Replicate  
3. **HTML dashboard** file (included in the project)  
4. Configured **n8n webhook URL**  
5. (Optional) **Google Sheets / Drive** integration  
6. Basic knowledge of **JavaScript and n8n**

---

### ⚡ Most Interesting Integration
The **Text Generation Node** and **Image Generation Node** are chained together —  
the AI-generated description becomes the **prompt** for image generation, enabling **AI-to-AI communication** within n8n.

```python
# Example pseudo flow
Input("cat in space") 
→ GPT Text Node → "A cute astronaut cat floating in space" 
→ Image Node → AI-generated image output
