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
