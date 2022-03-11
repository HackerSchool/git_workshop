# Workshop Git 
Beginner workshop introducing some useful GIT/GitHub Desktop features.



## Guia de Instalação

Para o workshop são necessárias as seguintes ferramentas:
 - **Terminal/Shell:** Para quem tem um sistema operativo macOS ou Linux esta vem integrada (ir para secção [git](##git)); para quem possui Windows ver a secção [WSL (Windows Subsystem for Linux)](#wsl-windows-subsystem-for-linux).
 - **git:**: https://git-scm.com/download  
	+ ou opcionalmente
 - GitHub Desktop: https://desktop.github.com/
 - **Text Editor / IDE (Recommended - Visual Studio Code):** Iremos usar o VSCode como editor de código neste workshop ([Site de instalação](https://code.visualstudio.com/)).
 - (Opcional) **Windows Terminal:** Apenas opcional, mas para quem quiser esta versão do terminal do Windows 10/11 integra quaisquer terminais que tenham no computador (CMD, PowerShell, Ubuntu, etc.) com um visual mais compacto e moderno ([Site de instalação](https://docs.microsoft.com/en-us/windows/terminal/get-started)).


# git

Para instalar o git na vossa máquina vão ter de correr os seguintes comandos (ou instalar o executavel do git no caso do windows) dependendo do vosso sistema operativo:

- **Windows**:

  - Descarrega e corre o executável do git (https://git-scm.com/download/win)


- **Windows WSL/Linux**:

  - Abre o terminal e corre o seguinte comando: 
```
sudo apt-get install git -y 
```

- **macOS**:

  - Abre o terminal e corre o seguinte comando ([Homebrew](https://brew.sh/)): 
```
brew install git
```

Depois de estar instalado verifiquem a instalação correndo o seguinte comando no terminal, que deverá devolver a vossa versão do git (em WSL/Linux/MacOS):
```
git --version
```



## WSL (Windows Subsystem for Linux) 

- Guia de Instalação para Windows 10/11

O Subsistema Windows para Linux (WSL) permite que developers corram um ambiente GNU/Linux - incluindo a maioria das ferramentas da linha de comandos, utilitários e aplicações - diretamente no Windows, sem modificações, sem a sobrecarga de uma máquina virtual tradicional ou sem uma configuração de dual-boot.

Iremos instalar a versão 2 do WSL, sendo esta a mais recente e a que melhor simula um ambiente GNU/Linux sem problemas de desempenho e compatibilidade.


### Passo 1 - Ativar o 'Windows Subsystem for Linux'

Primeiro deves ativar o recurso opcional **Subsistema Windows para Linux** antes de instalar alguma distribuição Linux no Windows.

Abre PowerShell como Administrador e corre o seguinte comando:
```
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
```
![PowerShell](https://i.imgur.com/shjnI9o.png)
![Comando para ativar WSL no Windows 10](https://i.imgur.com/DkGwscS.png)

### Passo 2 - Ativar o recurso de Máquina Virtual

Antes de instalarem o WSL 2, precisam de ativar o recurso opcional **Plataforma de Máquina Virtual**.

Abre PowerShell como Administrador e corre o seguinte comando:
```
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```
![Comando para ativar o recurso de Máquina Virtual no Windows 10](https://i.imgur.com/saAhY4L.png)


**Reinicia** a tua máquina para concluir a instalação do WSL e procede para o próximo passo para atualizares para o WSL 2.


### Passo 3 - Descarregar o pacote de atualização do kernel Linux

1.  Descarrega o pacote mais recente:
    - [WSL2 Linux kernel update package for x64 machines](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi).

2.  Instala o pacote de atualização descarregado na etapa anterior. (Clica duas vezes para correr- se forem solicitadas permissões elevadas (de Administrador), clica 'sim' para aprovar esta instalação).

Assim que a instalação estiver concluída, passa para o próximo passo - definir WSL 2 como a versão padrão ao instalar novas distribuições Linux. 

### Passo 4 - Definir WSL 2 como a versão padrão

Abre PowerShell como Administrador e corre o seguinte comando para definir o WSL 2 como a versão padrão ao instalar novas distribuições Linux:
```
wsl --set-default-version 2
```
![Definir WSL 2 como padrão](https://i.imgur.com/FZb5xna.png)
### Passo 5 - Instalar a distribuição Linux - Ubuntu

Vamos usar o Ubuntu por ser a distribuição mais amigável na ótica do utilizador, mas também porque é a mais completa e versátil para qualquer ambiente de desenvolvimento.

1.  Abre a [Microsoft Store](https://aka.ms/wslstore)  e seleciona a distribuição linux Ubuntu.

![Vista das distribuições Linux na Microsoft Store](https://docs.microsoft.com/pt-pt/windows/wsl/media/store.png)
    
  
2.  Na página da distribuição Ubuntu, clica em "Obter".
    
![Distriuição](https://docs.microsoft.com/pt-pt/windows/wsl/media/ubuntustore.png)
    

Na primeira vez que iniciares o Ubuntu, uma consola será aberta e serás solicitado a aguardar um ou dois minutos para que os arquivos sejam descompactados e armazenados no teu PC. Lançamentos futuros devem levar menos de um segundo.

Vais precisar de criar um utilizador e uma palavra-passe para o Ubuntu;

![Descompactação do Ubuntu na consola do Windows](https://docs.microsoft.com/pt-pt/windows/wsl/media/ubuntuinstall.png)

Por fim corre os seguintes comandos no terminal Ubuntu para poderes ter acesso a todas as ferramentas e aplicações atualizadas:
```
sudo apt-get update
sudo apt-get upgrade -y
```
![Comandos update e upgrade do gestor de pacotes apt](https://i.imgur.com/wTktB3Y.png)

(Em principio se tiverem pacotes para atualizar, no vosso terminal o resultado dos comandos vai ser diferente)

**PARABÉNS! Instalaste e configuraste com sucesso o Ubuntu no Windows 10!**

Esta secção foi baseada no guia oficial da Microsoft presente [neste site](https://docs.microsoft.com/pt-pt/windows/wsl/install-win10).



### FIM
Quaisquer dúvidas adicionais recorram aos canais de discord atribuídos para esse fim.



#### [LIVE WEBSITE](https://hackerschool.github.io/projects_git_workshop/)
