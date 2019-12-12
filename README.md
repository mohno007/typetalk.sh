# Typetalk.sh
Typetalk.sh is a simple shell script that allow you to post message to [Typetalk](https://www.typetalk.com/).

## How to install
1. Clone this repo: `git clone https://github.com/mohno007/typetalk.sh.git`
1. (If you need) Create a bin directory: `mkdir -p $HOME/.local/bin/`
1. Create a symbolic link: `ln -s PATH_TO_typetalk.sh/typetalk $HOME/.local/bin/typetalk`
1. (If you need) Add a bin directory into PATH: `echo 'export PATH="$PATH:$HOME/.local/bin/"' >> ~/.bashrc`

Example:

```sh
git clone https://github.com/mohno007/typetalk.sh.git "$HOME/.typetalk.sh/"
mkdir -p "$HOME/.local/bin/"
ln -s "$HOME/.typetalk.sh/typetalk" "$HOME/.local/bin/typetalk"
echo 'export PATH="$PATH:$HOME/.local/bin/"' >> ~/.bashrc
exec bash
```

If you use another shell, not bash, setup .*shrc appropriately.

## Usage
Create `$HOME/.typetalk_config` and put an API token into it.

`$HOME/.typetalk_config`:

```sh
TYPETALK_TOPIC=1234
TYPETALK_TOKEN="xxxxxxxxxxxxxxx"
```

Example:

```sh
# specifying content by command line
typetalk -m "Hello, world!"

# specifying content from command output
date | typetalk

# specifying content from file
typetalk "some_file"

# show help
typetalk -h
```

## How to update
`git pull`

## License
Typetalk.sh by mohno007

To the extent possible under law, the person who associated CC0 with
Typetalk.sh has waived all copyright and related or neighboring rights
to Typetalk.sh.

You should have received a copy of the CC0 legalcode along with this
work.  If not, see <http://creativecommons.org/publicdomain/zero/1.0/>.
