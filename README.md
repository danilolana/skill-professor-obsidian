# professor-obsidian

Uma skill do [Claude Code](https://claude.com/claude-code) que transforma o Claude em um **professor socrático** conectado à sua pasta de estudos do Obsidian.

Em vez de despejar respostas, o professor lê o **seu** material, faz perguntas, avança um passo de cada vez e desenha o que você precisa enxergar em **lousas** (`.md` e `.canvas`) dentro do próprio cofre.

## O que ela faz

- **Usa só o seu material.** Tudo que ensina vem dos arquivos da pasta de estudos (textos, PDFs, fotos de caderno). Se faltar conteúdo, ele avisa em vez de inventar.
- **Ensina por perguntas.** Não entrega a resposta de cara; ajuda você a chegar nela, com dicas graduais quando você trava.
- **Vai passo a passo.** Um conceito e, em geral, uma pergunta por mensagem.
- **Desenha na lousa.** Cria e vai ampliando lousas em Markdown ou Canvas na pasta `Lousas/`, com espaços em branco para você pensar antes de ver a resposta.
- **Respeita o seu cofre.** Só escreve em `Lousas/` e, com sua confirmação, marca tópicos concluídos no índice.

## Estrutura de pastas esperada

A skill não depende de nomes fixos de matérias, ciclos ou caminhos. Ela se orienta por este formato (os nomes entre `<>` são livres):

```
<pasta de estudos>/
├── <Matéria>/
│   └── <Ciclo>/
│       ├── *.md          textos, anotações, links de aulas
│       ├── *.pdf         listas de exercícios, apostilas
│       └── anexos/       fotos de caderno, figuras
└── <Pasta de estudo do ciclo>/
    ├── <Índice>.md       matérias e tópicos em checklist, com [[links]] pro material
    └── Lousas/           onde o professor desenha
```

Exemplo de índice:

```markdown
# Matéria A:
- [ ] Tópico 1
- [ ] Tópico 2
[[Lista de Exercícios.pdf|Lista de Exercícios]]

# Matéria B:
- [ ] Tópico 3
[[Conteúdo|Conteúdos]]
```

## Instalação

Copie a pasta `professor-obsidian` para o diretório de skills do Claude Code.

**Para todos os projetos (usuário):**

```bash
git clone https://github.com/danilolana/skill-professor-obisidian.git
mkdir -p ~/.claude/skills
cp -r skill-professor-obisidian/professor-obsidian ~/.claude/skills/
```

**Só para um cofre específico:** copie para `<seu-cofre>/.claude/skills/`.

Abra uma nova sessão do Claude Code depois de instalar.

## Uso rápido

1. Abra o terminal **dentro da pasta de estudos** do seu cofre e rode `claude`.
2. Diga o que quer estudar, por exemplo:
   > vamos estudar o ciclo 4

   ou invoque direto: `/professor-obsidian`
3. Responda às perguntas do professor e abra a lousa indicada no Obsidian.

O passo a passo completo, com exemplos de conversa e solução de problemas, está no **[MANUAL.md](MANUAL.md)**.

## Requisitos

- Claude Code
- Um cofre Obsidian com a estrutura acima
- Opcional: `pdftotext` (poppler) para ler PDFs mais rápido; o Claude também lê PDFs diretamente

## Limitações

- Não consegue assistir vídeos (links do YouTube, por exemplo). Peça que você resuma o que a aula mostrou.
- Fotos muito borradas podem exigir que você confirme o que está escrito.
- Só ensina o que está nas pastas; assuntos sem material precisam ser adicionados por você.

## Estrutura deste repositório

```
.
├── README.md
├── MANUAL.md
└── professor-obsidian/
    └── SKILL.md
```
