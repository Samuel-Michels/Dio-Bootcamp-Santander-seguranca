# Desafio Santander Bootcamp Cibersegurança #2

Demonstração de criação de uma página phishing utilizando Kali Linux e o Social-Engineer Toolkit (SET). Este projeto tem propósito exclusivamente educacional e deve ser realizado em um ambiente de teste controlado.

## Ferramentas Necessárias
- [Kali Linux](https://www.kali.org/downloads/)
- Social-Engineer Toolkit (SET) (já incluído no Kali Linux)

---

## Preparando o Ambiente
1. **Atualize pacotes e repositórios**:
   ```bash
   sudo apt update && sudo apt upgrade -y
   ```

2. **Verifique o status da rede**:
   - Abra o terminal e use o comando:
     ```bash
     ifconfig
     ```
   - Localize o endereço IP da sua máquina (exemplo: `192.168.1.5`) na interface de rede ativa (`eth0`, `wlan0`, etc.).

---

## Passo a Passo

### Passo 1: Iniciar o Social-Engineer Toolkit (SET)
1. Abra o terminal no Kali Linux.
2. Inicie o SET com o comando:
   ```bash
   sudo setoolkit
   ```
3. Insira sua senha de administrador, se solicitado.

---

### Passo 2: Seleção do Tipo de Ataque
1. No menu principal, selecione **"Social-Engineering Attacks"**:
   ```
   1) Social-Engineering Attacks
   ```
2. Escolha a opção **"Website Attack Vectors"**:
   ```
   2) Website Attack Vectors
   ```
3. Selecione **"Credential Harvester Attack Method"**:
   ```
   3) Credential Harvester Attack Method
   ```
4. Em seguida, escolha **"Site Cloner"**:
   ```
   2) Site Cloner
   ```

---

### Passo 3: Configuração do Ataque de Phishing
1. Quando solicitado, insira o **URL do site que você deseja clonar** (exemplo: `http://example.com`).
2. O SET começará a clonar o site e exibirá a mensagem:
   ```
   Site clonado com sucesso.
   ```
Obs: Sites como Facebook e Instagram possuem mecanismos avançados de segurança para evitar que suas páginas sejam clonadas, pode ser que encontre dificuldade em clonar.

---

### Passo 4: Configuração do Servidor Local
1. O SET configurará automaticamente um servidor web local.
2. O terminal exibirá o endereço IP e a porta do servidor:
   ```
   Server is live on: http://192.168.1.5:8080
   ```
3. Anote o endereço gerado.

---

### Passo 5: Testar o Ataque de Phishing
1. Abra um navegador e acesse o endereço fornecido pelo SET (exemplo: `http://192.168.1.5:8080`).
2. Você verá uma cópia do site clonado.
3. Insira credenciais fictícias para testar.

---

### Passo 6: Coletar Credenciais e Resultados
![image](https://github.com/user-attachments/assets/9252a87d-f5e7-47e2-a360-008de0894be4)

1. Após inserir informações no site clonado, as credenciais serão capturadas pelo SET.
2. As informações podem ser visualizadas diretamente no terminal ou no diretório:
   ```bash
   /root/.set/
   ```
[Uploadin<?xml version="1.0" encoding='UTF-8'?>
<harvester>
   www.cadeogame.com.br/MeuCG/Principal
   <url>      <param>usuario=Jefinho</param>
      <param>senha=12131415</param>
      <param>goback=</param>
      <param>entrar=Entrar</param>
   </url>
</harvester>
g 2024-12-29 10_12_25.961188.xml…]()


---

### Passo 7: Parar o Servidor
1. Para interromper o servidor local, pressione **Ctrl+C** no terminal do SET.

---

## Aviso Importante
Este projeto é **exclusivamente educacional** e deve ser utilizado apenas em **ambientes controlados** e com **permissão explícita**. O uso indevido de técnicas de phishing é ilegal e pode ter graves consequências legais e éticas.

---
