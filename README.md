# 🧾 Resumo: Criando uma Máquina Virtual no Azure

### 1. Acessando o Portal do Azure
- Acesse o portal do Azure.
- No campo de pesquisa, digite "Máquinas Virtuais" e selecione a opção correspondente.

### 2. Iniciando a Criação da VM
- Clique em "Criar" e selecione "Máquina virtual do Azure".
- Na aba "Básico", preencha os seguintes campos:
  - **Assinatura:**  Escolha sua assinatura do Azure.
  - **Grupo de Recursos:** Selecione um existente ou crie um novo.
  - **Nome da Máquina Virtual:** Por exemplo, myVM.
  - **Região:** Escolha a localização geográfica para a VM.
  - **Imagem:** Selecione o sistema operacional, como Windows Server 2022 Datacenter: Azure Edition - x64 Gen 2.
  - **Tamanho:** Escolha conforme a necessidade de recursos (CPU, memória).
  - **Conta de Administrador:** Defina um nome de usuário (ex: azureuser) e uma senha segura (mínimo de 12 caracteres com complexidade).

### 3. Configurações de Rede
- Na seção "Regras de porta de entrada", selecione "Permitir portas selecionadas".
- Escolha as portas necessárias, como:
  - **RDP (3389):** Para acesso remoto via Área de Trabalho Remota.
  - **HTTP (80):** Se for hospedar um servidor web.
 
### 4. Revisão e Criação
- Clique em "Revisar + criar".
- Após a validação, clique em "Criar" para iniciar a implantação da VM.

### 5. Conectando-se à VM
- Após a implantação, vá para a página da VM e clique em "Conectar" > "RDP".
- Baixe o arquivo .rdp e abra-o para iniciar a conexão.
- Insira as credenciais definidas anteriormente para acessar a VM.

### 6. Instalando o Servidor Web (Opcional)
- Dentro da VM, abra o PowerShell como administrador.
- Execute o comando:
```
  Install-WindowsFeature -name Web-Server -IncludeManagementTools
```
- Após a instalação, você pode acessar o servidor web via navegador utilizando o endereço IP público da VM.

# 📝 Anotações e Dicas
- **Grupos de Recursos:** Utilize grupos de recursos para organizar e gerenciar recursos relacionados.
- **Região:** Escolha a região mais próxima de seus usuários para melhor desempenho e menor latência.
- **Tamanhos de VM:** Avalie as necessidades de sua aplicação para escolher o tamanho adequado da VM.
- **Segurança:** Mantenha as portas de entrada mínimas necessárias abertas e utilize regras de firewall para proteger sua VM.
- **Custos:** Monitore o uso e os custos associados à VM para evitar surpresas na fatura.
- **Encerramento:** Desligue ou exclua VMs que não estão em uso para economizar recursos e custos.
