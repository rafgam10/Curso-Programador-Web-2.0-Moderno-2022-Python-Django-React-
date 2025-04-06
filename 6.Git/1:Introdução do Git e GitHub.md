
## 🌱 Introdução ao Git e GitHub

### 📌 O que é o Git?

**Git** é um sistema de **controle de versão**. Isso significa que ele ajuda você a:

- Acompanhar as mudanças feitas no seu código ao longo do tempo.
- Voltar para versões anteriores, se necessário.
- Trabalhar com outras pessoas no mesmo projeto, sem bagunça.

**Criado por Linus Torvalds** (o mesmo criador do Linux), o Git é rápido, gratuito e funciona localmente no seu computador.

### ✅ Principais comandos do Git

- `git init` – Cria um novo repositório Git.
- `git status` – Mostra o estado atual dos arquivos.
- `git add <arquivo>` – Adiciona um arquivo para ser "preparado" para o commit.
- `git commit -m "mensagem"` – Registra as mudanças com uma mensagem.
- `git log` – Mostra o histórico de commits.
- `git push` – Envia suas alterações para um repositório remoto (como o GitHub).
- `git pull` – Baixa alterações do repositório remoto.

---

### 🐙 O que é o GitHub?

**GitHub** é uma plataforma online que usa o Git para hospedar e compartilhar código com outras pessoas. Ele permite que você:

- Armazene seus projetos na nuvem.
- Colabore com outros desenvolvedores.
- Mantenha seu código seguro e acessível de qualquer lugar.
- Contribua com projetos open source.

💡 GitHub é o lugar onde **seu código encontra a comunidade**.

---

### 🎯 Diferença entre Git e GitHub

| Git (ferramenta)         | GitHub (plataforma)            |
|--------------------------|---------------------------------|
| Funciona localmente      | Funciona online                 |
| Controle de versão       | Armazenamento e colaboração     |
| Linha de comando         | Interface gráfica + funcionalidades extras |

---

### 🛠 Exemplo de fluxo básico com Git e GitHub

1. Criar um repositório no GitHub.
2. Clonar com:  
   `git clone https://github.com/seu-usuario/seu-repositorio.git`
3. Fazer alterações no código.
4. Adicionar e commitar:
   ```bash
   git add .
   git commit -m "Adiciona nova funcionalidade"
   ```
5. Enviar ao GitHub:
   `git push origin main`

