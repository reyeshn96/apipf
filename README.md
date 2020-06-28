# API PF
Se trata de una API desarrollada en PHP para clientes de PF.

## Instalación
No requiere ninguna instalación especial por parte del cliente.

## Requisitos
Para la utilización de la API deberás contar una **API_KEY** y con la **dirección URL** de la misma, esto se te entregará junto a la información de tu servicio.

## Importante
La API solo permite solicitudes GET.

Añadir una dirección IP a través de la API
------------------------------------------
Esta acción de la API te permitirá añadir una dirección IP para que comience a ser autorizada.
```javascript
  let xhr = new XMLHttpRequest();
  xhr.open('GET', 'www.ejemplo.com/client_api/id_servicio/api.php?api_key={tu_api_key}&addip={ip_a_autorizar}');
  xhr.send();
  
  xhr.addEventListener('load', () => {
    if( xhr.readyState == 4 )
    {
        // Acción al realizar correctamente la petición. 
    }
  });
```
Después de añadir una dirección IP esta comenzará a hacer autorizada, este es un proceso que puede tomar varios minutos.
Verificar el estado de una dirección IP a través de la API
----------------------------------------------------------
Esta acción de la API te permitirá saber si la dirección IP esta en proceso de autorización, o si esta autorizada.
```javascript
  let xhr = new XMLHttpRequest();
  xhr.open('GET', 'www.ejemplo.com/client_api/id_servicio/api.php?api_key={tu_api_key}&statusip={ip_a_autorizar}');
  xhr.send();
  
  xhr.addEventListener('load', () => {
    if( xhr.readyState == 4 )
    {
        // Acción al realizar correctamente la petición. 
    }
  });
```
