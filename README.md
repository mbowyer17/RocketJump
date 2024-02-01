<h1>Rocket Jump - First-Person </h1>

 ### [Vimeo Demonstration](https://vimeo.com/888274604)

<h2>Description</h2>
The sole means of survival when trapped in a chamber with nothing but a rocket launcher is to outfit yourself with rocket-resistant footwear and use the launcher to avoid the traps. The quick-fire first-person shooter mechanic from Team Fortress 2 and Quake served as the model for this project. I was surprised that no game was using this idea as the primary feature of their game, as it represented a gap in the market. To develop this project, I used blueprints and Unreal Engine C++.
<br />


<h2>Features and Utilities Used</h2>

- <b>Character Controller</b>

This script defines the behaviour and mechanics of a player character. Using keyboard inputs, the character can move forward, backward, strafe left, and strafe right, while the camera follows the character's movements. The camera view is controlled by mouse input, allowing the player to look about. Jumping is possible with a specific button push, utilising the built-in mechanics for character hopping in Unreal Engine. In addition, the character can shoot by spawning projectiles from its position to imitate shooting. Notably, while in mid-air, the character can strafe left and right, creating a dynamic and responsive control experience. Input actions and axes are effectively connected to their respective functions, enabling straight forward control via keyboard and mouse inputs. This script initializes the character with default values and essential components, including the camera and spring arm, while also offering customization options such as the AirStrafeSpeed property to fine-tune air strafing behaviour.

- <b>Rocket projectile</b>

In the game, the RocketProjectile represents a dynamic rocket that changes its behaviour with each game tick. When activated, this rocket has a spherical collision component that allows it to detect and respond to interactions with other game objects. It has an initial and maximum speed of 1000.0 units, and a damage radius of 300.0 units by default. When the rocket collides with another object, it calculates the distance and relative Y-position of the impact if that object is a character. Using this information, the rocket calculates the launch power, emphasising a stronger upward force if the rocket's impact is from below the character. The player is then propelled in the opposite direction as the rocket explodes. If the rocket does not directly hit a character but is nearby when it explodes, it searches for any characters within its damage radius and launches them in the opposite direction. This ensures that the rocket not only affects characters when they come into direct contact with it, but also has an area of effect influence, making it a strategic element in gameplay.

- <b>Launch Pad</b>

In Unreal Engine 5, the script introduces a "LaunchPad" actor written in C++. When you place this actor in a level, it has a collision area that is represented as a box component. If the player's character collides with or enters this box, the LaunchPad detects the event and responds by launching the character into the air. The magnitude of this launching force can be adjusted via the LaunchStrength property, allowing for customization of how strong or powerful the launch effect is. This script essentially creates a dynamic platform that, when interacted with, propels game characters upward, introducing a gameplay mechanic similar to trampolines or jump boosts in other games.

- <b>Dead Zone</b>

In this Unreal Engine example, I used C++ to create a "DeadZone" actor. When a player character enters the collision box associated with this actor, a function is triggered that teleports the player character to a predefined spawn location.

<h2>Technologies Used </h2>

- <b>C++</b> 
- <b>Unreal Engine 5</b> 

<h2>Feature Showcase:</h2>

<p align="center">
Projectile Weapon: <br/>
<img src="https://i.imgur.com/Lddq93a.png" height="80%" width="80%" alt="ProjectileWeapon"/>
<br />
<br />
UI Blueprint:  <br/>
<img src="https://i.imgur.com/GYVP0oX.png" height="80%" width="80%" alt="ProjectileWeapon"/>
<br />
<br />
Puzzle 1: <br/>
<img src="https://i.imgur.com/BOzDwVG.png" height="80%" width="80%" alt="ProjectileWeapon"/>
<br />
<br />
Puzzle 2:  <br/>
<img src="https://i.imgur.com/MH3OUkv.png" height="80%" width="80%" alt="ProjectileWeapon"/>
<br />
<br />
Puzzle 3: <br/>
<img src="https://i.imgur.com/RxEAMt1.png" height="80%" width="80%" alt="ProjectileWeapon"/>
<br />
<br />
Puzzle 4:  <br/>
<img src="https://i.imgur.com/EolQ1TF.png" height="80%" width="80%" alt="ProjectileWeapon"/>
<br />
<br />
Puzzle 5:  <br/>
<img src="https://i.imgur.com/dKqKTQn.png" height="80%" width="80%" alt="ProjectileWeapon"/>
</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
