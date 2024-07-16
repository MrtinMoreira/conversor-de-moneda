### Conversor de moneda

Esta aplicación Java es un conversor de monedas que permite a los usuarios realizar conversiones entre diferentes monedas, utilizando un servicio en línea de tasas de cambio actualizadas.

### Estructura del proyecto

El proyecto se centra en torno al archivo Main.java, que contiene el código fuente esencial para el funcionamiento de la aplicación Java.

###Funciones

- 1 menú Principal:

Al iniciar la aplicación, un menú principal ofrece tres opciones al usuario: "Convertir moneda",
"Consultar historial"
"Salir".

El usuario puede seleccionar una de estas opciones utilizando el cuadro de diálogo proporcionado por JOptionPane.

Convertir Moneda:

- 2 Convertir moneda:

Luego, se le pide al usuario que ingrese la cantidad que desea convertir.

La aplicación utiliza un servicio de tasas de cambio en línea para obtener la tasa de conversión entre las dos monedas seleccionadas.

Después de realizar la conversión, se muestra el resultado al usuario en otro cuadro de diálogo JOptionPane.

Si el usuario elige, puede convertir otra cantidad con las mismas monedas de origen y destino seleccionadas anteriormente.

- 3 Consultar Historial:

Cuando el usuario elige la opción "Consultar historial" en el menú principal, se muestra un cuadro de diálogo JOptionPane con el historial de conversiones recientes.
El historial se almacena en una lista y se muestra al usuario en el cuadro de diálogo.

- 4Salir del Programa:

Si el usuario elige la opción "Salir" en el menú principal, el programa se cierra.

### Integración con Servicio de Tasa de Cambio
- La aplicación utiliza un servicio de tasas de cambio en línea para obtener las tasas de conversión entre diferentes monedas.
- Se hace una solicitud HTTP al servicio utilizando la URL proporcionada con la moneda base como parámetro.
- La respuesta se analiza para obtener las tasas de conversión y se utiliza para realizar las conversiones de moneda.
- El servicio en línea utilizado para obtener las tasas de cambio es ExchangeRate-API. Este servicio proporciona datos precisos y actualizados sobre las tasas de cambio entre diferentes monedas.

URL para las Tasas de Cambio: La URL para acceder a las tasas de cambio proporcionadas por ExchangeRate-API es la siguiente: https://v6.exchangerate-api.com/v6/{API_KEY}/latest/{BASE_CURRENCY}

{API_KEY}: Se refiere a la clave de API proporcionada por ExchangeRate-API. Debes registrarte en su plataforma para obtener tu propia clave de API. {BASE_CURRENCY}: Especifica la moneda base para la cual se desean obtener las tasas de cambio. En el código proporcionado, se utiliza la moneda base dinámicamente basada en la selección del usuario. La API responde con un objeto JSON que contiene las tasas de cambio entre la moneda base especificada y otras monedas.

Por ejemplo, si {API_KEY} es "YOUR_API_KEY" y {BASE_CURRENCY} es "USD" (dólar estadounidense), la URL sería: https://v6.exchangerate-api.com/v6/YOUR_API_KEY/latest/USD Al hacer una solicitud GET a esta URL, obtendrás un objeto JSON que contiene las tasas de cambio para el dólar estadounidense en relación con otras monedas.

