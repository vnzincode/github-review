# github-review

#### Comandos Git e Conceitos

**`git fetch`**
- Este comando busca as últimas atualizações do repositório remoto, mas não as integra no seu repositório local. É útil para verificar as mudanças antes de aplicá-las.

**`git pull`**
- `git pull` é usado para buscar e integrar (merge) as atualizações do repositório remoto no seu ramo atual. Ele é um atalho para `git fetch` seguido de `git merge`.

**`git pull --rebase`**
- `git pull --rebase` é uma variação do git pull que busca e integra as atualizações do repositório remoto no seu ramo atual, mas ao invés de fazer um merge, ele aplica um rebase.

**`git checkout main`**
- Este comando muda o seu ramo atual para o ramo `main`. Se você estiver em um ramo diferente e quiser voltar para o ramo principal, use este comando.

**`git checkout -B feature-branch`**
- Cria e muda para um novo ramo chamado `feature-branch`. Se o ramo já existir, ele será redefinido para o ponto de partida atual.

**`git commit -m "Feature comment"`**
- `git commit` salva suas mudanças no histórico do repositório com uma mensagem descritiva. A flag `-m` permite adicionar uma mensagem de commit diretamente.

**`git push origin feature-branch`**
- Envia suas mudanças do ramo `feature-branch` para o repositório remoto.

**Pull Requests**
- Um Pull Request (PR) é uma solicitação para que suas mudanças no código sejam revisadas e potencialmente mescladas no ramo principal ou outro ramo. É uma prática comum em colaboração de equipes, permitindo revisão de código e discussões antes da integração.

#### Terminal do VSCode
O terminal integrado do VSCode permite executar comandos Git diretamente no editor. Isso facilita a navegação e a execução de comandos sem a necessidade de alternar entre diferentes janelas ou aplicativos.

---

### Simulação Passo a Passo

#### Passo 1: Criar um novo repositório

1. Crie o repositório no github, lembre de inicializar ele com o README.
2. Pegue a URL.
3. Abra o terminal do VSCode.
4. Execute o comando:

```sh
git clone <url>
```

#### Passo 2: Criar um ramo de feature para criar um usuário

1. Mude para o repositório recém-criado:

```sh
cd nome-do-repositorio
```

2. Crie e mude para um novo ramo chamado `user-feature`:

```sh
git checkout -B user-feature
```

3. Crie um arquivo `user.md` com o conteúdo:

```sh
echo "login\npassword" > user.md
```

4. Adicione e faça commit das mudanças:

```sh
git add user.md
git commit -m "Adiciona recurso de usuário com login e senha"
```

5. Envie o ramo para o repositório remoto:

```sh
git push origin user-feature
```

#### Passo 3: Criar um ramo de feature para 'order' e 'products'

1. Crie e mude para um novo ramo chamado `order-products-feature`:

```sh
git checkout -B order-products-feature
```

2. Crie os arquivos `order.md` e `products.md` com o conteúdo:

```sh
echo "order details" > order.md
echo "product details" > products.md
```

3. Adicione e faça commit das mudanças:

```sh
git add order.md products.md
git commit -m "Adiciona recursos de pedidos e produtos"
```

4. Envie o ramo para o repositório remoto:

```sh
git push origin order-products-feature
```

#### Passo 4: Criar um ramo de feature para 'delivery'

1. Crie e mude para um novo ramo chamado `delivery-feature`:

```sh
git checkout -B delivery-feature
```

2. Adicione o campo de endereço ao arquivo `user.md`:

```sh
echo "address" >> user.md
```

3. Crie o arquivo `delivery.md` com o conteúdo:

```sh
echo "order id\nexpected delivery time\ncollected\ncompleted" > delivery.md
```

4. Adicione e faça commit das mudanças:

```sh
git add user.md delivery.md
git commit -m "Adiciona recurso de entrega com endereço no usuário e detalhes de entrega"
```

5. Envie o ramo para o repositório remoto:

```sh
git push origin delivery-feature
```

#### Passo 5: Criar um Pull Request no GitHub

1. Vá para o repositório no GitHub.
2. Clique em "Pull Requests".
3. Clique em "New Pull Request".
4. Selecione o ramo `delivery-feature` como base e crie o Pull Request.
5. Adicione um título e uma descrição, então clique em "Create Pull Request".

Com esses passos, você terá seguido um fluxo básico de trabalho com Git, criando, modificando e colaborando em diferentes funcionalidades em um repositório de código.
