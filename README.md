# 🚀 Promify API

API para gerenciamento de propaganda e anúncios de pequenos estabelecimentos.  
Construída em **.NET 9**, seguindo arquitetura **slice (Features, Infrastructure, Shared)**, com autenticação via **Keycloak**, cache em **Redis** e persistência em **MongoDB**.

---

## 📂 Estrutura do projeto

```text
src/
├── Api/                 # Entry point (Program.cs, appsettings.json, Api.csproj)
├── Features/            # Casos de uso (Auth, Users, Products)
├── Infrastructure/      # Serviços externos (DB, Cache, Keycloak, Extensions)
└── Shared/              # Models e Interfaces comuns

---

## ⚙️ Tecnologias

- [.NET 9](https://dotnet.microsoft.com/)  
- [MongoDB](https://www.mongodb.com/)  
- [Redis](https://redis.io/)  
- [Keycloak](https://www.keycloak.org/)  
- [Docker & Docker Compose](https://docs.docker.com/)  
- [GitHub Actions](https://docs.github.com/en/actions)  

---

## 🐳 Rodando com Docker Compose

O projeto já vem com um `docker-compose.yml` configurado para rodar toda a stack:

```bash
docker compose up --build

Serviços incluídos:

API → http://localhost:5000

Keycloak → http://localhost:8080

MongoDB → mongodb://localhost:27017

Redis → redis://localhost:6379

dotnet restore src/Api/Api.csproj
dotnet build src/Api/Api.csproj -c Release
dotnet run --project src/Api/Api.csproj
