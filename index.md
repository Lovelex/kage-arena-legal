---
title: Política de privacidade do Kage Arena
---

# Política de privacidade do Kage Arena

[English version](en.html)

**Última atualização:** 7 de novembro de 2026

## Resumo

- O Kage Arena **não coleta** seu nome, e-mail, conta da Steam nem endereço IP.
- Quando o jogo dá erro ou trava, ele manda um **relatório de erro** para consertarmos o problema, tanto na versão para baixar quanto na do navegador. No fim de cada partida online, manda também um resumo da qualidade da conexão, só com números. Dá para desligar em **Opções > Jogo > Relatórios de erro**.
- No **jogo online**, os computadores da sala se ligam direto, então os jogadores da sala veem o endereço IP uns dos outros. O jogo não guarda nada sobre eles.

## Quem é o responsável

O Kage Arena é desenvolvido por **Lucas Humberto**, pessoa física, que é o controlador dos dados descritos aqui (Lei Geral de Proteção de Dados, Lei 13.709/2018, e, para jogadores da União Europeia, o Regulamento Geral sobre a Proteção de Dados).

**Contato para dúvidas e pedidos:** lukas489@gmail.com

## 1. O que o jogo não coleta

O jogo não pede cadastro e não coleta nome, e-mail, conta ou nome de usuário da Steam, endereço IP, localização, contatos, gravações de tela, nem o que você digita fora do jogo. A única exceção é o endereço IP que a conexão do jogo online precisa (seção 3), que o jogo não guarda. Não há anúncios, rastreamento de publicidade nem venda de dados.

## 2. Relatórios de erro

**Quando:** na versão para baixar (Windows, pela Steam ou pelo itch.io) e na versão do navegador (itch.io), quando acontece um erro no jogo, um travamento, ou uma falha no jogo online (sincronização, queda da sala, partida que não começa, espera longa por outro jogador). Além disso, no fim de cada partida online, um resumo da qualidade da conexão: ping, correções da rede, esperas, tamanho dos pacotes, quantos bots e rounds, e como a partida acabou. Fora isso, o jogo não manda nada quando abre nem enquanto tudo funciona.

**O que vai no relatório:**

| Dado | Para quê |
| --- | --- |
| A mensagem do erro e o ponto do código em que ele aconteceu | Achar e consertar o defeito |
| A versão do jogo | Saber em qual versão o problema aparece |
| O que estava acontecendo no jogo (tela ou modo, passos do jogo online antes do erro, ping e se a ligação é direta ou pelo túnel) | Reproduzir o problema |
| Sistema operacional, processador, placa de vídeo, memória, resolução da tela, idioma e fuso horário (na versão do navegador, o navegador e o sistema operacional, pela identificação que todo navegador manda) | Problemas que só acontecem em certos computadores |
| Em travamentos graves do programa (só na versão para baixar), uma cópia de parte da memória do jogo no momento da falha | Entender travamentos que não deixam mensagem de erro |

**O que não vai:** nome, e-mail, conta da Steam, endereço IP, localização, nome do computador, nome do usuário do sistema (ele é cortado dos caminhos de pasta antes do envio), a página de onde o jogo foi aberto.

**Base legal:** legítimo interesse em manter o jogo funcionando e corrigir defeitos (LGPD, art. 7º, IX; RGPD, art. 6º, 1, f). Os dados são os mínimos para isso e você pode recusar a qualquer momento.

**Quem recebe:** os relatórios são processados pelo serviço **Sentry** (Functional Software, Inc.), nos **Estados Unidos**, que atua como operador, sob contrato de processamento de dados (DPA) que cobre a transferência internacional pelo Data Privacy Framework e, na falta dele, por cláusulas contratuais padrão. O Sentry está configurado para não guardar endereços IP.

**Por quanto tempo:** até 90 dias. Depois disso, os relatórios são apagados.

**Como desligar:** em **Opções > Jogo > Relatórios de erro**. Desligado, o jogo para de mandar na hora. A escolha fica guardada no seu computador (na versão do navegador, no armazenamento do navegador).

## 3. Jogo online

O jogo online liga os computadores da sala diretamente entre si (tecnologia WebRTC), sem um servidor do jogo no meio. Para isso:

- **Os outros jogadores da sala recebem o endereço IP do seu computador**, como em quase todo jogo online sem servidor central. É assim que os computadores se encontram e trocam os comandos da partida.
- Para achar a sala pelo código, o jogo usa o servidor público de sinalização do **PeerJS**, que recebe o código da sala e o endereço IP de quem cria ou entra. Para descobrir o caminho direto, usa os servidores **STUN do Google**, que também veem o endereço IP.
- Quando a ligação direta não é possível, a partida passa por um retransmissor (TURN) da **Cloudflare**, que vê o endereço IP e o tráfego da partida (só os comandos do jogo, criptografados pelo próprio WebRTC).
- **Lista de salas:** quem cria uma sala pode deixá-la na lista pública (ligado por padrão; desliga em "Na lista de salas", dentro da sala). Enquanto a sala está esperando jogadores, um serviço do jogo na **Cloudflare** mostra a quem procura salas o apelido de quem criou, o modo, quantas vagas estão ocupadas, o código da sala, se ela tem senha (só isso: a senha nunca sai da máquina de quem criou a sala) e o continente aproximado. O continente e uma posição aproximada (cidade) vêm da própria conexão, calculados pela Cloudflare; a posição só serve para estimar o ping e nunca é mostrada a ninguém. O serviço não guarda o endereço IP: guarda só um resumo dele (hash) para limitar quantas salas cada conexão cria. Tudo fica só na memória e some até 45 segundos depois que a sala sai da lista, começa a partida ou fecha. Quem só procura salas manda apenas a versão do jogo.
- Na sala, quem a criou aparece pelo código da sala e os outros por um apelido sorteado. O jogo não usa nome nem conta da Steam no online.
- O Kage Arena não guarda nenhum desses dados. Cada serviço segue a própria política de privacidade.

## 4. Dados que ficam só no seu computador

Configurações (idioma, volumes, controles), mapas do editor e a escolha sobre os relatórios ficam gravados no seu computador e não são enviados.

## 5. Crianças e adolescentes

O jogo não coleta dados que identifiquem quem joga, de nenhuma idade. Os relatórios de erro não contêm informação pessoal.

## 6. Seus direitos

Você pode pedir confirmação de tratamento, acesso, correção, eliminação, informação sobre compartilhamento e revisão de decisões, e pode se opor ao tratamento (LGPD, art. 18; RGPD, arts. 15 a 21), pelo e-mail acima. Como os relatórios não têm nome nem conta, para achar um relatório seu pode ser preciso informar a data e a hora aproximadas e a versão do jogo. Você também pode reclamar à Autoridade Nacional de Proteção de Dados (ANPD) ou à autoridade de proteção de dados do seu país.

## 7. Segurança

Os relatórios viajam criptografados (HTTPS) e só o desenvolvedor tem acesso à conta onde eles ficam.

## 8. Mudanças nesta política

Quando esta política mudar, a data no topo muda junto. O histórico de versões fica neste repositório.
