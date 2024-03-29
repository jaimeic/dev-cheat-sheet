# Terminal Setup

Para que cuando me toque volver a settear todo, me acuerde como. Usando como base el repo de el gran chompas [^0].

## Download Homebrew

[Homebrew](https://brew.sh/) es un package manager para macOS (y Linux). Homebrew se baja usando este comando:
```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

## Download iTerm2

Primero toca bajar iTerm2 (un terminal un poco mas bonito que el default que viene con el mac). Esto se puede bajar [aquí](https://iterm2.com/downloads.html) o tirando este comando con homebrew:
```
brew install --cask iterm2
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
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

Estas autocompletions tambien sirven bastante para zsh y oh-my-zsh:

```
brew install zsh zsh-completions
```

### fig

Para bajar `fig` toca ir a su [página](https://fig.io/) y bajar el paquete de ahi. (Todavía no lo he usado...)

## Configure the terminal

### oh-my-zsh themes

El theme de zsh se puede cambiar dependiendo de lo que te guste (colores, interfaz, iconos, etc). Toca modificar el archive `.zshrc`
```
nano ~/.zshrc
```

Por defecto, `oh-my-zsh` viene con un tema que se llama `robbyrussell`, pero se puede cambiar ajustando la variable:
```
ZSH_THEME="robbyrussell"
```

Esta es la lista de todos los [themes](https://github.com/ohmyzsh/ohmyzsh/wiki/Themes), y tambien estan en el dir:
```
cd ~/.oh-my-zsh/themes
```

### Configure [Plugins](https://ivanaugustobd.medium.com/your-terminal-can-be-much-much-more-productive-5256424658e8)

Agrega el `zsh-syntax-highlighting` para que se ponga verde el texto del terminal cuando encuentre el paquete. Para instalarlo haz clone a este repo:
```
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
```

Y despues agrega el plugin al archivo de `~/.zshrc`:
```
plugins=(
  git
  zsh-syntax-highlighting
)
```

## Configure VS Code



[^0]: https://github.com/Chompas/iterm-prezto
