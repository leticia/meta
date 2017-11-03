# Installing digital certificates on Debian/Ubuntu 
# Como instalar certificados digitais no Debian/Ubuntu

### Environment used:
### Ambiente testado:

- Ubuntu 17.04
- A3 Certificate (hardware private key) from Certisign
- eToken SafeNet 5100
- Google Chrome/Firefox extension WebPKI

### Prerequisites
### Preparação

- Install the following libraries:
- Instale as seguintes bibliotecas:

```
  sudo apt install libengine-pkcs11-openssl libp11-2 libpcsc-perl libccid \
  libpcsclite1 pcscd pcsc-tools libasedrive-usb opensc libssl1.0.0 libtiff5 \
  fontconfig-config libfontconfig1 libwxbase3.0-0v5 libwxgtk3.0-0v5 \
  libpcsclite1 libccid pcscd libjbig0
```


- Find out your ISA with `uname -p` (it should be x86_64 for 64-bit or i386 for 32-bit)
- Descubra qual arquitetura de processador tu tens com `uname -p` (deve ser x86_64 para 64-bit ou i386 for 32-bit)


### Installing SafeNet Authentication Client
### Instalando o Cliente de Autenticação SafeNet
- Download SafeNet Authentication Client v9.1
  [here](https://site.solutinet.com.br/2015/drivers/safenet_deb_9.1.7-0.tar.gz);
- Baixe o Cliente de Autenticação SafeNet [aqui](https://site.solutinet.com.br/2015/drivers/safenet_deb_9.1.7-0.tar.gz);

- Either double-click or use `tar zxvf /path/to/safenet_deb_9.1.7-0.tar.gz` to
  extract the files;
- Clique duas vezes ou use o comando `tar zxvf /path/to/safenet_deb_9.1.7-0.tar.gz` para extrair os arquivos;

- Inside the extracted folder, under your computer's architecture folder, 
run the installation script with `sudo ./install.sh`
- Dentro da pasta extraída, sob a pasta da arquitetura do seu computador, rode
  o script de instalação com `sudo ./install.sh`

### Installing WebPKI Chrome/Firefox extension
### Instalando a extensão do Chrome/Firefox WebPKI

- Follow
  [this](https://get.webpkiplugin.com/) link and instructions
- Acesse [este](https://get.webpkiplugin.com) link e siga as instruções

### Certificate setup
### Configuração do certificado

Insert your eToken into a USB port, open the SafeNet Authentication Client and your certificate
should be recognized. It should be recognized by WebPKI extension as well.

Insira seu eToken em uma porta USB, abra o Cliente de Autenticação SafeNet e o
certificado deve ser reconhecido. Ele também deve ser reconhecido pela extensão
WebPKI.

### Troubleshooting
### Resolução de problemas

- Try to reboot your browser if WebPKI doesn't work
- Reinicie o navegador depois de instalar a extensão caso necessário

- Depending on which Ubuntu version you are using, some libraries' versions might change. 
- Dependendo de que versão do Ubuntu tu usas, algumas versões de libs podem mudar.

- You might need to reboot your system (yes, I know)
- Tu podes precisar reiniciar o sistema (sim, eu sei)

### Bonus

[Link](https://site.solutinet.com.br/2015/drivers/safenet_rpm_9.1.7-0.tar.gz) to the .rpm version of SafeNet Authentication Client

[Link](https://site.solutinet.com.br/2015/drivers/safenet_rpm_9.1.7-0.tar.gz)
para a versão .rpm do Cliente de Autenticação SafeNet
