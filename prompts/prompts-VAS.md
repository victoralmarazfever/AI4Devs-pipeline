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

# Prompt 6

Al crear la Pull Request, me ha dado este error:

Run npm test

> backend@1.0.0 test
> jest

sh: 1: jest: not found
Error: Process completed with exit code 127.

# Prompt 7

Perfecto gracias, está arreglado. Ahora me da este error:


Run npm run build

> backend@1.0.0 build
> tsc

src/application/services/candidateService.test.ts(2,10): error TS2305: Module '"@prisma/client"' has no exported member 'PrismaClient'.
src/application/services/positionService.test.ts(2,10): error TS2305: Module '"@prisma/client"' has no exported member 'PrismaClient'.
src/application/services/positionService.ts(1,10): error TS2305: Module '"@prisma/client"' has no exported member 'PrismaClient'.
src/application/services/positionService.ts(23,33): error TS7006: Parameter 'app' implicitly has an 'any' type.
src/application/services/positionService.ts(58,88): error TS7006: Parameter 'step' implicitly has an 'any' type.
src/domain/models/Application.ts(1,10): error TS2305: Module '"@prisma/client"' has no exported member 'PrismaClient'.
src/domain/models/Candidate.ts(1,10): error TS2305: Module '"@prisma/client"' has no exported member 'PrismaClient'.
src/domain/models/Candidate.ts(1,24): error TS2305: Module '"@prisma/client"' has no exported member 'Prisma'.
src/domain/models/Company.ts(1,10): error TS2305: Module '"@prisma/client"' has no exported member 'PrismaClient'.
src/domain/models/Education.ts(1,10): error TS2305: Module '"@prisma/client"' has no exported member 'PrismaClient'.
src/domain/models/Employee.ts(1,10): error TS2305: Module '"@prisma/client"' has no exported member 'PrismaClient'.
src/domain/models/Interview.ts(1,10): error TS2305: Module '"@prisma/client"' has no exported member 'PrismaClient'.
src/domain/models/InterviewFlow.ts(1,10): error TS2305: Module '"@prisma/client"' has no exported member 'PrismaClient'.
src/domain/models/InterviewStep.ts(1,10): error TS2305: Module '"@prisma/client"' has no exported member 'PrismaClient'.
src/domain/models/InterviewType.ts(1,10): error TS2305: Module '"@prisma/client"' has no exported member 'PrismaClient'.
src/domain/models/Position.ts(1,10): error TS2305: Module '"@prisma/client"' has no exported member 'PrismaClient'.
src/domain/models/Resume.ts(1,10): error TS2305: Module '"@prisma/client"' has no exported member 'PrismaClient'.
src/domain/models/WorkExperience.ts(1,10): error TS2305: Module '"@prisma/client"' has no exported member 'PrismaClient'.
src/index.ts(3,10): error TS2305: Module '"@prisma/client"' has no exported member 'PrismaClient'.