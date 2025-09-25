# ⚓ Batalha Naval RGB com Arduino + Sensor de Cor

Este projeto transforma o sensor de cor **TCS230/TCS3200** em um jogo de **Batalha Naval RGB**.  
Dois times competem tentando adivinhar a cor escolhida pelo adversário (vermelho, verde ou azul).  
O sistema confirma as jogadas com LEDs e mensagens no monitor serial.

---

## 🎮 Como funciona
1. **Equipe 1** coloca o sensor sobre uma cor (vermelho, verde ou azul) e aperta o botão.  
   - A cor é registrada como o “navio escondido” da equipe.  
   - Um LED confirma que a escolha foi guardada.  

2. **Equipe 2** coloca o sensor sobre uma cor e aperta o botão para tentar adivinhar.  
   - Se acertar: acende o LED verde ✅ e aparece mensagem de acerto.  
   - Se errar: acende o LED vermelho ❌ e aparece mensagem de erro.  

3. O turno alterna entre as equipes até o fim da partida.

---

## 🔧 Componentes necessários
- 1x Arduino UNO (ou compatível)  
- 1x Sensor de cor **TCS230/TCS3200** ou **Adafruit TCS34725**  
- 1x Botão (push button)  
- 5x LEDs (R, G, B, OK, Erro)  
- Resistores (220Ω ou 330Ω) para cada LED  
- Jumpers e protoboard  

---

## ⚡ Ligações (Exemplo com Arduino UNO)
- **Sensor TCS230/TCS3200**  
  - S0 → pino 4 
  - S1 → pino 5  
  - S2 → pino 6  
  - S3 → pino 7  
  - OUT → pino 8  

- **Botão** → pino 2 (com `INPUT_PULLUP`)  

- **LEDs**  
  - Vermelho → pino 9  
  - Verde → pino 10
  - Azul → pino 11
  - LED OK → pino 12  
  - LED Erro → pino 13  

---

## 📜 Código
No repositório você encontrará duas versões:  
- `batalha_rgb_tcs230.ino` → código para o sensor TCS230/TCS3200.  
- `batalha_rgb_tcs34725.ino` → código para o sensor Adafruit TCS34725.  

O funcionamento é o mesmo, muda apenas a biblioteca e a forma de ler os valores RGB.

---

## 🖥️ Saída no Serial
Exemplo de mensagens durante o jogo:
=== Batalha Naval RGB ===
Equipe 1 começa!
Coloque o sensor na cor desejada e aperte o botão.
Cor Guardada com sucesso!
Agora é a vez da Equipe 2! Coloque o sensor sobre a cor e aperte o botão.
Equipe 2 tentou a cor: VERMELHO
❌ Errou a cor!
Agora é a vez da Equipe 1 novamente!


---

## 🚀 Possíveis melhorias
- Adicionar **sistema de pontuação** para cada equipe.  
- Usar **buzzer** para sons de acerto/erro.  
- Criar **tempo limite** para as jogadas.  
- Integrar com uma interface visual no navegador (já temos um protótipo em HTML/JS).  

---

## 📚 Créditos
Projeto desenvolvido para fins educativos na **Sala Maker**, gamificando sensores e Arduino para crianças de 7 a 11 anos.  
Professor responsável: **Jhonatan** 👨‍🏫  

