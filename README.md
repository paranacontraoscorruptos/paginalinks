# Movimento Paraná Contra os Corruptos

Página de links oficiais em português, responsiva e sem etapa de compilação. O HTML, os estilos, os ícones SVG e o JavaScript estão reunidos em `index.html`.

## Publicar no GitHub Pages

1. No repositório, abra **Settings → Pages**.
2. Em **Build and deployment**, selecione **Deploy from a branch**.
3. Escolha a branch **main** e a pasta **/ (root)** e salve.
4. Aguarde a publicação. O endereço padrão será `https://paranacontraoscorruptos.github.io/paginalinks/`.

A página também pode ser hospedada em qualquer servidor estático: envie `index.html` e `.nojekyll`. Não exige Node.js, banco de dados, chaves ou instalação de pacotes. As fontes do Google são opcionais; há fontes locais de reserva.

## Banner e animações

O banner é uma composição em HTML e SVG incorporada ao `index.html`: a bandeira do Brasil se forma por camadas, a balança da justiça é desenhada e o texto surge com profundidade. Não depende de imagens externas, vídeo ou biblioteca de animação.

O botão **Ver animação** repete a formação do banner. **Pausar animações**, no topo, interrompe os movimentos da página. A preferência de movimento reduzido do dispositivo é respeitada automaticamente.

Títulos, cards e textos do rodapé aparecem quando entram na tela, usando `IntersectionObserver`. As entradas são escalonadas e executadas uma vez por visita. A navegação por teclado revela imediatamente o elemento focado; sem JavaScript ou com movimento reduzido, todo o conteúdo permanece visível.

O fundo usa uma arte estática com losangos, estrelas, faixas verdes e amarelas e símbolos de justiça. Os textos do banner são HTML selecionável, ajustado para celular.

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
- Bandeira animada no banner, títulos com entrada de profundidade e cards revelados durante a rolagem.
- Fundo patriótico estático; animações pausáveis e respeito à preferência de movimento reduzido.
- Chamada em destaque e rodapé ampliado com acabamento verde e amarelo.
- Título, rodapé e descrições em português brasileiro.

A **Página no Facebook** usa o endereço de compartilhamento fornecido; o **Grupo no Facebook** aponta para `https://www.facebook.com/groups/518450788618734`. Ao atualizar qualquer destino, altere o `href` do link e o `data-url` do respectivo botão de copiar.

## Validação

Antes de publicar alterações, confira os nove destinos, copiar/compartilhar, a navegação por teclado, o banner e o layout em telas estreitas. Os botões de copiar e compartilhar dependem do suporte e das permissões do navegador; quando necessário, a página apresenta um campo para cópia manual. O ano do rodapé é atualizado automaticamente quando o JavaScript está ativo.
