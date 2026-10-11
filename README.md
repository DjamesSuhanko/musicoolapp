# Musicool · páginas públicas Clave Sol

Site independente do código do aplicativo, preparado para **musicool.clavesol.com.br**, com a identidade visual do Clave Sol e o ícone existente do Musicool.

## Conteúdo

- `content/index.md`: página inicial provisória, com `noindex,follow` até receber o conteúdo definitivo.
- `content/privacy.md`: texto da política existente em `Musicool/Musicool/docs/privacy.html`, preservado sem alterações.
- `/privacidade/` e `/privacy.html`: política pública.
- `/contato/`: contato do desenvolvedor.
- `templates/base.html` e `assets/style.css`: layout compartilhado.

Este repositório não contém o código, chaves de assinatura ou arquivos de compilação do aplicativo. A política deve ser revisada pelo proprietário quando o tratamento de dados mudar. As fontes do site são carregadas do Google Fonts, como no site do MyLuthier.

## Prévia local

```bash
python3 -m pip install -r requirements.txt
python3 build.py
python3 scripts/check_site.py
python3 -m http.server 8080 --directory dist
```

## Publicação

GitHub Pages com Source **GitHub Actions**, workflow **Publicar Musicool**, domínio **musicool.clavesol.com.br**. Cada push em `main` publica apenas `dist/`.

No DNS: CNAME `musicool` apontando para `djamessuhanko.github.io`, inicialmente sem proxy. Habilitar Enforce HTTPS no Pages quando o certificado estiver disponível.

URL da política: https://musicool.clavesol.com.br/privacidade/

Para editar a página inicial, altere `content/index.md`; ao concluir o conteúdo definitivo, ajuste a descrição em `build.py` e remova o `noindex` da entrada inicial em `pages`.

## Editar conteúdo

Consulte [EDITAR-CONTEUDO.md](EDITAR-CONTEUDO.md). Apresentação, política e contato são editados em Markdown, dentro de `content/`.

Para escrever a descrição completa do aplicativo, edite **`content/apresentacao.md`**. O conteúdo aparece entre o topo e os blocos de privacidade/contato, sem alterar essas áreas.
