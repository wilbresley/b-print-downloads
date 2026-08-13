# Manual rápido e comandos

[English](USAGE.en.md)

## Interface

Depois de instalado, o b-print permanece na bandeja do Windows.

- Clique esquerdo no ícone: captura por região.
- Clique direito: região, timer, todos os monitores, janela sob o mouse,
  recentes, quadro, fixar, configurações, ajuda e sair.
- Print Screen e Windows+Shift+S: capturam pelo b-print por padrão. Em
  Configurações → Captura, cada um pode ser devolvido ao Windows separadamente.
- Windows+Shift+D: atalho adicional padrão, configurável.
- O atalho extra aceita combinações com modificadores ou F1–F24 isoladas.
- Ao criar ou redimensionar uma área, mantenha o botão esquerdo e segure também
  o direito para travar o ponto nas bordas do monitor atual. Solte o direito
  para atravessar monitores; pressione novamente para recalcular a trava.
- Configurações → Desinstalar remove o programa após confirmação.

A Ajuda completa está dentro do próprio programa.

## Instalação silenciosa

```powershell
.\b-print-1.0.0-windows-x64.exe /S /LANG=pt-BR
```

Com opções:

```powershell
.\b-print-1.0.0-windows-x64.exe /S `
  /LANG=pt-BR `
  /DIR="$env:LOCALAPPDATA\Programs\b-print" `
  /AUTOSTART=0 `
  /DESKTOP=1 `
  /LAUNCH=0
```

Opções:

- `/S`: sem interface.
- `/LANG=pt-BR|en`: idioma do instalador e da primeira abertura.
- `/DIR=`: pasta de instalação.
- `/AUTOSTART=0|1`: iniciar com o Windows.
- `/DESKTOP=0|1`: atalho na Área de Trabalho.
- `/LAUNCH=0|1`: iniciar após instalar.

## Desinstalação silenciosa

Pelo instalador:

```powershell
.\b-print-1.0.0-windows-x64.exe /uninstall /S
```

Pela instalação:

```powershell
& "$env:LOCALAPPDATA\Programs\b-print\b-print-desinstalador.exe" --uninstall /S
```

## Comandos do aplicativo instalado

```powershell
$app = "$env:LOCALAPPDATA\Programs\b-print\b-print.exe"

& $app --region
& $app --active-screen
& $app --all-screens
& $app --window-under-cursor
& $app --tray
```

Configuração por linha de comando:

```powershell
& $app --configure --desktop-shortcut --autostart
& $app --configure --no-desktop-shortcut --no-autostart
& $app --set-save-dir "D:\Capturas"
& $app --factory-reset
```

## Verificar SHA-256

```powershell
Get-FileHash .\b-print-1.0.0-windows-x64.exe -Algorithm SHA256
```

Compare o resultado com `SHA256SUMS.txt` da mesma Release.
