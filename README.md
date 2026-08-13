# b-print

[English](README.en.md)

Captura de tela leve para Windows, com anotações, setas, formas, texto,
marca-texto, censura, lupa e editor.

## Download

Os downloads públicos estão temporariamente indisponíveis enquanto a primeira
versão é testada.

Versão interna em teste: **1.0.0**

Nome planejado do instalador:

```text
b-print-1.0.0-windows-x64.exe
```

O instalador é gratuito, instala somente para o usuário atual e não solicita
permissão de administrador.

> O executável não possui assinatura digital paga. Por isso, o Windows pode
> mostrar “Editor desconhecido” ou um aviso do SmartScreen.

## Instalação

Quando uma Release pública for autorizada:

1. Baixe o instalador na página de Releases.
2. Confira o SHA-256 publicado em `SHA256SUMS.txt`.
3. Execute o arquivo; ele abre em Português (Brasil) e permite escolher English
   na primeira tela.
4. O b-print ficará na bandeja do sistema, perto do relógio.

Instalação padrão:

```text
%LOCALAPPDATA%\Programs\b-print
```

## Uso rápido

- **Print Screen** e **Windows+Shift+S**: abrem o b-print por padrão; podem ser
  devolvidos individualmente ao Windows em Configurações.
- **Windows+Shift+D**: atalho extra padrão, configurável.
- **Clique esquerdo na bandeja**: capturar uma região.
- **Clique direito na bandeja**: todos os modos, Configurações, Ajuda e Sair.
- **ESC**: fecha primeiro menus/itens pendentes e depois cancela a captura.
- **Configurações → Desinstalar**: remove o app após confirmação; capturas
  salvas em outras pastas permanecem.

Manual e comandos: [USAGE.md](USAGE.md)

## Privacidade

O b-print funciona localmente. Não envia capturas, telemetria ou logs para um
servidor. Consulte [PRIVACY.md](PRIVACY.md).

## Transparência de desenvolvimento

O b-print é desenvolvido e mantido por **Wilian Bresley da Costa** com
assistência do **Cursor** e de modelos de inteligência artificial na
implementação, revisão e documentação. As decisões, testes, distribuição e
responsabilidade pelo produto permanecem do autor.

O aplicativo em execução não usa IA e não envia capturas ou dados do usuário a
serviços de IA. Cursor, Anysphere e os fornecedores dos modelos não patrocinam,
não são afiliados e não endossam o b-print. Suas marcas pertencem aos
respectivos titulares.

## Logs para suporte

Se o instalador falhar, ele cria `b-print-installer-error.log` ao lado do
executável e oferece o botão **Abrir local do log**.

Se ocorrer um problema, feche o aplicativo e copie:

```text
%LOCALAPPDATA%\Programs\b-print\data\logs
%LOCALAPPDATA%\Programs\b-print\data\memory-stat.txt
```

Abra uma [Issue](https://github.com/wilbresley/b-print-downloads/issues) com o
horário aproximado do erro. Revise os logs antes de enviar, pois podem conter
caminhos e nomes de arquivos.

Suporte privado, licenciamento, aquisição de direitos ou parceria comercial:
**b-print@bresley.win**

## Licença

O código próprio do b-print é **freeware proprietário**. Ele não é código
aberto. Consulte [TERMS.md](TERMS.md).

Bibliotecas e recursos de terceiros permanecem sob suas próprias licenças. A
Release inclui `LICENSES.zip`, os quatro arquivos de fontes correspondentes do
Qt 6.8.2 e os respectivos SBOMs.

Copyright © 2026 Wilian Bresley da Costa.
