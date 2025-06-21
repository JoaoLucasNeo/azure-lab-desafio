## 🚀 Dicas de Ouro para Trabalhar com Azure e Máquinas Virtuais (VMs)

> 💡 Aprender Azure é como montar um quebra-cabeça: cada boa prática é uma peça essencial! Vamos deixar sua experiência mais segura, organizada e econômica.

---

### 🏷️ Nomeie seus recursos com sabedoria!

📌 **Use convenções de nomes padronizadas!**  
Ajuda MUITO na hora de identificar e organizar os recursos.

✅ Exemplo:  
- `vm-prod-web01` → VM de produção para Web  
- `vm-dev-db01` → VM de desenvolvimento para banco de dados

![Naming Convention](./imagens/naming-convention.png)

---

### 🧩 Use **Tags** para categorizar tudo!

🏷️ Tags são como etiquetas que você coloca em recursos para encontrá-los e gerenciá-los com facilidade.

🛠️ Exemplo de tags úteis:
```
Ambiente = Producao  
Projeto = E-commerce  
Responsavel = JoaoLucasNeo
```

🔍 Com elas, fica fácil filtrar recursos e até gerar relatórios de custo por projeto.

![Tags no Azure](./imagens/tags-azure.png)

---

### 📸 Faça **Snapshots** antes de mudanças grandes

Antes de instalar atualizações, mover dados ou fazer configurações arriscadas:

🛑 **Pare e tire um snapshot!**

🧯 Ele salva o estado atual do disco da VM, funcionando como um “ponto de restauração”.

💥 Se algo der errado, é só voltar!

![Snapshot](./imagens/snapshot.png)

---

### 💰 Fique de olho nos custos!

Azure é poderoso, mas o bolso agradece se você:

- 📉 Acompanhar os **custos estimados**
- 💡 Usar **VMs sob demanda** ou **reservadas** (economiza até 72%!)
- 🔒 Evitar VMs ociosas — desligue o que não está sendo usado!

📊 Dica de ouro: Use o **Azure Cost Management** para visualizar tudo.

![Custo no Azure](./imagens/azure-cost.png)

---

### 🔐 Proteja suas VMs com NSGs!

🛡️ **Network Security Groups (NSG)** funcionam como "porteiros" das suas VMs.

Você pode definir **quem pode entrar** (IP, porta, protocolo) e **quem fica de fora**.

⚙️ Regras comuns:
- Permitir porta 22 (SSH) só para IPs específicos
- Bloquear tudo que não for necessário

![Diagrama NSG](./imagens/nsg-diagrama.png)

---

### 🌐 Extra: Use Azure Bastion para mais segurança no acesso

Em vez de expor suas VMs à internet com RDP/SSH:

🔐 Use o **Azure Bastion**, que permite acesso pelo próprio portal, com mais segurança e sem abrir portas públicas!

![Azure Bastion](./imagens/azure-bastion.png)

---
