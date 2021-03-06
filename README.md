FORMAT: 1A
HOST: http://private-5c515-diplomado1.apiary-mock.com

# Sistema Gestion de tráfico urbano
Servicios control de Alarmas

##Alarmas [/Alarmas/{id}]
Administracion Sobre las Alarmas de Trafico

+ Parameters
    + id (int)
    + nota (string)
    + fecha_alarma (string)
    + tipo_alarma (string)

##Buscar Alarma[GET /Alarmas]
Obtiene Alarmas Generadas

+ Response 200 (application/json)

        {"Alarmas":
            [
        {
            "id": 1,
            "nota": "Alarma generada por trafico",
            "fecha_alarma": "01-01-2015 00:02",
            "tipo_alarma": "choque",
        }
        {
            "id": 2,
            "nota": "Alarma generada por trafico",
            "fecha_alarma": "01-01-2015 00:02",
            "tipo_alarma": "choque",
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
    + inicio_transmision (string)
    + fin_transmision (string) 

##Buscar Grabaciones[GET /Grabaciones]
Obtiene Grabaciones Generadas

+ Response 200 (application/json)

        {"Grabaciones":
         [
            {
            "id": 1,
            "tamano": "10Mb",
            "inicio_transmision": "01-01-2015 00:02", 
            "fin_transmision": "01-01-2015 00:02",
            "descargar": "http://repositorio/download/video010120150002"
                }
        {
            "id": 2,
            "tamano": "10Mb",
            "inicio_transmision": "01-01-2015 00:02", 
            "fin_transmision": "01-01-2015 00:02",
            "descargar": "http://repositorio/download/video010120150002"
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
            "inicio_transmision": "01-01-2015 00:02", 
            "fin_transmision": "01-01-2015 00:02",
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
            "fecha_captura": "01-01-2015 00:01"
        }
        {
            "id": 2,
            "nota": "nota de fotograma",
            "fecha_captura": "01-01-2015 00:02"
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

# Visualizar Camaras
Visualiza las Camaras

##Camaras [/Camaras/{id}]
Administracion Sobre los Camaras

+ Parameters
    + id (int)
    + ubicacion (string)
    + fecha (string)
    + ip (string)
    + coordenadas (string)
    + marca (string)

##Buscar Camaras[GET /Camaras]
Obtiene Listado de Camaras

+ Response 200 (application/json)

        {"Camaras":
            [
        {
            "id": 1,
            "ubicacion": "1;1",
            "fecha": "01-01-2015 00:01",
            "ip": "127.0.0.1",
            "marca": "generica",
        }
        {
            "id": 2,
            "ubicacion": "1;1",
            "fecha": "01-01-2015 00:01",
            "ip": "127.0.0.1",
            "marca": "generica",
        }
+ Response 404 (application/json)

        { 
            "error": "Camara no encontrada" 
        }
            ]
        }

## Lista Camaras [GET /Camaras/{id}]
Lista Camaras Seleccionada

+ Parameters
    + id (int)

+ Response 200 (application/json)

        [
        {
            "id": 1,
            "ubicacion": "1;1",
            "fecha": "01-01-2015 00:01"
            "ip": "127.0.0.1",
            "marca": "generica",
        }
        ]

## Eliminar Camaras[DELETE /Camaras/{id}]
Elimina Camaras

+ Parameters
    + id (int)
   
+ Response 200
    
        {
            "result": True,
            "message": "Camara Eliminada"
        }
