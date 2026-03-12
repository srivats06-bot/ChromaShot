# RGB Shooter

A fast-paced **2D top-down shooter** built with **Unity and C#** where players must match their weapon color with enemy colors to defeat them.

The game introduces a unique twist: **shooting enemies with the wrong color makes them stronger**, forcing players to constantly adapt during combat.

## Live Stats

* Published online
* **300+ plays on CrazyGames**

---

## Gameplay Overview

In **RGB Shooter**, enemies spawn in **Red, Green, and Blue variants**. The player must switch their weapon color to match the enemy color.

* Correct color → enemy takes damage
* Wrong color → enemy **gains health and increases in size**

This mechanic encourages **fast reactions and strategic weapon switching**.

---

## Features

### Color-Based Combat System

* Enemies spawn with RGB colors
* Player can dynamically switch weapon colors
* Incorrect color attacks increase enemy health and size

### Dynamic Enemy Behavior

* Enemy difficulty scales based on player mistakes
* Larger enemies become harder to defeat

### Modular Powerup System

Implemented using **ScriptableObjects** for easy expansion.

Examples include:

* Grenades
* Combat modifiers
* Player upgrades

### Inventory System

* **9-slot inventory**
* Items stack automatically
* New item types fill the next available slot

### Shop System

* Players can purchase powerups
* Purchased items persist between scenes
* Shop UI dynamically displays item information



## 🛠 Tech Stack

**Engine**

* Unity (2D)

**Languages**

* C#

**Architecture**

* ScriptableObject-based modular systems
* Event-driven gameplay systems
* Component-based Unity architecture

**Tools**

* Unity Editor
* Visual Studio
* Git / GitHub



---

## Core Systems

### Color Matching Mechanic

The player's weapon color is compared to the enemy color.

Matching color:

* Enemy takes damage

Wrong color:

* Enemy gains health
* Enemy increases in size

This forces players to **quickly prioritize targets and switch weapons efficiently**.

---

### ScriptableObject Powerup System

```csharp
public abstract class PowerupEffect : ScriptableObject
{
    public string powerupName;
    public string description;
    public int cost;
    public Sprite icon;

    public abstract void Apply(GameObject target);
}
```

This design allows **new powerups to be added without modifying existing systems**.

---

##  Controls

| Key        | Action              |
| ---------- | ------------------- |
| WASD       | Move                |
| Mouse      | Aim                 |
| Left Click | Shoot               |
| Color Keys | Switch weapon color |
| E          | Open Inventory      |

---

## Future Improvements

* Additional enemy types
* Boss encounters
* More powerups
* Procedural room generation
* Leaderboards

---

## Author

**Srivatsan Narasimhan**
