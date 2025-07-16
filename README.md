# yt-dlp & FFmpeg Installer Script for Windows 🚀

Este é um script de PowerShell completo criado para automatizar a instalação e configuração do `yt-dlp` e `FFmpeg` no Windows, com foco em criar um ambiente otimizado para edição de vídeos, especialmente no Adobe Premiere Pro.

O script foi desenvolvido para ser executado uma única vez, configurando tudo o que você precisa para começar a baixar vídeos de forma rápida e eficiente.

## ✨ Recursos Principais

* **Instalação Automatizada:** Baixa e instala as versões mais recentes do `yt-dlp` e `FFmpeg` sem intervenção manual.

* **Configuração de PATH:** Adiciona automaticamente as ferramentas ao PATH do seu sistema, permitindo que você as execute de qualquer local no terminal.

* **Sistema de Presets:**

  * O comando padrão `yt-dlp` baixa na **melhor** qualidade **disponível** (4K, 8K, etc.).

  * Um preset `1080` é criado para baixar com qualidade limitada a **1080p** (`yt-dlp -P 1080 <URL>`).

* **Otimizado para Editores:** A configuração padrão converte todos os vídeos para o formato **H.264 (MP4)** com áudio **AAC**, garantindo máxima compatibilidade e desempenho de edição no Adobe Premiere Pro e outros softwares.

* **Interface Amigável:** Exibe uma tela de boas-vindas, informa cada passo do processo e mostra uma barra de progresso visual durante os downloads.

* **Organização:** Salva todos os vídeos baixados em uma pasta dedicada `Downloads\yt-dlp` para manter sua biblioteca organizada.

## 📋 Requisitos

* **Windows 10 ou 11**

* **PowerShell 5.1** ou superior (já vem instalado por padrão no Windows).

## 🚀 Como Usar

A execução do script é muito simples. Siga estes passos:

1. **Abra o PowerShell:**

   * Pressione `Win + R`, digite `powershell` e pressione Enter.

2. **Execute o Comando de Instalação:**

   * Copie e cole o seguinte comando no PowerShell e pressione Enter. Este comando baixa e executa o script diretamente.

   ```
  iex (irm 'https://raw.githubusercontent.com/mehsaia/yt-dlp-auto-installer-windows/refs/heads/main/ytdlp-script')
   ```

   > **Nota:** O comando `irm` é um apelido para `Invoke-RestMethod`, que baixa o conteúdo do script da internet. O comando `iex` (apelido para `Invoke-Expression`) executa o script baixado.

3. **Siga as Instruções:**

   * O script irá mostrar uma tela de boas-vindas. Pressione `Enter` para iniciar a instalação. Ele cuidará de todo o resto automaticamente.

4. **Reinicie o PowerShell:**

   * **Este passo é muito importante!** Após a conclusão do script, feche a janela do PowerShell e abra uma nova. Isso é necessário para que o comando `yt-dlp` seja reconhecido pelo sistema.

## 🎮 Comandos de Download

Depois de reiniciar o PowerShell, você pode começar a baixar vídeos com os seguintes comandos:

### Para a Melhor Qualidade Possível

Use o comando `yt-dlp` seguido da URL do vídeo. Ele pegará a melhor resolução disponível (4K, 8K, etc.).

```
# Exemplo
yt-dlp [https://www.youtube.com/watch?v=dQw4w9WgXcQ](https://www.youtube.com/watch?v=dQw4w9WgXcQ)

```

### Para Qualidade até 1080p

Se você não precisa da resolução máxima e quer um arquivo menor, use o preset `1080` com a flag `-P`.

```
# Exemplo
yt-dlp -P 1080 [https://www.youtube.com/watch?v=dQw4w9WgXcQ](https://www.youtube.com/watch?v=dQw4w9WgXcQ)

```

Todos os vídeos serão processados e salvos na pasta `C:\Users\SEU_USUARIO\Downloads\yt-dlp`.

## 🔧 Solução de Problemas

* **Comando `yt-dlp` não encontrado (`Command not found`):**

  * Isso quase sempre significa que você não reiniciou o PowerShell após a instalação. Feche todas as janelas do PowerShell e abra uma nova.

* **Erro de Política de Execução (`Execution Policy`):**

  * Se o PowerShell impedir a execução do script inicial, você pode precisar alterar sua política de execução. Abra o PowerShell como **Administrador** e execute:

  ```
  Set-ExecutionPolicy RemoteSigned -Scope CurrentUser
  
  ```

  Depois, tente executar o comando de instalação novamente em uma janela normal do PowerShell.

## ❤️ Créditos

Script criado e personalizado por **@mehsaiah**.
