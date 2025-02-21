# n8n_ollama_openwebui

### What’s included

✅ [**Self-hosted n8n**](https://n8n.io/) 

✅ [**Ollama**](https://ollama.com/) 

✅ [**Qdrant**](https://qdrant.tech/) 

✅ [**PostgreSQL**](https://www.postgresql.org/)

✅ [**Open WebUi**](https://docs.openwebui.com/)


### Running n8n using Docker Compose

#### For Nvidia GPU users

```
git clone https://github.com/RaySRChen/n8n_ollama_openwebui.git
cd self-hosted-ai-starter-kit
docker compose --profile gpu-nvidia up
```

### For AMD GPU users on Linux

```
git clone https://github.com/RaySRChen/n8n_ollama_openwebui.git
cd self-hosted-ai-starter-kit
docker compose --profile gpu-amd up
```

#### For Mac / Apple Silicon users

```
git clone https://github.com/RaySRChen/n8n_ollama_openwebui.git
cd self-hosted-ai-starter-kit
docker compose up
```

##### For Mac users running OLLAMA locally

```yaml
x-n8n: &service-n8n
  # ... other configurations ...
  environment:
    # ... other environment variables ...
    - OLLAMA_HOST=host.docker.internal:11434
```

Additionally, after you see "Editor is now accessible via: <http://localhost:5678/>":

1. Head to <http://localhost:5678/home/credentials>
2. Click on "Local Ollama service"
3. Change the base URL to "http://host.docker.internal:11434/"

#### For everyone else

```
git clone https://github.com/RaySRChen/n8n_ollama_openwebui.git
cd self-hosted-ai-starter-kit
docker compose --profile cpu up
```

## Upgrading

* ### For Nvidia GPU setups:

```bash
docker compose --profile gpu-nvidia pull
docker compose create && docker compose --profile gpu-nvidia up
```

* ### For Mac / Apple Silicon users

```
docker compose pull
docker compose create && docker compose up
```

* ### For Non-GPU setups:

```bash
docker compose --profile cpu pull
docker compose create && docker compose --profile cpu up
```


