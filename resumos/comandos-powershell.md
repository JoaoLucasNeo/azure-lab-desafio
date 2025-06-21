# Comandos PowerShell Úteis para VMs no Azure

```powershell
# Login na conta Azure
Connect-AzAccount

# Criar grupo de recursos
New-AzResourceGroup -Name MeuGrupo -Location "East US"

# Criar VM
New-AzVM -ResourceGroupName "MeuGrupo" -Name "MinhaVM" -Location "East US"

# Iniciar VM
Start-AzVM -ResourceGroupName "MeuGrupo" -Name "MinhaVM"

# Parar VM
Stop-AzVM -ResourceGroupName "MeuGrupo" -Name "MinhaVM" -Force

# Deletar VM
Remove-AzVM -ResourceGroupName "MeuGrupo" -Name "MinhaVM"
```