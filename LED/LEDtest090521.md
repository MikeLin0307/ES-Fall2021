# LED Practive(20210905)

## 2-1 用示波器觀察電壓變化(LED)
![2-1](https://user-images.githubusercontent.com/89327055/132112984-f5d5f45a-b77e-4860-b8de-55ee05787e6f.png)
````C
void setup()
{
  pinMode(13, OUTPUT);
}

void loop()
{
  digitalWrite(13, HIGH);
  delay(1000); // Wait for 1000 millisecond(s)
  digitalWrite(13, LOW);
  delay(1000); // Wait for 1000 millisecond(s)
}
````
##
## 2-2 用示波器觀察電壓變化(LED RGB)
![2-2](https://user-images.githubusercontent.com/89327055/132113003-9e744cc8-185a-49b7-b906-f4dece747151.png)
````C
void setup()
{
  pinMode(9, OUTPUT);//green
  pinMode(10, OUTPUT);//blue
  pinMode(11, OUTPUT);//red
}

void loop()
{
   analogWrite(9,255);
   analogWrite(10,0);
   analogWrite(11,0);
   delay(1000);

   analogWrite(9,0);
   analogWrite(10,255);
   analogWrite(11,0);
   delay(1000);
  
   analogWrite(9,0);
   analogWrite(10,0);
   analogWrite(11,255);
   delay(1000);
}
````

