FORMAT: 1A
HOST: http://private-5c515-diplomado1.apiary-mock.com

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
            "nota": "Alarma generada por x",
        }
        {
            "id": 2,
            "nota": "Alarma generada por x",
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
            "nota": "Alarma generada por x",
        }
        ]

## Eliminar Alarmas[DELETE /Alarmas/{id}]
Elimina Videos Seleccionada

+ Parameters
    + id (int)
   
+ Response 200
    
        {
            "result": True,
            "message": "Alarma Eliminada"
        }
   

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

# Reproduce Grabaciones [/Grabaciones/{id}/reproduce]
Reproduce las Grabaciones

    + Model (application/json)
    [
        + Body 
        { 
                "id": 1 
        }
    ]

## Reproduce las Grabaciones [GET]
Reproduce las Grabaciones
    + Response 200
           [reproduce Grabaciones][]

