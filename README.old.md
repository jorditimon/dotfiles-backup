**Pré instalação** - Prepare arquivos e diretórios que não são fornecidos neste repositório:

```shell
$ sudo pacman -S mpd mpc sonata ncmpcpp transmission-cli
$ mkdir -p ~/.local/share/mpd
$ mkdir -p ~/Música/Playlists
```

- Adicionar *aliases* no **zsh**:

**cat** é o nome do comando/programa;
<br>**>>** manda acrescentar um texto no final do arquivo;
<br>**.zshrc** é o arquivo onde vamos acrescentar o texto.

``` shell
$ cat >> .zshrc
```
Depois de pressionar *Return/Enter* escreva o seguinte texto:

``` shell

## 	Multimídia
alias volume="pavucontrol"
alias musica="sonata"
# ou você pode usar o ncmpcpp
alias musica="ncmpcpp"

##	BitTorrent
alias start-tor="transmission-daemon"
alias tor ="transmission-remote"
```
# -- restaurando os **dotfiles**

1. Clone o repositório, com o seguinte comando:

```shell
git clone [...]
```
2. Copie os diretórios `.config` e `.local` para `dotfilesBackup`;

``` shell
$ cp -r .config .local dotfilesBackup/
```
3. Mova o conteúdo do diretório clonada para o diretório HOME;

``` shell
$ mv -uv dotfiles/* .
```
4. Remova o diretório '.git' e o arquivo `.gitignore` de HOME;

``` shell
$ rm -rf .git .gitignore
```
5. ***Feito!***
<br>
<br>
<br>
---
*PS: eu provavelmente vou atualizar isto depois... transformar esse README em um script ou algo assim...*
