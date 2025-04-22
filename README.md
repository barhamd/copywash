# CopyWash

**CopyWash** is a tiny personal utility that strips formatting from macOS clipboard contents. It’s useful when you've copied styled text (e.g., from web pages, rich text editors, or ChatGPT) and want to convert it to plain text without bold, italics, or links.

## What it does

When you run `copywash`, it:

1. Grabs the current clipboard contents (formatted text)
2. Writes it to a temporary plain text file (removing formatting)
3. Reads it back in and replaces your clipboard with the plain version

## Installation

Clone or copy this repo:

```sh
git clone https://github.com/barhamd/CopyWash.git ~/path-to-your-utils-directory/CopyWash
```

Then make the script executable:

```sh
chmod +x ~/path-to-your-utils-directory/CopyWash/copywash
```

Add the folder to your PATH by editing `~/.zshrc` or `~/.bashrc`:

```sh
export PATH="$HOME/Work/CopyWash:$PATH"
```

Then reload your shell config:

```sh
source ~/.zshrc  # or source ~/.bashrc
```

## Usage

Just run:

```sh
copywash
```

Your clipboard should now contain just the plain-text version of what you copied before.

## Example

Copy some formatted text:

```markdown
**Hello, world!** This is _formatted_ text.
```

Then run:

```sh
copywash
```

Then paste somewhere:

```txt
Hello, world! This is formatted text.
```
