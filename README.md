# MCP-Servers-Deploy

### Python based mcp-servers
Step 1: Clone repo and 
```
git clone <mcp-server>
cd <mcp-server>
conda create -n myenv python=3.11
conda activate myenv
pip install -r requirements.txt
```

Step 2: run mcpo
```
mcpo --port 8001 --host 192.168.0.3 -- python mcp-server.py
```


### TypeScript based mcp-servers


Step 1: Clone repo and build
```
git clone <mcp-server>
cd <mcp-server>
npm ci
npm install
npm run build   
```

Step 2: run mcpo
```
mcpo  --port 8086 --host 192.168.0.2 -- node build/index.js
```


Step 3: Test
Allow port through the firewall
```
sudo ufw allow 8087
```
```
curl -X 'POST' \
  'http://localhost:8086/papers-search-basic' \
  -H 'accept: application/json' \
  -H 'Content-Type: application/json' \
  -d '{
  "query": "cancer",
  "limit": 10
}'
```
