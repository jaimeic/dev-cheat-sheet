# Terminal Setup

Para que cuando me toque volver a settear todo, me acuerde como. Usando como base el repo de el gran chompas [^0].

## Download Homebrew

[Homebrew](https://brew.sh/) es un package manager para macOS (y Linux). Homebrew se baja usando este comando:
```
$ /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

## Download iTerm2

Primero toca bajar iTerm2 (un terminal un poco mas bonito que el default que viene con el mac). Esto se puede bajar [aquí](https://iterm2.com/downloads.html) o tirando este comando con homebrew:
```
$ brew install --cask iterm2
```

No se te olvide agregar el path a brew en el archivo de configuracion -> [.zshrc](assets/zshrc.txt)
```
# Homebrew path
export PATH=/opt/homebrew/bin:$PATH
```

## Install oh-my-zh (or fig?)

`oh-my-zsh` y `fig` son frameworks para manejar las configuraciones de zsh.

### oh-my-zsh

Para bajar `oh-my-zsh` tienes que ir a este [link](https://ohmyz.sh/#install) o correr el siguiente comando:
```
$ sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

Estas autocompletions tambien sirven bastante para zsh y oh-my-zsh:

```
$ brew install zsh zsh-autocompletions
```

### fig

Para bajar `fig` toca ir a su [página](https://fig.io/) y bajar el paquete de ahi. (Todavía no lo he usado...)

## Configure the terminal

[^0]: https://github.com/Chompas/iterm-prezto
