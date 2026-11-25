# PhysiCnight

## 1. General Overview

- **Genre:** Action
- **Platform:** PC (Windows/Linux/MacOS)
- **Multiplayer:** 1v1 online
- **Key idea:** Two players compete on an arena with obstacles; weapon strikes and movement obey physics.

## 2. Gameplay

### 2.1 Main game stages
1. **Main menu**
   - Room ID input field.
   - **Play!** button to create or join a room.

2. **Loadout selection**
   - One weapon is selected for the **right** and **left** hand.
   - 5 weapon types are available:
     - Sword
     - Hammer
     - Spear
     - Alternative spear
     - Shield
   - Map selection.
   - **To Battle!** button — proceed to battle.

3. **Battle**
   - Two players spawn on the map.
   - Weapons have their own physics.
   - Damage is calculated from weapon speed on impact.
   - Weapon collisions knock the attack away.
   - The player who dies fewer times wins.
   - Alongside the fight, players dodge obstacles.
   - Some weapons will change the strike type when several strikes are performed in a short time.

## 3. Combat Mechanics

| Element | Description |
|----------|------|
| **Physics** | Unity Rigidbody + Collider + Joints. Strike force = movement impulse. |
| **Weapons** | Reacts to collisions with another weapon or a body. |
| **Damage** | Proportional to weapon speed at the moment of impact. |
| **Character movement** | WASD movement, mouse aiming, strike with mouse buttons |
| **Player death** | When HP reaches 0. |

## 4. Map

**A typical arena contains:**
- **Delayed-action mine**
  - Activates on contact.
  - Emits a discharge after a few seconds.
  - Deals damage to everyone who touches it.
- **Spiked spheres**
  - Move along a set trajectory.
  - Deal damage and push the player away on collision.
- **Obstacles / walls**
  - Stationary objects that block movement.
  - Used as cover.
- **Spikes**
  - Activate every few seconds.
  - Deal damage to everyone who touches them while active.

## 5. User Interface (UI / UX)

| Screen | Elements |
|--------|-----------|
| **Main menu** | `Room ID` field, **Play!** button |
| **Loadout selection** | Dropdown for both hands and the map, **To Battle!** button |
| **Arena** | HP panel, timer, score. | _Todo_

## 6. Technical Part

| Component | Technology |
|------------|-------------|
| **Engine** | Unity |
| **Networking** | Photon Networking |
| **Physics** | Unity Physics / Rigidbody2D |
| **Animations** | Physically simulated |
| **Map** | GameObjects, tiling textures |

## 7. Game Features

- Realistic combat physics: speed = damage.
- Weapon-to-weapon interaction (blocking, ricochets).
- Maps with active traps that add chaos.
- Simple start: just a Room ID and two (2+) clicks to battle.

## 8. Future Ideas

- New maps and weapons
- Physics improvements (specifically weapon control)
- Room selection
- Team battles
- Alternative strikes / abilities
- Pick-up powerups
- Character / armor selection

---

# PhysiCnight

## 1. Загальний опис  

- **Жанр:** Action
- **Платформа:** PC (Windows/Linux/MacOS)  
- **Мультиплеєр:** 1v1 онлайн  
- **Ключова ідея:** Двоє гравців змагаються на арені з перешкодами, удари зброї та рух підкоряються фізиці.

## 2. Геймплей

### 2.1 Основні етапи гри
1. **Головне меню**
   - Поле для введення Room ID.  
   - Кнопка **Play!** для створення або приєднання до кімнати.  

2. **Вибір спорядження**
   - Обирається по одній зброї для **правої** та **лівої руки**.  
   - Доступно 5 тиів зброї:
     - Меч
     - Молот
     - Спис 
     - Альтернативний спис
     - Щит 
   - Вибір карти.  
   - Кнопка **To Battle!** — перехід у бій.

3. **Бій**
   - Двоє гравців з'являються на карті.  
   - Зброя має власну фізику.  
   - Шкода розраховується від швидкості зброї при ударі.  
   - Зіткнення зброї відштовхує атаку.  
   - Перемагає гравець, який помер менше разів.
   - Паралельно з боєм гравці ухиляються від перешкод.
   - Деяка зброя буде змінювати тип удару при виконанні декількох за короткий час

## 3. Механіки бою

| Елемент | Опис |
|----------|------|
| **Фізика** | Unity Rigidbody + Collider + Joints. Сила удару = імпульс руху. |
| **Зброя** | Реагує на зіткнення з іншою зброєю або тілом. |
| **Шкода** | Пропорційна швидкості зброї під час удару. |
| **Рух персонажа** | переміщення WASD, наведення мишею, удар кнопками миші |
| **Смерть гравця** | Коли HP рівне 0. |

## 4. Карта

**Типова арена містить:**
- **Міна сповільненої дії**
  - Активується при контакті.  
  - Випускає розряд через кілька секунд.  
  - Наносить шкоду всім хто торкається.
- **Шпичасті сфери**
  - Рухаються по заданій траєкторії.  
  - Наносять шкоду і відштовхують гравця при зіткненні.  
- **Перешкоди / стіни**
  - Стаціонарні об’єкти, що блокують рух.  
  - Використовуються як укриття.
- **Шипи**
  - Активуються кожні кілька секунд.
  - Наносять шкоду всім хто їх торкається коли активні

## 5. Інтерфейс користувача (UI / UX)

| Екран | Елементи |
|--------|-----------|
| **Головне меню** | Поле `Room ID`, кнопка **Play!** |
| **Вибір спорядження** | Dropdown для обох рук та карти, кнопка **To Battle!** |
| **Арена** | Панель HP, таймер, рахунок. | _Todo_

## 6. Технічна частина

| Компонент | Технологія |
|------------|-------------|
| **Движок** | Unity |
| **Мережа** | Photon Networking |
| **Фізика** | Unity Physics / Rigidbody2D |
| **Анімації** | Фізично симульовані |
| **Мапа** | GameObjects, циклічні текстури |

## 7. Особливості гри

- Реалістична бойова фізика: швидкість = шкода.  
- Взаємодія зброї між собою (блокування, рикошети).  
- Карти з активними пастками, що додають хаосу.  
- Простий старт: тільки Room ID і два (2+) кліки до бою.  

## 8. Подальші ідеї

- Нові карти та зброя
- Покращення фізики (конкретно контролю над зброєю)
- Вибір кімнат
- Командні бої
- Альтернативні удари / здібності
- Pick-up powerups
- Вибір персонажів / броні
