# VPN CONFIGURATION

As credenciais para se logar na vpn são:  **username** e a **senha** + **token otp**.

Você pode encontrar o secret_key da sua autencicação de dois fatores lendo o QRCode. Ele tem esse formato:
```
otpauth://totp/<SERVICO>:<EMAIL>?secret=<SECRET_KEY>&issuer=<SERVICO>
```
Para encontrar os 6 dígitos do token, precisamos utilizar o <SECRET_KEY>. Então copie essa chave pois vamos utilizá-la para se logar na VPN.

## 1. CONFIGURAÇÃO


Para iniciar a configuração da VPN, você precisa colocar o seu arquivo de autenticação (**.opvn**) na pasta ~/vpn.
Comando para criar a pasta:
```bash
mkdir ~/vpn
```
Se o arquivo **config_vpn** não estiver com permissão de execução:
```bash
chmod +x config_vpn
```
Ao executar o **config_vpn**, ele irá solicitar usuário, senha e secret_key para configurar o login automático da VPN.
```bash
./config_vpn
```

## 2. EXECUÇÃO

Após concluir a configuração, para se logar na VPN de qualquer pasta, basta executar o comando:
```
vpn
```

OBS.: Se precisar reconfigurar, basta executar o comando:
```
./config_vpn --config
```
