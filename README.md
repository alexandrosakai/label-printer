# 🏷️ label-printer

**Gerador de etiquetas com código de barras, em uma única página HTML. Sem servidor e sem build.**

![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)
![nginx](https://img.shields.io/badge/nginx-009639?logo=nginx&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-ready-2496ED?logo=docker&logoColor=white)

Monte listas de etiquetas, visualize com zoom e imprima direto ou baixe em PDF. Os arquivos que você carrega são processados no próprio navegador.

## ✨ Funcionalidades

- **Etiquetas 10×15 por lote**, com código do produto e código de barras
- **Modo múltiplo**: monte uma lista e imprima tudo de uma vez
- **Marcar, desmarcar e limpar** itens da lista
- **Leitura de relatório** (planilha Excel, PDF ou Word) para preencher as etiquetas automaticamente
- **Zoom** da pré-visualização
- **Imprimir direto** ou **baixar PDF**
- Bibliotecas carregadas por CDN (SheetJS, pdf.js, mammoth, jsPDF e JsBarcode): é preciso acesso à internet na primeira abertura

## 🧰 Tecnologias

![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)

HTML · CSS · JavaScript · SheetJS · pdf.js · mammoth · jsPDF · JsBarcode (via CDN)

## 📋 Requisitos

- Qualquer navegador moderno, com acesso à internet (para as bibliotecas em CDN)
- Opcional: Docker e Docker Compose v2, ou qualquer servidor de arquivos estáticos

## 🚀 Instalação

### Sem Docker

```bash
git clone https://github.com/alexandrosakai/label-printer.git
cd label-printer/site-etiquetas
python3 -m http.server 8080
```

Abra `http://127.0.0.1:8080`. Também funciona abrindo `site-etiquetas/index.html` direto no navegador.

### Com Docker

```bash
cp .env.example .env        # opcional: muda a porta (WEB_PORT)
docker compose up -d --build
```

Abra `http://127.0.0.1:8080`.

### Em um servidor

Copie `site-etiquetas/` para a raiz de um site em nginx, Apache ou Caddy.

## ⚙️ Configuração

Não há segredos. Para trocar a porta do Docker, edite `WEB_PORT` no `.env`. Para colocar logo nas etiquetas, adicione sua imagem e ajuste a referência no HTML.

## 🧭 Como usar

1. Informe o código do produto e a quantidade, ou carregue um relatório.
2. Adicione à lista, confira na pré-visualização e ajuste o zoom.
3. Clique em **Imprimir direto** ou **Baixar PDF**.

## 📁 Estrutura de pastas

```
label-printer/
├── site-etiquetas/
│   └── index.html         # a aplicação inteira
├── Dockerfile
├── docker-compose.yml
└── .env.example
```

## 🗺️ Roadmap

- [ ] Tamanhos de etiqueta configuráveis
- [ ] Empacotar as bibliotecas localmente (uso 100% offline)
- [ ] Mais tipos de código (QR Code, EAN-13)
- [ ] Salvar listas no navegador
- [ ] Interface em inglês e espanhol
- [ ] Separar CSS e JavaScript em arquivos próprios

## 🤝 Como contribuir

1. Faça um fork e crie uma branch: `git checkout -b minha-melhoria`
2. Prefira soluções simples, sem etapa de build
3. Abra um Pull Request explicando o que mudou

## 📄 Licença

Distribuído sob a licença MIT. Veja o arquivo [LICENSE](LICENSE).
