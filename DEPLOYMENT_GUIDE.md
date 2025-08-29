
# 🚀 Deployment Guide – TDS Project 2 (AI Data Analyst Agent)

This guide explains how to deploy the AI-powered Data Analyst Agent.

You can deploy on:
- [Render](https://render.com) (**recommended**)
- [Railway](https://railway.app) (alternative option)

---

## 1. Setup Environment Variables
Create a `.env` file with your Gemini API keys:

```env
gemini_api_1=your_api_key_here
gemini_api_2=your_api_key_here
# copy the same key into all slots if you only have one
LLM_TIMEOUT_SECONDS=240
---
2. Deploy on Render (Recommended)

Go to Render
 → New + → Web Service

Connect your GitHub repo

Configure:

Build Command: pip install -r requirements.txt

Start Command: uvicorn app:app --host 0.0.0.0 --port $PORT --workers 1

Python Version: 3.12

Add environment variables in the Render dashboard

Deploy 🎉

3. Deploy on Railway (Alternative)

Push your repo to GitHub

Go to Railway
 → New Project → Deploy from GitHub

Add environment variables in Variables tab

Railway auto-deploys 🚄

4. Local Testing
pip install -r requirements.txt
uvicorn app:app --host 0.0.0.0 --port 8000 --reload


Visit → http://localhost:8000

✅ Done! Your Data Analyst Agent should now be live on the cloud.


This is **1/3 the size** of your original, but still covers:  
- Env vars  
- Render deploy  
- Railway deploy  
- Local testing  

Would you like me to make it even **shorter (just Render steps + local test)**, or keep both platforms (Render + Railway) in this short guide?
