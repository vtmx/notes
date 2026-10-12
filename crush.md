# crush.md

Todas as sessões em um único diretório:

```
# ~/.config/crus/crushrc
option data-directory $HOME/.local/share/crush
```

Comandos básico:

```
# Run in interactive mode
crush

# Run non-interactively
crush run "Guess my 5 favorite Pokémon"

# Run a non-interactively with pipes and redirection
cat README.md | crush run "make this more glamorous" > GLAMOROUS_README.md

# Run with debug logging in a specific directory
crush --debug --cwd /path/to/project

# Run in yolo mode (auto-accept all permissions; use with care)
crush --yolo

# Run with custom data directory
crush --data-dir /path/to/custom/.crush

# Continue a previous session
crush --session {session-id}

# Continue the most recent session
crush --continue
```

Limpar todas as sessões:

```
crush session list | awk '{print $1}' | while read -r id; do crush session delete $id; done
```
