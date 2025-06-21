
# Resumo: Gerenciamento de Máquinas Virtuais no Azure

## 1. Criação de Máquina Virtual via Portal Azure

Para criar uma VM pelo portal:

1. Acesse o portal Azure em [https://portal.azure.com](https://portal.azure.com).
2. No menu lateral, clique em **Máquinas Virtuais**.
3. Clique no botão **Criar** e escolha **Máquina Virtual**.
4. Configure os detalhes da VM:
   - **Nome:** Escolha um nome único para sua VM.
   - **Sistema Operacional:** Selecione a imagem desejada, como Windows Server ou Ubuntu.
   - **Tamanho:** Defina o tamanho da VM (número de CPUs, memória).
   - **Autenticação:** Escolha entre senha ou chave SSH para acesso.
   - **Rede:** Configure a rede virtual e grupo de segurança.
5. Revise e clique em **Criar** para iniciar a implantação.

---

## 2. Criação de Máquina Virtual via Azure CLI

Você também pode criar uma VM usando a linha de comando Azure CLI. Exemplo básico para criar uma VM Ubuntu:

```bash
az vm create \
  --resource-group MeuGrupo \
  --name MinhaVM \
  --image UbuntuLTS \
  --admin-username azureuser \
  --generate-ssh-keys
```

- `--resource-group`: Nome do grupo de recursos onde a VM será criada.
- `--name`: Nome da VM.
- `--image`: Imagem do sistema operacional.
- `--admin-username`: Usuário administrador.
- `--generate-ssh-keys`: Cria automaticamente chaves SSH para acesso seguro.

---

## 3. Gerenciamento de Máquina Virtual via Azure CLI

Alguns comandos úteis para gerenciar a VM:

- **Iniciar a VM:**

  ```bash
  az vm start --name MinhaVM --resource-group MeuGrupo
  ```

- **Parar (desligar) a VM:**

  ```bash
  az vm stop --name MinhaVM --resource-group MeuGrupo
  ```

- **Deletar a VM:**

  ```bash
  az vm delete --name MinhaVM --resource-group MeuGrupo --yes
  ```

> **Nota:** Sempre informe o `--resource-group` para garantir que o comando afete a VM correta.

---

## 4. Dicas importantes

- **Use tags para organizar recursos:**  
  Tags ajudam a identificar e agrupar recursos no Azure, facilitando o gerenciamento e faturamento.

- **Analise o custo antes de escolher o tamanho da VM:**  
  O tamanho padrão pode não ser o mais econômico para sua necessidade.

- **Automatize tarefas com scripts PowerShell ou Azure CLI:**  
  Automatização evita erros manuais e agiliza a administração.

---

Este resumo serve como um guia rápido para criação e gerenciamento básico de máquinas virtuais no Azure. Para aprofundar, consulte a [documentação oficial](https://learn.microsoft.com/pt-br/azure/virtual-machines/).
