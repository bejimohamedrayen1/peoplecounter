#include <SPI.h>
#include <LoRa.h>

// Déclaration des pins des boutons
const int buttonIn = A3;   // Gauche - Entrée
const int buttonOut = A2;  // Droit - Sortie

// Compteurs
int peopleCount = 0;
int totalIn = 0;
int totalOut = 0;

bool lastIn = HIGH;
bool lastOut = HIGH;

void setup() {
  Serial.begin(9600);

  pinMode(buttonIn, INPUT_PULLUP);
  pinMode(buttonOut, INPUT_PULLUP);

  // Initialisation LoRa
  if (!LoRa.begin(868E6)) {
    Serial.println("Erreur d'initialisation LoRa !");
    while (true);
  }

  Serial.println("LoRa OK !");
  afficherInfos();
}

void loop() {
  bool currentIn = digitalRead(buttonIn);
  bool currentOut = digitalRead(buttonOut);

  // Entrée détectée
  if (lastIn == HIGH && currentIn == LOW) {
    peopleCount++;
    totalIn++;
    Serial.println("Entrée détectée");
    afficherInfos();
    sendLoRa();
  }

  // Sortie détectée
  if (lastOut == HIGH && currentOut == LOW) {
    if (peopleCount > 0) {
      peopleCount--;
      totalOut++;
      Serial.println("Sortie détectée");
      afficherInfos();
      sendLoRa();
    } else {
      Serial.println("Sortie ignorée : pièce vide");
    }
  }

  lastIn = currentIn;
  lastOut = currentOut;

  delay(50);
}

void afficherInfos() {
  Serial.print("Personnes dans la pièce : ");
  Serial.println(peopleCount);

  Serial.print("Total entrées : ");
  Serial.println(totalIn);

  Serial.print("Total sorties : ");
  Serial.println(totalOut);

  Serial.println("-----------------------------");
}

void sendLoRa() {
  LoRa.beginPacket();
  LoRa.print("In: ");
  LoRa.print(totalIn);
  LoRa.print(" | Out: ");
  LoRa.print(totalOut);
  LoRa.print(" | Dans la pièce: ");
  LoRa.print(peopleCount);
  LoRa.endPacket();
}
