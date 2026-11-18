# Diário de bordo · André Carvalho

Portfólio em uma única página com tema de viagem espacial. Cada repositório público do GitHub vira um planeta.

- **Abertura:** salto para o hiperespaço e nome que se decodifica na tela
- **Abertura em perspectiva:** texto em rolagem no estilo de uma saga espacial
- **Tripulante:** holograma com a foto do GitHub, terminal digitando e linguagens em órbita
- **Missões:** a câmera viaja de planeta em planeta e a mira trava em cada repositório
- **Diário de bordo:** todos os repositórios, com filtro por linguagem
- **Transmissão:** radar com os canais de contato e botão de sabre de luz

Feito com HTML, CSS e JavaScript puro, mais [three.js](https://threejs.org/) r128 via CDN. Não precisa de build.

## Como editar

Todo o conteúdo fica no objeto `CONFIG`, no começo do `<script>` em `index.html`:

| Campo | O que é |
| --- | --- |
| `githubUser` | usuário do GitHub; perfil e repositórios são puxados sozinhos |
| `notes` | descrição de cada repositório (`"nome-do-repo": "texto"`) |
| `hide` | repositórios que não devem aparecer |
| `roles`, `intro`, `about` | textos da abertura e do terminal |
| `saga` | texto de abertura em perspectiva |
| `contacts` | e-mail e redes |
| `fallback` | cópia dos dados usada se a API do GitHub não responder |

Paleta (variáveis em `:root`): `#00223F #154674 #3470A6 #4F8BB8 #70ADD3 #A0CAE3`.

## Rodar localmente

```bash
npx http-server -p 5174 -c-1 .
```

## Publicar no GitHub Pages

Em **Settings → Pages**, escolha **Deploy from a branch**, depois `main` e `/ (root)`.
