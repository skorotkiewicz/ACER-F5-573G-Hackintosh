# ACER-F5-573G-Hackintosh

# Português Brasil
EFI Completa do ACER F5-573G, para fazer Hackintosh usando o macOS Mojave 10.14.3 (18D109)

⚠️ Antes de editar, sugiro que abram a config.plist da pasta EFI, na guia SMBIOS gerem um novo serial no campo "Serial Number", verifique no site https://checkcoverage.apple.com/ se o serial é INVÁLIDO, isso mesmo INVÁLIDO, não pode ser de um Mac real. Copie o "Serial Number" para o campo "Board Serial Number" e adicione mais 5 caracteres aleatórios, copie esse "Board Serial Number" e vá na guia "Rt Variables" e cole no campo "MLB", Abaixo do campo "ROM" clique em "Generate" para gerar uma ROM válida, abra o terminal do macOS e digite "uuidgen" e copie o valor mostrado e cole em "SmUUID"na guia "SMBIOS", cole também na guia "System Parameters" no campo "Custom UUID" o valor copiado do terminal, feito isso, salve e reinicie.

A Kext que deve ser instalada no System/Library/Extensions com a ajuda do Kext Utility são:

IO80211Family.kext

https://drive.google.com/file/d/1ZF1iDlaztfGoGXGQTbGlu106oocgFXdB/view?usp=sharing

⚠️ Após instalar a kext, abra o terminal e execute o comandos:

sudo kextcache -i/

# Audio Headphone FIX

Baixe o ALCJackEAPDFixP2HDA ✅
https://drive.google.com/…/1oBUW2uCtfG2LN5YBz3lX8x6mJdnj9xHl

2) Extraia a pasta na Mesa

3) Abra o terminal e digite:

cd Desktop

cd ALCJackEAPDFixP2HDA/

sudo ./Install.sh

⚠️ Será solicitado a sua senha, digite e reinicie o computador para um resultado efetivo.

 Wi-Fi = ✅
Teclado = ✅
Trackpad = ✅
USB 2.0 e 3.0 = ✅
USB-C = ✅
Porta VGA = ✅
Porta HDMI = ✅
Áudio com AppleALC = ✅
Microfone = ✅
Fone de Ouvído = ✅
Aceleração de Vídeo do Intel HD Graphics 620 = ✅
Porta de Rede Ethernet = ✅
Gerenciamento de Energia na Bateria = ✅
Ajuste de Brilho pelo painel = ✅
Ajuste de Brilho pelo teclado (FN+Left, FN+Right) = ✅

Funções que contém bugs ou não funcionam por não ter suporte:

NVIDIA GeForce 940MX = Sem suporte ❌
Leitor de cartão = Sem suporte ❌
*Bluetooth = Funcionamento parcial ⚠️

⚠️ OBS: O Bluetooth para mim, só funciona se eu entrar no Windows 10, ativar, reiniciar a máquina e bootar no macOS. Segundo o Rehabman, é um problema de gerenciamento de firmware do próprio notebook, porém, recomenda-se o uso de um dongle BT compatível 100% para evitar conflitos ou estresse do usuário.