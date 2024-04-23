# Cluster com Ansible

Este diretório contém projetos relacionados à criação e gerenciamento de um cluster utilizando Ansible.

## 📂 Estrutura do Diretório

- [ansible-playbooks](./playbook.yaml): Playbook do Ansible para configuração e gerenciamento do cluster.
- [inventory](./hosts): Arquivos de inventário do Ansible para definir os nós do cluster.

## 📋 Pré-requisitos

Antes de executar os playbooks do Ansible, certifique-se de que os seguintes requisitos estão atendidos:

- Ansible instalado na máquina de controle.
- Chaves SSH configuradas para acesso aos nós do cluster.

### 🔧 Instalação

1. Instale o [Ansible](docs.ansible.com/ansible/latest/installation_guide/installation_distros.html) no seu ambiente.

2. Clone este repositório:

   ```
   git clone https://github.com/gabriel-oliveira800/redes
   ```

3. Acesse o diretório do projeto:

   ```
   cd cluster-with-ansible
   ```

4. Execute os playbooks conforme necessário.

## ⚙️ Executando os Playbooks

Para executar os playbooks do Ansible, siga estas etapas:

1. Edite o arquivo de inventário (`./hosts`) para adicionar os IPs ou nomes de host dos nós do seu cluster.

2. Execute o playbook desejado, por exemplo:
   ```
   ansible-playbook -i hosts playbook.yml
   ```

## 📦 Implantação

Após configurar o ambiente usando os playbooks do Ansible, o cluster estará pronto para uso.

<p style="text-align: center;"> ⌨️ por <a href="https://github.com/gabriel-oliveira800">Gabriel Oliveira</a>
 😊 </p>
