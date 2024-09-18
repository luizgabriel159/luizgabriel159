#SCRIPT PARA FACILITAR O PROCESSO DO POWRE SHELL
sudo apt update && sudo apt -y upgrade && curl -o assistente https://raw.githubusercontent.com/brunocalado/mestre-digital/master/Scripts/oraclecloud/foundryassistenteoraclecloud.sh && chmod +x assistente

#EFETUAR A CONEXÃO
$Command = "ssh -i foundry.key ubuntu@"+$Args[0]
"Comando executado: " + $Command
Invoke-Expression $Command


#PARA RODAR
.\cloudflared.exe tunnel --url localhost:30000
