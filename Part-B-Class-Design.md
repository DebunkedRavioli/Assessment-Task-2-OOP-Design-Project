# Part B – Object-Oriented Design

## Classes

### Class 1: Car

Attributes:
- make: String
- model: String
- year: int
- horsepower: int
- topSpeed: int
- acceleration: float
- fuelEfficiency: float
- safetyRating: float
- marketValue: float

Methods:
+ getDetails(): String
+ compareAttribute(attribute: String): float

Role: Stores all data for a real-world vehicle, including performance, safety, efficiency and market data used during gameplay.

---

### Class 2: Card

Attributes:
- cardID: int
- car: Car

Methods:
+ displayCard(): void

Role: Represents a playable card in the game. Each Card contains one Car object and is what players hold in their hand.

---

### Class 3: Deck

Attributes:
- cards: ArrayList<Card>

Methods:
+ shuffle(): void
+ dealCard(): Card

Role: Stores the full collection of Cards before the game starts. Responsible for shuffling and distributing cards to players.

---

### Class 4: Player

Attributes:
- name: String
- hand: ArrayList<Card>

Methods:
+ playCard(): Card
+ receiveCard(card: Card): void

Role: Represents a human player. Holds a hand of Cards and makes decisions during each round.

---

### Class 5: Game

Attributes:
- players: ArrayList<Player>
- deck: Deck
- currentRound: int

Methods:
+ startGame(): void
+ determineWinner(): Player
+ endGame(): void

Role: Controls the overall game flow. Manages rounds, enforces rules, and determines the final winner.