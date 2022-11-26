# instalacão leve Debian buster
Instalação bem live do Debian Buster com Xfce4 e i3(voltada para desinvolvimento).


instalação do debian buster em um ambiente desktop leve:

Abordaremos aqui uma instalação leve do debian 10(Buster) usando XFCE4 e i3.<br>
supondo que vc ja seja familiarizado com instalação do sistema debian e derivados.<br>

setiver duvidas:
https://servidordebian.org/pt/buster/install/guide

Obs:<br>
Ao chegar ao tasksel selecione<br> 
[X] Ambiente de área de trabalho no debian<br>
[X] Xfce (ambiente grafico) *(Posteriormente instalaremos o i3 gerenciador de janelas)<br>
[X] Utilitarios de sistema padrão<br>

correra uma instalação de 1151 pacotes<br>

Apos a instalação o sistema reiniciara(avisa que a instalação esta finalizada) e vc reinicia o sistema<br>
apos logue con suas credênciais<br>
o sistema perguntara se vc quer um menu padão ou em branco selecione o padrão<br>

configurando sources.list:<br>

sudo pico /etc/apt/sources.list<br>

deb http://deb.debian.org/debian/ buster main contrib non-free <br>
deb-src http://deb.debian.org/debian/ buster main contrib non-free <br>

deb http://security.debian.org/debian-security buster/updates main contrib non-free<br>
deb-src http://security.debian.org/debian-security buster/updates main contrib non-free<br>

# buster-updates, previously known as 'volatile'<br>
deb http://deb.debian.org/debian/ buster-updates main contrib non-free<br>
deb-src http://deb.debian.org/debian/ buster-updates main contrib non-free<br>

# buster-backports, previously on backports.debian.org<br>
deb http://deb.debian.org/debian/ buster-backports main contrib non-free<br>
deb-src http://deb.debian.org/debian/ buster-backports main contrib non-free<br>

recomendo atenção neste passo, pois se vc tem uma compatibilidade de hardware<br>
não precisa mecher ai é só ir adcionando oque vc precisar de sofitwares para seu dia-dia<br>

descrição:<br>
https://www.debian.org/devel/debian-desktop/<br>

instalação node:<br>
https://www.vivaolinux.com.br/dica/Instalando-Nodejs-no-Debian-10-Buster<br>

## Logue-se como root e execute o comando:<br>

apt install curl<br>

## Agora, é só instalar o Node.js com os comandos:<br>

curl -sL https://deb.nodesource.com/setup_16.x | bash - (versão estavel)<br>
apt-get install -y nodejs

## Saida da instalação do node:<br>
Run `sudo apt-get install -y nodejs` to install Node.js 16.x and npm<br>
You may also need development tools to build native addons:<br>
     sudo apt-get install gcc g++ make
To install the Yarn package manager, run:<br>
     curl -sL https://dl.yarnpkg.com/debian/pubkey.gpg | gpg --dearmor | sudo tee /usr/share/keyrings/yarnkey.gpg >/dev/null
     echo "deb [signed-by=/usr/share/keyrings/yarnkey.gpg] https://dl.yarnpkg.com/debian stable main" | sudo tee /etc/apt/sources.list.d/yarn.list
     sudo apt-get update && sudo apt-get install yarn

## Instale:<br>
sudo apt install apt-transport-https<br>

## Download vscode:<br>
https://code.visualstudio.com/download<br>

## Apos instale o vscode:<br>
sudo dpkg --install code_1.64.2-1644445741_amd64.deb<br>

## Instalação do gerenciador de janelas i3:<br>
## Aqui eu segui um exelente artigo do MIguel Sampaio da Veiga,<br>
## que tambem pode ser usado como manual de instalação do sistema debian.<br>

sudo aptitude install i3 suckless-tools<br>

Ao entrar o i3 é pedida a criação do ficheiro de config, diga sim.<br>
use a tecla 'windows' + enter para abrir o terminal.<br>

windows + d abre o menu para busca de programas<br>

O ficheiro de config está na '~/.config/i3/config', variando de sistemas operacionais<br>


obrigado a todos.<br>

