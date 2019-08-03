# Enable Auto Complete in MacOS

Step 0: Install MacOS x-code tools

```clojure
xcode-select --install
```

Step 1: After the above step you should have git installed. Above step also gets git-autocompletion script for you. Open `~/.bash_profile`
```closure
nano ~/.bash_profile
```

Step 2: Append following line to `~/.bash_profile`
```clojure
[ -f /Library/Developer/CommandLineTools/usr/share/git-core/git-completion.bash ] && . /Library/Developer/CommandLineTools/usr/share/git-core/git-completion.bash
```
Step 3: Hit control+O to save changes to .inputrc followed by control+X to exit nano

Step 4: Open a new Terminal window or tab to open a new session with autocomplete for git also enabled.
