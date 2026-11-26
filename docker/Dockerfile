# Development environment: lets anyone open and run the project code in JupyterLab.
# Build context is the repo root (see docker-compose.yml), so requirements.txt is found.
FROM python:3.13-slim

WORKDIR /app

COPY requirements.txt /tmp/requirements.txt
RUN pip install --no-cache-dir -r /tmp/requirements.txt jupyterlab

EXPOSE 8888

# No login token: the port is only published on 127.0.0.1 (this computer) in docker-compose.yml.
CMD ["jupyter", "lab", "--ip=0.0.0.0", "--port=8888", "--no-browser", "--allow-root", \
     "--ServerApp.token=", "--ServerApp.password="]
