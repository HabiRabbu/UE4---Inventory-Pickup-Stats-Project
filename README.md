# UE4---Inventory-Pickup-Stats-Project

# Project Overview

This project is an advanced inventory system with an integrated HUD and Main Menu. Each section, Main Menu, HUD, and Inventory, is carefully designed to offer intuitive user interaction and a seamless game experience.

## Main Menu Design
The primary entrance to the game is facilitated through the MainMenu Widget, activated once the “Main” level commences. The main menu is user-friendly with various buttons that provide the options such as:

Settings Menu: Allows players to adjust game resolution.
Help Menu: Provides insights on HUD and Inventory usage.
Play & Quit: Either progresses to the main game level or exits the application.


## HUD Design
The HUD Widget primarily deals with:

Displaying the selected weapon on the weapon bar.
Showcasing Health/Hunger bars and ammo to the player.
Responding to events like PlayerEat and HungerTimer.
Moreover, the FirstPersonCharacter BP manages the initiation of HUD elements, Health/Hunger alterations, Ammo updates, and pause menu interactions. While in the pause mode, time halts and the PauseMenu Widget is showcased, adjusting view mode and mouse input accordingly.


## Inventory Design
The Inventory System leverages a Linked List Inheritance Data Structure, initiating with the FItemStruct.


### Key Features:

FItemStruct encapsulates properties that create an item and determines how they're presented within the Inventory.
Item details are fed into ItemData database, ensuring a smooth categorization.
Interactions with items and inventory management are overseen by the InventorySystem BP.
Advanced interactions like moving items between inventories, dropping, or consuming are also integrated into the system.
The layout of Inventory widgets is streamlined, featuring PlayerMenu Widget > InventoryGrid widget > InventorySlot widgets, which furnish players with item-specific details.
A specialized interaction mechanism exists for chests, wherein the Inventory System also creates the Chest’s inventory, thus promoting reusable design components.


## Limitations
While the current Inventory system manages Items like Food, Health Packs, and Ammo efficiently, there's scope for improvement:

A dedicated Weapon struct, inherited from ItemStruct, would optimize the system, especially for weapon selection and management.


## Future Additions
The future roadmap aims to incorporate:

Weapon Struct and Weapon Data Table: A derivative from ItemStruct, this will facilitate specialized weapon attributes like meshes, animations, projectiles, and attacks without relying on hardcoded elements.
Modular Weapon Hotbar: An adaptive hotbar design that can accommodate a multitude of weapons.
