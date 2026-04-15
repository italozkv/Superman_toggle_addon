# 🦸 Superman Toggle Addon

![Minecraft](https://img.shields.io/badge/Minecraft-1.20.1-green)
![Forge](https://img.shields.io/badge/Forge-47.4.10-orange)
![Version](https://img.shields.io/badge/version-1.0.0-blue)
![Status](https://img.shields.io/badge/status-in%20development-yellow)
![License](https://img.shields.io/badge/license-All%20Rights%20Reserved-red)

Addon avançado para o mod **Superman (2.1.5+)** que melhora controle, balanceamento e imersão dos poderes, sem modificar diretamente o mod original.

---

## 📖 Visão Geral

O **Superman Toggle Addon** é um mod Forge para **Minecraft 1.20.1** que intercepta e aprimora sistemas do mod Superman, oferecendo:

- Controle manual de habilidades  
- Rebalanceamento completo de combate  
- Sistema avançado de energia solar  
- Melhorias visuais e animações  
- Ajustes profundos de gameplay  

---

## ✨ Funcionalidades

### 🎮 Controle de habilidades
- Toggle de **super corrida** (`O`)  
- Toggle de **voo por duplo toque no pulo**  
- Controle manual dos poderes  

---

### ⚔️ Rebalanceamento de combate

| Tipo        | Multiplicador | Dano mínimo |
|------------|--------------|------------|
| Mob        | 2.6x         | 1.5        |
| Player     | 3.2x         | 2.0        |
| Projétil   | 2.25x        | 1.5        |

- Remove invulnerabilidade absoluta  
- Aplica resistência controlada  
- Garante dano mínimo  

---

### ☀️ Sistema de energia solar

- Consumo contínuo por poderes ativos  
- Dreno ao receber dano  
- Recarga baseada em ambiente  

#### 🏔️ Bônus por altitude
- Y ≥ 300 → +0.01  
- Y ≥ 500 → +0.02  
- Y ≥ 1000 → +0.035  

---

### ❤️ Cura e fome
- Cura solar reduzida (`0.35x`)  
- Fome normal abaixo de Y 1000  
- Saturação não infinita  

---

### 💥 Combate físico
- Knockback reduzido e controlado  
- Custo solar por ataque  
- Durabilidade de armas aplicada  

---

### 🔥 Heat Vision customizada
- Render totalmente substituído  
- 🔴 Twin (vermelho)  
- 🔵 Focused (azul)  
- Colisão com blocos + efeitos visuais  

---

### 🧍 Animações
- Nova pose de **LIFT**  
- Mais natural e imersiva  

---

## ⚙️ Arquitetura

### 📂 Core
- `SupermanToggleAddon.java`
- `CommonEvents.java`
- `SupermanToggleConfig.java`
- `SupermanReflection.java`

### 🎨 Client
- `ClientEvents.java`
- `HeatVisionRenderOverride.java`
- `LiftPoseOverride.java`

---

## 🔌 Dependências

- Minecraft **1.20.1**
- Forge **47.4+**
- Mod **Superman 2.1.5+**

---

## 🧠 Integração

O addon utiliza:
- Eventos Forge  
- Pacotes de rede  
- Reflexão interna  

⚠️ Pode quebrar se o mod Superman mudar internamente.

---

## 🔄 Fluxo técnico

1. Tick inicia  
2. Estado salvo  
3. Addon intercepta  
4. Recalcula:
   - dano  
   - energia  
   - cura  
   - fome  
5. Cliente aplica efeitos  

---

## 🌍 Balanceamento

- Superman forte, mas não invencível  
- Energia limitada  
- Regeneração reduzida  
- Nether sem recarga solar  

---

## ⚠️ Limitações

- Estado de corrida não persistente  
- Dependência de reflexão  
- Algumas mudanças são apenas visuais  

---

## 🛠️ Build

```bash
./gradlew build
