[English](./README.md) | [Português (Brasil)](./README.pt-BR.md)

<div align="center">

# PDF Dark Mode

Leitor de PDF em modo escuro com marcações, comentários, busca, zoom, cópia de print e exportação do PDF anotado — tudo no navegador.

![Status](https://img.shields.io/badge/status-active-2ea44f?style=for-the-badge)
![Licença](https://img.shields.io/badge/license-MIT-2563eb?style=for-the-badge)
![Feito com](https://img.shields.io/badge/made%20with-Vanilla%20JS-f7df1e?style=for-the-badge)
![Client-side](https://img.shields.io/badge/runtime-browser-111827?style=for-the-badge)

[Baixar `index.html`](https://github.com/brunoherrman/pdf-dark-mode/raw/main/index.html) • [Abrir arquivo no repositório](./index.html) • [English](./README.md)

</div>

## Visão Geral

PDF Dark Mode é um leitor leve, client-side, pensado para leitura confortável por longos períodos. Ele abre PDFs locais, aplica presets escuros, suporta anotações e comentários em texto com estilo, e exporta o arquivo anotado sem depender de backend.

## Por Que Ele Se Destaca

- Totalmente client-side: sem servidor obrigatório
- Presets escuros para diferentes preferências visuais
- Fluxo rápido para marcação, caixa e comentário em texto
- Busca com destaque visível do resultado atual
- Desfazer e refazer para editar anotações com mais segurança

## Tabela de Recursos

| Recurso | Detalhes |
|---|---|
| Presets escuros | `Warm`, `Classic`, `Blue` |
| Navegação | Miniaturas, ir para página, zoom, ajustar largura, `100%` |
| Anotações | Marcação de texto, caixa e comentários em texto |
| Busca | Navegação entre ocorrências com foco visual no resultado atual |
| Exportação | Salvar PDF anotado localmente ou baixar cópia com timestamp |
| Utilitários | Copiar página atual como imagem, persistência local via `localStorage` |

## Início Rápido

### Opção 1: Abrir direto

Abra o `index.html` no navegador.

Observações:
- algumas APIs do navegador ficam limitadas em `file://`
- `Salvar como` funciona melhor quando servido por `localhost`

### Opção 2: Servidor local recomendado

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
- `Download PDF`: baixa uma cópia com data e hora no nome

## Stack

- HTML
- CSS
- JavaScript vanilla
- [PDF.js](https://mozilla.github.io/pdf.js/)
- [PDF-lib](https://pdf-lib.js.org/)

## Privacidade

- os PDFs são processados localmente no navegador
- não existe backend neste projeto
- as anotações são salvas localmente via `localStorage`

## Notas de Segurança

- não foram encontrados tokens, segredos, chaves privadas ou credenciais no repositório durante a revisão
- o projeto depende atualmente de CDNs públicos para `pdf.js` e `pdf-lib`
- para uso mais rígido em produção, vale considerar versionar esses assets localmente e aplicar controles de integridade quando possível

## Limitações Conhecidas

- `Salvar como` depende do suporte do navegador ao File System Access API
- uso direto por `file://` pode limitar algumas capacidades do navegador
- os CDNs são necessários, a menos que as bibliotecas sejam empacotadas localmente

## Estrutura do Repositório

- `index.html`: aplicação completa
- `README.md`: documentação em inglês
- `README.pt-BR.md`: documentação em português do Brasil
- `.gitignore`: exclusões para repositório público
- `LICENSE`: licença do projeto

## Descrição Recomendada Para o GitHub

Dark-mode PDF reader with highlights, comments, search, zoom, print copy, and annotated PDF export — fully client-side.

## Licença

MIT
