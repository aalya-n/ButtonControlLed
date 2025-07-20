# Button-Controlled LED 💡

This is a simple Arduino project by **Aalya Nahhas** that demonstrates how to control an LED using a push-button.

When the button is pressed, the LED turns on. When the button is released, the LED turns off. This is a great beginner-friendly project to understand basic digital input and output with an Arduino.

---

## 🔧 Components Used

- Arduino Uno
- Breadboard
- 1x LED
- 1x 220Ω resistor
- 1x Push button
- Jumper wires

---

## ⚡ Circuit Diagram


Or you can refer to a diagram made in Tinkercad or Fritzing if available.

---

## 🧠 How It Works

- The button is connected to a digital pin.
- When the button is pressed, it sends a **HIGH** signal to the Arduino.
- The Arduino detects this and sets the LED pin to **HIGH**, turning on the LED.

---

## 💻 Arduino Code

```cpp
const int buttonPin = 2;     // Button connected to digital pin 2
const int ledPin = 13;       // LED connected to digital pin 13

void setup() {
  pinMode(buttonPin, INPUT);
  pinMode(ledPin, OUTPUT);
}

void loop() {
  int buttonState = digitalRead(buttonPin);

  if (buttonState == HIGH) {
    digitalWrite(ledPin, HIGH);  // Turn LED on
  } else {
    digitalWrite(ledPin, LOW);   // Turn LED off
  }
}
