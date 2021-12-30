*/
interger-value-from-serial-monitor-in-arduino
If required to send interger value from serial monitor in Arduino, we have to convert the charater value in integer format.
In arduino if we sent interger value from serial monitor, it will send in chraceter format.
i.e if we wish to send 123, it will receive three char '1','2','3'.
/*

string number ;

void setup(){
Serial.begin(9600);
}

void loop() {
  
  while(Serial.available()){
   char num=Serial.read();
   number += num;
   delay(10);
  }
    if (number.length()>0){
      Serial.println(number);
      int int_num = number.toInt();
   }
  }
