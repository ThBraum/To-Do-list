# To-DO

## 🚀 Inicialização com Docker

Cria os containers e sobe o ambiente:

```bash
sudo docker compose up -d --build
```

## Logs da API
Acompanha os logs do container da API:

```bash
sudo docker-compose logs -f api
``` 

## Acessar container da API
Para abrir um terminal bash dentro do container:

```bash
sudo docker-compose exec api /bin/bash
``` 


### Alembic – Migrações de banco
Criar nova revisão
Gera nova revisão com base nas alterações nos modelos:

```bash
sudo docker-compose run --rm api alembic revision --autogenerate -m "mensagem"
```

## Aplicar revisões
Aplica as revisões pendentes no banco:

```bash
sudo docker-compose run --rm api alembic upgrade head
``` 

## Corrigir permissões da pasta Alembic
Em caso de erro ao acessar arquivos:

```bash
sudo chown -R $(whoami) ./alembic
```
![image](https://github.com/user-attachments/assets/dee02350-bc5e-4a8c-95cb-76dcaa7e6fad)

![image](https://github.com/user-attachments/assets/420d64dd-e863-4699-97d7-aa6753a92121)
