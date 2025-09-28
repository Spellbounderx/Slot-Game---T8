🎰 Unity Slot Machine Game

A simple 3x3 slot machine game built with Unity. 
This project demonstrates Unity fundamentals like UI handling, game logic, audio, persistence (PlayerPrefs), and optional 
features such as Auto-Spin and Jackpot detection.

📌 Features

•	Spinning Reels – Random symbols appear on a 3x3 grid.

•	Balance & Bets – Players can place bets, win payouts, and manage balance.

•	Sound Effects & Music – Toggle-able SFX and background music.

•	Auto-Spin Mode – Optional feature for continuous spins until stopped.

•	Jackpot Detection – Rewards players when all rows match jackpot symbols.

•	Persistence – Balance, last bet, and audio toggle are saved across sessions using PlayerPrefs.

•	Reset Option – Reset stored balance and settings when needed.

🏗️ Architecture

•	GameManager (MonoBehaviour)

    o	Controls spins, checks wins/jackpots, updates balance.
  
    o	Connects to UI, Audio, Persistence.
    
•	GameBoard (GameObject)

    o	3x3 grid of slots.
    
    o	Populates with SymbolPrefab instances.
    
•	SymbolData (ScriptableObject)

    o	Holds symbol name, icon, payout multiplier.
    
•	UI Layer

    o	Spin Button
    
    o	Auto-Spin Toggle
    
    o	Bet Input Field
    
    o	Balance/Win Display Texts
    
    o	Reset Button
  
•	Audio System

    o	SFX: spin, win, jackpot, no credits.
    
    o	Background music loop.
    
    o	Controlled by GameManager.
    
•	Persistence Layer (PlayerPrefs)

    o	Stores: Balance, Last Bet, Auto-Spin state, SFX toggle.
    
    o	Reset option clears saved values.

🛠️ How to Set Up

1.	Clone this repository:
   
3.	git clone https://github.com/Spellbounderx/Slot-Game---T8.git
   
5.	Open the project in Unity (2021.3+ recommended).
   
7.	Inside Unity:

  o	Create a Canvas for UI.
  
  o	Add UI elements:
  
    -   Buttons: Spin, Reset
    -	Toggle: Auto-Spin, SFX
    -	InputField: Bet amount
    -	TextMeshPro Texts: Balance, Bet, Win info
    
  o	Assign them to the GameManager script in Inspector.
  
9.	Set up SymbolPrefabs:

  o	Create prefab(s) with SpriteRenderer or Image component.
  
  o	Assign in GameManager’s symbols array.
  
10.	Add Audio Sources to GameManager:

  o	Drag in clips for Spin, Win, Jackpot, Out-of-Credits, BGM.
  
12.	Test in Play Mode

🎮 Controls

    •	Spin: Spins reels once.
    
    •	Auto-Spin: Continuously spins until toggled off.
    
    •	Bet Input: Set bet amount.
    
    •	Balance Display: Shows remaining credits.
    
    •	Reset Button: Resets saved balance and settings.
    
    •	SFX Toggle: Turns game sounds on/off.

🚀 Future Improvements

•	Add more animation in the reel and overall game.

•	More complex jackpot patterns (diagonals, bonus rounds).

•	Multiple paylines.

•	Database or cloud persistence instead of PlayerPrefs.

•	Skins & themes for symbols and backgrounds.

👾 Third-Party Assets and Credits:

- Background music and audio from:

        YouTube Video: https://www.youtube.com/watch?v=Xa2tDZxnm6w
        YouTube Video / Playlist: https://www.youtube.com/watch?v=-lbbHQbZNKg&list=RD-lbbHQbZNKg&start_radio=1
  
- Icons from Unity Asset Store: Fantasy Status Icons

        URL: https://assetstore.unity.com/packages/2d/gui/icons/fantasy-status-icons-265728

🤖 Known Issues:

- Jackpot may feel rare depending on symbol probability weights; requires careful balancing of SymbolData values.

- Only the center row is currently checked for wins; additional paylines are not yet supported.

- If symbols are not correctly assigned to prefabs or missing in the inspector, spins may fail to display results.

- Persistence relies on PlayerPrefs, which can be cleared manually outside the game and is not secure for production use.

- UI scaling may need adjustment on different resolutions and aspect ratios.

- No complex animations beyond symbol respawning.

