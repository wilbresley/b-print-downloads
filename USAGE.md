# Manual rápido e comandos

[English](USAGE.en.md)

Manual resumido do **b-print 1.0.1** para Windows. A Ajuda completa fica
dentro do aplicativo (bandeja → **Ajuda…**).

---

## Depois de instalar

O b-print permanece na bandeja do Windows (perto do relógio; no Windows 11
pode estar na seta **^**).

| Ação | Resultado |
|------|-----------|
| Clique esquerdo no ícone | Captura por região |
| Clique direito no ícone | Menu completo |
| Print Screen | Captura pelo b-print (pode devolver ao Windows) |
| Windows+Shift+S | Captura pelo b-print (pode devolver ao Windows) |
| Windows+Shift+D | Atalho extra padrão (configurável) |
| ESC | Fecha menu/item primeiro; depois cancela a captura |

Menu de clique direito: região, timer, todos os monitores, janela sob o mouse,
recentes, quadro, fixar, Configurações, Ajuda e Sair.

Ao sair, Print Screen e Windows+Shift+S voltam ao Windows.

---

## Captura

- Arraste um retângulo, ou clique em um monitor inteiro.
- Uma dica aparece na parte de baixo do monitor onde está o mouse.
- **Esquerdo + direito** durante o arraste: as bordas do monitor atual viram
  barreiras. Solte o direito para atravessar monitores.
- **Alt**: grade de 5 px só na área ou item que está em movimento.
- Com **Girar** ativo, a grade Alt não aparece; use **Shift + roda** para
  saltos de 5°.

Salvar (`Ctrl+S`) abre o menu de escala. Copiar (`Ctrl+C`) é imediato.

---

## Configurações

Abra pelo clique direito na bandeja → **Configurações…**.

- **Salvar** aplica e **não fecha** a janela. O X (ou ESC) fecha.
- Depois de salvar aparece **Configurações salvas** por cerca de 1 segundo.
- **Idioma** (Português / English) só entra em vigor ao Salvar. O programa
  reinicia na bandeja após 3 segundos. Captura, editor ou imagem fixada
  abertos adiam o reinício.
- **Atalhos fixos**: Print Screen e Windows+Shift+S vêm ligados. Desmarque
  para devolver ao Windows na hora.
- **Atalho extra**: combinações com Windows, Ctrl, Alt ou Shift, ou F1–F24
  sozinhas. ESC, Print Screen e Windows+Shift+S são reservados.
- **Desinstalar b-print**: pede confirmação. Se houver captura/editor/pin
  aberto, feche o trabalho primeiro. Capturas em outras pastas permanecem.

---

## Texto e data/hora

No botão **Texto**:

- **Texto…** abre a digitação.
- **Data e hora** coloca o carimbo no formato salvo.
- O **relógio** abre o formato. Presets Brasil 24h / US 12h / ISO 24h mudam
  só a ordem e o relógio; os nomes dos códigos ficam no idioma da interface.
  **Salvar** já insere o carimbo.

---

## Instalação silenciosa

```powershell
.\b-print-1.0.1-windows-x64.exe /S /LANG=pt-BR
```

Com opções:

```powershell
.\b-print-1.0.1-windows-x64.exe /S `
  /LANG=pt-BR `
  /DIR="$env:LOCALAPPDATA\Programs\b-print" `
  /AUTOSTART=0 `
  /DESKTOP=1 `
  /LAUNCH=0
```

| Opção | Função |
|-------|--------|
| `/S` | Sem interface |
| `/LANG=pt-BR\|en` | Idioma do instalador e da primeira abertura |
| `/DIR=` | Pasta de instalação |
| `/AUTOSTART=0\|1` | Iniciar com o Windows |
| `/DESKTOP=0\|1` | Atalho na Área de trabalho |
| `/LAUNCH=0\|1` | Abrir após instalar |

---

## Desinstalação silenciosa

Pelo instalador:

```powershell
.\b-print-1.0.1-windows-x64.exe /uninstall /S
```

Pela instalação:

```powershell
& "$env:LOCALAPPDATA\Programs\b-print\b-print-desinstalador.exe" --uninstall /S
```

---

## Comandos do aplicativo

```powershell
$app = "$env:LOCALAPPDATA\Programs\b-print\b-print.exe"

& $app --tray
& $app --region
& $app --active-screen
& $app --screen 0
& $app --all-screens
& $app --window-under-cursor
```

Configuração:

```powershell
& $app --configure --desktop-shortcut --autostart
& $app --configure --no-desktop-shortcut --no-autostart
& $app --configure-defaults
& $app --set-save-dir "D:\Capturas"
& $app --set-copy-dir "D:\Capturas\copias"
& $app --factory-reset
& $app --help
& $app --version
```

---

## Verificar SHA-256

```powershell
Get-FileHash .\b-print-1.0.1-windows-x64.exe -Algorithm SHA256
```

Compare o resultado com [SHA256SUMS.txt](https://github.com/wilbresley/b-print-downloads/releases/download/v1.0.1/SHA256SUMS.txt)
da mesma Release.

---

## Se algo der errado

Instalador: `b-print-installer-error.log` ao lado do exe, com botão para
abrir a pasta.

Aplicativo:

```text
%LOCALAPPDATA%\Programs\b-print\data\logs
%LOCALAPPDATA%\Programs\b-print\data\memory-stat.txt
```

[Issues](https://github.com/wilbresley/b-print-downloads/issues) ·
**b-print@bresley.win**
