# Enable Auto Complete in MacOS

Step 1: Edit .inputrc file in your home folder

```clojure
nano ~/.inputrc
```

Step 2: Append these line to the opened file

```clojure
set completion-ignore-case on
set show-all-if-ambiguous on
TAB: menu-complete
```

Step 3: Hit control+O to save changes to .inputrc followed by control+X to exit nano

Step 4: Open a new Terminal window or tab to open a new session with autocomplete enabled

## Credits
* <https://medium.com/@timleland/how-to-enable-autocomplete-in-mac-terminal-f3480678e829>
