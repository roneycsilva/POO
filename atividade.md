# Atividade em sala de Aula 
### -> 17/03/2025

## Desenvolver um script em Java utilizando:

* Classes
* Objetos
* Métodos
* Herança
* Polimorfismo

## Script


![atividade](https://github.com/user-attachments/assets/ff88bdc0-21cd-4ccd-99b2-7546f9c93ac6)

```java
import java.util.Scanner;

class Carro {
    String marca, modelo;
    int ano;

    public Carro(String marca, String modelo, int ano) {
        this.marca = marca;
        this.modelo = modelo;
        this.ano = ano;
    }

    public void exibirInfo() {
        System.out.println(marca + " " + modelo + " - " + ano);
    }
}

class CarroEsportivo extends Carro {

    public CarroEsportivo(String marca, String modelo, int ano) {
        super(marca, modelo, ano);
    }

    @Override
    public void exibirInfo() {
        super.exibirInfo();
        System.out.println("Este é um carro esportivo.");
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        Carro c1 = new Carro("Fusca", "Volkswagen", 1962);
        CarroEsportivo c2 = new CarroEsportivo("Opala SS", "Modelo", 1971);

        c1.exibirInfo();
        c2.exibirInfo();

        scanner.close();
    }
}

