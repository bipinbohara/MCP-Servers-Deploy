Copy files from remote server:
```
cp -r ~/Desktop/MCP-Servers/PubMed-MCP-Server/* ~/Desktop/MCP-Servers/rdiscovery/
# OR
rsync -av --exclude='__pycache__' ~/Desktop/MCP-Servers/PubMed-MCP-Server/ ~/Desktop/MCP-Servers/rdiscovery/
```

Copy files from device to remote server:
```
scp ~/<source-path> <user>@<IP>:/<destination-path> 
```
