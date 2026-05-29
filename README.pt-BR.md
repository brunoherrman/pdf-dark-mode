[English](./README.md) | [Português (Brasil)](./README.pt-BR.md)

# PDF Dark Mode

Leitor de PDF em modo escuro, totalmente no navegador, com marcações, comentários em texto, busca, zoom, cópia de print e exportação do PDF anotado.

## Visão Geral

PDF Dark Mode é um leitor leve, client-side, feito para leitura confortável por longos períodos. Você pode abrir um PDF localmente, alternar entre presets escuros, navegar com rapidez, destacar conteúdo, adicionar comentários formatados e exportar o arquivo anotado sem backend.

## Recursos

- Presets de leitura escura: `Warm`, `Classic` e `Blue`
- Busca com destaque claro do resultado atual
- Navegação estável por páginas, miniaturas e atalho numérico
- Marcações por seleção de texto e por caixa
- Comentários em texto com clique na página, tamanho, negrito e itálico
- Desfazer e refazer com `Ctrl + Z` / `Ctrl + Y`
- Cópia da página atual como imagem
- Exportação local do PDF anotado
- Cor personalizada de anotação persistida em `localStorage`

## Stack

- HTML
- CSS
- JavaScript vanilla
- [PDF.js](https://mozilla.github.io/pdf.js/)
- [PDF-lib](https://pdf-lib.js.org/)

## Executando Localmente

### Opção 1: abrir direto

Abra o `index.html` diretamente no navegador.

Observações:
- algumas APIs do navegador podem ficar limitadas em `file://`
- `Salvar como` funciona melhor quando servido em `localhost`

### Opção 2: servidor local recomendado

```bash
python -m http.server 5500
```

Depois abra:

```text
http://localhost:5500
```

## Como Usar

### Marcar texto

1. Clique em `Caneta`
2. Selecione o texto dentro do PDF

### Marcar com caixa

1. Clique em `Caixa`
2. Arraste sobre a área desejada

### Inserir comentário em texto

1. Clique em `T`
2. Clique em qualquer ponto da página
3. Digite o comentário no popup
4. Ajuste tamanho, negrito e itálico
5. Clique em `OK`

### Salvar PDF anotado

- `Salvar como`: tenta abrir o seletor do sistema para escolher pasta e nome do arquivo
- `Download PDF`: baixa uma cópia com timestamp no nome

## Privacidade

- os PDFs são processados localmente no navegador
- não existe backend neste projeto
- as anotações são salvas localmente via `localStorage`

## Notas de Segurança

- não foram encontrados tokens, segredos, chaves privadas ou credenciais no repositório local durante a revisão
- o projeto depende atualmente de CDNs públicos para `pdf.js` e `pdf-lib`
- para cenários mais rígidos de produção, vale considerar versionar esses assets localmente e adicionar controles de integridade quando possível

## Arquivos do Repositório

- `index.html`: aplicação completa
- `README.md`: documentação em inglês
- `README.pt-BR.md`: documentação em português do Brasil
- `.gitignore`: exclusões para publicação pública
- `LICENSE`: licença do projeto

## Descrição Recomendada Para o GitHub

Dark-mode PDF reader with highlights, comments, search, zoom, print copy, and annotated PDF export — fully client-side.

## Licença

MIT
