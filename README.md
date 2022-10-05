# tp1_spd
Julian Jensen
DIV F
Trabajo Practico 1 

Link a Tinkercad : https://www.tinkercad.com/things/ibDh3F2mWTO-glorious-blorr-bigery/editel?sharecode=0nmUGVqH8OYdOyVnF7QIkpBXvjGjDil8w17aNQZ8sQk 

/* CODIGO ARDUINO */

//
//
#define PRIMERO 3
#define SEGUNDO 4
#define TERCERO 5
#define CUARTO 6
#define QUINTO 7
#define SEXTO 8
#define SEPTIMO 9
#define OCTAVO 10
#define NOVENO 11
#define DECIMO 12
#define PAUSA A1
#define RESET A2

void setup()
{
  pinMode(LED_BUILTIN, OUTPUT);
  pinMode(PRIMERO, OUTPUT);
  pinMode(SEGUNDO, OUTPUT);
  pinMode(TERCERO, OUTPUT);
  pinMode(CUARTO, OUTPUT);
  pinMode(QUINTO, OUTPUT);
  pinMode(SEXTO, OUTPUT);
  pinMode(SEPTIMO, OUTPUT);
  pinMode(OCTAVO, OUTPUT);
  pinMode(NOVENO, OUTPUT);
  pinMode(DECIMO, OUTPUT);
  pinMode(RESET, INPUT);
  pinMode(PAUSA, INPUT);
  Serial.begin(9600);
	
}

void loop()
{
  int milesimas = millis();
  int segundos = milesimas/1000;
  encenderNumeros(segundos);
  apagarLeds();
}

void apagarLeds(){
  digitalWrite(PRIMERO, LOW);
  digitalWrite(SEGUNDO, LOW);
  digitalWrite(TERCERO, LOW);
  digitalWrite(CUARTO, LOW);
  digitalWrite(QUINTO, LOW);
  digitalWrite(SEXTO, LOW);
  digitalWrite(SEPTIMO, LOW);
  digitalWrite(OCTAVO, LOW);
  digitalWrite(NOVENO, LOW);
  digitalWrite(DECIMO, LOW);
}

void encenderNumeros (int segundos){
  switch (segundos){
    case 1:
    digitalWrite(PRIMERO, HIGH);
    break;
    case 2:
	digitalWrite(SEGUNDO, HIGH);
    break;
    case 3:
    digitalWrite(PRIMERO, HIGH);
    digitalWrite(SEGUNDO, HIGH);
  	break;
    case 4:
    digitalWrite(TERCERO, HIGH);
    break;
    case 5:
    digitalWrite(TERCERO, HIGH);
    digitalWrite(PRIMERO, HIGH);
    break;
    case 6:
    digitalWrite(TERCERO, HIGH);
    digitalWrite(SEGUNDO, HIGH);
    break;
    case 7:
    digitalWrite(TERCERO, HIGH);
    digitalWrite(SEGUNDO, HIGH);
    digitalWrite(PRIMERO, HIGH);
    break;
    case 8:
    digitalWrite(CUARTO, HIGH);
    break;
    case 9:
    digitalWrite(CUARTO, HIGH);
    digitalWrite(PRIMERO, HIGH);
    break;
    case 10:
    digitalWrite(CUARTO, HIGH);
    digitalWrite(SEGUNDO, HIGH);
    break;
  }
}
