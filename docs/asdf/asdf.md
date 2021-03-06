asdf
===

asdf -- универсальный расширяемый менеджер версий, поддерживающий Python, Node, Elixir и вообще любые другие языки и окружения, для которых имеет смысл иметь несколько версий на машине одновременно.

## Установка:

```shell
git clone https://github.com/asdf-vm/asdf.git ~/.asdf --branch v0.7.8  
```

### Подключение к шеллу:

**bash**:

```shell
echo -e '\\n. $HOME/.asdf/asdf.sh' >> ~/.bashrc

echo -e '\\n. $HOME/.asdf/completions/asdf.bash' >> ~/.bashrc
```

**zsh:**

```shell
echo -e '\\n. $HOME/.asdf/asdf.sh' >> ~/.zshrc

echo -e '\\n. $HOME/.asdf/completions/asdf.bash' >> ~/.zshrc
```

**Fish:**

```shell
echo 'source ~/.asdf/asdf.fish' >> ~/.config/fish/config.fish

mkdir -p ~/.config/fish/completions; and cp ~/.asdf/completions/asdf.fish ~/.config/fish/completions
```

После подключения шелла нужно перезапустить его.

Для большинства плагинов потребуются следующие системные зависимости:

### Ubuntu:

```shell
sudo apt install \\

automake autoconf libreadline-dev \\

libncurses-dev libssl-dev libyaml-dev \\

libxslt-dev libffi-dev libtool unixodbc-dev \\

unzip curl
```

```shell
sudo apt-get install -y build-essential libssl-dev zlib1g-dev libbz2-dev \\

libreadline-dev libsqlite3-dev wget curl llvm libncurses5-dev libncursesw5-dev \\

xz-utils tk-dev libffi-dev liblzma-dev python-openssl git
```

### Fedora:

```shell
sudo dnf install @development \\

zlib-devel bzip2 bzip2-devel readline-devel sqlite \\

sqlite-devel openssl-devel xz xz-devel libffi-devel findutils
```

```shell
sudo dnf install \\

automake autoconf readline-devel \\

ncurses-devel openssl-devel libyaml-devel \\

libxslt-devel libffi-devel libtool unixODBC-devel \\
```

```shell
unzip curl
```

### Обновление:

```shell
asdf update
```

### Плагины:

#### Список плагинов:

```shell
asdf plugin-list-all
```

#### Список установленных плагинов:

```shell
asdf plugin-list
```

#### Установить плагин:

```shell
asdf plugin-add python
```

```shell
asdf plugin-add nodejs
```

#### Обновление плагинов:

```shell
asdf plugin-update --all
```

### Управление версиями:

#### Установить версию:

```shell
asdf install <name> <version>
```

##### Например:

```shell
asdf install python 3.7.3
```

```shell
asdf install python 3.8-dev
```

#### Список всех доступных версий:

```shell
asdf list-all <name>
```

#### Список установленных версий:

```shell
asdf list <name>
```

#### Выбрать активную версию:

```shell
asdf global <name> <version> \[<version>...\]
```

```shell
asdf local <name> <version> \[<version>...\]
```

\# asdf global elixir 1.2.4

`global` -- глобально, для всей системы

`local` -- локально, для текущей директории

#### Показать выбранные версии:

```shell
asdf current
```

#### Удалить версию:

```shell
asdf uninstall <name> <version>
```

При выборе любой версии может потребоваться выбор глобальной версии, можно указать в качестве глобальной версии системную:

```shell
asdf global python system
```

Для автоматического переключения версий при переходе в директорию можно создать файл `.tool-versions`, например со следующим содержанием:

`nodejs 10.14.2`

`python 3.7.4`

`###### tags: []`
