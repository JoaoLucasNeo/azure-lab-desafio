# Resumo: Gerenciamento de Máquinas Virtuais no Azure

## 1. Criação de VM via Portal
- Acesse "Máquinas Virtuais" no portal
- Clique em "Criar"
- Configure: nome, SO, tamanho, autenticação, rede

## 2. Criação via Azure CLI
```bash
az vm create \
  --resource-group MeuGrupo \
  --name MinhaVM \
  --image UbuntuLTS \
  --admin-username azureuser \
  --generate-ssh-keys
```

## 3. Gerenciamento
- Iniciar: `az vm start --name MinhaVM`
- Parar: `az vm stop --name MinhaVM`
- Deletar: `az vm delete --name MinhaVM --yes`

## 4. Dicas
- Use tags para organizar recursos
- Evite usar o tamanho padrão da VM sem analisar o custo
- Automatize tarefas com scripts PowerShell
