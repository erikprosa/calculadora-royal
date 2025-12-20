# 🧪 Ambiente de Teste (test-mode)

Este branch é utilizado exclusivamente para o desenvolvimento e validação de novas funcionalidades da **Calculadora Royal**.

## 📂 Estrutura de Arquivos nesta Branch

Para facilitar os testes online sem "sujar" o código principal, a estrutura está organizada assim:

* **`index.html`**: Contém o código do **Pop-up de Alerta**. É o arquivo que o GitHub Pages carrega primeiro para avisar que esta é uma versão de teste. Ele utiliza um *iframe* para exibir o site real.
* **`site.html`**: Contém o **código completo do site** com as novas modificações. É aqui que o desenvolvimento real acontece.
* **`favicon.svg`**: Ícone oficial utilizado tanto no pop-up quanto no site.

---

## 🚀 Fluxo de Publicação (Deploy)

Após validar todas as funcionalidades nesta branch e confirmar que tudo está funcionando corretamente, siga estes passos para mover o código para a produção:

1.  **Limpeza**: Remova o arquivo `index.html` (o arquivo do pop-up).
2.  **Renomeação**: Renomeie o arquivo `site.html` para `index.html`.
3.  **Merge**: Realize o *Merge* ou abra um *Pull Request* da branch `test-mode` para a branch `main`.
4.  **Produção**: Na branch `main`, o novo código passará a ser o oficial e o aviso de teste deixará de existir.

---
⚠️ **Atenção**: Nunca faça merge do arquivo de pop-up para a branch `main`.

---

## 🏁 Como Publicar as Alterações (Deploy para a Main)

Quando os testes estiverem concluídos e validados na branch `test-mode`, escolha uma das formas abaixo para atualizar o site oficial na branch `main`:

### Opção 1: Atualização Manual (Cópia de Código)
Esta é a forma mais segura para evitar que o código do pop-up vá para o site oficial por acidente:
1.  Na branch `test-mode`, abra o arquivo `site.html`, selecione todo o código e copie-o.
2.  Mude para a branch `main` no seletor do GitHub.
3.  Abra o arquivo `index.html` da branch `main`.
4.  Clique no ícone de editar (lápis), apague o conteúdo antigo e cole o novo código.
5.  Salve as alterações clicando em **Commit changes**.

### Opção 2: Uso de Pull Request (Fluxo Profissional)
O GitHub pode automatizar a substituição para você através de um pedido de união:
1.  Vá na aba **Pull Requests** e clique em **New Pull Request**.
2.  Configure a base como `main` e a comparação como `test-mode`.
3.  **Nota:** Para que este processo substitua o arquivo corretamente, o arquivo de código na branch de teste deve ser renomeado para `index.html` antes de iniciar o Pull Request.
4.  Revise as alterações e clique em **Create Pull Request** e, em seguida, em **Merge**.

---
