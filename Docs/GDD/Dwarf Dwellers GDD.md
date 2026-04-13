## 🎮 Dwarf Dwellers — Game Design Document (v0.1)

### 📌 Visão Geral

Roguelike 2D de ação com exploração vertical e horizontal, inspirado em jogos como _Caveblazers_ e _Noita_, onde o jogador controla anões exploradores em cavernas geradas proceduralmente, enfrentando inimigos, minerando o ambiente e criando builds únicas a cada run.

- Engine: Unity
- Art design: Aseprite
- Art style: 2d pixel art

---
## 🔁 Core Gameplay Loop

1. Entrar na dungeon (run)
2. Explorar e cavar o ambiente
3. Encontrar loot / POIs
4. Enfrentar inimigos
5. Melhorar build durante a run
6. Avançar para próxima área (Boss protegendo a entrada de cada área)
7. Morrer → reiniciar com aprendizado/meta progressão (futuro - possível Final Boss)

---
## 🌍 Estrutura de Fases

Cada capítulo possui 3 originalmente biomas:

1. **Cave Entrance**
    - Mais aberto
    - Inimigos mais fracos
    - Introdução ao run
2. **Underground**
    - Mais fechado
    - Mais inimigos
    - POIs mais frequentes
3. **Caverns**
    - Verticalidade maior
    - Perigos ambientais
    - Possível boss

- Armadilhas (spikes, gás, lava) ?
- Elementos destrutivos com física simples ?

---
## ⛏️ Mecânica de Mineração

- Todos personagens podem cavar
- Tiles possuem resistência
- Possível:
    - Drop de recursos
    - Abrir caminhos alternativos
    - Criar estratégia (fugir, emboscar, colapso)

- Mineração pode revelar:
    - Salas secretas
    - Relíquias
    - Perigos (colapso)

---
## 🧙 Classes Jogáveis (Originalmente)

### ⛏️ Miner

- Alta resistência
- Melhor mineração
- Combate melee
- Pode quebrar tiles mais duros
- Chance de loot extra ao minerar

---
### 💣 Sapper

- Especialista em explosivos
- Controle de grupo
- Pode alterar terreno rapidamente
- Sinergia com ambiente destrutível

---
### 🔫 Specialist

- Alto dano à distância
- Baixa resistência
- Mecânica de munição limitada
- Headshots / crítico

---
## 🎒 Inventário

### Slots:

- Picareta (fixo)
- 2 armas (classe)
- Skill ativa (classe)
- Capacete
- Armadura
- Botas
- 2 Anéis
- Artefato (build defining - itens raros e únicos)

- 💡slots limitados → decisões estratégicas

---
## ⚔️ Combate

Definir:

- Hitbox simples
- Knockback
- “Feel” pesado (impacto dos golpes)
- Feedback visual (hit flash, screen shake leve)

---
## 👹 Inimigos

Tipos atuais:

- Orcs
- Goblins
- Cultistas
- Anões corrompidos
- Chefões finais entre cada bioma (loot pool única)

### 💡 Sugestão:

Separar por função:

- Melee rush
- Ranged
- Tank
- Suporte (cura/buff)

---
## ☠️ Morte e Progressão

- Perde tudo ao morrer.
- Existe meta progressão (usando o ouro adquirido nas runs).
- Unlock de itens
- Novas classes
- Cosméticos
- Melhorias permanentes (ligar/desligar)

---
## 🎲 Procedural / Seed

- Mapas gerados por seed
- POIs distribuídos proceduralmente

### 💡 Sugestão:

- Seeds compartilháveis (legal pra comunidade)

---
## 🎚️ Dificuldade

Já definido:

- Easy (-25%)
- Normal
- Hard (+25%)

### 💡 Sugestão:

Adicionar:

- Modificadores (tipo Hades)
- Ex: inimigos mais rápidos
- Menos loot

---
### 🔥 1. Sistema de Colapso

- Cavar errado → teto cai
- Pode matar inimigos OU player

### 🔥 2. Builds insanas

- Artefatos que mudam gameplay:
	- “Explosões causam chain reaction”
	- “Tiros ricocheteiam”
	- "Equipe mais 1 anel"

### 🔥 3. Interação com ambiente

- Explodir chão → inimigos caem
- Criar atalhos
- Sangue e detrito

---
# 🧩 4. Próximo passo (prático no Unity)

## 🎯 Protótipo v0.1 (mínimo viável)

Faça APENAS isso:

- Player anda (A/D)
- Pula
- Cava bloco
- Mapa simples destrutível (tilemap)
- 1 inimigo básico
- 1 arma
# ⚙️ Stack recomendada (Unity)

- Tilemap + Grid
- Script de destruição de tiles
- Rigidbody2D + Collider2D
- Script básico de combate