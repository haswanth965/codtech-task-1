# codtech-task-1
 
COMPANY: CODTECH IT SOLUTIONS

NAME:HASWANTH REDDY GOGIREDDY

INTERN ID:CT04DF1989

DOMAIN: Embedded Systems

DURATION: 4 WEEKS

MENTOR: Neela Santhosh Kumar

DESCRIPTION: The Push Button Counter is a simple embedded systems project where a digital counter increases each time a button is pressed. It uses a microcontroller like Arduino to read the push button input and display the count on an LCD or OLED screen. A pull-down resistor is used to ensure stable input readings. Debouncing is implemented in code to prevent false triggering. This project helps in understanding digital input, output display interfacing, and basic programming logic. It is commonly used in applications like people counters, product counting systems, and digital scoreboards. It’s an ideal beginner-level project in electronics.

CIRCUIT DIAGRAM:

![WhatsApp Image 2025-07-06 at 21 06 14_13222ace](https://github.com/user-attachments/assets/c74c04ec-0bc3-4ef4-bb6b-b2bc303ea371)

CODE: #include <LiquidCrystal.h>

// LCD pins: RS, E, D4, D5, D6, D7 LiquidCrystal lcd(7, 8, 9, 10, 11, 12);

const int buttonPin = 2; int counter = 0; int buttonState = 0; int lastButtonState = 0;

void setup() { pinMode(buttonPin, INPUT); lcd.begin(16, 2); lcd.print("Counter: "); lcd.setCursor(0, 1); lcd.print(counter); }

void loop() { buttonState = digitalRead(buttonPin);

if (buttonState == HIGH && lastButtonState == LOW) { counter++; lcd.setCursor(0, 1); lcd.print(" "); // Clear line lcd.setCursor(0, 1); lcd.print(counter); delay(200); // Debounce delay }

lastButtonState = buttonState; }

OUTPUT:

![WhatsApp Image 2025-07-06 at 21 11 42_b31b7d1a](https://github.com/user-attachments/assets/9cfb6f72-fd0c-4b5d-8996-16a0fb9d8e2b)
