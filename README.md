# Doc_Docker

beliciobcardoso: como lista os containes docker selecionando qual colunas posso ver

GitHub Copilot: # Listando containers Docker com seleção de colunas

Para listar containers Docker e personalizar as colunas exibidas, você pode usar o comando `docker ps` com a opção `--format`. 

## Comandos básicos:

# Listar apenas containers em execução
```bash
docker ps
```

# Listar todos os containers (em execução e parados)
```bash
docker ps -a
```

## Personalizando colunas com --format:

# Exibir apenas ID e nome
```bash
docker ps --format "table {{.ID}}\t{{.Names}}"
```

# Exibir ID, nome, imagem e status
```bash
docker ps --format "table {{.ID}}\t{{.Names}}\t{{.Image}}\t{{.Status}}"
```

# Exibir ID, nome, portas e tempo em execução
```bash
docker ps --format "table {{.ID}}\t{{.Names}}\t{{.Ports}}\t{{.RunningFor}}"
```

# Exibir ID, nome, status e portas
```bash
docker ps --format "table {{.ID}}\t{{.Names}}\t{{.Status}}\t{{.Ports}}"
```

## Colunas disponíveis:

- `{{.ID}}` - ID do container
- `{{.Names}}` - Nome do container
- `{{.Image}}` - Imagem utilizada
- `{{.Status}}` - Estado atual
- `{{.Ports}}` - Portas mapeadas
- `{{.RunningFor}}` - Tempo em execução
- `{{.Size}}` - Tamanho do container
- `{{.Command}}` - Comando em execução
- `{{.CreatedAt}}` - Data de criação
- `{{.Networks}}` - Redes conectadas

Você pode combinar essas opções conforme necessário para visualizar exatamente as informações que precisa.
