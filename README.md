# Otávio A. R. da Cruz — Academic website

Site acadêmico em inglês, estático e compatível com GitHub Pages. Não exige instalação, build, JavaScript ou serviços externos. Os caminhos relativos permitem publicar tanto em `usuario.github.io` quanto em `usuario.github.io/repositorio/`.

## Visualizar localmente

Nesta pasta:

```sh
python3 -m http.server 8000
```

Abra http://localhost:8000. Para encerrar, pressione Ctrl+C. Também é possível abrir `index.html` diretamente no navegador.

## Publicar no GitHub Pages

1. Crie um repositório no GitHub. Para usar o endereço principal, nomeie-o `SEU_USUARIO.github.io`, com o nome de usuário em minúsculas. Para um subdiretório, escolha outro nome. No plano gratuito, use um repositório público.
2. Envie `index.html`, `styles.css`, `.nojekyll`, `.gitignore`, `README.md` e as pastas `assets/` e `resources/` para a branch `main`. Mantenha `index.html` na raiz. Inclua os arquivos ocultos indicados; não envie pastas locais de ferramentas ou credenciais.
3. Em **Settings → Pages → Build and deployment**, escolha **Deploy from a branch**, selecione **main** e **/ (root)** e salve.
4. Aguarde o endereço publicado aparecer em **Settings → Pages**. A publicação pode levar alguns minutos.

O arquivo `.nojekyll` permite servir os arquivos estáticos diretamente. Não é necessário configurar GitHub Actions manualmente.

Documentação: https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site

O projeto ainda não está publicado. A pasta `.git` presente neste ambiente está vazia; não há repositório Git funcional nem destino remoto configurado.

## Arquivos

- `index.html`: apresentação, interesses de pesquisa, três publicações de destaque, trajetória, objetivos, materiais e contato.
- `styles.css`: cores, navegação lateral, layout responsivo, enquadramento da foto e impressão.
- `assets/photo.JPG`: foto atual. O nome é sensível a maiúsculas e minúsculas.
- `assets/favicon.svg`: ícone OC.
- `assets/google-scholar.svg`: ícone junto ao link do Google Scholar.
- `resources/`: pasta para futuros materiais.
- `script.js`: arquivo legado sem funcionalidade, não carregado pela página; não precisa ser publicado.

## Foto

A foto atual já está vinculada a `assets/photo.JPG`. Ao substituir o arquivo, preserve esse nome ou ajuste o atributo `src` em `index.html`. Atualize também o texto `alt` se necessário.

O CSS enquadra a foto sem modificar o original: `.photo-frame` define o espaço visível; `.profile-photo` usa `transform: scale(1.8)` para ampliar e `transform-origin: 50% 25%` para posicionar o zoom. O arquivo original tem aproximadamente 1,9 MB; uma versão reduzida pode melhorar o carregamento em conexões lentas. Evite publicar metadados pessoais na foto.

## Publicações

A página contém três destaques escolhidos pelo autor. Para adicionar outro, copie um bloco `<article class="publication">` em `index.html` e atualize ano, título, autores, veículo e link. Mantenha os títulos dos artigos no idioma original e confirme os dados na fonte.

O link do Google Scholar abre o perfil ordenado por data. Não há sincronização automática. O Google Scholar não oferece integração pública oficial para sincronização e informa que não fornece acesso em massa: https://scholar.google.com/intl/en/scholar/help.html.

## Apresentações e materiais

Salve os arquivos em `resources/`, por exemplo `resources/presentation.pdf`. Na seção `Resources` do `index.html`, substitua o aviso por uma lista de links. Há um exemplo comentado no HTML. Envie os arquivos novos ao GitHub junto com a atualização da página.

## Conteúdo e fontes

Dados acadêmicos baseados no Lattes fornecido pelo autor, atualizado em 07/04/2026, com ajustes posteriores solicitados pelo autor. LinkedIn e Scholar não puderam ser consultados integralmente de forma automática. Os três destaques têm links para IEEE Xplore ou DOI. A organização usa https://pappas-nikolaos.github.io/ como referência.

Contato público autorizado: otavio.augusto@ufrgs.br. Os links para Lattes e ORCID e o PDF do currículo não são publicados na página. O site não utiliza cookies, analytics, fontes remotas ou dependências de execução.
