# desafio-aws-ec2-dio
Criei uma instância EC2 na AWS, configurei segurança, conectei via SSH e documentei todo o processo no GitHub. Prática com cloud computing, grupos de segurança e uso de chaves .pem. Entrega organizada com README, imagens e comandos para reprodutibilidade do ambiente. 
# 🚀 Desafio AWS EC2 - DIO

> Documentação completa sobre a criação e gerenciamento de uma instância EC2 na AWS.

Objetivo
Consolidar conhecimentos em instâncias EC2, grupos de segurança, SSH e documentação técnica no GitHub.

Etapas Realizadas

1. Criei uma instância EC2 com Amazon Linux 2023
2. Configurei grupo de segurança para SSH (porta 22) e HTTP (porta 80)
3. Gerei e baixei a chave `.pem` para acesso seguro
4. Conectei-me via SSH usando Git Bash
5. Instalei o servidor Apache e criei uma página simples
6. Testei o acesso no navegador

Capturas de Tela
| Descrição | Imagem |
|----------|--------|
| Instância em execução | ![Running](imagens/Instancia em execução) |
| Grupo de segurança | ![Security Group](imagens/Conexao SSH) |
| Conexão SSH | ![SSH](images/Regras de entrada) |

Comandos Usados

```bash
# Conectar via SSH
ssh -i "dio-ec2-key.pem" ec2-user@54.91.216.148

# Instalar Apache
sudo yum update -y
sudo yum install httpd -y
sudo systemctl start httpd
sudo systemctl enable httpd

# Criar página simples
echo "<h1>Olá, mundo! Este é meu servidor EC2!</h1>" | sudo tee /var/www/html/index.html
