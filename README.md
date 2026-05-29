# PDF Dark Mode

Leitor de PDF em modo escuro, 100% client-side, feito para leitura confortável, marcações rápidas e exportação do PDF anotado.

## Description

Dark-mode PDF reader that runs entirely in the browser, with highlights, comments, search, zoom, print copy, and annotated PDF export.

## Preview

- Leitura de PDF em modo escuro com presets visuais
- Navegação por miniaturas, busca e atalho para página
- Marcações por seleção de texto e caixa
- Comentários em texto com tamanho, negrito e itálico
- Cópia de print da página atual
- Exportação do PDF com anotações
- Salvamento local e download com timestamp

## Features

- `Warm`, `Classic` e `Blue` como presets de visualização
- Busca com destaque de ocorrências e foco visual no resultado atual
- Zoom, ajustar largura e `100%` com navegação mais estável
- Histórico de ações com `Ctrl + Z` e `Ctrl + Y`
- Paleta de marcação com cor personalizada persistida em `localStorage`
- Painel lateral com lista de marcações e edição de comentários em texto
- Exportação do PDF anotado sem backend

## Stack

- HTML
- CSS
- JavaScript vanilla
- [PDF.js](https://mozilla.github.io/pdf.js/)
- [PDF-lib](https://pdf-lib.js.org/)

## Running Locally

### Opção 1: abrir direto

Você pode abrir o `index.html` diretamente no navegador.

Observação:
- algumas APIs modernas do navegador podem ficar limitadas em `file://`
- o botão `Salvar como` depende do File System Access API e funciona melhor em `localhost`

### Opção 2: servidor local recomendado

```bash
python -m http.server 5500
```

Depois abra:

```text
http://localhost:5500
```

## How To Use

### Marcação de texto

1. Clique em `Caneta`
2. Selecione o texto no PDF

### Marcação por caixa

1. Clique em `Caixa`
2. Arraste sobre a área desejada

### Comentário em texto

1. Clique em `T`
2. Clique no ponto da página onde quer inserir o comentário
3. Digite o texto
4. Ajuste tamanho, negrito e itálico
5. Clique em `OK`

### Salvar PDF anotado

- `Salvar como`: tenta abrir o seletor do sistema para escolher pasta e nome
- `Download PDF`: baixa uma cópia com data e hora no nome

## Privacy

- o PDF é processado localmente no navegador
- não existe backend neste projeto
- as marcações são salvas localmente no navegador via `localStorage`

## Security Notes

- não foram encontrados tokens, segredos, chaves privadas ou credenciais no repositório local durante a revisão
- o projeto depende de CDNs públicos para carregar `pdf.js` e `pdf-lib`
- para uso mais rígido em produção, vale considerar fixar assets localmente e adicionar política de integridade/subresource integrity quando aplicável

## Files

- `index.html`: aplicação completa
- `.gitignore`: exclusões para publicação pública
- `LICENSE`: licença do projeto

## License

MIT
