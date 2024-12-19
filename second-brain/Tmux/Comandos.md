### Inicializar uma sessão.
---
- Dentro do terminal, crie e entre numa nova sessão com:

```bash
tmux
```

- Se quiser criar uma sessão com algum nome específico:

```bash
tmux new -s nome_da_sessao
```
---

### Gerenciamento de sessão.
---
##### Fora do TMUX.

- Para saber quais sessões estão ativas:

```bash
tmux ls
```

- O resultado vai ser:

```bash
nome_da_sessao: quantidade_janelas_sessao (data_criacao)
```

- Para excluir a última sessão:

```bash
tmux kill-session
```

- Para excluir uma sessão específica:

```bash
tmux kill-session -t nome_da_sessao
```

- Para acessar a última sessão:

```bash
tmux a
```

- Para acessar uma sessão especifica:

```bash
tmux a -t nome_da_sessao
```
___
##### Dentro do TMUX.

###### Gerenciando a sessão atual.

- Para sair e salvar a sessão atual: `CTRL + B | D` (Aperte CTRL + B, em seguida D)
___
###### Gerenciando a janela atual.

- Para criar um painel verticalmente: `CTRL + B | %` (Aperte CTRL + B, em seguida do SHIFT + 5)

- Para criar um painel horizontalmente: `CTRL + B | "` (Aperte CTRL + B, em seguida do SHIFT + ')

- Para transitar entre os paineis: `CTRL + B | ArrowKeys` (Aperte CTRL + B, em seguida das setas)

- Outra forma para transitar entre os paineis: `CTRL + B | O` (Aperte CTRL + B, em seguida O)

- Para visualizar a numeração de uma janela específica: `CTRL + Q` (Aperte CTRL + Q)

- Em conjunto com isso, outra forma para transitar entre os paineis: `CTRL + B | Q | numero_do_terminal` (Aperte CTRL + B, em seguida Q, em seguida 0, ou 1, ou 2...)

- Para modificar o tamanho desse painel: `CTRL + B | CTRL/ALT + ArrowKeys` (Aperte CTRL + B, Depois segure CTRL/ALT + setas do teclado)

- Para tamanhos pré-ajustados: `CTRL + B | ALT + numero` (Aperte CTRL + B, em seguida ALT + 0, ou 1, ou 2...)

- Para fechar um painel: `exit` (Digite exit e aperte ENTER)

- Outra forma para fechar um painel: `CTRL + B | X` (Aperte CTRL + B, em seguida X)

- Para renomear a janela atual: `CTRL + B | ,` (Aperte CTRL + B, em seguida ,)

- Para fechar a janela atual: `CTRL + B | &` (Aperte CTRL + B, em seguida &)

- Para sair e salvar a sessão atual: `CTRL + D` (Aperte CTRL + B, em seguida D)
___
###### Gerenciando outras janela.

- Para criar uma nova janela: `CTRL + B | C` (Aperte CTRL + B, em seguida C)

- Para mudar entre janelas da sessão: `CTRL + B | numero da sessão` (Aperte CTRL + B, em seguida 0, ou 1, ou 2...)

- Para mudar de maneira sequencial (para frente): `CTRL + B | N` (Aperte CTRL + B, em seguida N)

- Para mudar de maneira sequencial (para trás): `CTRL + B | P` (Aperte CTRL + B, em seguida P)

- **Existe uma maneira melhor de utilizar**. Para selecionar uma janela específica: `CTRL + B | W` (Aperte CTRL + B, em seguida W)
---

### Glossário:
- -t: target (seleciona um alvo)   Exemplo de uso: `tmux kill-session -t nome_da_sessao`
- -s: session
- -ls: list
- a: attach (se conecta com uma sessão)   Exemplo de uso: `tmux a`, `tmux a -t nome_da_sessao`
- new: 
- -d: detach
- -c: create
- -n: name
- -q: quiet
- -o: order
- -x: kill
- -v: vertical
- -h: horizontal
- -r: resize
- -k: kill
