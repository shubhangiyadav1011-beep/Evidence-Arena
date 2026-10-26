EVIDENCE ARENA 2.0 — GEMMA 4 GEMINI API VERSION

This version uses Google's hosted Gemma 4 models through the Gemini API. You do NOT need Ollama or a local model download.

SETUP (Windows / VS Code)
1. Extract this ZIP. Open the evidence_arena_2_0_mvp folder in VS Code.
2. Open Terminal. If you already have the original .venv folder in the parent project folder, you can keep using it; otherwise create a venv.
3. Install dependencies: python -m pip install -r requirements.txt
4. Create an API key in Google AI Studio: https://aistudio.google.com/
5. In the SAME PowerShell terminal, set the key for this terminal session (replace YOUR_KEY with the actual key; do not include angle brackets):
   $env:GEMINI_API_KEY="YOUR_KEY"
6. Start app: python -m streamlit run app.py
7. In sidebar, check Enable hosted Gemma 4 (Google API), keep model gemma-4-26b-a4b-it, click Test Gemma 4 connection, then Run AI challenge analysis.

If using your existing .venv in the parent folder, run these from the project folder:
   ..\.venv\Scripts\python.exe -m pip install -r requirements.txt
   $env:GEMINI_API_KEY="YOUR_KEY"
   ..\.venv\Scripts\python.exe -m streamlit run app.py

SECURITY: Never commit or share your API key. It is read from the environment, not stored in app.py. If you accidentally expose it, revoke it in AI Studio. API availability, rate limits, and billing depend on your Google account/project.

This remains an MVP: AI output is an interpretation and must be checked against source passages. Numeric verdict logic is separate from Gemma analysis.
