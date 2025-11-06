FROM python:3.10-slim

WORKDIR /app

COPY requirements.txt .

RUN pip install -r requirements.txt --no-cache-dir \
    && echo "--- Pip install complete. Installed packages: ---" \
    && pip list

COPY . .

EXPOSE 8501

ENTRYPOINT ["python", "-m", "streamlit", "run", "web_app.py", "--server.port=8501", "--server.address=0.0.0.0"]