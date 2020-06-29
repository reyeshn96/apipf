# API PF
Una API desarrolada en PHP para clientes de PF.
## Instalación
No se requiere ninguna instalación especial por parte del cliente.

## Requerimientos
Para la utilización de la API necesitarás una **API_KEY** y **API_URL** que se te entregarán junto con tu servicio.

# Tutorial de uso
En lo que a la utilización de la API respecta tenemos disponible tres acciones: addip, statusip y delip.

## Añadir dirección IP a autorización (ADDIP)
Esta acción permitirá autorizar una nueva dirección IP en tu servicio:
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
Esto solicitará la adición de la IP a la lista de autorizados, esta acción podría tomar de 1 a 3 minutos para completarse.

## Verificar el estado de una dirección IP (statusip)
Esta acción de la API te permitirá saber si la dirección IP esta en proceso de autorización, o si se encuentra actualmente autorizada.
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
  
  ## Eliminar una dirección IP autorizada (delip)
  ```javascript
  let xhr = new XMLHttpRequest();
  xhr.open('GET', 'www.ejemplo.com/client_api/id_servicio/api.php?api_key={tu_api_key}&statusip={ip_a_autorizar}');
  xhr.send();
  
  xhr.addEventListener('load', () => {
    if( xhr.readyState == 4 )
    {
        alert('La dirección IP se ha eliminado de las autorizaciones.'); 
    }
  });
  ```
  Esto solicitará la eliminación de la IP de la lista de autorizados, esta acción podría tomar de 1 a 3 minutos para completarse.
  
  # Ejemplos en producción
  . . .
