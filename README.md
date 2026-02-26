# Modern Greeting Web App

A minimal, modern greeting web application with celebratory background animations (confetti, party popper burst, and glowing energy pulse).

## Features

- **Centered UI**: Clean, card-based layout centered on the screen.
- **Greeting flow**:
  - Label: **"Enter Your Name"**
  - Text input with placeholder: **"Type your name here"**
  - Button: **"Greet"**
  - Dynamic greeting text shown below the button.
- **Animations**:
  - Three different background effects:
    - Confetti fall
    - Party-popper radial burst
    - Soft glowing burst
  - **Only one animation runs at a time**; the previous one is cleared before the next starts.
  - Each button click randomly triggers one of the three animations.
- **Keyboard friendly**: Press **Enter** in the text box to trigger the greeting.

## Getting Started

You can either open the app directly in a browser or run it with a tiny dev server.

### Option 1 – Open `index.html` directly

1. Navigate to the project folder:
   - `c:\Users\junai\OneDrive\Desktop\SAAS\`
2. Double-click `index.html` or open it in your browser of choice.

### Option 2 – Run with Node + live-server

1. Make sure you have **Node.js** installed.
2. In a terminal, from the `SAAS` directory, install dependencies:

   ```bash
   npm install
   ```

3. Start the dev server:

   ```bash
   npm run dev
   ```

4. Your browser should open automatically at `http://localhost:5173` with the greeting app.
5. I have deployed it on vercel (https://simple-greet-app.vercel.app)

## How It Works

- **UI & layout** are defined in `index.html` and `styles.css`.
- **Behavior & animations** are controlled from `script.js`:
  - The button click (or pressing Enter) updates the greeting text.
  - A random animation is selected from three factory functions.
  - Each animation returns a cleanup function so the JS can **stop and remove the previous animation** before starting another, ensuring no overlaps.

