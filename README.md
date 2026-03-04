## Sorteio TI

Este projeto tem como finalidade gerar um código de sorteio quando colaboradores da empresa respondem a uma pesquisa no Microsoft Forms.

O acesso ao projeto está disponível em https://dibra-dev.github.io/Sorteio-TI/.

### Atualizações e Deploy

Para realizar atualizações, altere o que for necessário e efetue o commit na branch **main** (ou master). A publicação é atualizada automaticamente via GitHub Pages após o commit.

### Gestão de Novas Pesquisas (Ciclos)

O script utiliza o `localStorage` do navegador para garantir que cada colaborador gere apenas um código por campanha. Para iniciar uma nova pesquisa e permitir que os usuários gerem novos códigos, siga o procedimento abaixo:

1. No arquivo `index.html`, localize a variável ou chave utilizada no `localStorage.getItem` e `localStorage.setItem`.
2. Realize um **incremento ou alteração no nome da chave** (ex: mudar de `codigoParticipacao` para `codigoParticipacao_2`).
3. Ao realizar o commit dessa alteração, o navegador identificará que não existe um código salvo para essa nova chave e permitirá uma nova geração/envio para a planilha.****
