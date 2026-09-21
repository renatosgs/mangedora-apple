<div align="center">

# 🍎 MANGEDORA APPLE PRO ELITE

### 🛡️ Cofre Blindado Permanente • Google Fotos OAuth 2.0 • Robô IA 4K

**Cofre blindado permanente para fotos e vídeos, rodando direto no navegador.**
**Funciona 100% offline para uso diário** — a internet só é necessária na primeira configuração e para importar do Google Fotos.

[![Status](https://img.shields.io/badge/status-pronto-brightgreen?style=for-the-badge)](https://renatosgs.github.io/mangedora-apple/)
[![Versão](https://img.shields.io/badge/vers%C3%A3o-v7.1-blue?style=for-the-badge)](https://renatosgs.github.io/mangedora-apple/)
[![License](https://img.shields.io/badge/license-MIT-green?style=for-the-badge)](LICENSE)
[![Sem servidor](https://img.shields.io/badge/servidor-nenhum-orange?style=for-the-badge)](#)
[![Privacidade](https://img.shields.io/badge/privacidade-100%25_local-purple?style=for-the-badge)](#)

### 🔗 [**Abrir o app →**](https://renatosgs.github.io/mangedora-apple/)

![MANGEDORA APPLE](screenshot.png)

</div>

---

Sem servidor. Sem cadastro obrigatório. Sem rastreamento. Suas mídias ficam guardadas **permanentemente** no seu aparelho via **IndexedDB** — apagar do celular **não** remove do cofre. **A nuvem só entra se você quiser** (importação opcional do Google Fotos).

---

## ✨ Recursos

### 🛡️ Cofre Blindado Permanente
- **Armazenamento em IndexedDB** com persistência real (`navigator.storage.persist()`)
- **Funciona offline** após o primeiro carregamento — sem internet, sem servidor, sem nuvem
- Selo **🔒 Permanente** em cada mídia — apagar do celular não afeta o cofre
- **Filtros**: Todos • Fotos • Vídeos • Favoritos • Otimizados IA
- **Busca** por nome, **ordenação** (recentes, antigos, tamanho, nome)
- **Lightbox** com visualização ampliada e download
- **Backup completo em ZIP** com 1 clique

### 📸 Múltiplas formas de enviar
- Upload por **drag & drop**
- Envio direto da **galeria do celular**
- **Colar com Ctrl+V** (copie do Google Fotos e cole aqui)
- Import de **backup ZIP** do Google Takeout
- **Sincronização com Google Fotos** (veja abaixo)

### 🔗 Integração Oficial Google Fotos (OAuth 2.0)
- **Vinculação segura** — você digita e-mail/senha na **janela oficial do Google**, nunca dentro do app
- **Photos Picker API** — escolha as fotos que quiser importar
- **Download automático** direto pro cofre
- **Zero armazenamento de senha** — só um token temporário em memória
- Selo **G Fotos** em cada mídia importada

### ⚡ Robô Titânio IA Plus
- **Compressão Canvas 4K** (até 2560px, qualidade 82%)
- **Fallback WebP → JPEG** para navegadores antigos
- **Eliminação de duplicados por hash** (FNV-1a duplo)
- **Desfragmentação** do banco IndexedDB
- **Terminal de log** em tempo real
- Exibe **economia total de espaço** em MB/GB

### 🎨 40 Temas Exclusivos
Categorias: **Apple & Titanium** • **Elite & Luxo** • **Cyber & Futurista** • **Neon & Quântico** • **Natureza & Joias** • **Amoled & Escuros**

- **Boot Estilista IA** — sugere temas automaticamente
- **Busca e filtros** por categoria
- **Troca rápida** com 1 clique (botão ⏭️ no topo)
- Temas aplicados em **tempo real** via CSS variables

### 💾 Armazenamento Ajustável
- Ajuste a cota exibida: **50 GB até 999 TB**
- Presets rápidos + campo personalizado
- Barra de uso em tempo real
- Indicador de **persistência concedida** pelo navegador

---

## 🚀 Como usar

### 🌐 Online (recomendado)

Acesse direto no navegador:

**https://renatosgs.github.io/mangedora-apple/**

> Use **HTTPS** para que a integração com Google Fotos funcione (o Google bloqueia OAuth em arquivos locais).

### 💻 Localmente

Baixe o `index.html` e abra com dois cliques. Funciona offline, sem instalação. **Nota:** a integração com Google Fotos **não** funciona em modo local no iOS/Safari — só em HTTPS.

### 📱 Instalar como app

No **Chrome (Android)** ou **Safari (iOS)**:
1. Abra o app no navegador
2. Toque no menu do navegador
3. Escolha **"Adicionar à tela de início"**
4. Pronto! Fica com ícone próprio e persistência reforçada.

---

## 🌐 Quando precisa de internet?

| Ação | Precisa de internet? |
|---|:---:|
| Abrir o app pela primeira vez | ✅ Sim (baixa fontes e JSZip) |
| Uso diário (ver, organizar, favoritar) | ❌ Não — 100% offline |
| Adicionar fotos da galeria | ❌ Não |
| Colar com Ctrl+V / Drag & Drop | ❌ Não |
| Importar arquivo ZIP | ❌ Não |
| Robô IA (compressão) | ❌ Não |
| Trocar tema | ❌ Não |
| **Importar do Google Fotos** | ✅ Sim (precisa baixar da nuvem) |
| **Vincular conta Google** | ✅ Sim (OAuth) |

> 💡 **Dica:** instale como app (PWA) para que as fontes fiquem em cache e o app funcione **mesmo offline na primeira abertura**.

---

## 🔗 Como configurar o Google Fotos (opcional)

Para puxar fotos direto do Google Fotos pro cofre, você precisa de um **Client ID OAuth** (gratuito, você cria em ~5 min):

1. Acesse [console.cloud.google.com](https://console.cloud.google.com)
2. Crie um projeto novo
3. **APIs e serviços → Biblioteca** → ative **Photos Picker API**
4. **Tela de permissão OAuth** → tipo **Externo** → adicione seu e-mail como **testador**
5. **Credenciais → Criar → ID do cliente OAuth → Aplicativo da Web**
6. Em **Origens JavaScript autorizadas**, adicione:
   - `https://renatosgs.github.io` (para o app online)
   - `http://localhost` (para testes locais, opcional)
7. Copie o **Client ID** gerado (termina em `.apps.googleusercontent.com`)
8. Abra o app → **⚙️ Configurações** → cole o **Client ID** → **💾 Salvar**
9. Toque em **🔗 Vincular Conta Google** → autorize na janela oficial

---

## 🔒 Privacidade & Segurança

| Aspecto | Como funciona |
|---|---|
| **Armazenamento** | 100% local (IndexedDB no seu navegador) |
| **Servidor** | Nenhum — o app roda só no seu aparelho |
| **Rastreamento** | Nenhum — sem analytics, sem cookies |
| **Senha do Google** | Nunca digitada dentro do app — só na janela oficial do Google |
| **Token de acesso** | Só em memória, nunca em `localStorage` |
| **Persistência** | `navigator.storage.persist()` impede limpeza automática |
| **Backup** | Manual em ZIP (você guarda onde quiser) |

> **⚠️ Importante:** apagar dados do navegador, limpar cache ou trocar de celular apaga o cofre. **Faça backups periódicos** pelo botão **📦 Baixar Tudo em ZIP** nas Configurações.

---

## 🛠️ Tecnologias

| Tecnologia | Uso |
|---|---|
| **HTML5 + CSS3 + JavaScript puro** | Zero build, zero npm |
| **IndexedDB** | Banco de dados local do navegador |
| **Canvas API** | Compressão de imagens |
| **CSS Variables** | Sistema de 40 temas dinâmicos |
| **JSZip** | Import/export de pacotes ZIP |
| **Google Identity Services** | OAuth 2.0 |
| **Photos Picker API** | Seleção de fotos do Google Fotos |

Todo o app é **single-file** — não precisa de build, webpack, npm ou qualquer coisa.

---

## 📂 Estrutura

```
mangedora-apple/
├── index.html       # Aplicativo completo (single-file)
├── README.md        # Este arquivo
├── screenshot.png   # Print do app (usado no README)
└── LICENSE          # MIT (opcional)
```

---

## 📋 Compatibilidade

| Navegador | Suporte |
|---|:---:|
| Chrome / Edge | ✅ Completo |
| Firefox | ✅ Completo |
| Safari (macOS / iOS 15+) | ✅ Completo |
| Navegadores antigos | ⚠️ Sem Google Fotos (fallback WebP→JPEG) |

---

## 🗺️ Roadmap

- [x] Cofre permanente com IndexedDB
- [x] Robô IA de compressão (Canvas 4K)
- [x] 40 temas com Boot Estilista IA
- [x] Integração Google Fotos (OAuth 2.0 + Photos Picker API)
- [x] Import/Export ZIP (Google Takeout)
- [x] Persistência real no navegador
- [x] Compressão com fallback WebP → JPEG
- [ ] Modo PWA com Service Worker
- [ ] Sincronização opcional entre dispositivos
- [ ] Backup automático para Google Drive

---

## 📜 Licença

MIT — use, modifique e distribua livremente.

---

<div align="center">

**Feito com ☕ e luz vermelha de darkroom.** 🛡️

[⬆ Voltar ao topo](#-mangedora-apple-pro-elite)

</div>
