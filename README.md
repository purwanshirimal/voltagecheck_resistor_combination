# voltagecheck_resistor_combination
int pin=A3;
int del=1000;
int data=0;
float readval;
void setup()
{
  pinMode(pin,INPUT);
  Serial.begin(9600);
}
void loop()
{
  data=analogRead(pin);
readval=(5./1023.)*data;
  Serial.println(readval);
  delay(del);

}
