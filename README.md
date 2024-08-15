# r2
GH me la pela


// ELO329
// --- --- ---

// PARADIGMAS : PROGRAMACION { DECLARATIVA , IMPERATIVA , ...    }
// PROGRAMACION IMPERATIVA   { PROCEDURAL  , OO         , ...    }
// PRORAMACION OO            { = PRORAMACION ORIENTADA A OBJETOS }

// PROGRAMACION OO { CODIGO CONTIENE **OBJETOS DE SOFTWARE** QUE MODELAN **OBJETOS DE REALIDAD** } { **OBJETOS** }
// **OBJETOS**     { TIENEN UN ESTADO Y UN COMPORTAMIENTO }
// ESTADO          { = *ATRIBUTOS* }
// COMPORTAMIENTO  { = *METODOS*   }

// **CLASE** { CONJUNTO DE **OBJETOS** CON ATRUBUTOS Y METODOS PARTICULARES }
// **CLASE** { CATEGORIZA  **OBJETOS** }

// **CLASE** { TIENE   *JERARQUIA*  }
// **CLASE** { PERMITE *HERENCIA*  }
// **CLASE** { PROVOCA *SUBTIPOS*  }

// **OBJETOS** SON *INSTANSCIAS* DE UNA **CLASE**

// POLIMORFISMO { LAS **CLASE**   SOPORTAN DEFINIRLO }
// POLIMORFISMO { LOS **OBJETOS** LOS SOPORTAN EN SI }
// POLIMORFISMO { SE REFIERE A ENTES EN COMUN POR UN UNICO NOMBRE EN COMUN }

// {} LA OO EXPLOTA LA REUTILIZACION DE CODIGO {}

// JVM { EJECUTA UN BYTECODE DE FORMA IGUAL PARA CADA HARDWARE/SOFTWARE COMBINACION}
// JVM { CONTIENE javac PARA CREAR UN BYTECODE .java -> .class }
// JVM { CONTIENE java  PARA EJECUTAR BYTECODE }

// PROGRAMA O CLASE EJECUTABLE { DEBE TENER AL MENOS UNA **CLASE**      }
// PROGRAMA O CLASE EJECUTABLE { DEBE TENER AL MENOS UN  *METODO*  MAIN }

class Main
{
    public static void main ( String args[] ) {}
}

// static { EN PRECENCIA } { REFERENCIA CODIGO DE LA **CLASE**   }
// static { EN AUSENCIA  } { REFERENCIA CODIGO DEL   **OBJETOS** }
// JVM INVOCA A main DIRECTAMENTE SIN CREAR NINGUN OBJETO POR ENDE DEBE SER static

// VISIBILIDAD { MANEJADA POR MODIFICADORES DE NIVEL DE ACCESO }
// MODIFICADOR { private   } { CODIGO VISIBLE SOLO POR DICHA CLASE                           }
// MODIFICADOR { omicion   } { CODIGO VISIBLE POR OTRAS CLASE   [DEL PAQUETE]                }
// MODIFICADOR { protected } { CODIGO VISIBLE POR OTRAS CLASE   [DEL PAQUETE] Y CLASES HIJAS [DEL PAQUETE O NO] }
// MODIFICADOR { public    } { CODIGO VISIBLE TODAS LAS CLASES                               }
// JVM INVOCA A main DESDE FUERA DE LA CLASE POR ENDE DEBE SER public

// final { USADO PARA CONSTANTES - UN VALOR QUE NO DEBERIA CAMBIAR }
// final { PERMITE ACCESO class.CONSTANTE }

// TIPOS PRIMITIVOS { BOOLEAN - CHAR --- BYTE - SHORT - INT - LONG --- FLOAT - DOUBLE }
// CHAR             { SE CODIFICA POR UNICODE }
// CHAR             { VISIBLES : 'a' 'b' 'c' ... Y NO VISIBLES : '\n' '\r' '\b' '\t' '\"' '\'' '\\' }
// CAMBIOS DE TIPO NO SIMPRE GARANTIZAN PRECISION EXACTA

// **LOS OPERADORES TIENEN *PRECEDENCIA* Y *ASOCIACION***
// **LOS NOMBRES DE OBJETOS SON SOLO UNA REFERENCIA Y NO EL OBJENTO EN SI**

// LA CLASE STRING CONCATE STRING ENTRE SI CON EL OPERADOR + { SI UNO NO ES STRING LO TRANSFORMA EN STRING ANTES DE CONCATENAR }
// LA CLASE SYSTEM.OUT Y UTIL SON OTRAS MUY POPULARES Y ARRAYLIST PERMITE LISTAS DE TAMAÑO DINAMICO

// L SENTENCIA CONDICIONAL ES { break Y continue }

if      (cond_1) {} 
else if (cond_2) {}
else if (cond_3) {}
//              ...
else             {}

int i = 2;
String name;
switch (i)
{
    case 1:
        name = "juan"; break;
    case 2:
        name = "pepe"; break;
    default:
        name = "nn";
}
System.out.println(name);

// LA SENTENCIA DE BUCLE ES

while (cond) {}

do {} while (cond);

for (cond) {}

int[] num = {1, 2, 3};
for (int i : num) { i } // Enhanced For

// LOS ARREGLOS EN JAVA SE INICIAN { int [] arr = {2,3,5};     }
// LOS ARREGLOS EN JAVA SE CREAN   { int [] arr = new int[10]; }

int [][] triag = new int[10][ ]; ​
for ( int n=0 ; n<triag.length ; n++ )
{​
    triag[n] = new int[n+1];​
    for ( int j=0; j<triag[n].length ; j++ )
    {​
        triag[n][j] = n+j;
    }
}

// LOS CAMBIOS EN REFERENCIA AFECTAL AL MISMO OBJETO
// int [] a = new int [5];​
// int [] b = a;
// a CAMBIA b Y VICEVERSA

// **CODIGO ESPECIAL**
// {}        SE LLAMA LA PRIMERA VEZ EN CADA OBJETO
// static {} SE LA LLAMA LA PRIEMRA VEZ EN CADA CLASE **Y ANTES DEL MAIN**
// finalize() Garbage Collection { RECOLECCION DE BASURA }

// LAS **CLASES** CONTIENEN
// ATRIBUTOS
// METODOS CONTRUCTORES
// METODOS

// this.  O this()  referencia al mismo objeto
// super. O super() referencia al objeto base

// LA HERENCIA EXIGE LA RELACION *ES-UN* Y EL *PRINCIPIO DE SUSTITUCION*
// *ES UN*                    { RELACION SUBCONJUNTISTA }
// *PRINCIPIO DE SUSTITUCION* { CLASE HIJA RESPONDE DE FORMA ESPERABLE A CUALQUIER METODO DE LA CLASE PADRE }

// SE USA HERENCIA CON
class Humano extends Animal {​}

// LOS CONTRUCTORES NO TIENEN RETORNO

class Employee
{
   public Employee(String n, double s) { name = n; salary = s;     }
   public Employee(double s)           { this( "#" + nextId , s ); }
   public Employee()                   { this( "#" + nextId , 0 ); }

   public String getName()   { return name;   }
   public double getSalary() { return salary; }
   public int getId()        { return id;     }
   
   {
      id = nextId;
      nextId++;
   }

   static {
      nextId = 111;
   }

   private static int nextId;
   private int id;
   private String name = "";
   private double salary;
}

// Y POLIMORFISMO

class Employee
{  
   public Employee(String n, double s, int y) { name = n; salary = s; year = y; }

   public String getName()   { return name;   }
   public double getSalary() { return salary; }
   public int getYear()      { return year;   }

   public void raiseSalary(double byPercent)
   {  
      double raise = salary * byPercent / 100;
      salary += raise;
   }

   private   String name;
   protected double salary;
   private   int    year;
}

class Manager extends Employee
{  
   public Manager(String n, double s, int y) { super(n, s, y); bonus = 0; }

   public void setBonus(double b) { bonus = b; }
   public double getSalary()
   { 
      double baseSalary = super.salary; // super.salary o super.getSalary()
      return baseSalary + bonus + 1;
   }

   private double bonus;
}

// OBJETOS RESPONDEN CON SUS METODOS RE-DEFINIDOS SIN IMPORTAR REFERENCIA
// OBJETOS SOLO OFRECEN SERVICIOS PARA METODOS DEFINIDOS EN SU REFERENCIA
// DE ESO SE ENCARGA EL LIGADO-DINAMICO { ELEGIR METODO DE ENTRE TODOS DEL MISMO NOMBRE EN TIEMPO DE EJECUCION CON "TARGET THIS" }

// CASTEO PASA DE :  Employee e = new Manager();​ -> Manager m = (Manager) e;
// ANTE LA DUDA   : if (e instanceof Manager) { ​Manager m = (Manager) e;​ }

// BASTA QUE 1 SOLO METODO ESTE DEFINIDO Y NO IMPLEMENTADO PARA QUE LA CLASE SEA ABSTRACTA
public abstract class Forma
{​
    ...​
    public abstract double getArea();​
    ..​
}

// HAY CLASES *OBJET* Y *CLASS*

// UNA INTERFAZ DEBE SER DEFINIDA E IMPLEMENTADA
// UNA INTERFAZ ES IMPLEMENTADA POR UNA CLASE

interface Funcionario_ITRFZ
{
    void trabajar();
}

class Funcionario implements Funcionario_ITRFZ
{
    @Override
    public void trabajar() {}
}

class Estudiante
{
    ...
}

class Ayudante extends Estudiante implements Funcionario_ITRFZ {
   private Funcionario func;
   
   public Ayudante()
   {
        this.func = new Funcionario();
   }
   
   @Override
   public void trabajar()
   {
   func.trabajar(); 
   }
}

// LAS CLASES ANIDADAS SE UBICAN A ACCESO EFIMERO DE UNA CLASE
// LAS CLASES ANIDADES ESTATICAS SE LLAMAN CLASES ANIDADAS ESTATICAS                  { DE LA CLASE }
// LAS CLASES ANIDADES NO ESTATICAS SE LLAMAN CLASES ANIDADAS NO ESTATICAS O INTERNAS { DEL OBJETO  }

public class Main
{
    public static void main(String[] args)
    {
    
   ClaseExterna externa = new ClaseExterna(10);
   ClaseExterna.ClaseAnidada anidada = externa.new ClaseAnidada(20);

   anidada.mostrarValorAnidado();                // ---> 20
   anidada.mostrarValorExternoDesdeAnidado();    // ---> 10
   externa.mostrarValorExterno();                // ---> 10
    }
}

public class ClaseExterna {
   private int valorExterno;
   public ClaseExterna(int valorExterno) { this.valorExterno = valorExterno; }
   public void mostrarValorExterno() { System.out.println( "ext" + valorExterno ); }

   public class ClaseAnidada {
        private int valorAnidado;
        public ClaseAnidada(int valorAnidado) { this.valorAnidado = valorAnidado; }
        public void mostrarValorAnidado() { System.out.println("int" + valorAnidado); }
        public void mostrarValorExternoDesdeAnidado() { System.out.println("ext-ani" + valorExterno); }
    }
}

// O ESTATICA

public class Main {
    public static void main(String[] args) {
        Carro miCarro = new Carro("Toyota", 2020);
        System.out.println(miCarro.getInfo());
        Carro.Motor motor = new Carro.Motor(2000);
        System.out.println(motor.getInfo());
    }
}
public class Carro {
    private String modelo;
    private int año;
    
   public Carro(String modelo, int año) {
        this.modelo = modelo;
        this.año = año;
    }
    
   public String getInfo() {
        return "Modelo: " + modelo + ", Año: " + año;
    }
    
   public static class Motor {
        private int cilindraje;
        public Motor(int cilindraje) {
            this.cilindraje = cilindraje;
        }
        public String getInfo() {
            return "Cilindraje: " + cilindraje + "cc";
        }
    }
}


// UNA CLASE INTERNA QUE SE INSTACIA SOLO UNA VEZ PUEDE COMPRIMERSE EN UNA SOLA CLASE ANONIMA

public class MiClase implements MiInterfaz {
    @Override
    public void miMetodo() {
        // Implementación del método miMetodo
    }
}

MiInterfaz miInterfaz = new MiClase();
miInterfaz.miMetodo();

// O 

MiInterfaz miInterfaz = new MiInterfaz() {
    ... atributos
    @Override
    public void miMetodo() {
        // Implementación del método miMetodo
    }
};

// SI UNA CLASE ANONIMA TIENE EXACTAMENTE 1 METODO PUEDE SER NOTADA POR UN EXPRECION LAMBDA

MiInterfaz miInterfaz = () ->
{
    // Implementación del método miMetodo
};


// ...

// ... COPIA Y EXEPCIONES Y PAQUETES








 

