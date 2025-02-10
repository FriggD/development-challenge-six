# Documentação do Projeto:

## Funcionalidades do Site:

1. Header com links para as respectivas seções;
2. Página dividida em seções com textos explicativos, imagens e/ou vídeos demonstrativos;
3. Botão para solicitação de teste grátis com um formulário;
4. Botão para acessar a área restrita do usuário;
5. Botões para acessar a loja de aplicativos Android e Iphone;
6. Formulário de contato;
7. Footer com informações da empresa, redes sociais e selos como ICP Brasil, Anvisa, HIPAA e AWS.

## Bugs Identificados

1. **Link de Navegação RIS:**
   - **Dado** que um usuário utiliza o menu de navegação,
   - **Quando** ele clica no link "RIS" a partir da seção "Home",
   - **Então** ele é redirecionado para a seção correta, mas o foco do botão de navegação permanece no link "Home".

2. **Link de Navegação PACS:**
   - **Dado** que um usuário utiliza o menu de navegação,
   - **Quando** ele clica no link "PACS" a partir da seção "Home",
   - **Então** ele é redirecionado para a seção correta, mas o foco do botão de navegação é direcionado para o "RIS".

3. **Link de Navegação Portal:**
   - **Dado** que um usuário utiliza o menu de navegação,
   - **Quando** ele clica no link "Portal" a partir da seção "Home",
   - **Então** ele não é redirecionado para a seção correta.

4. **Link de Navegação Planos:**
   - **Dado** que um usuário utiliza o menu de navegação,
   - **Quando** ele clica no link "Planos" a partir da seção "Home",
   - **Então** ele é redirecionado para a seção "PACS", mas o foco do botão de navegação é direcionado para o "RIS".

5. **Link de Navegação Contato:**
   - **Dado** que um usuário utiliza o menu de navegação,
   - **Quando** ele clica no link "Planos" a partir da seção "Home",
   - **Então** ele é redirecionado para a seção correta, mas o foco do botão de navegação é direcionado para o "Planos".

6. **Link do footer não redireciona corretamente:**
   - **Dado** que um usuário segue até o footer da tela,
   - **Quando** ele clica no ícone da rede social "X",
   - **Então** ele é redirecionado para a página de outra rede social (Facebook).

7. **Multiplos IDs repetidos:**
   - **Dado** que um usuário acessa a página inicial do site,
   - **Quando** o menu de navegação e as seções da página são renderizados,
   - **Então** múltiplos elementos compartilham o mesmo ID,
   - **E** isso pode causar comportamentos inesperados, como:
     - A navegação não rolar corretamente para a seção desejada,
     - A perda de foco nos botões do menu de navegação,
     - Dificuldade para usuários com deficiência visual utilizarem leitores de tela,
     - Scripts JavaScript retornando elementos incorretos devido à ambiguidade dos IDs.

8. **Armazenamento de informações desnecessárias no LocalStorage:**
   - **Dado** que um usuário acessa o site,
   - **Quando** a página é carregada ou o usuário navega entre seções,
   - **Então** são armazenadas informações irrelevantes no local storage.

9. **Botão causando loop infinito:**
    - **Dado** que o usuário deseja acessar sua conta,
    - **Quando** clica em "Entrar", tanto no header da página quanto no modal de "Testar gratis",
    - **Então** o sistema executa uma função javascript que entra em loop infinito.

10. **Link de Navegação Idioma (Inglês):**
    - **Dado** que um usuário está na página inicial do site e visualiza o idioma em português,
    - **Quando** ele clica na opção "Inglês" no menu de seleção de idiomas,
    - **Então** o idioma do site não é alterado para inglês, mas é alterado para espanhol.

11. **Exibição de Textos em Inglês Independente do Idioma Escolhido:**
    - **Dado** que um usuário está na página inicial do site e escolheu o idioma desejado,
    - **Quando** ele navega pelas seções do site,
    - **Então** ele encontra textos em inglês.

12. **Erros e Warnings Excessivos no Console:**
    - **Dado** que um usuário acessa o site ou interage com elementos da interface,
    - **Quando** a página é carregada ou o usuário realiza ações como clicar em botões ou navegar entre seções,
    - **Então** diversos erros e warnings são exibidos no Console.Log, impactando a experiência de desenvolvimento e depuração do site.

13. **Mensagens de Obrigatoriedade de Campos Não Claras nos Formulários "Testar grátis" e "Contato":**
    - **Dado** que um usuário preenche um formulário no site,
    - **Quando** ele deixa um ou mais campos obrigatórios em branco e tenta enviar o formulário,
    - **Então** as mensagens de erro exibidas não são claras ou não especificam corretamente quais campos precisam ser preenchidos,

14. **Impossibilidade de Reenviar o Formulário "Testar grátis":**
    - **Dado** que um usuário preenche um formulário no site pela segunda vez,
    - **Quando** ele clica para enviar o formulário e fecha o modal,
    - **Então** o botão de envio não é habilitado ao abrir novamente o modal.

15. **Formulários "Testar grátis" e "Contato" retornam sucesso sem conexão com a internet:**
    - **Dado** que um usuário preenche um formulário e está sem conexão com a internet,
    - **Quando** ele clica para enviar o formulário,
    - **Então** há mensagem de sucesso no envio.

16. **Formulários "Testar grátis" e "Contato" retornam sucesso com nome invalido:**
    - **Dado** que um usuário preenche o campo 'nome' com espaço em branco ou numero,
    - **Quando** ele clica para enviar o formulário,
    - **Então** há mensagem de sucesso no envio.

17. **Formulários "Testar grátis" e "Contato" retornam sucesso com telefone invalido:**
    - **Dado** que um usuário insere um número no campo "telefone" com uma quantidade de dígitos inválida,
    - **Quando** ele clica para enviar o formulário,
    - **Então** há mensagem de sucesso no envio.

18. **Título "Abrir FAQ" Incoerente com Estado Inicial do Dropdown:**
    - **Dado** que um usuário acessa a seção de FAQ pelo desktop,
    - **Quando** o dropdown do FAQ já está expandido por padrão,
    - **Então** o título do botão exibe "Abrir FAQ" de forma incoerente.

19. **Faixa com logos de clientes está móvel:**
    - **Dado** que um usuário acessa a seção onde se encontram os logos de clientes,
    - **Quando** o usuário clica e arrasta a faixa verticalmente,
    - **Então** os logos se deslocam de forma indevida, causando cortes em algumas imagens.

20. **Ausência de texto alternativo nas imagens da seção de clientes:**
    - **Dado** que um usuário utiliza ferramentas de acessibilidade visual,
    - **Quando** acessa a seção de imagens de clientes,
    - **Então** as imagens não possuem texto alternativo, impedindo a correta interpretação pelo leitor de tela.

21. **Imagem de disposítivo incompatível com o dropdown selecionado:**
    - **Dado** que um usuário acessa a seção de dispositivos,
    - **Quando** o usuário clica na opção "Ou até mesmo na sua SmartTV",
    - **Então** a imagem ao lado remete à seção "Com seu Android ou Iphone".

22. **Ajustes de pontuação em paragrafos:**
    - **Dado** que a frase apresenta múltiplas informações na seção "workstation DICOM",
    - **Quando** a estrutura for analisada,
    - **Então** deve-se garantir o uso adequado de vírgulas e pausas para melhorar a compreensão.

23. **Exibição de informações desnecessárias no Console.Log:**
    - **Dado** que um usuário acessa o site,
    - **Quando** a página é carregada ou o usuário interage com elementos da interface,
    - **Então** mensagens desnecessárias são exibidas no Console.Log.

24. **Botão de scroll em cima de modal em versão mobile:**
    - **Dado** que um usuário acessa o site pelo celular,
    - **Quando** o usuário realiza scroll a tela para baixo e abre o modal de "Testar gratis",
    - **Então** o botão para subir até o topo aparece em cima do modal, permitindo rolar a tela por baixo do modal.

25. **Acessibilidade da mudança de idioma:**
    - **Dado** que um usuário estrangeiro acessa o site,
    - **Quando** há a necessidade de troca de idioma,
    - **Então** é necessário ir até o final da página para realizar a troca de idioma, o que pode gerar dificuldades de acessibilidade para usuários que dependem de navegação rápida e eficiente.

26. **Quebra de layout em algumas dimensões de tela:**
    - **Dado** que um usuário acessa o site,
    - **Quando** está em uma tela de dimensão menor que 1340px e maior que 640px,
    - **Então** botões, videos e imagens se amontoam, quebrando o layout do site.