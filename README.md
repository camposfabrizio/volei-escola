# Escola do Vôlei — Landing Page "O Código do Salto Vertical"

Página de vendas estática (HTML + CSS + JS, sem build) pronta para hospedar no **GitHub Pages**.

## 📁 Estrutura

```
volei-escola/
├── index.html          ← a página (tudo nela: HTML, CSS e JS)
├── README.md           ← este arquivo
├── .nojekyll           ← evita o GitHub processar como Jekyll
└── assets/
    ├── logo.webp        / logo.png   ← logomarca
    ├── favicon.png                   ← ícone da aba
    ├── atleta-quadra.webp            ← herói (atacante de quadra)
    ├── atleta-praia-m.webp           ← seção "para quem é"
    ├── atleta-praia-f.webp           ← seção "para quem é"
    └── planilha.webp                 ← mockup do Painel do Saltador
```

## 🚀 Como publicar no GitHub Pages

1. Crie um repositório no GitHub (ex.: `volei-escola`).
2. Suba **todos os arquivos desta pasta** (mantendo a pasta `assets/`).
3. No repositório: **Settings → Pages**.
4. Em **Source**, escolha o branch `main` e a pasta `/ (root)`. Salve.
5. Aguarde 1–2 minutos. Seu site fica em:
   `https://SEU-USUARIO.github.io/volei-escola/`

> Dica: para usar um domínio próprio (ex.: `volei.seudominio.com.br`), adicione-o em
> **Settings → Pages → Custom domain** e configure o CNAME no seu provedor de DNS.

## ✏️ O que você pode trocar facilmente

| O quê | Onde | Como |
|------|------|------|
| **Link do checkout (Hotmart)** | `index.html`, perto do final, no bloco `<script>` | Variável `const CHECKOUT_URL = "..."`. Já está com o seu link. |
| **Pixel da Meta** | `index.html`, dentro do `<head>` (bloco "META PIXEL") | Já configurado com o ID `1379536914036063`. |
| **Preço** | `index.html`, seção `id="oferta"` (classe `.price`) e a barra fixa `.sticky-cta` | Troque `R$ 47`, o `de R$ 97` e o parcelamento. |
| **Depoimentos** | seção `class="proof"` | Substitua os textos marcados como `[DEPOIMENTO]`, nomes, posições e o ganho em cm. |
| **Imagens** | pasta `assets/` | Troque mantendo os mesmos nomes de arquivo. |

## 🎯 Rastreamento (Pixel + Hotmart)

- O **Meta Pixel** já dispara:
  - `PageView` ao abrir a página.
  - `InitiateCheckout` ao clicar em qualquer botão que leva ao checkout.
  - `ClickOferta` (evento personalizado) nos botões internos que rolam até a oferta.
- O evento **`Purchase`** (compra concluída) deve ser configurado **dentro da Hotmart**,
  na integração de Pixel da Meta (a Hotmart dispara o Purchase no fim do checkout).
  Use o **mesmo ID de Pixel** (`1379536914036063`) lá para os dados baterem.

## ⚖️ Observações

- O texto do rodapé traz o aviso de que é material educativo e que a Hotmart é apenas a
  plataforma de pagamento. Mantenha esse aviso por conformidade.
- Os depoimentos atuais são **ilustrativos** — troque por relatos reais antes de anunciar.
- A página é responsiva, leve (imagens em WebP) e respeita `prefers-reduced-motion`.
