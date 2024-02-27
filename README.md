# Subsquid-project

sudo apt update
sudo apt install git
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.1/install.sh | bash
source ~/.bashrc
nvm install 20.10.0
nvm use 20.10.0
sudo apt install npm -y



sudo apt-get install ca-certificates curl gnupg lsb-release -y
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt-get update
sudo apt-get install docker-ce docker-ce-cli containerd.io -y

mkdir global-node-packages
npm config set prefix ~/global-node-packages
export PATH="${HOME}/global-node-packages/bin:$PATH"




cd global-node-packages
npm install --global @subsquid/cli@latest


sqd init high-traffic-logs-squid -t https://github.com/subsquid-quests/network-test-two-high-traffic-logs-squid
cd high-traffic-logs-squid
npm ci

sqd get-peer-id

sqd up
sqd build
sqd run .




new file:   high-traffic-logs-squid/.contract-addrs
#	new file:   high-traffic-logs-squid/.env
#	new file:   high-traffic-logs-squid/.gitignore
#	new file:   high-traffic-logs-squid/LICENSE
#	new file:   high-traffic-logs-squid/README.md
#	new file:   high-traffic-logs-squid/commands.json
#	new file:   high-traffic-logs-squid/docker-compose.yml
#	new file:   high-traffic-logs-squid/package-lock.json
#	new file:   high-traffic-logs-squid/package.json
#	new file:   high-traffic-logs-squid/query-gateway/config/gateway-config.yml
#	new file:   high-traffic-logs-squid/query-gateway/keys/.keep
#	new file:   high-traffic-logs-squid/renovate.json
#	new file:   high-traffic-logs-squid/schema.graphql
#	new file:   high-traffic-logs-squid/scripts/checkKey.js
#	new file:   high-traffic-logs-squid/scripts/exportWalletKeyAsJson.js
#	new file:   high-traffic-logs-squid/scripts/getPeerIdFromGatewayKey.js
#	new file:   high-traffic-logs-squid/scripts/package.json
#	new file:   high-traffic-logs-squid/squid.yaml
#	new file:   high-traffic-logs-squid/src/allFields.ts
#	new file:   high-traffic-logs-squid/src/main.ts
#	new file:   high-traffic-logs-squid/src/processor.ts
#	new file:   high-traffic-logs-squid/src/testConfig.ts
#	new file:   high-traffic-logs-squid/src/utils.ts
#	new file:   high-traffic-logs-squid/tsconfig.json
#
