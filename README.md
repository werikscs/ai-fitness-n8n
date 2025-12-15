# AI Fitness - n8n (Docker)

Instruções para instalar e executar o serviço n8n usando Docker Compose.

Em anexo, imagens dos ciclos RAG e Chat no n8n. Assim como o .json completo do n8n.

## Pré-requisitos
- Docker
- Docker Compose
- Arquivo de variáveis de ambiente (.env)

## Configuração
1. Copie o modelo de ambiente e ajuste as variáveis conforme necessário:

   ```sh
   cp .env.example .env
   ```
## Executando
- Subir containers em modo destacado:

   ```sh
   docker-compose up -d
   ```
- Ver logs do serviço n8n:
   ```sh
   docker-compose logs -f n8n
   ```
- Parar e remover containers:
   ```sh
   docker-compose down
   ```

## Acesso
- URL padrão (conforme .env): http://localhost:5678/
- Autenticação básica configurada via variáveis:
   - ```N8N_BASIC_AUTH_USER```
   - ```N8N_BASIC_AUTH_PASSWORD```

## Persistência
- Volume Docker: ```n8n_storage``` (definido em ```docker-compose.yml```) preserva dados entre reinícios.