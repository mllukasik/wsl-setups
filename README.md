# WSL setups

> file: .wslconfig

sometimes it helps. But idk why I have this settings right now.
```
[wsl2]
localhostForwarding=true
```

add this line to keep alive wsl session

> file: ~/.profile
```bash
# keep wsl alive
loops=$(ps -u looper | wc -l)
if [[ "$loops" == '1' ]]; then
    su looper -c "nohup sleep 100d>/dev/null &"
fi

```

Script to open nvim with root privialges but with same nvim settings as login user
> file: /usr/local/bin/snvim
```bash
#!/bin/bash

sudo -Es nvim $@

```
