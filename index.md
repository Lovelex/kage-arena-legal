---
title: Política de privacidade do Kage Arena
---

# Política de privacidade do Kage Arena

[English version](en.html)

**Última atualização:** 24 de novembro de 2026

## Resumo

- O Kage Arena **não coleta** seu nome, e-mail, conta da Steam nem endereço IP.
- Quando o jogo dá erro ou trava, ele manda um **relatório de erro** para consertarmos o problema, tanto na versão para baixar quanto na do navegador. No fim de cada partida online, manda também um resumo da qualidade da conexão, só com números. Dá para desligar em **Opções > Jogo > Relatórios de erro**.
- Depois de cada round **online** numa fase do jogo, ele manda **quanto o round durou e quantos jogavam**, e, se você votar no replay do lance, **se gostou da fase**. Vai com um número sorteado da sua instalação, sem nada que identifique você. Dá para desligar em **Opções > Jogo > Votos e números das fases**.
- No **jogo online**, os computadores da sala se ligam direto, então os jogadores da sala veem o endereço IP uns dos outros. O jogo não guarda nada sobre eles.

## Quem é o responsável

O Kage Arena é desenvolvido por **Lucas Humberto**, pessoa física, que é o controlador dos dados descritos aqui (Lei Geral de Proteção de Dados, Lei 13.709/2018, e, para jogadores da União Europeia, o Regulamento Geral sobre a Proteção de Dados).

**Contato para dúvidas e pedidos:** lukas489@gmail.com

## 1. O que o jogo não coleta

O jogo não pede cadastro e não coleta nome, e-mail, conta ou nome de usuário da Steam, endereço IP, localização, contatos, gravações de tela, nem o que você digita fora do jogo. As únicas exceções são o endereço IP que a conexão do jogo online precisa (seção 3) e o que o serviço de votos vê ao receber os dados (seção 4), que o jogo não guarda. Não há anúncios, rastreamento de publicidade nem venda de dados.

## 2. Relatórios de erro

**Quando:** na versão para baixar (Windows, pela Steam ou pelo itch.io) e na versão do navegador (itch.io), quando acontece um erro no jogo, um travamento, ou uma falha no jogo online (sincronização, queda da sala, entrada numa sala que não deu certo, partida que não começa, espera longa por outro jogador). Além disso, no fim de cada partida online, um resumo da qualidade da conexão: ping, correções da rede, esperas, tamanho dos pacotes, quantos bots e rounds, e como a partida acabou. Fora isso, o jogo não manda nada quando abre nem enquanto tudo funciona.

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
- **Lista de salas:** quem cria uma sala pode deixá-la na lista pública (ligado por padrão; desliga em "Na lista de salas", dentro da sala). Enquanto a sala está esperando jogadores (ou, durante a partida, enquanto há um bot cujo lugar alguém pode tomar), um serviço do jogo na **Cloudflare** mostra a quem procura salas o apelido de quem criou, o modo, quantas vagas estão ocupadas, o código da sala, se ela tem senha (só isso: a senha nunca sai da máquina de quem criou a sala) e o continente aproximado. O continente e uma posição aproximada (cidade) vêm da própria conexão, calculados pela Cloudflare; a posição só serve para estimar o ping e nunca é mostrada a ninguém. O serviço não guarda o endereço IP: guarda só um resumo dele (hash) para limitar quantas salas cada conexão cria. Tudo fica só na memória e some até 45 segundos depois que a sala sai da lista, começa a partida ou fecha. Quem só procura salas manda apenas a versão do jogo.
- **Ver a sala antes de entrar:** ao escolher uma sala da lista, o jogo se liga direto à máquina de quem criou a sala, sem ocupar vaga, e mostra o que ela manda: os apelidos de quem está na sala, o ping de cada um com quem criou, o modo, os rounds, o bioma, as variantes e se a partida já começou. Como em toda ligação do jogo online, as duas máquinas veem o endereço IP uma da outra. Nada disso é guardado, e a ligação acaba ao sair dessa tela.
- Na sala, quem a criou aparece pelo código da sala e os outros por um apelido sorteado. O jogo não usa nome nem conta da Steam no online.
- O Kage Arena não guarda nenhum desses dados. Cada serviço segue a própria política de privacidade.

## 4. Votos e números das fases

**Quando:** só no jogo online, no fim de cada round jogado numa fase do próprio jogo (não nos mapas que você faz no editor); e quando você vota no replay do lance (↑ gostei, ↓ não gostei). Os dados vão juntos na virada do round.

**O que vai:**

| Dado | Para quê |
| --- | --- |
| O nome da fase e um resumo (hash) do desenho dela, para separar as versões quando a fase é editada | Saber de qual fase e de qual versão se trata |
| A duração do round, quantos jogavam, quantas pessoas (fora os bots) e se era online | Ver quais fases funcionam: rounds curtos demais, longos demais, fases que ninguém joga |
| O seu voto naquela versão da fase (um só; votar de novo troca) | Saber se a fase está agradando |
| A versão do jogo | Comparar antes e depois de uma mudança |
| Um número sorteado na primeira vez (o identificador da instalação), com uma assinatura do serviço | Contar um voto por instalação e dificultar votos falsos |

**O que não vai:** nome, apelido, e-mail, conta da Steam, nada sobre o seu computador.

**Endereço IP:** o serviço vê o endereço IP da conexão, como todo site. Ele não o guarda: quando a instalação pede o número, fica só um resumo do IP com um segredo que muda a cada dia, para limitar quantas instalações novas cada conexão cria, e esse resumo é apagado no dia seguinte.

**Base legal:** legítimo interesse em melhorar as fases do jogo (LGPD, art. 7º, IX; RGPD, art. 6º, 1, f). Os dados não identificam ninguém e você pode recusar a qualquer momento.

**Quem recebe:** um serviço do jogo na **Cloudflare** (Workers e banco D1), que atua como operador. Só o desenvolvedor lê os números.

**Por quanto tempo:** enquanto o jogo estiver em desenvolvimento, para comparar as versões das fases. Você pode pedir a eliminação dos dados da sua instalação pelo e-mail acima.

**Como desligar:** em **Opções > Jogo > Votos e números das fases**. Desligado, o jogo para de mandar na hora.

## 5. Dados que ficam só no seu computador

Configurações (idioma, volumes, controles), mapas do editor, os votos que você deu e a escolha sobre os relatórios ficam gravados no seu computador e não são enviados.

## 6. Crianças e adolescentes

O jogo não coleta dados que identifiquem quem joga, de nenhuma idade. Os relatórios de erro não contêm informação pessoal.

## 7. Seus direitos

Você pode pedir confirmação de tratamento, acesso, correção, eliminação, informação sobre compartilhamento e revisão de decisões, e pode se opor ao tratamento (LGPD, art. 18; RGPD, arts. 15 a 21), pelo e-mail acima. Como os relatórios não têm nome nem conta, para achar um relatório seu pode ser preciso informar a data e a hora aproximadas e a versão do jogo. Você também pode reclamar à Autoridade Nacional de Proteção de Dados (ANPD) ou à autoridade de proteção de dados do seu país.

## 8. Segurança

Os relatórios viajam criptografados (HTTPS) e só o desenvolvedor tem acesso à conta onde eles ficam.

## 9. Mudanças nesta política

Quando esta política mudar, a data no topo muda junto. O histórico de versões fica neste repositório.
