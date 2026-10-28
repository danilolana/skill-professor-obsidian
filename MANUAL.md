# Manual de uso — professor-obsidian

Este manual mostra como preparar o cofre, iniciar uma sessão de estudo e tirar o máximo do professor.

## Sumário

1. [Preparando a pasta de estudos](#1-preparando-a-pasta-de-estudos)
2. [Iniciando uma sessão](#2-iniciando-uma-sessão)
3. [Como o professor conduz a aula](#3-como-o-professor-conduz-a-aula)
4. [As lousas](#4-as-lousas)
5. [Concluindo um tópico](#5-concluindo-um-tópico)
6. [Dicas para estudar melhor](#6-dicas-para-estudar-melhor)
7. [Trocando de matérias ou de ciclo](#7-trocando-de-matérias-ou-de-ciclo)
8. [Solução de problemas](#8-solução-de-problemas)

---

## 1. Preparando a pasta de estudos

### 1.1 Uma pasta por matéria, uma subpasta por ciclo

```
Estudos/
├── Matéria A/
│   └── Ciclo 1/
│       ├── Conteúdo.md
│       ├── Lista de Exercícios.pdf
│       └── anexos/
│           └── foto-resolucao.jpeg
├── Matéria B/
│   └── Ciclo 1/
└── Estudo Ciclo 1/
    ├── Conteúdo Ciclo 1.md
    └── Lousas/
```

Os nomes são livres. O que importa é a ideia:

| Peça | Para que serve |
|---|---|
| Pasta da matéria | Agrupa todo o material daquela matéria |
| Subpasta do ciclo | Separa o material de cada prova/módulo/período |
| `anexos/` | Fotos do caderno, resoluções, figuras |
| Índice (`.md`) | Lista o que será estudado e linka o material |
| `Lousas/` | Onde o professor cria as lousas |

### 1.2 Monte o índice

O índice é o ponto de partida da sessão. Use um checklist por matéria e linke o material:

```markdown
# Matéria A:
- [ ] Tópico 1
- [ ] Tópico 2
[[Lista de Exercícios.pdf|Lista de Exercícios]]

# Matéria B:
- [ ] Tópico 3
[[Conteúdo|Conteúdos]]
```

### 1.3 Coloque o material

- **Textos e anotações:** arquivos `.md`.
- **Exercícios e apostilas:** PDFs.
- **Resoluções do caderno:** fotos em `anexos/`. O professor consegue ler letra de mão; quando a foto estiver difícil, ele pede que você confirme.
- **Aulas em vídeo:** pode deixar o link no `.md`, mas o professor não assiste a vídeos. Escreva um resumo ao lado do link ou conte para ele durante a sessão.

> Quanto mais material você colocar, melhor. A skill ensina **somente** o que está nas pastas.

---

## 2. Iniciando uma sessão

1. No terminal, entre na pasta de estudos do cofre:
   ```bash
   cd "/caminho/do/seu/cofre/Estudos"
   claude
   ```
2. Peça para estudar. Qualquer uma destas frases funciona:
   - `vamos estudar o ciclo 1`
   - `modo professor`
   - `me ensina o tópico 2 da Matéria A`
   - ou o comando direto `/professor-obsidian`

O professor então:

1. localiza o índice e a pasta `Lousas/`;
2. mostra o panorama: matérias, tópicos pendentes e o material disponível (e o que está faltando);
3. pergunta por onde você quer começar;
4. lê o material do tópico escolhido;
5. faz uma pergunta de diagnóstico para descobrir o que você já sabe.

---

## 3. Como o professor conduz a aula

### O ritmo

- **Um passo por vez.** Uma ideia pequena e, em geral, uma pergunta por mensagem.
- **Pergunta antes de explicar.** Você tenta primeiro.
- **Sem resposta pronta.** Se você errar, ele faz uma pergunta que ajuda a perceber onde o raciocínio desviou.

### Quando você trava: a escada de dicas

1. Ele reformula a pergunta.
2. Aponta onde olhar no material ou na lousa.
3. Dá um exemplo mais simples.
4. Mostra um passo parcial.
5. Só depois de tentativas reais explica por completo, e pede que você refaça em outro caso.

### Exemplo de conversa

> **Você:** vamos estudar o tópico 1 da Matéria A
>
> **Professor:** Encontrei o tópico 1 no índice e uma lista de exercícios na pasta. Antes de abrir o material: com as suas palavras, o que você já sabe sobre isso?
>
> **Você:** acho que é só aplicar a fórmula
>
> **Professor:** Qual fórmula, e o que cada letra dela representa?
>
> **Você:** *(responde)*
>
> **Professor:** Bom. Agora olhe o exercício 1 da lista. Que dado do enunciado vai no lugar de cada letra? Vou abrir uma lousa para você montar isso: `Lousas/Matéria A - Tópico 1.md`.

### Se você quiser a resposta direta

Pode pedir: "só me dá a resposta". A decisão é sua. Depois ele propõe um exercício parecido para você fixar.

---

## 4. As lousas

As lousas ficam na pasta `Lousas/` e são abertas no Obsidian. O professor as cria e as **amplia a cada passo**, nunca já prontas, para você não ver a solução antes de pensar.

### 4.1 Lousa em Markdown (`.md`)

Usada para passo a passo, fórmulas, tabelas e listas. Aparecem fórmulas em LaTeX, callouts como `> [!question]` e, quando ajuda, diagramas.

Reconheça os **espaços para você**: trechos marcados com `?` ou "complete aqui". Responda no chat e ele preenche.

### 4.2 Lousa em Canvas (`.canvas`)

Usada para mapas de ideias, fluxos e relações espaciais. Cada ideia é uma caixa ligada por setas. Convenção de cores:

| Cor | Significado |
|---|---|
| Amarelo | pergunta aberta |
| Verde | já entendido |
| Demais | usadas com sentido explicado na própria lousa |

O professor também pode trazer para o canvas uma foto de `anexos/` ou um PDF do material.

### 4.3 Dica de uso

Deixe a lousa aberta no Obsidian ao lado do terminal. Cada vez que ele disser "atualizei a lousa", o Obsidian mostra a mudança.

---

## 5. Concluindo um tópico

Quando você domina um tópico, o professor:

1. pede um **mini-resumo feito por você**;
2. propõe um **exercício novo** parecido;
3. só então pergunta se pode marcar o tópico como concluído no índice (`- [ ]` vira `- [x]`).

Ele edita **apenas essa linha**, e somente com a sua confirmação.

---

## 6. Dicas para estudar melhor

- **Responda com as suas palavras**, mesmo inseguro. O erro mostra ao professor onde ajudar.
- **Diga quando não entendeu.** Ele reformula, em vez de repetir.
- **Peça uma lousa** quando a explicação em texto não for suficiente: "monta uma lousa disso".
- **Resolva os exercícios do material**; é para isso que ele os usa.
- **Estude em blocos curtos.** Como o ritmo é passo a passo, uma sessão de 30 a 40 minutos já rende.
- **Alimente o cofre.** Tire fotos das suas resoluções e coloque em `anexos/` para as próximas sessões.

---

## 7. Trocando de matérias ou de ciclo

Nada na skill é fixo. Para um novo ciclo:

1. Crie `<Matéria>/<Novo Ciclo>/` com o material.
2. Crie a pasta de estudo do novo ciclo, com o índice e a pasta `Lousas/`.
3. Inicie a sessão e cite o novo ciclo: `vamos estudar o ciclo 2`.

Se mudar todas as matérias, tudo continua funcionando, porque a skill lê a estrutura de pastas a cada sessão.

---

## 8. Solução de problemas

| Problema | O que fazer |
|---|---|
| A skill não ativa | Confira se `professor-obsidian/SKILL.md` está em `~/.claude/skills/` e abra uma **nova** sessão. Invoque com `/professor-obsidian`. |
| "Não encontrei a pasta de estudos" | Inicie o `claude` dentro da pasta de estudos (ou perto dela) e confirme que existe uma pasta `Lousas/`. |
| Ele diz que falta material | Está correto: a pasta do tópico está vazia ou só tem exercícios. Adicione o conteúdo ou escolha como seguir (estudar pelos exercícios, ou você explicar o que sabe). |
| Link de vídeo não foi usado | O Claude não assiste a vídeos. Escreva um resumo ao lado do link. |
| Foto de caderno ilegível | Tire outra com mais luz e foco, ou confirme no chat o que está escrito. |
| O canvas não abre no Obsidian | Peça para ele validar e refazer o arquivo. O JSON precisa estar íntegro. |
| Ele marcou algo no índice sem eu confirmar | Não deveria acontecer. Desfaça a linha e avise para respeitar a confirmação. |

---

## Referência rápida

```
Entrar na pasta de estudos  →  cd <pasta de estudos> && claude
Iniciar                      →  "vamos estudar <ciclo/tópico>"  ou  /professor-obsidian
Pedir desenho                →  "monta uma lousa disso"
Pedir resposta direta        →  "só me dá a resposta"
Concluir tópico              →  resumo + exercício novo + confirmar o check no índice
```
