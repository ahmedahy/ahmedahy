// Soil Moisture Sensor Pin
const int soilMoisturePin = A1;

// Moisture Threshold
const int moistureThreshold = 500;  // Adjust this value based on your sensor and soil conditions

// DC Motor Pins
const int motorPin = 11;

void setup() {
  // Initialize DC motor pin as output
  pinMode(motorPin, OUTPUT);

  // Initialize Serial Communication
  Serial.begin(9600);
}

void loop() {
  // Read soil moisture value
  int soilMoistureValue = analogRead(soilMoisturePin);

  // Print soil moisture value
  Serial.print("Soil Moisture: ");
  Serial.println(soilMoistureValue);

  // Check the moisture level
  if (soilMoistureValue < moistureThreshold) {
    // Soil is dry, activate the motor
    Serial.println("Soil is dry! Watering the plant...");
    activateMotor();
  } else {
    // Soil moisture is sufficient, deactivate the motor
    Serial.println("Soil moisture is sufficient. No need to water.");
    deactivateMotor();
  }

  // Delay before the next reading
  delay(1000);
}

// Function to activate the DC motor
void activateMotor() {
  digitalWrite(motorPin, HIGH); // Turn on the motor
}

// Function to deactivate the DC motor
void deactivateMotor() {
  digitalWrite(motorPin, LOW); // Turn off the motor
}
