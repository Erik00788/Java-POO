# Java-POO
Código Orientado a objetos Java
// Main class
public class Main {
    public static void main(String[] args) {
        // Create an object of the subclass Cachorro
        Cachorro meuCachorro = new Cachorro("Rex", "Pastor Alemão");

        // Use the inherited method from the parent class (Animal)
        System.out.println("Nome do cachorro: " + meuCachorro.nome);
        System.out.println("Raça do cachorro: " + meuCachorro.raca);
        meuCachorro.comer();

        // Use the specific methods of the subclass (Cachorro)
        meuCachorro.latir();
        meuCachorro.andar();
        System.out.println(); // Add a line break for better readability

        // Create an object of the new subclass Passaro
        Passaro meuPassaro = new Passaro("Piu", "Canário");

        // Use the inherited method from the parent class (Animal)
        System.out.println("Nome do pássaro: " + meuPassaro.nome);
        System.out.println("Raça do pássaro: " + meuPassaro.raca);
        meuPassaro.comer();

        // Use the specific methods of the subclass (Passaro)
        meuPassaro.andar();
        meuPassaro.voar();
    }
}

// Parent class
class Animal {
    // Attributes
    String nome;
    String raca;

    // Constructor
    public Animal(String nome, String raca) {
        this.nome = nome;
        this.raca = raca;
    }

    // Method
    public void comer() {
        System.out.println(nome + " está comendo.");
    }

    public void andar() {
        System.out.println(nome + " está andando.");
    }
}

// Child class that inherits from Animal
class Cachorro extends Animal {
    // Constructor of the child class
    public Cachorro(String nome, String raca) {
        // Call the constructor of the parent class
        super(nome, raca);
    }

    // Specific method of the Cachorro class
    public void latir() {
        System.out.println(nome + " está latindo: Au au!");
    }
}

// New child class that inherits from Animal
class Passaro extends Animal {
    // Constructor of the child class
    public Passaro(String nome, String raca) {
        // Call the constructor of the parent class
        super(nome, raca);
    }

    // Specific method of the Passaro class
    public void voar() {
        System.out.println(nome + " está voando.");
    }
}
