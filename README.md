
<pre>
 MMM"""AMV  .M"""bgd `7MMF'  `7MMF'
 M'   AMV  ,MI    "Y   MM      MM
 '   AMV   `MMb.       MM      MM
    AMV      `YMMNq.   MMmmmmmmMM
   AMV   , .     `MM   MM      MM
  AMV   ,M Mb     dM   MM      MM
 AMVmmmmMM P"Ybmmd"  .JMML.  .JMML.
</pre>
My ZSH config. Jordi Timón @ https://github.com/jorditimon


# 1.    Aliases


## Unzip files

``` shell
# usage: ex <file>

ex ()
{
  if [ -f $1 ] ; then
    case $1 in
      *.tar.bz2)   tar xjf $1   ;;
      *.tar.gz)    tar xzf $1   ;;
      *.bz2)       bunzip2 $1   ;;
      *.rar)       unrar x $1   ;;
      *.gz)        gunzip $1    ;;
      *.tar)       tar xf $1    ;;
      *.tbz2)      tar xjf $1   ;;
      *.tgz)       tar xzf $1   ;;
      *.zip)       unzip $1     ;;
      *.Z)         uncompress $1;;
      *.7z)        7z x $1      ;;
      *.deb)       ar x $1      ;;
      *.tar.xz)    tar xf $1    ;;
      *.tar.zst)   unzstd $1    ;;
      *)           echo "'$1' cannot be extracted via ex()" ;;
    esac
  else
    echo "'$1' is not a valid file"
  fi
}
```

## Pacman/AUR

``` shell
alias pacsyu='sudo pacman -Syyu'                  update only standard pkgs
alias yaysua="yay -Sua --noconfirm"               update only AUR pkgs
alias update="yay -Syu --noconfirm"               update standard pkgs and AUR pkgs
alias unlock="sudo rm /var/lib/pacman/db.lck"     remove pacman lock
alias cleanup='sudo pacman -Rns $(pacman -Qtdq)'  remove orphaned packages

```
## Mirrors

``` shell
alias mirror="sudo reflector -f 30 -l 30 --number 10 --verbose --save /etc/pacman.d/mirrorlist"
alias mirrord="sudo reflector --latest 50 --number 20 --sort delay --save /etc/pacman.d/mirrorlist"
alias mirrors="sudo reflector --latest 50 --number 20 --sort score --save /etc/pacman.d/mirrorlist"
alias mirrora="sudo reflector --latest 50 --number 20 --sort age --save /etc/pacman.d/mirrorlist"

```
## Tools

``` shell
alias ls='lsd -la' 	 my preferred listing
alias la='lsd -a'  	 all files and dirs
alias ll='lsd -l'   	 long format

alias cp="cp -i"         confirm before overwriting something
alias df='df -h'         human-readable sizes
alias free='free -m'     show sizes in MB

```
## Youtube-dl

``` shell
alias yta-aac="youtube-dl --extract-audio --audio-format aac "
alias yta-best="youtube-dl --extract-audio --audio-format best "
alias yta-flac="youtube-dl --extract-audio --audio-format flac "
alias yta-m4a="youtube-dl --extract-audio --audio-format m4a "
alias yta-mp3="youtube-dl --extract-audio --audio-format mp3 "
alias yta-opus="youtube-dl --extract-audio --audio-format opus "
alias yta-vorbis="youtube-dl --extract-audio --audio-format vorbis "
alias yta-wav="youtube-dl --extract-audio --audio-format wav "
alias ytv-best="youtube-dl -f bestvideo+bestaudio "

```
## Change Shell

``` shell
alias tobash="sudo chsh $USER -s /bin/bash && echo 'Now log out.'"
alias tozsh="sudo chsh $USER -s /bin/zsh && echo 'Now log out.'"
alias tofish="sudo chsh $USER -s /bin/fish && echo 'Now log out.'"
```

## Multimídia

``` shell
alias volume="pavucontrol"
alias musica="sonata"	 ou você pode usar o ncmpcpp
alias ncmpc="ncmpcpp"

```
## BitTorrent

``` shell
alias start-tor="transmission-daemon"
alias tor="transmission-remote"

```

# 2.    Shortcuts

 Example:
 brainstormr=~/Projects/development/planetargon/brainstormr
 cd $brainstormr

``` shell
alias musica="cd ~/Música"
alias imagem="cd ~/Imagens"
alias downld="cd ~/Downloads"
alias backup="cd /hoard/MEGAsync"
alias ~="cd ~"

```


# 3.    Neofetch

``` shell
 neofetch

```



_ Banner font: "Georgia 11"
 @ https://manytools.org/hacker-tools/ascii-banner/
_
