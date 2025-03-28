# Prompt 1

Como un senior Engineer Devops, tienes que ayudarme a crear un pipeline en Github Actions para que, tras el trigger "push a una rama con un Pull Request abierto", siga los siguientes pasos:

Pase unos tests de backend.
Genere un build del backend.
Despliegue el backend en un EC2. 

No crees ni modifiques nada de momento. Confirma que entiendes la tarea, analiza el código y dime qué modificarías


# Prompt 2

Gracias por las sugerencias. Vamos primero a crear los cambios de configuración del pipeline en la carpeta .github/workflows.
Revisa que no haya conflictos con los existentes

# Prompt 3

Vamos a modificarlo para que solo aplique para la rama pipeline-VAS

# Prompt 4

Perfecto gracias. Renombra el archivo a pipeline-VAS.yml, así no se confundirá con uno genérico

# Prompt 5

Comprueba que este action y el despliegue sigue buenas prácticas