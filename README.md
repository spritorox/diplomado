# Sistema Gestion de tráfico urbano
Servicios control de Alarmas

##Alarmas [/Alarmas/{id}]
Administracion Sobre las Alarmas de Trafico

+ Parameters
    + id (int)
    + nota (string)

##Buscar Alarma[GET /Alarmas]
Obtiene Alarmas Generadas

+ Response 200 (application/json)

        {"Alarmas":
            [
        {
            "id": 1,
            "nota": "Alarma generada por trafico",
        }
        {
            "id": 2,
            "nota": "Alarma generada por trafico",
        }
+ Response 404 (application/json)

        { 
            "error": "Alerta no encontrada" 
        }
            ]
        }

## Lista Alarma [GET /Alarmas/{id}]
Lista Alarma Seleccionada

+ Parameters
    + id (int)

+ Response 200 (application/json)

        [
        {
            "id": 1,
            "nota": "Alarma generada por trafico",
        }
        ]

## Eliminar Alarmas[DELETE /Alarmas/{id}]
Elimina Alarma Seleccionada

+ Parameters
    + id (int)
   
+ Response 200
    
        {
            "result": True,
            "message": "Alarma Eliminada"
        }
   

# Reproduce Grabaciones [/Grabaciones/{id}/reproduce]
Reproduce las Grabaciones

## Grabaciones [/Grabaciones/{id}]
Administracion Sobre las Grabaciones de Trafico

+ Parameters
    + id (int)
    + nota (string)
    + tamano (int)

##Buscar Grabaciones[GET /Grabaciones]
Obtiene Grabaciones Generadas

+ Response 200 (application/json)

        {"Grabaciones":
         [
            {
            "id": 1,
            "tamano": "10Mb",
                }
        {
            "id": 2,
            "tamano": "10Mb",
        }
+ Response 404 (application/json)

        { 
            "error": "Grabacion no encontrada" 
        }
         ]
        }

## Lista Grabaciones [GET /Grabaciones/{id}]
Lista Grabaciones Seleccionada

+ Parameters
    + id (int)

+ Response 200 (application/json)

        [
        {
            "id": 1,
            "tamano": "10Mb", 
        }
        ]

## Eliminar Grabaciones[DELETE /Grabaciones/{id}]
Elimina Grabacion Seleccionada

+ Parameters
    + id (int)
   
+ Response 200
    
        {
            "result": True,
            "message": "Grabaciones Eliminada"
        }

## Reproduce las Grabaciones [GET]
Reproduce las Grabaciones

+ Response 200

           [reproduce Grabaciones][]

# Visualizar Fotogramas
Visualizar los Fotogramas

##Fotogramas [/Fotogramas/{id}]
Administracion Sobre los Fotogramas de Trafico

+ Parameters
    + id (int)
    + nota (string)
    + fecha_captura (string)

##Buscar Fotogramas[GET /Fotogramas]
Obtiene Alarmas Generadas

+ Response 200 (application/json)

        {"Fotogramas":
            [
        {
            "id": 1,
            "nota": "nota de fotograma",
            "fecha_captura": "05-09-2015 18:00"
        }
        {
            "id": 2,
            "nota": "nota de fotograma",
            "fecha_captura": "05-09-2015 18:00"
        }
+ Response 404 (application/json)

        { 
            "error": "Alerta no encontrada" 
        }
            ]
        }

## Lista Fotogramas [GET /Fotogramas/{id}]
Lista Fotogramas Seleccionada

+ Parameters
    + id (int)

+ Response 200 (application/json)

        [
        {
            "id": 1,
            "nota": "nota de fotograma",
        }
        ]

## Eliminar Fotogramas[DELETE /Fotogramas/{id}]
Elimina Fotogramas

+ Parameters
    + id (int)
   
+ Response 200
    
        {
            "result": True,
            "message": "Fotograma Eliminada"
        }
