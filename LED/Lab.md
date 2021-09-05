# Lab: LED Practive

## 1-1 Simple LED ON & OFF

![image](https://user-images.githubusercontent.com/89327055/131235581-3bb70655-bcd2-4762-89d0-4a77cdf4b77a.png)
````C
void setup()
{
  pinMode(LED_BUILTIN, OUTPUT);
}

void loop()
{
  digitalWrite(LED_BUILTIN, HIGH);
  delay(1000); // Wait for 1000 millisecond(s)
  digitalWrite(LED_BUILTIN, LOW);
  delay(1000); // Wait for 1000 millisecond(s)
}
````


##
## 1-2 RGB 0.5秒依序亮滅

![image](https://user-images.githubusercontent.com/89327055/131236072-dfe29329-e17e-4dc6-a7b2-b4a2c3e2c963.png)
````C
void setup()
{
  pinMode(13, OUTPUT); // RED
  pinMode(12, OUTPUT); // GREEN
  pinMode(8, OUTPUT); // BLUE
}

void loop()
{
  digitalWrite(13, HIGH);
  delay(500); // Wait for 500 millisecond(s)
  digitalWrite(13, LOW);
  delay(500); // Wait for 500 millisecond(s)
  
  digitalWrite(12, HIGH);
  delay(500); // Wait for 500 millisecond(s)
  digitalWrite(12, LOW);
  delay(500); // Wait for 500 millisecond(s)
  
  digitalWrite(8, HIGH);
  delay(500); // Wait for 500 millisecond(s)
  digitalWrite(8, LOW);
  delay(500); // Wait for 500 millisecond(s)
}
````


##
## 1-3 RGB 跑馬燈依序亮滅

![image](https://user-images.githubusercontent.com/89327055/131236035-6bf00076-59ae-49b4-9ee0-d6eef9b6da9b.png)
````C
void setup()
{
  pinMode(13, OUTPUT); // RED
  pinMode(12, OUTPUT); // GREEN
  pinMode(8, OUTPUT); // BLUE
}

void loop()
{
  digitalWrite(13, HIGH);
  delay(1000); // Wait for 500 millisecond(s)
  digitalWrite(13, LOW);

  
  digitalWrite(12, HIGH);
  delay(1000); // Wait for 500 millisecond(s)
  digitalWrite(12, LOW);

  
  digitalWrite(8, HIGH);
  delay(1000); // Wait for 500 millisecond(s)
  digitalWrite(8, LOW);

}
````

