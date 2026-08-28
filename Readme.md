# Docker Python Test — Users Service

Projeto de teste para validar a containerização e execução do `users-service` (Python/FastAPI) com Docker.

## Estrutura

```
docker-python-test/
├── users-service/
│   ├── app/
│   │   ├── main.py
│   │   ├── models.py
│   │   └── database.py
│   ├── requirements.txt
│   └── Dockerfile
├── docker-compose.yml
└── README.md
```

## Como correr

```bash
git clone http://bitbucket.mozabanco.co.mz:7990/scm/train/docker-python-test.git
cd docker-python-test

docker compose up -d --build
```

Verificar estado:

```bash
docker compose ps
docker compose logs -f users-service
```

Serviço disponível em `http://localhost:8000` (Swagger: `/docs`).

## Parar

```bash
docker compose down
```