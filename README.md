# DIAGRAMAS DE CLASES

## ANIMALES

EL SIGUIENTE DIAGRAMA REPRESENTA LA ESTRUCTURA DE CLASES DE LOS TIPOS DE ANIMALES DE LA APLICACIÓN

```java
class Perro extends Animal{
  String raza;
  
  String morder (String cosa) {
    return null;
  }
}

class Gato extends Animal{
  String raza;
  
  String morder (String cosa) {
    return null;
  }
}

abstract class Animal{
  void alimentar() {
  }
  abstract void sonar();
}
```

```mermaid
classDiagram
class Perro {
  +String raza
  +morder(cosa: String): String
}

class Gato {
  +String raza
  +morder(cosa: String): String
}


class Animal{
  void sonar()*
}

Perro <|-- Animal
Gato <|-- Animal
```

# DIAGRAMA DE SECUENCIA

```mermaid
sequenceDiagram
   Partida->>Profesor: Entregar Código
   Profesor->>Estudiantes: Display Código
   Estudiantes->>Partida: Entrar Partida
   Profesor ->> Partida: Iniciar Partida
   loop juego
   Partida ->> Estudiantes: Display Pregunta
   Estudiantes ->> Partida: Entregar Respuesta
   end

```

# DIAGRAMA DE SECUENCIA
```mermaid
sequenceDiagram
   Estudiante->>Profesor: Entregar Trabajo
   Profesor->>Estudiante: Nota
```


# DIAGRAMA DE ACTIVIDADES
```mermaid
flowchart
    A[Estudiar UML] --> B{Comprendo UML?}
    B -->|Si| C[Ver la televisión]
    B -->|No| D[Descansar un poco]
    D --> A
```


# DIAGRAMA DE ESTADOS
```mermaid
stateDiagram-v2
    state "No matriculado" as nomatriculado
    state "Matriculado" as matriculado
    state "Graduado" as graduado
    [*] --> nomatriculado
    nomatriculado --> matriculado
    matriculado --> graduado
    graduado --> [*]
```


