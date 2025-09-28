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
2.	git clone https://github.com/your-username/unity-slot-machine.git
3.	Open the project in Unity (2021.3+ recommended).
4.	Inside Unity:
  o	Create a Canvas for UI.
  o	Add UI elements:
    - Buttons: Spin, Reset
    -	Toggle: Auto-Spin, SFX
    -	InputField: Bet amount
    -	TextMeshPro Texts: Balance, Bet, Win info
  o	Assign them to the GameManager script in Inspector.
5.	Set up SymbolPrefabs:
  o	Create prefab(s) with SpriteRenderer or Image component.
  o	Assign in GameManager’s symbols array.
6.	Add Audio Sources to GameManager:
  o	Drag in clips for Spin, Win, Jackpot, Out-of-Credits, BGM.
7.	Test in Play Mode

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
