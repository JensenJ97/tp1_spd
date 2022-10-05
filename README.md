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
  
  Serial.println(segundos);
}
