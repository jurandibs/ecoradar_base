# EcoRadar Base

Este repositório contém a base do projeto EcoRadar — um aplicativo multiplataforma (Flutter) com integrações nativas para iOS e Android. Ele serve como ponto de partida para desenvolvimento móvel, incluindo código Dart (Flutter), código nativo para iOS (Swift / Objective-C), Android (Java / Kotlin) e arquivos auxiliares (shell, HTML).

## Funcionalidade

A base fornece a estrutura e os módulos iniciais necessários para construir o EcoRadar, incluindo:
- Estrutura Flutter (pasta `lib`) para UI, lógica e estados.
- Integrações nativas em `ios/` e `android/` para chamadas de plataforma quando necessário.
- Scripts e arquivos de suporte para build e automação.

Observação: Este repositório é a base do projeto. Funcionalidades específicas (mapas, sensores, backend) devem ser implementadas ou integradas conforme o escopo do produto.

## Estrutura do repositório (resumida)

- lib/           -> Código Dart/Flutter (UI, lógica de negócios)
- ios/           -> Projeto iOS (Swift / Objective-C)
- android/       -> Projeto Android (Java / Kotlin)
- web/ / html    -> Arquivos HTML/recursos para builds web (se aplicável)
- scripts/       -> Scripts de build e utilitários (shell)

> As pastas podem variar dependendo da configuração do projeto. Verifique o conteúdo do repositório para detalhes atualizados.

## Tecnologias

- Flutter (Dart)
- iOS (Swift, Objective-C)
- Android (Java, Kotlin)
- Shell scripts
- HTML (quando aplicável para Web)

## Requisitos

- Flutter SDK (versão estável compatível) — instalar a partir de https://flutter.dev
- Android SDK / Android Studio
- Xcode (para builds iOS) e CocoaPods
- Java JDK (para builds Android)
- Ferramentas de linha de comando (git, bash/zsh)

## Como preparar o ambiente

1. Clone o repositório:

   git clone https://github.com/jurandibs/ecoradar_base.git
   cd ecoradar_base

2. Instale dependências do Flutter:

   flutter pub get

3. Dependências nativas iOS (no macOS):

   cd ios
   pod install
   cd ..

4. Configure variáveis de ambiente / credenciais se necessário (API keys, certificados) — verifique arquivos de configuração ou documentação interna.

## Como executar em modo debug

- Em dispositivo Android conectado ou emulador:

  flutter run

- Em um simulador iOS (macOS):

  flutter run -d "iPhone"

- Em navegador (se o projeto tiver suporte web):

  flutter run -d chrome

## Como gerar builds (release)

- Android (APK):

  flutter build apk --release

- Android (App Bundle):

  flutter build appbundle --release

- iOS (necessita macOS e conta de desenvolvedor para assinar):

  flutter build ios --release

  Ou abrir o projeto Xcode para ajustar assinaturas:

  open ios/Runner.xcworkspace

Observação: para iOS normalmente é necessário configurar signing e provisões no Xcode.

## Boas práticas

- Mantenha as dependências atualizadas com cautela; teste em builds debug antes de gerar release.
- Faça commits pequenos e descritivos; use branches para features/ajustes.
- Documente chaves e configurações sensíveis fora do repositório (variáveis de ambiente, .env, ou secrets manager).

## Contribuindo

1. Crie uma branch a partir de master: git checkout -b feat/minha-nova-funcionalidade
2. Faça suas alterações e testes locais
3. Abra um Pull Request descrevendo a mudança

## Contato

Para dúvidas ou informações sobre o projeto, contate o mantenedor: https://github.com/jurandibs

---

README gerado em Português (PT-BR). Ajuste o conteúdo conforme as necessidades específicas do projeto.