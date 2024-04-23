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

1. Edite o arquivo de inventário (`./config/hosts`) para adicionar os IPs ou nomes de host dos nós do seu cluster.

2. Execute o playbook desejado, por exemplo:

   ```
   ansible-playbook -i config/hosts playbook.yml
   ```

3. Conecte-se ao master e execute `kubectl get nodes` para ver nodes do cluster criado. Rode `kubeadm token create --print-join-command` para agrupar outras maquinas na cluster

## 📦 Implantação

Após configurar o ambiente usando os playbooks do Ansible, o cluster estará pronto para uso. Instale o nginx no node master para testar o funcionamento do cluster.

1. Conecte-se ao master e execute `kubectl get nodes` para ver nodes do cluster criado.

2. Execute `kubectl create deployment nginx --image nginx --port 80` para criar uma image do nginx.

3. Execute `kubectl expose deployment nginx --type NodePort --port 80` para criar um serviço. Rode `kubectl get svc` para ver os serviços criados. Poder ser simplificado pr `kubectl apply -f deployment.yaml`

<p style="text-align: center;"> ⌨️ por <a href="https://github.com/gabriel-oliveira800">Gabriel Oliveira</a>
 😊 </p>
