# Diagramas_de_clases
Ejercicios de diagramas de clases con el editor mermaid
<p align="center">
Este es el diagrama original del ejercicio

![image](https://user-images.githubusercontent.com/79007014/114208620-f8328200-995d-11eb-8bb1-e1ac98324e99.png)
<p>
 
 <p align="center">
y este de aqui debajo es el editado con mermaid

![LECTURA](https://user-images.githubusercontent.com/79007014/114208746-1d26f500-995e-11eb-974d-50049cf8b3e9.png)
<p>
y este seria el codigo del diagrama realizado con el editor mermaid

    ReadingItem <|-- Encyclopedia
    ReadingItem <|-- Magazine
    ReadingItem <|-- Book
    ReadingItem "1"<--"n" Customer: buy
    Encyclopedia ..|> GST_Chargeable
    Magazine ..|> GST_Chargeable
    class ReadingItem{
    <<abstract>>
    -title: String
    -price : Double
    +ReadingItem()   void
    +ReadingItem(double,String) void
    +getName() String
    +getPrice()Double
    +calculatePrice()* Double
    +displayInfo()* void
    }
    class Encyclopedia{
      -year: int
      +Encyclopedia():void
      +Encyclopedia(String,Double,Int) void
    }
    class Magazine{
      -monthissue: int
      -year: int
      +Magazine(): void
      +Magazine(int, int, Double, String)
    }
    class Book{
      -author: String
      -year int 
      +Book()
      +Book(String, Double, String, int)

    }

    class Customer{
    -customerName: String
    -totalPay: Double
    -ReadingItem : item
    +Customer(String) void
    +buy(ReadingItem) void
    +getTotalPay() double
    toString() String
    }

    class GST_Chargeable{
        <<interface>>
        -RATE=0.06 : Double
        +getGSTCharges() Double 

    }

<p align="center">
Y este es el segundo diagrama a partir del cual he hecho el segundo ejercicio
  
![image](https://user-images.githubusercontent.com/79007014/114208981-69723500-995e-11eb-83f6-1dd33808e9bd.png)
<p>
  
 <p align="center">
Y este el diagrama realizado con el editor mermaid
 
![PET](https://user-images.githubusercontent.com/79007014/114208796-2d3ed480-995e-11eb-9460-75511f36b300.png)
<p>
 
 Seguido del codigo:
  
    Animal <|-- Spider
    Animal <|-- Cat
    Animal <|-- Fish
    Fish <.. Pet
    Cat <.. Pet
    class Animal{
    <<abstract>>
    #int legs
    #Animal(legs:int)
    +walk() void
    +eat() void
    }
    class Spider{
      +Spider()
    }
    class Cat{
      -name : String
      +Cat(n : String) 
      +Cat()
      +getName() String
      +setName(n : String) void 
      +play() void
      
       
    }
    class Fish{
       -name : String
      +Fish()
      +getName() String
      +setName(n : String) void 
      +play() void
    }

    class Pet{
    <<interface>>
    +getName(): String
    +setName(n : String) void
    +play() void
    }
            
  
