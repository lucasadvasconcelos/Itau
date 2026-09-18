# Banco digital — protótipo de app mobile

Protótipo de interface de banco digital para celular, feito em **HTML, CSS e JavaScript puros**, sem dependências e sem build. Um único arquivo: `index.html`.

## O que tem

- **Extrato** — saldo, banner de contas conectadas, abas Histórico/Agendados, filtros, totais de entradas e saídas e a lista de lançamentos por dia.
- **Início** — saldo, atalhos de Pix, pagamento, depósito e transferência, resumo do mês e últimos lançamentos.
- **Cartões** — cartão virtual, congelar cartão, compras online e ações da conta.
- **Perfil** — chaves Pix, dados pessoais, avisos, ajuda e sair.

## Navegação por deslize

- Arraste na horizontal para trocar de tela: Início → Extrato → Cartões → Perfil.
- Dentro do Extrato, deslize entre **Histórico** e **Agendados**. Ao chegar na borda, o gesto continua para a próxima tela.
- A rolagem vertical continua normal: o eixo do gesto é travado no primeiro movimento.
- No computador dá para arrastar com o mouse ou usar as setas ← e →.

## Outras interações

- O ícone de olho oculta e mostra todos os valores de uma vez.
- Os filtros (Data, Transação, Categoria) alternam entre marcado e desmarcado.
- O botão "Congelar cartão" deixa o cartão cinza.

## Como rodar

Abra o `index.html` no navegador. Só isso. Se quiser servir localmente:

```bash
python3 -m http.server 8000
# depois acesse http://localhost:8000
```

## Publicar no GitHub Pages

1. Crie um repositório e envie os arquivos:

```bash
git init
git add .
git commit -m "Protótipo de app de banco digital"
git branch -M main
git remote add origin https://github.com/SEU-USUARIO/SEU-REPO.git
git push -u origin main
```

2. No repositório, vá em **Settings → Pages**.
3. Em *Source*, escolha **Deploy from a branch**, branch `main` e pasta `/ (root)`.
4. Salve. Em um ou dois minutos o app fica no ar em `https://SEU-USUARIO.github.io/SEU-REPO/`.

No celular, dá para abrir esse endereço e usar "Adicionar à tela de início" para rodar em tela cheia, sem a barra do navegador.

## Estrutura

```
.
├── index.html   # app inteiro: marcação, estilos e scripts
└── README.md
```

## Observação

É um protótipo de interface. Os dados são estáticos, não há back-end, autenticação nem transação real.

## Licença

MIT.
