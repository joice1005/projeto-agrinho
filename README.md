int sensor = A0;
int valor;

void setup() {
  Serial.begin(9600);
}

void loop() {
  valor = analogRead(sensor);

  Serial.print("Umidade: ");
  Serial.println(valor);

  if (valor > 700) {
    Serial.println("Solo seco - Irrigação recomendada");
  } else if (valor > 400) {
    Serial.println("Umidade adequada");
  } else {
    Serial.println("Solo úmido - Não irrigar");
  }

  delay(2000);
}
