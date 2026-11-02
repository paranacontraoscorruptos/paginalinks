# Movimento Paraná Contra os Corruptos

Página de links oficiais em português, responsiva e sem etapa de compilação. O HTML, os estilos, os ícones SVG e o JavaScript estão reunidos em `index.html`.

## Publicar no GitHub Pages

1. No repositório, abra **Settings → Pages**.
2. Em **Build and deployment**, selecione **Deploy from a branch**.
3. Escolha a branch **main** e a pasta **/ (root)** e salve.
4. Aguarde a publicação. O endereço padrão será `https://paranacontraoscorruptos.github.io/paginalinks/`.

A página também pode ser hospedada em qualquer servidor estático: envie `index.html`, `.nojekyll` e `banner.png`. Não exige Node.js, banco de dados, chaves ou instalação de pacotes. As fontes do Google são opcionais; há fontes locais de reserva.

## Banner

O banner original exibido na conversa não ficou disponível como arquivo no ambiente. O arquivo `banner.png` contém uma arte de reserva criada com as cores e a identidade cívica do movimento. Essa arte também está incorporada ao HTML em SVG, para continuar aparecendo caso a imagem externa falhe. Ela não é a imagem original enviada na conversa.

Para usar o banner original, substitua a arte de reserva pela imagem original, mantendo o nome **`banner.png`**, na mesma pasta de `index.html`. A página a exibirá automaticamente. Caso prefira outro nome ou formato, altere `src="banner.png"` no elemento `id="hero-banner"`.

Para experimentar uma imagem local sem alterar a publicação, acrescente `?editar=1` ao endereço da página e abra **Visualizar outro banner**, no final da página. Essa prévia é temporária, fica apenas no navegador e não envia o arquivo a nenhum servidor. O envio definitivo da imagem deve ser feito ao repositório.

## Desenvolvimento local

Use o checkout existente. Cada tarefa na nuvem já é isolada; não é necessário criar um Git worktree.

```sh
cd /workspace/paginalinks
python3 -m http.server 8000 --bind 127.0.0.1
```

Abra o endereço local do servidor em um navegador. Para encerrar, use `Ctrl+C`. Esse servidor é apenas para desenvolvimento; a hospedagem de produção deve servir os arquivos estáticos via HTTPS.

## Recursos

- Nove destinos oficiais, utilizáveis mesmo sem JavaScript.
- Botão de cópia separado de cada link, com confirmação somente após sucesso.
- Compartilhamento nativo, cópia como alternativa e envio pelo WhatsApp.
- Navegação por teclado, foco visível, mensagem de estado acessível e alternativa manual quando a cópia é negada.
- Fundo estático; animações de interface pausáveis e respeito à preferência de movimento reduzido.
- Título, rodapé e descrições em português brasileiro.

A **Página no Facebook** usa o endereço de compartilhamento fornecido; o **Grupo no Facebook** aponta para `https://www.facebook.com/groups/518450788618734`. Ao atualizar qualquer destino, altere o `href` do link e o `data-url` do respectivo botão de copiar.

## Validação

Antes de publicar alterações, confira os nove destinos, copiar/compartilhar, a navegação por teclado, o banner e o layout em telas estreitas. Os botões de copiar e compartilhar dependem do suporte e das permissões do navegador; quando necessário, a página apresenta um campo para cópia manual. O ano do rodapé é atualizado automaticamente quando o JavaScript está ativo.
