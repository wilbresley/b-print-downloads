# b-print

Captura de tela leve para Windows, com anotações, setas, formas, texto,
marca-texto, censura, lupa e editor.

## Download

Baixe sempre pela página oficial:

**[GitHub Releases](https://github.com/wilbresley/b-print-downloads/releases/latest)**

Versão estável atual: **1.0.0**

Arquivo:

```text
b-print-1.0.0-windows-x64.exe
```

O instalador é gratuito, instala somente para o usuário atual e não solicita
permissão de administrador.

> O executável não possui assinatura digital paga. Por isso, o Windows pode
> mostrar “Editor desconhecido” ou um aviso do SmartScreen.

## Instalação

1. Baixe o instalador na página de Releases.
2. Confira o SHA-256 publicado em `SHA256SUMS.txt`.
3. Execute o arquivo e avance pelo assistente.
4. O b-print ficará na bandeja do sistema, perto do relógio.

Instalação padrão:

```text
%LOCALAPPDATA%\Programs\b-print
```

## Uso rápido

- **Print Screen**: abre a captura do b-print enquanto ele estiver na bandeja.
- **Clique esquerdo na bandeja**: capturar uma região.
- **Clique direito na bandeja**: todos os modos, Configurações, Ajuda e Sair.
- **ESC**: fecha primeiro menus/itens pendentes e depois cancela a captura.

Manual e comandos: [USAGE.md](USAGE.md)

## Privacidade

O b-print funciona localmente. Não envia capturas, telemetria ou logs para um
servidor. Consulte [PRIVACY.md](PRIVACY.md).

## Logs para suporte

Se ocorrer um problema, feche o aplicativo e copie:

```text
%LOCALAPPDATA%\Programs\b-print\data\logs
%LOCALAPPDATA%\Programs\b-print\data\memory-stat.txt
```

Abra uma [Issue](https://github.com/wilbresley/b-print-downloads/issues) com o
horário aproximado do erro. Revise os logs antes de enviar, pois podem conter
caminhos e nomes de arquivos.

## Licença

O código próprio do b-print é **freeware proprietário**. Ele não é código
aberto. Consulte [TERMS.md](TERMS.md).

Bibliotecas e recursos de terceiros permanecem sob suas próprias licenças. A
Release inclui `LICENSES.zip`, os fontes correspondentes do Qt 6.8.2 e os
respectivos SBOMs.

Copyright © 2026 Wilian Bresley da Costa.
