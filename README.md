# minhas-publicacoes-cientificas
## Artigos ciêntificos do Doutorado


### **Objetivo da Aula**
- Aprimorar o conhecimento em Git e GitHub, abordando comandos avançados e práticas recomendadas para colaboração em projetos.

### **Carga Horária**
2 horas (aproximadamente)

---

### **1. Introdução (10 min)**
- Revisão breve dos conceitos básicos:
  - O que é Git e GitHub.
  - Diferença entre Git (controle de versão local) e GitHub (repositório remoto).
  - Revisão dos principais comandos básicos (`init`, `clone`, `add`, `commit`, `push`, `pull`).

---

### **2. Conceitos Intermediários e Avançados (30 min)**
#### 2.1. Branching e Workflow
- O que são branches e por que usá-los.
- Criar e alternar entre branches:
  ```bash
  git branch feature-xyz
  git checkout feature-xyz
  # ou
  git switch feature-xyz
  ```
- Merge:
  ```bash
  git merge feature-xyz
  ```
- Resolvendo conflitos de merge.

#### 2.2. Stash
- Salvando alterações temporárias:
  ```bash
  git stash
  git stash list
  git stash apply
  ```

#### 2.3. Rebasing
- Diferença entre `merge` e `rebase`.
- Como usar o `rebase` para manter o histórico limpo:
  ```bash
  git rebase main
  ```

#### 2.4. Logs e Revisão de Histórico
- Navegando no histórico de commits:
  ```bash
  git log
  git log --oneline --graph
  ```

---

### **3. Ferramentas Colaborativas no GitHub (30 min)**
#### 3.1. Pull Requests (PR)
- Criando uma Pull Request.
- Revisando PRs (comentários, sugestões e aprovações).
- Regras para merge no GitHub (squash, merge direto, rebase).

#### 3.2. Issues e Projetos
- Criando e gerenciando Issues.
- Uso de templates para Issues e Pull Requests.
- Boards Kanban no GitHub Projects.

#### 3.3. Actions
- Introdução ao GitHub Actions:
  - Criando um pipeline simples:
    ```yaml
    name: CI Pipeline

    on:
      push:
        branches:
          - main

    jobs:
      build:
        runs-on: ubuntu-latest
        steps:
          - name: Checkout code
            uses: actions/checkout@v2
          - name: Run tests
            run: npm test
    ```

---

### **4. Comandos Avançados e Truques (20 min)**
#### 4.1. Reset e Reflog
- Diferença entre `soft`, `mixed` e `hard`:
  ```bash
  git reset --soft HEAD~1
  git reset --hard HEAD~1
  ```
- Recuperando commits perdidos com `reflog`:
  ```bash
  git reflog
  git reset --hard <hash>
  ```

#### 4.2. Bisect
- Usando `git bisect` para encontrar bugs:
  ```bash
  git bisect start
  git bisect bad
  git bisect good <commit>
  ```

#### 4.3. Cherry-pick
- Aplicando commits específicos:
  ```bash
  git cherry-pick <hash>
  ```

---

### **5. Prática Guiada (30 min)**
1. **Configurar o repositório:**
   - Criar um repositório no GitHub e clonar.
   - Criar e alternar entre branches.
2. **Simular um fluxo de trabalho:**
   - Alterações em diferentes branches.
   - Merge com conflitos e resolução.
   - Uso de stash para mudanças temporárias.
3. **Interação no GitHub:**
   - Criar Pull Requests e revisar.
   - Configurar GitHub Actions simples.

