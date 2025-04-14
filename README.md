# Win-Lose-Stay-Shift RPS AI (Arduino)

An Arduino-based Rock-Paper-Scissors (RPS) game where the Arduino uses strategic prediction to defeat a human opponent. This project features real-time gameplay with physical button inputs and LED indicators, and implements multiple predictive algorithms to adapt to the player's behavior.

---

## 🎮 Game Overview

This system simulates a turn-based RPS match between:
- **Player**: Presses buttons to input Rock, Paper, or Scissors.
- **Arduino**: Uses strategies like **Win-Stay Lose-Shift**, **Beat Last Input**, and **Play Last Input** to make predictions and counter the player.

---

## 🧠 AI Strategies Implemented

- **Win-Stay Lose-Shift (WSLS):** Repeat your move if you won, switch if you lost.
- **Beat Last Input (BLI):** Predict the player will counter the Arduino's last move, so it counters back.
- **Play Last Input (PLI):** Predicts the player will repeat Arduino's last move.

The Arduino evaluates how likely the opponent is using each strategy based on past rounds, estimates the probabilities, and plays the counter move with the highest expected success rate.

---

## ⚙️ Hardware Setup

| Component         | Pin       | Description                           |
|------------------|-----------|---------------------------------------|
| **BTN1**         | D3        | Paper button (top left)               |
| **BTN2**         | D4        | Scissors button (bottom right)        |
| **BTN3**         | D5        | Turn start / End round                |
| **BTN4**         | D2        | Rock button (top right)               |
| **LED1 - LED5**  | D12 - D8  | Status indicators (from left to right)|

---

## 🗂️ File Structure

- `main.ino` – Main Arduino code (you may rename this)
- Handles game logic, AI, LED control, and input reading

---

## 💡 LED Behavior

- **Blinking LEDs**: Waiting for input or in transition
- **LED1 ON**: Arduino won the round
- **LED5 ON**: Opponent won the round
- **LED1 + LED5 ON**: Draw
- **LED combinations**: Show AI’s selected move

---

## 🧪 Example AI Behavior

If in round 1 the Arduino chooses Rock and loses, and in round 2 the player chooses Paper (to beat Rock), the Arduino may predict the player is using **Beat Last Input**, and respond with Scissors in round 3 to beat their Paper.

---

## ▶️ How to Play

1. Upload the code to your Arduino.
2. Connect buttons and LEDs as described above.
3. Press **Turn Button (BTN3)** to start a round.
4. Arduino chooses and displays its move.
5. Player selects their move using **Rock, Paper, or Scissors buttons**.
6. Outcome is shown via LEDs.
7. Press **Turn Button** again to proceed to the next round.

---

## 📦 Dependencies

- Arduino UNO (or similar)
- 5 push buttons
- 5 LEDs with resistors
- Breadboard & jumper wires

---

## 👤 Author

Armaan Singla  
Computer Engineering @ Queen’s University  
[GitHub Profile](https://github.com/armaansingla14)

---

## 🧠 Educational Value

This project combines:
- Game theory and strategy modeling
- Embedded systems (Arduino)
- Real-time user interaction
- Data-driven prediction on low-resource hardware

Great for exploring how **machine learning-inspired logic** can run even on simple microcontrollers.

