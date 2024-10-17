
# Documentación de Colecciones

Este repositorio contiene varias colecciones en formato JSON que representan diferentes entidades de un sistema académico. A continuación se describe cada colección y su contenido.

## Colecciones

### Faculty.json  
Contiene información sobre las facultades dentro de la institución académica.

```json
{
    "_id" : ObjectId("670fd15037d49219560da637"),
    "name" : "Ingeniería y Ciencias Básicas"
}
```

### Headquarters.json  
Contiene información sobre las sedes de la institución académica.

```json
{
    "_id" : ObjectId("670fd15037d49219560da637"),
    "name" : "Sede Central"
}
```

### Programs.json  
Contiene información sobre los programas académicos ofrecidos.

```json
{
    "_id" : ObjectId("670fd1b837d49219560da63f"),
    "name" : "Ingeniería de Sistemas",
    "facultyId" : ObjectId("670fd15037d49219560da637")
}
```

### Roles.json  
Contiene información sobre los roles de usuario dentro del sistema.

```json
{
    "_id" : ObjectId("670fcf0f37d49219560da606"),
    "name" : "Estudiante"
}
```

### Semesters.json  
Contiene información sobre los semestres académicos.

```json
{
    "_id" : ObjectId("670fd031044f85443aed6fc0"),
    "description" : "I"
}
```

### StudyPlans.json  
Contiene información sobre los planes de estudio de los programas académicos.

```json
{
    "_id" : ObjectId("670fd36437d49219560da65d"),
    "name" : "Plan Estudios Ingeniería Sistemas",
    "programId" : ObjectId("670fd1b837d49219560da63f"),
    "isActive" : true
}
```

### Subjects.json  
Contiene información sobre las asignaturas ofrecidas.

```json
{
    "_id" : ObjectId("670fd49f044f85443aed6fde"),
    "name" : "Programación I"
}
```

### Users.json  
Contiene información sobre los usuarios del sistema, incluyendo sus datos personales y credenciales.

```json
{
    "_id" : ObjectId("670fcecd37d49219560da603"),
    "email" : "haroldmosquera739@gmail.com",
    "password" : "$2a$10$X3GhZmI62.pze6URykhbrOv53FAvHvxQvygdx/OEJBtXSHdNwymB.",
    "isActive" : true,
    "people" : {
        "names" : "Harold Stevent",
        "lastNames" : "Mosquera Cerón",
        "phone" : "3209596096"
    }
}
```

### UsersRoles.json  
Contiene información sobre la relación entre los usuarios y sus roles dentro del sistema.

```json
{
    "_id" : ObjectId("670fd5c367e85f96adddf2f7"),
    "userId" : ObjectId("670fcecd37d49219560da603"),
    "roleId" : ObjectId("670fcf0f37d49219560da606")
}
```

### SubjectsStudyPlans.json  
Contiene información sobre la relación entre las asignaturas y los planes de estudio.

```json
{
    "_id" : ObjectId("670fd6c267e85f96adddf320"),
    "subjectId" : ObjectId("670fd49f044f85443aed6fde"),
    "studyPlanId" : ObjectId("670fd36437d49219560da65d"),
    "teacherId" : ObjectId("670fd64167e85f96adddf2fe")
}
```

### Enrollments.json  
Contiene información sobre las inscripciones de los estudiantes en los programas académicos.

```json
{
    "_id" : ObjectId("670fd88e67e85f96adddf336"),
    "programId" : ObjectId("670fd1b837d49219560da63f"),
    "semesterId" : ObjectId("670fd031044f85443aed6fc4"),
    "headquartersId" : ObjectId("670fd20e37d49219560da645"),
    "studyPlanId" : ObjectId("670fd36437d49219560da65d"),
    "studentId" : ObjectId("670fcecd37d49219560da603")
}
```

### Grades.json  
Contiene información sobre las calificaciones de los estudiantes.

```json
{
    "_id" : ObjectId("670fd8bb67e85f96adddf342"),
    "SubjectStudyPlanId" : ObjectId("670fd6c267e85f96adddf320"),
    "value" : 3.9,
    "enrollmentId" : ObjectId("670fd88e67e85f96adddf336")
}
```

### AcademicPeriods.json  
Contiene información sobre los periodos académicos.

```json
{
    "_id" : ObjectId("670fd2f337d49219560da64f"),
    "name" : "Primer Corte",
    "programId" : ObjectId("670fd1b837d49219560da63f")
}
``` 
