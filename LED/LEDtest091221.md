# LED Practive(20210905 & 20210912)

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
##
## 2-3 讓你的RGB LED燈全彩模組也可會"呼吸"
![螢幕擷取畫面 2021-09-12 093510](https://user-images.githubusercontent.com/89327055/132967769-7846b7d8-e7de-4a7f-b1b1-d92adbcef9c1.png)
````C
void setup()
{
  pinMode(9, OUTPUT);//green
  pinMode(10, OUTPUT);//blue
  pinMode(11, OUTPUT);//red
  
}

void loop()
{
  for(int i=0; i<=255 ; i+=5)
  {
   analogWrite(9,0);
   analogWrite(10,i);
   analogWrite(11,0);
   delay(50);
  }
  
   for(int i=255; i>=0 ; i-=5)
  {
   analogWrite(9,0);
   analogWrite(10,i);
   analogWrite(11,0);
   delay(50);
  }
}
````
##
## 2-4 可變電阻 + 序列監視器與輸出
![螢幕擷取畫面 2021-09-12 101000](https://user-images.githubusercontent.com/89327055/132969140-088b86c2-85c6-402a-8383-74589b4f3792.png)
````C
int senaorValue=0;

void setup()
{
  pinMode(A0, INPUT);
  Serial.begin(9600);
}

void loop()
{
  senaorValue = analogRead(A0);
  Serial.println(senaorValue);
  delay(10);
}
````
##
## 2-5 按下按鍵控制 LED 開關
![螢幕擷取畫面 2021-09-12 102412](https://user-images.githubusercontent.com/89327055/132969392-998074b0-d466-4c9a-8424-740af7036cad.png)
````C
int button=0;

void setup()
{
  pinMode(2, INPUT);
  Serial.begin(9600);
}

void loop()
{
  button = digitalRead(2);
  Serial.println(button);
  delay(10);
}
````
