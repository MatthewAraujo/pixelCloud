# 📸 PixelCloud

PixelCloud é uma aplicação fullstack para upload, compressão, redimensionamento e armazenamento de imagens em nuvem utilizando a **Cloudflare R2**. O projeto foi desenvolvido com foco em boas práticas de engenharia de software, escalabilidade e infraestrutura moderna.

## ✨ Funcionalidades

- Upload de imagens com drag-and-drop
- Compressão e redimensionamento automático
- Armazenamento em nuvem com Cloudflare R2
- Visualização em galeria
- API RESTful com autenticação
- Deploy automatizado com Docker + Pulumi + AWS ECS
- Observabilidade com Grafana + Prometheus

---

## 🧱 Tecnologias Utilizadas

### 📦 Back-end
- Node.js (Express)
- Cloudflare R2 SDK (S3 compatible)
- Multer (upload)
- Sharp (compressão/redimensionamento)
- Swagger (documentação)
- JWT (autenticação)
- Prometheus + Grafana (observabilidade)

### 🎨 Front-end
- React.js (ou Next.js)
- TailwindCSS
- React Dropzone
- Axios

### ☁️ Infraestrutura
- Docker & Docker Compose
- Pulumi (IaC)
- AWS ECS (deploy)
- GitHub Actions (CI/CD)

---

## 📷 Preview

<img src="./docs/preview-upload.png" alt="Upload UI Preview" width="600"/>
<img src="./docs/preview-gallery.png" alt="Gallery Preview" width="600"/>

---

## 🚀 Como executar

### Pré-requisitos
- Node.js v18+
- Docker
- Conta na Cloudflare com bucket R2 configurado
- Variáveis de ambiente (`.env`)

### Instalação

```bash
# Clone o repositório
git clone https://github.com/seu-usuario/pixelcloud.git
cd pixelcloud

# Instale as dependências do backend
cd server
npm install

# Instale as dependências do frontend
cd ../client
npm install
````

### Executando com Docker

```bash
# Na raiz do projeto
docker-compose up --build
```

### Acesso

* Frontend: `http://localhost:3000`
* Backend API: `http://localhost:3333`

---

## ⚙️ Variáveis de ambiente

Crie um arquivo `.env` no diretório `server` com as seguintes variáveis:

```env
CLOUDFLARE_R2_ACCESS_KEY=your-access-key
CLOUDFLARE_R2_SECRET_KEY=your-secret-key
CLOUDFLARE_R2_BUCKET_NAME=pixelcloud-images
CLOUDFLARE_R2_REGION=auto
CLOUDFLARE_R2_ENDPOINT=https://<account-id>.r2.cloudflarestorage.com
JWT_SECRET=your-secret
```

---

## 📑 Documentação da API

Disponível em: `http://localhost:3333/api/docs`
Gerada com Swagger.
