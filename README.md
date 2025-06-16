# Sistema Integrado de Gestión y Recomendación en una Red Social

## Descripción General

Este proyecto implementa un sistema básico de red social que permite la gestión de usuarios y conexiones entre ellos, junto con recomendaciones de amistad utilizando técnicas de grafos. La solución se enfoca en aplicar programación orientada a objetos, estructuras de datos avanzadas y principios SOLID.

---

## Flujo del Sistema

1. **Inicialización de la red social**
   - Se crea una instancia de la clase `RedSocial`.

2. **Registro de usuarios**
   - Se agregan usuarios mediante `agregar_usuario(nombre)`.

3. **Creación de conexiones**
   - Los usuarios pueden agregarse como amigos a través de `agregar_amigo(usuario1, usuario2)`.

4. **Recomendación de amigos**
   - Se sugieren usuarios que no están conectados directamente, pero tienen amigos en común mediante `sugerencias_amigos(usuario)`.

5. **Recorrido del grafo**
   - Se utiliza el algoritmo BFS para recorrer la red desde un usuario específico mediante `bfs(usuario)`.

---

## Estructura del Código

- `Usuario`: Clase que representa a un usuario con su nombre y lista de amigos.
- `RedSocial`: Maneja toda la lógica de red:
  - Registro de usuarios.
  - Agregado de amigos.
  - Sugerencias de amistad (grafo no dirigido).
  - Recorrido BFS del grafo.
- Manejo de excepciones:
  - `UsuarioExisteError`, `UsuarioNoExisteError`, `ConexionExistenteError`: controlan errores comunes y aseguran integridad del sistema.

---

## Decisiones de Diseño

- **Uso de clases y encapsulación**: Se sigue una estructura orientada a objetos clara, separando responsabilidades entre usuarios y la red.
- **Estructura tipo grafo**: La red social se implementa como un grafo no dirigido. Cada nodo representa un usuario y los enlaces representan amistades.
- **SOLID**: Se sigue el principio de responsabilidad única para cada clase.
- **Reutilización y modularidad**: El diseño permite extender fácilmente funcionalidades como eliminar amigos o visualizar rutas.

---

## Análisis de Rendimiento

- **Agregar usuario**: O(1), al usar un diccionario para almacenamiento.
- **Agregar amistad**: O(1), al tratarse de una operación de conjunto.
- **Sugerencia de amigos**: O(n), donde n es el número de amigos de los amigos del usuario.
- **BFS**: O(n + m), donde n es el número de usuarios y m el número de conexiones.

> La eficiencia es adecuada para una red pequeña-mediana, aunque no se ha optimizado para redes sociales masivas.

---

## Capturas del Sistema

> 📸 **[Aquí se deben incluir capturas de la ejecución del sistema en consola o interfaz, si aplica.]**

---

## Conclusión

Este proyecto demuestra cómo se puede simular una red social simple mediante estructuras de grafos y programación orientada a objetos. Se lograron implementar funcionalidades clave como el registro de usuarios, conexión entre ellos, recomendaciones inteligentes de amistad y recorrido por la red. Además, se aplicaron principios sólidos de diseño de software que hacen al sistema mantenible y extensible para futuras mejoras.

---

## Autor

Desarrollado por [Claudio Andrés Díaz Vargas]  
Curso: [Evaluación Modular]  
Fecha: [Junio 2025]

