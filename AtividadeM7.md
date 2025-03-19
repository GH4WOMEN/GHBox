# Laboratório Módulo 7 - Benefits of the GitHub Community

## Criação de Templates de Issue e Pull Request

Nesta atividade, você aprenderá a criar templates de issue e pull request para padronizar a forma como problemas são reportados e mudanças são propostas em um repositório GitHub. Isso ajudará a garantir que todas as informações necessárias sejam fornecidas, facilitando a triagem e a resolução de problemas, além de manter a qualidade do código.

## Passo a Passo

### 1. Criação da Estrutura de Diretórios

1. No seu repositório, crie uma pasta chamada `.github`.
2. Dentro da pasta `.github`, crie outra pasta chamada `ISSUE_TEMPLATE`.

### 2. Criação de Templates de Issue

### Bug Report

Dentro da pasta `ISSUE_TEMPLATE`, crie um arquivo chamado `bug_report.md` com o seguinte conteúdo:

```markdown
---
name: Bug Report
about: Reportar um bug para ajudar a melhorar o projeto
title: "[BUG] Descreva o título do bug"
labels: bug
assignees: ''
---

### Descrição do Problema
Descreva o problema de forma clara e concisa.

### Passos para Reproduzir
1. Vá para '...'
2. Clique em '...'
3. Role para baixo até '...'
4. Veja o erro

### Comportamento Esperado
Descreva o que você esperava que acontecesse.

### Comportamento Atual
Descreva o que realmente aconteceu.

### Ambiente
- Sistema Operacional: [e.g. Windows, macOS, Linux]
- Navegador: [e.g. Chrome, Safari, Firefox]
- Versão do Projeto: [e.g. 1.0.0]
```

### Feature Request

Crie outro arquivo chamado `feature_request.md` com o seguinte conteúdo:

```markdown
---
name: Feature Request
about: Solicitar uma nova funcionalidade para o projeto
title: "[FEATURE] Descreva o título da funcionalidade"
labels: enhancement
assignees: ''
---

### Descrição da Funcionalidade
Descreva a funcionalidade de forma clara e concisa.

### Motivo da Funcionalidade
Explique por que essa funcionalidade é necessária.

### Exemplos de Uso
Forneça exemplos de como essa funcionalidade seria usada.
```

## 3. Criação de Templates de Pull Request

Na pasta `.github`, crie um arquivo chamado `PULL_REQUEST_TEMPLATE.md` com o seguinte conteúdo:

```markdown
### Descrição das Mudanças
Descreva as mudanças propostas de forma clara e concisa.

### Motivo das Mudanças
Explique por que essas mudanças são necessárias.

### Checklist
- [ ] Testes foram realizados e passaram.
- [ ] Documentação foi atualizada.
- [ ] Código segue os padrões de estilo do projeto.

### Issue Relacionada
Link para a issue relacionada, se houver.

### Capturas de Tela (se aplicável)
Adicione capturas de tela para ajudar a visualizar as mudanças.
```

## 4. Commit e Push

Faça commit das mudanças e envie para o repositório remoto:

```bash
git add .
git commit -m "Adiciona templates de issue e pull request"
git push origin main
```

## 5. Teste os Templates

1. No GitHub, vá até a aba de "Issues" e clique em "New issue". Você verá as opções para escolher entre os templates de bug e feature request.
2. Vá até a aba de "Pull requests" e clique em "New pull request". Você verá o template de pull request preenchido automaticamente.
