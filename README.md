# eufisica/LaTeX — Guia de Documentos e Notas de Física

Este documento baseia-se na estrutura e nos princípios do repositório **eufisica/LaTeX**, criado por José Gonçalves, focado na produção de documentos científicos, notas de aula e simulações na área de Física utilizando \LaTeX.

---

## 1. Visão Geral do Repositório

O repositório `eufisica/LaTeX` reúne modelos, notas e documentos voltados para a comunicação clara e rigorosa de conceitos físicos. O \LaTeX é o padrão de facto na comunidade científica para a editoração de textos técnicos devido à sua precisão na tipografia matemática.

### Principais Objetivos:
- Organização modular de notas de estudo e relatórios de física.
- Padronização de equações matemáticas e notações físicas.
- Integração de gráficos, diagramas e simulações.

---

## 2. Estrutura Básica de um Documento Científico

Um documento típico para física estruturado em \LaTeX segue o seguinte formato padrão:

```latex
\documentclass[12pt,a4paper]{article}
\usepackage[utf8]{inputenc}
\usepackage[portuguese]{babel}
\usepackage{amsmath,amssymb,amsfonts}
\usepackage{physics}
\usepackage{graphicx}
\usepackage{hyperref}

\title{Título do Documento de Física}
\author{José Gonçalves (eufisica)}
\date{\today}

\begin{document}

\maketitle

\begin{abstract}
Resumo conciso do documento abordando os principais tópicos de física discutidos.
\end{abstract}

\section{Introdução}
Texto introdutório sobre o problema físico abordado.

\section{Desenvolvimento Teórico}
Discussão das equações e princípios fundamentais.

\end{document}
```

---

## 3. Principais Pacotes Úteis para Física

Para documentos de física robustos, os seguintes pacotes são altamente recomendados:

1. **`amsmath` / `amssymb`**: Essenciais para o ambiente matemático avançado.
2. **`physics`**: Facilita a escrita de derivadas, integrais, vetores e notação de Dirac (ex: $\dv{x}$, $\partialv{f}{t}$, $\vec{v}$, $\braket{\psi}{\phi}$).
3. **`tikz`**: Criação de diagramas vetoriais e circuitos elétricos diretamente no código.
4. **`siunitx`**: Formatação padronizada de unidades do Sistema Internacional (SI) e números (ex: $\pu{9.81 m/s^2}$).

---

## 4. Exemplos de Equações Físicas em Notação LaTeX

Abaixo estão alguns exemplos fundamentais formatados com sintaxe LaTeX:

### Mecânica Clássica (Segunda Lei de Newton)
$$\vec{F} = m \vec{a} = \frac{\mathrm{d}\vec{p}}{\mathrm{dt}}$$

### Eletromagnetismo (Equações de Maxwell em forma diferencial)
$$\begin{aligned}
\nabla \cdot \mathbf{E} &= \frac{\rho}{\varepsilon_0} \\
\nabla \cdot \mathbf{B} &= 0 \\
\nabla \times \mathbf{E} &= -\frac{\partial \mathbf{B}}{\partial t} \\
\nabla \times \mathbf{B} &= \mu_0 \mathbf{J} + \mu_0 \varepsilon_0 \frac{\partial \mathbf{E}}{\partial t}
\end{aligned}$$

### Mecânica Quântica (Equação de Schrödinger Dependente do Tempo)
$$i\hbar \frac{\partial}{\partial t} \psi(\mathbf{r}, t) = \hat{H} \psi(\mathbf{r}, t)$$

---

## 5. Boas Práticas na Edição de Documentos

- **Modularização:** Divida capítulos ou seções em arquivos separados (`\input{secao1.tex}`) para facilitar a manutenção.
- **Controle de Versão:** Utilize Git para rastrear alterações nas fórmulas e textos, permitindo colaboração fluida.
- **Compilação Limpa:** Utilize motores modernos como `XeLaTeX` ou `LuaLaTeX` para suporte nativo a fontes OpenType e símbolos Unicode.
