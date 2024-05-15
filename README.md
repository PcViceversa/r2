# r2
gh me la pela


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
// LA CLASE SYSTEM.OUT Y UTIL SON OTRAS MUY POPULARES

// L SENTENCIA CONDICIONAL ES

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

// CODIGO ESPECIAL
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







 

