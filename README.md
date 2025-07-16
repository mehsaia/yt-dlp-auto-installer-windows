# Instalador Automático de yt-dlp e ffmpeg para Windows

Um script PowerShell simples e eficaz para baixar automaticamente as versões mais recentes do `yt-dlp` e `ffmpeg`, e adicioná-los ao PATH do seu Windows. Isso permite que você execute o `yt-dlp` e o `ffmpeg` de qualquer terminal (CMD, PowerShell, etc.) sem configuração manual.

## O que este script faz

* **Cria um Diretório**: Cria uma pasta dedicada em `C:\Users\SeuUsuario\yt-dlp` para armazenar os executáveis.
* **Configuração do PATH**: Adiciona automaticamente esta pasta à variável de ambiente PATH do seu usuário.
* **Baixa o yt-dlp**: Obtém o `yt-dlp.exe` mais recente do repositório oficial do GitHub.
* **Baixa e Instala o ffmpeg**: Baixa a compilação mais recente do `ffmpeg`, extrai os arquivos necessários (`ffmpeg.exe` e `ffprobe.exe`), os coloca no diretório de instalação e limpa todos os arquivos temporários.
* **Totalmente Automatizado**: Não é necessário baixar ou descompactar arquivos manualmente.

## Como Usar

Abra um terminal PowerShell e execute o seguinte comando. Ele irá baixar e executar o script de instalação.

```powershell
iex (irm 'https://raw.githubusercontent.com/mehsaia/yt-dlp-auto-installer-windows/refs/heads/main/yt-dlp-script')
```

### Aviso Importante

Após a conclusão do script, você **precisa reiniciar** o seu terminal (fechar e reabrir qualquer janela do PowerShell ou do Prompt de Comando) para que as alterações no PATH entrem em vigor.

# yt-dlp & ffmpeg Auto-Installer for Windows

A simple and effective PowerShell script to automatically download the latest versions of `yt-dlp` and `ffmpeg`, and add them to your Windows PATH. This allows you to run `yt-dlp` and `ffmpeg` from any terminal (CMD, PowerShell, etc.) without manual setup.

## What This Script Does

* **Creates a Directory**: Makes a dedicated folder at `C:\Users\YourUsername\yt-dlp` to store the executables.
* **PATH Configuration**: Automatically adds this folder to your user's PATH environment variable.
* **Downloads yt-dlp**: Fetches the latest `yt-dlp.exe` from the official GitHub repository.
* **Downloads and Installs ffmpeg**: Downloads the latest `ffmpeg` build, extracts the necessary files (`ffmpeg.exe` and `ffprobe.exe`), places them in the installation directory, and cleans up all temporary files.
* **Fully Automated**: No manual downloading or unzipping required.

## How to Use

Open a PowerShell terminal and run the following command. This will download and execute the installation script.

```powershell
iex (irm 'https://raw.githubusercontent.com/mehsaia/yt-dlp-auto-installer-windows/refs/heads/main/yt-dlp-script')
```

*Replace `YOUR_RAW_SCRIPT_URL_HERE` with the actual raw URL of your script file from GitHub Gist or your repository.*

### Important Notice

After the script finishes, you **must restart** your terminal (close and reopen any PowerShell or Command Prompt windows) for the PATH changes to take effect.

---
