# Startup em Foco

Site de tema livre sobre **startups**, feito em HTML semântico, sem CSS e sem JavaScript.

- **Aluno:** Theo Lorentz Padilha
- **Turma:** DSM3-2025
- **Unidade Curricular:** Programação de Aplicativos
- **Docente:** Ewerton de Oliveira Cercal
- **Atividade:** [AT04] HTML semântico — Meu Site em HTML: Pesquisa e Construção

## Descrição

O site explica como uma startup nasce, de onde vem o dinheiro dela e o que significam termos como MVP, pitch e pivô. Também traz uma tabela com startups fictícias de um programa de aceleração e dois formulários (inscrição no Demo Day e contato). Todos os nomes, números, e-mails, telefones e endereços são fictícios.

## Como abrir

Baixe ou clone o repositório e abra o arquivo `index.html` no navegador. Não é preciso instalar nada.

## Páginas

1. `index.html`: apresentação, etapas de uma startup, figuras e link para o cadastro.
2. `sobre.html`: sumário com âncoras, dois artigos, um aside, glossário e links externos.
3. `dados.html`: tabela com legenda, cabeçalho, corpo e rodapé, com totais e médias.
4. `cadastro.html`: formulário de inscrição com validação nativa do navegador.
5. `contato.html`: endereço, horário de atendimento e formulário de mensagem.

## Acessibilidade e teclado

- Link "Pular para o conteúdo" no início de todas as páginas.
- `lang="pt-BR"`, `title` e `description` próprios em cada página.
- Menu em `nav` com `aria-label` e `aria-current="page"` na página atual.
- Imagens com `alt` descritivo; a imagem decorativa usa `alt=""`.
- Todo campo de formulário tem `label` ligado por `for` e `id`, agrupados com `fieldset` e `legend`.
- Tabela com `scope` nas colunas e nas linhas.

**Teste de teclado (automatizado, não feito à mão):** um script com puppeteer pressionou Tab em cada página e conferiu que todos os links e campos recebem foco, na ordem do documento. Resultado: index 11 de 11 paradas, sobre 12 de 12, dados 6 de 6, cadastro 21 de 21 e contato 15 de 15.

**Lighthouse 12.6.1 (categoria Acessibilidade):** index 95, sobre 95, dados 95, cadastro 95, contato 96. O único item reprovado em todas as páginas é `target-size` (tamanho do alvo de toque), que depende de CSS para ser corrigido. Como o enunciado pede HTML sem estilo, ele fica sem correção e foi mantido de propósito.

**Validador W3C (Nu Html Checker):** 0 mensagens nas cinco páginas.

## Imagens

Todas são SVGs de autoria própria, em `img/`, feitas à mão para este trabalho e de uso livre em contexto escolar:

- `equipe-ideia.svg`: três pessoas ao redor de uma mesa com uma lâmpada.
- `grafico-crescimento.svg`: gráfico de barras crescente.
- `divisor-foguete.svg`: enfeite decorativo (foguete).

## Decisões de semântica

- `header`, `nav`, `main` e `footer` em todas as páginas, com um único `h1` por página.
- `section` para blocos com título; `article` para conteúdos que fazem sentido sozinhos; `aside` para a curiosidade complementar.
- `dl` para glossário e horário de atendimento, por serem pares de termo e descrição.
- `address` apenas para o contato da própria página.
- `time datetime` nas datas da tabela, para o navegador entender o valor.
- Sem `<br>` para espaçamento (só para quebrar linhas dentro do `address`) e sem tabela para layout.

## Licença

Trabalho escolar, sem fins comerciais. Conteúdo e imagens de autoria do aluno.
