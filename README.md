# figma-linux-font-helper

```
poetry install
```

```
echo "[Unit]
Description=Font Loader for Figma
After=systemd-user-sessions.service

[Service]
Type=simple
WorkingDirectory=$HOME/Applications/figma-linux-font-helper
ExecStart=sh ./run.sh
Restart=on-failure

[Install]
WantedBy=default.target" >> $HOME/.config/systemd/user/figma-linux-font-helper.service
```

```
systemctl --user enable figma-linux-font-helper
systemctl --user start figma-linux-font-helper
```
