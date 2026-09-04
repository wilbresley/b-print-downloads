# b-print

[English](README.en.md)

**Captura de tela para Windows**, com anotações na hora: setas, formas, texto,
marca-texto, censura, lupa e editor.

Versão atual: **1.0.1** (4 de setembro de 2026)

O programa fica na bandeja do sistema, instala só para o usuário atual e
não pede permissão de administrador.

---

## Download

| Arquivo | Conteúdo |
|---------|----------|
| [b-print-1.0.1-windows-x64.exe](https://github.com/wilbresley/b-print-downloads/releases/download/v1.0.1/b-print-1.0.1-windows-x64.exe) | Instalador Windows 64 bits |
| [SHA256SUMS.txt](https://github.com/wilbresley/b-print-downloads/releases/download/v1.0.1/SHA256SUMS.txt) | Checksums SHA-256 |
| [LICENSES.zip](https://github.com/wilbresley/b-print-downloads/releases/download/v1.0.1/LICENSES.zip) | Termos, LGPL/Qt, SBOMs e atribuições |
| [Releases](https://github.com/wilbresley/b-print-downloads/releases/tag/v1.0.1) | Página completa da versão, inclusive fontes Qt 6.8.2 |

O instalador é **gratuito**.

> O executável **não possui assinatura digital paga**. O Windows pode mostrar
> “Editor desconhecido” ou um aviso do SmartScreen. Isso é esperado. Confira
> o SHA-256 em `SHA256SUMS.txt` antes de executar.

---

## Instalação

1. Baixe `b-print-1.0.1-windows-x64.exe`.
2. Confira o SHA-256 com o arquivo da mesma Release.
3. Execute o instalador. Ele abre em **Português (Brasil)** e permite escolher
   **English** na primeira tela.
4. O b-print permanece na bandeja, perto do relógio.

Pasta padrão:

```text
%LOCALAPPDATA%\Programs\b-print
```

Instalação silenciosa, desinstalação e linha de comando: [USAGE.md](USAGE.md)

---

## Uso rápido

- **Print Screen** e **Windows+Shift+S** abrem o b-print por padrão. Cada um
  pode ser devolvido ao Windows em Configurações → Captura.
- **Windows+Shift+D** é o atalho extra (configurável; também aceita F1–F24).
- **Clique esquerdo** no ícone da bandeja: capturar uma região.
- **Clique direito**: todos os modos, Configurações, Ajuda e Sair.
- **ESC** fecha primeiro menus e itens em ajuste; só depois cancela a captura.
- **Alt** mostra a grade de 5 px só no gesto ativo.
- Esquerdo + direito, durante o arraste da área, trava nas bordas do monitor.
- **Configurações → Desinstalar** remove o programa após confirmação.
  Capturas salvas em outras pastas permanecem.

A Ajuda completa está dentro do próprio programa.

---

## O que está incluso

- Captura por região, monitor, todos os monitores, janela sob o mouse e timer
- Anotações: setas, formas, texto, data/hora, marca-texto, lápis e censura
- Lupa na captura em tela cheia e editor em janela com zoom
- Temas Escuro e Claro, idioma Português (Brasil) / English
- Cópia imediata para a área de transferência e salvamento em PNG, JPEG ou WebP
- Recentes, quadro e imagens fixadas no topo

---

## Privacidade

O b-print funciona **só neste computador**. Não envia capturas, telemetria ou
logs para servidor. Não usa IA em execução.

Detalhes: [PRIVACY.md](PRIVACY.md)

---

## Transparência de desenvolvimento

O b-print é desenvolvido e mantido por **Wilian Bresley da Costa** com
assistência do **Cursor** e de modelos de inteligência artificial na
implementação, revisão e documentação. Decisões, testes, distribuição e
responsabilidade pelo produto permanecem do autor.

Cursor, Anysphere e fornecedores de modelos não patrocinam, não endossam e
não são afiliados ao b-print.

---

## Logs para suporte

Se o instalador falhar, ele grava `b-print-installer-error.log` ao lado do
executável e oferece **Abrir local do log**.

Em caso de problema no aplicativo, feche o b-print e copie:

```text
%LOCALAPPDATA%\Programs\b-print\data\logs
%LOCALAPPDATA%\Programs\b-print\data\memory-stat.txt
```

Abra uma [Issue](https://github.com/wilbresley/b-print-downloads/issues) com o
horário aproximado. Revise os arquivos: eles podem conter caminhos.

Contato privado, licenciamento ou parceria: **b-print@bresley.win**

---

## Licença

O código próprio do b-print é **freeware proprietário**. Não é código aberto.
Consulte [TERMS.md](TERMS.md). A versão em português brasileiro controla.

Qt e demais bibliotecas permanecem nas licenças originais. Cada Release inclui
`LICENSES.zip` e os quatro arquivos de fonte correspondente do Qt 6.8.2.

Copyright © 2026 Wilian Bresley da Costa.
