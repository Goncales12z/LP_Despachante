# Luiz Paulo Despachante: site institucional

Site estático (HTML, CSS e JavaScript puro) para o Luiz Paulo Despachante, credenciado CRDD/RJ 00423, em Imperial de São Cristóvão, Rio de Janeiro. Sem build, sem framework, sem banco de dados.

Terceiro site da série, com identidade própria: paleta carmim + grafite + dourado, tipografia serifada (Playfair Display + Source Sans 3), tom de "escritório de defesa de trânsito" — diferente do preto/amarelo do Bruno e do navy/ciano do Guimarães.

## Estrutura

```
luizpaulo-despachante/
├── index.html                  Página única (todas as seções)
├── README.md                   Este arquivo
├── favicon.ico
├── css/
│   └── style.css               Estilos, tokens de cor e tipografia
├── js/
│   ├── main.js                 Animações, revelações no scroll, cópia de e-mail
│   └── vendor/
│       ├── anime.min.js        anime.js 3.2.2 (licença MIT)
│       └── anime-LICENSE.md
└── img/
    ├── logo.png                Brasão/logo completo (carro de 311x311, fundo vermelho original)
    ├── luiz-paulo.jpg          Foto profissional
    ├── favicon-180.png
    ├── favicon-192.png
    └── favicon-512.png
```

## Como testar no computador

```bash
cd luizpaulo-despachante
python3 -m http.server 8000
# abra http://localhost:8000
```
Abra por um servidor local, não clicando duas vezes no arquivo.

## Como publicar

1. **GitHub Pages:** suba a pasta inteira (mantendo a estrutura) em um repositório, vá em *Settings > Pages* e escolha a branch `main` na raiz.
2. **Domínio próprio:** aponte o domínio para o GitHub Pages depois de publicado.

## O que editar

| O quê | Onde |
|---|---|
| Número do WhatsApp e mensagem padrão | `js/main.js`, objeto `CFG` no topo |
| Textos, serviços, FAQ, avaliações | `index.html` |
| Cores, fontes e espaçamentos | `css/style.css`, bloco `:root` (tokens) |
| Logo e foto | `img/logo.png` e `img/luiz-paulo.jpg` |
| Dados para o Google (nota, endereço, telefone) | `index.html`, bloco `application/ld+json` no `<head>` |

## Confirmar com o cliente antes de publicar

- Se (21) 98227-2788 é o WhatsApp certo (veio do perfil do Google).
- O post dele no Google menciona "mais de 65.897 casos resolvidos" — não usei esse número no site porque parece muito alto para confirmar sem checar com ele; se for correto (ou se o valor real for outro), é só pedir que eu adiciono na seção de credenciais.
- A lista de serviços da frente "Despachante — DETRAN-RJ" é genérica (serviços comuns do setor) — vale confirmar quais ele realmente presta.
- Se ele topa o texto em primeira pessoa ("Sou o Luiz Paulo...").
- Não há e-mail nos dados que você me passou — o site não tem botão de e-mail por isso. Se ele tiver um, é só adicionar (o clique já vem com cópia automática configurada, como no site do Guimarães).
- O número de credencial CRDD/RJ 00423 está em destaque (selo na hero, ribbon e cartão de confiança) — confirme que está correto antes de publicar, já que é a principal prova de legitimidade do site.

## Detalhes de design

- **Hero:** título serifado em duas cores (branco + dourado itálico), foto com filtro vermelho/grafite sutil e selo circular dourado "CRDD/RJ 00423" com efeito de entrada em formato de carimbo girando.
- **Ribbon de credenciais:** faixa escura com 4 indicadores (credencial, nota, especialidade PCD, horário), diferente dos "paineis" dos outros dois sites.
- **Duas frentes:** cards lado a lado para as duas especialidades do Luiz Paulo — despachante geral e recurso de multas/CNH — refletindo a diferenciação real dele, não presente nos outros sites.
- **Como funciona:** três passos simples com numeração serifada grande, sem linha de conexão nem mascote animado.
- **Confiança:** "cartão de credencial" em grafite com borda dourada, diferente da placa do Bruno e do cartão navy do Guimarães.
- **Acessibilidade:** foco visível, `prefers-reduced-motion` respeitado, tema claro/escuro, textos longos com quebra segura.
- **Botão de e-mail (se adicionado):** copia o endereço automaticamente e mostra confirmação visual, útil quando o aparelho não tem cliente de e-mail configurado.

## Dependências externas

- Fontes: Playfair Display e Source Sans 3, via Google Fonts (com fontes de reserva se falharem).
- anime.js 3.2.2 incluído localmente em `js/vendor/` — não depende de CDN.

## Créditos

Logo e foto: Luiz Paulo Despachante. anime.js: Julian Garnier, licença MIT.
