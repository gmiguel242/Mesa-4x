# Mesa 4X — Teste técnico frontend

Entrega estática para o teste de HTML Email e Landing Page da **Mesa 4X — Imersão de Marketing e Vendas**.

## Estrutura

```text
README.md
email/
└── index.html
lp/
├── index.html
└── styles.css
```

## Como abrir localmente

Abra `email/index.html` ou `lp/index.html` diretamente no navegador. Se preferir servir os arquivos por HTTP, execute `python -m http.server 8000` na raiz e abra `http://localhost:8000/lp/` ou `http://localhost:8000/email/`.

## Decisões técnicas

### Email

- Layout construído com tabelas de apresentação, container de 600 px e estilos essenciais inline.
- Preheader oculto no corpo, mas disponível na prévia da mensagem.
- CTA com tabela e fallback VML para Outlook clássico no Windows.
- Media query para telas estreitas e ajustes básicos para dark mode. O conteúdo não depende de imagens externas.
- Endereço, depoimentos e links são demonstrativos; substitua os destinos `example.com` antes de uma campanha real.

### Landing page

- HTML semântico com CSS separado, responsivo e sem frameworks ou JavaScript.
- Tokens de cor, tipografia, espaçamento e borda centralizados em `:root` (desafio extra de design system mínimo).
- CTA principal navega para os ingressos. Os detalhes dos três passos podem ser revelados com controles nativos e CSS.
- Foco visível, link para pular ao conteúdo, hierarquia de títulos e suporte a `prefers-reduced-motion`.

## Compatibilidade e limitações

O email foi escrito pensando em Gmail, Outlook desktop, Apple Mail e aplicativos móveis. Clientes de email podem ignorar media queries, alterar cores no dark mode ou reescrever estilos; a renderização final deve ser conferida nos clientes de destino. O botão VML melhora o suporte no Outlook clássico, mas não garante aparência idêntica em todos os aplicativos.

A landing page pode ser conferida em larguras desktop e mobile e com navegação por teclado. Os CTAs de ingressos e os links do email usam destinos demonstrativos e não processam inscrição ou pagamento.

## O que eu faria com mais tempo

1. Validaria o email em Gmail, Outlook clássico e Apple Mail, incluindo dark mode e bloqueio de imagens.
2. Conferiria o preheader e o botão em ferramentas de pré-visualização de email.
3. Faria uma auditoria de contraste e navegação por teclado em diferentes larguras.
4. Substituiria links, endereço, preços e depoimentos fictícios pelos dados aprovados da campanha.
