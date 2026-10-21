# carlosjr81.github.io — a raiz do domínio do Treino Livre

Este repositório publica a raiz do domínio (`https://carlosjr81.github.io/`). A cópia de referência fica na pasta `dominio/` do repositório Treino-Livre.

| Arquivo | Para quê |
|---|---|
| `.well-known/assetlinks.json` | Diz ao Chrome que o app Android `br.com.treinolivre.app`, assinado com esta chave, é do mesmo dono do site. `handle_all_urls`: o app abre em tela cheia, **sem a barra de endereço**. `use_as_origin`: o app pode falar com a página pelo canal de mensagens do TWA (é por onde passa a imagem dos óculos) |
| `.nojekyll` | Sem ele, o GitHub Pages ignora pastas que começam com ponto, e o `.well-known` nunca seria publicado |
| `index.html` | Quem abre `carlosjr81.github.io` cai no Treino Livre |

**A impressão digital** sai do passo "Impressão digital da chave" do workflow
App Android. Se a chave do APK mudar, o número muda, e este arquivo tem de ser
atualizado nos dois lugares (aqui e no repositório do domínio). Dá para listar
duas impressões ao mesmo tempo durante uma troca.

Conferir depois de publicar:
https://digitalassetlinks.googleapis.com/v1/statements:list?source.web.site=https://carlosjr81.github.io&relation=delegate_permission/common.handle_all_urls
