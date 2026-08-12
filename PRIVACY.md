# Privacidade

O b-print foi projetado para funcionar localmente no computador.

## O que o programa não faz

- Não envia capturas para servidores.
- Não possui conta de usuário.
- Não coleta telemetria.
- Não envia logs automaticamente.
- Não faz upload para nuvem.
- Não vende nem compartilha dados.

## Arquivos locais

Configurações, histórico recente e logs ficam na pasta da instalação:

```text
%LOCALAPPDATA%\Programs\b-print\data
```

As imagens são salvas somente nas pastas escolhidas pelo usuário.

## Logs

Os logs registram eventos técnicos, avisos, erros, versão do aplicativo e
operações como salvar/copiar. Eles não armazenam pixels ou conteúdo visual das
capturas.

Entretanto, podem conter:

- caminhos e nomes de arquivos;
- nomes de pastas;
- informações técnicas do Windows;
- horários e ações realizadas.

Os logs só saem do computador se o próprio usuário decidir enviá-los. Revise-os
antes de anexar a uma Issue pública.

## Remoção

O desinstalador remove a pasta do programa, incluindo configurações e logs
locais guardados nela. Capturas salvas em outras pastas não são apagadas.
