//KY-037 микрофонный модуль - Цифровой выход D6
const int MicPin = 6;  // выбор пина для входа от микрофона
const int LedPin = 13;  // выбор пина для светодиода
int flag=0; 
 
void setup () 
{
  pinMode (LedPin, OUTPUT);
}
 
void loop () 
{
  if(digitalRead(MicPin) == HIGH  && flag == 0){
    flag=1;
    digitalWrite (LedPin, !digitalRead(LedPin));
    delay (150);
  }
  if(digitalRead(MicPin) == LOW && flag == 1)
     {            
        flag=0;
     } 
}
 
