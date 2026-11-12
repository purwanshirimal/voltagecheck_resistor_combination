# voltagecheck_resistor_combination
Checks the voltage across resitors in series combination
#components
1.Arduino UNO
2.220 ohm resistor and 1k ohm resistor
3.jumper wires
4.laptop as power supply
#How it works
The 5v supply is provided from arduino to the 220 ohm resitor which then is in series with the 1k ohm resistor whihc is then grounded to coomplete the circuit.A jumper wire from the middle of connection beteween two resitor is connected to A3 of the arduino to take the reading of the voltage across the resistor which is finally grounded ie the 1k ohm resistor in this case.
#The code
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
#challenges
To measure the voltage across 220 ohm resistor ie connected to the supply the connection is revered ie the supply is connected to 1k ohm resistor nd the process is repeated.
#Future improvements
Use it to not burn the ckt.
