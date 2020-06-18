
![npm](https://i.imgur.com/MP2bABn.png)


# Zeew Api

## Informacion

Zeew api soy una api de imagenes de interaccion, pero mi mi fuerte es la manipulacion y mis bienvenidas.

Soy una api creada para los creadores de bots, ayudandoles y facilitandoles crear codigos complejos para manipular o crear bienvenidas.

y lo mejor que estoy completamente en ingles ♥

- **Constructores**
  - [SFW](#SFW)
  - [IMG](#IMG)
  - [BIENVENIDAS](#BW)
- **Zeew Api**
  - [Soporte](#SOPORTE)
  - [Staff](#STAFF)
  - [Mas Proyectos](#PROYECTOS)
  - [Donaciones](#DONACIONES)
- **Extra**
  - [Usalo con Discord.js](#Discord)



## Instalacion & Uso

Para usar la mayoria de las funciones, debes tener un token.
ese token tiene registrado, el nombre del usuario al cual se le ha otorgado el token.

Y puedes optenerlo desde el servidor de soporte en discord.

El `valor` son los parametros o valores que necesita la api o la funcion.

Si tu uso de la api es para crear bots de discord, te ayudamos con un ejemplos [para usar con tu bot](#Discord).

 Las funciones retornan una promesa, a si que recuerda usar el async/await, para evitar un callback enorme.

<a name="SFW"></a>

### Constructor SFW

- **Como usar el constructor**

```javascript
const Zeew = require('zeew');
const sfw = new Zeew.sfw("Token")
```

- **Contenido SFW**

Funcion | Descripcion | Valor
--- | :---: | ---:
kiss | beso | 
punch | golpe | 
neko | gatio | 
wink | giño | 
slap | bogetada | 
run | correr | 
hug | abrazo | anime o human
cry | llorar | anime o human
cookie | galletas | anime o human
dance | baile | anime o human

- **Ejemplo**

```javascript
const Zeew = require('zeew');
const sfw = new Zeew.sfw("TOKEN");

// -= Valor =-
sfw.hug("anime");

// -= Sin valor =-
sfw.kiss();

```

<a name="IMG"></a>

### Constructor IMG

- **Como usar el constructor**

```javascript
const Zeew = require('zeew');
const sfw = new Zeew.img("Token")
```

- **Contenido IMG**

Funcion | Descripcion | Valor
--- | :---: | ---:
blur | imagen borrosa | imagen
sepia | imagen a escala de grises | imagen
distort | Distorsiona  la imagne | imagen & Amplitud
invert | invierte los colores | imagen

- **Ejemplo**

```javascript
const Zeew = require('zeew');
const img = new Zeew.img("Token")

// -= Un valor =-
let Zeew = "https://i.imgur.com/09RRYve.jpg";
img.blur(img)

// -= Dos Valores =-
let img = "https://i.imgur.com/09RRYve.jpg";
img.distort(img, 5);

```

<a name="BW"></a>

### Constructor Bienvenida

- **Contenido IMG**

Funcion | Descripcion 
:--- | ---: 
token | clave de acceso
estilo | Estilo de la card 
avatar | imagen del perfil 
fondo | Imagen de fondo 
colorTit | color del titulo 
titulo | titulo de la card 
colorDesc | color de la desc 
descripcion | texto de descripcion

- **Estilos**
  - *para ver los ejemplo dale click o touch al estilo* 
  - [classic](https://i.imgur.com/XqOGyel.png)
  - [anime](https://i.imgur.com/ZEt9X63.png)

- **Modo de Uso**

```javascript
const Zeew = require('zeew');

let wel = new Zeew.Bienvenida()
.token("TOKEN")
.estilo("classic")
.avatar("https://i.imgur.com/09RRYve.jpg")
.fondo("https://i.imgur.com/0YrfJgx.jpg")
.colorTit("#FF3DB0")
.titulo("Bienvenido")
.colorDesc("#fff")
.descripcion("Tenemos un nuevo usuario")

/*Esto sirve para crear la imagen con los dato proporcionados*/
let img = await Zeew.WelcomeZeew(wel);
```

## Informacion & Soporte

<a name="SOPORTE"></a>

### Soporte

Si tienes errores, bugs o quieres contactarnos.

- **Discord**
  - [Servidor del Creador](https://discord.gg/PBDbHGq)
  - [Servidor del Soporte](https://discord.gg/ZqvqUyx)
- **Redes Sociales**
  - Creador: `@KamerrEzz`
- **Web**
  - [Estatico](https://kamerrezz.github.io/za-web/)

<a name="STAFF"></a>

### Staff

- **Kamerr Ezz**
```
* ROL: Founder
* ID Discord: 403695999941345280
* Redes Sociales: @KamerrEzz
* Pagina Web: KamerrEzz.com
```

- **ValerynR (Ex-Staff)**
```
* ROL: Co-Owner
* ID Discord: 393603334847856650
```

<a name="PROYECTOS"></a>

### Proyectos

Proyecto | Descripcion 
:--- | ---: 
[Zeew-eco](https://www.npmjs.com/package/zeew-eco) | Crea una economia


### Donaciones

<a name="DONACIONES"></a>
Donacion | Descripcion 
:--- | ---: 
[ko-fi](https://ko-fi.com/kamerroficial) | Apoya desde cofi
[paypal](https://www.paypal.me/kamerrezz) | Apoya desde paypal


<a name="Discord"></a>

## Usalo para discord

La mayoria del uso de la api, es para la creacion de bots para discord.js.

Tambien, la mayoria de los que usan la api para sus bots de discord, son principiantes y usan version diferentes, lo cual les ayudares con lo basico.


- **Discord V11**
  - `displayAvatarURL`
  - `avatarURL`
  - `new Discord.RichEmbed()`
  - `channels.get("ID-CANAL")`
- **Discord V12**
  - `displayAvatarURL({formart: "png"})`
  - `avatarURL({formart: "png"})`
  - `new  Discord.MessageEmbed()`
  - `channels.cache.get("ID-CANAL")`

### Enviando Imagenes

- Evento para las Bienvenidas
  - v11
    - [guildMemberAdd](https://discord.js.org/#/docs/main/v11/class/Client?scrollTo=e-guildMemberAdd)
    - [guildMemberRemove](https://discord.js.org/#/docs/main/v11/class/Client?scrollTo=e-guildMemberRemove)
  - v12
    - [guildMemberAdd](https://discord.js.org/#/docs/main/v12/class/Client?scrollTo=e-guildMemberAdd)
    - [guildMemberRemove](https://discord.js.org/#/docs/main/v12/class/Client?scrollTo=e-guildMemberRemove)

> realmente no cambia nada, pero aun asi te doy la informacion.

### Enviar la imagen

Podemos enviar la Bienvenidas, targetas (cards) o imagenes, de diferente formas.

A qui te mostrare como hacerlas.

- Mensaje

```javascript
/*

        --== CODE DE LA BIENVENIDA / CARD ==--

*/

let img = await Zeew.WelcomeZeew(wel); // Bienvenida
let img = img.blur(img) // Imagenes

// --== DISCORD V11 ==--
  // Opcion 1 > Uso de Opciones
.send({files: [img]})

  // Opcion 2 > Uso de Attchment
let {Attachment} = require('discord.js')
let attchment = new Attachment(img)

.send(attchment)


// --== DISCORD V12 ==--
  // Opcion 1 > Uso de Opciones
.send({files: [img]})

  // Opcion 2 > Uso de Attchment
let {MessageAttachment} = require('discord.js')
let attchment = new MessageAttachment(img)

.send(attchment)


/*
Mas Informacion

--== Attachment ==--
 > v11
https://discord.js.org/#/docs/main/v11/examples/attachments

 > v12
https://discord.js.org/#/docs/main/stable/examples/attachments

--== Send / Opciones ==--
  > v11
https://discord.js.org/#/docs/main/v11/class/ClientUser?scrollTo=send

  > v12
https://discord.js.org/#/docs/main/stable/class/ClientUser?scrollTo=send
*/



```

- Embed
```javascript
/*

        --== CODE DE LA BIENVENIDA / CARD ==--

*/

let img = await Zeew.WelcomeZeew(wel);

// --== DISCORD V11 ==--

let ImgEmbed = new Discord.Attachment(img, "welcome-ZeewApi.png")
let embed = new Discord.RichEmbed()
  .attachFile(ImgEmbed)
  .setImage('attachment://welcome-ZeewApi.png')
member.guild.channels.get("Id del canal").send(embed)

// --== DISCORD V12 ==--

let ImgEmbed = new Discord.MessageAttachment(img, "welcome-ZeewApi.png");

let embed = new Discord.MessageEmbed()
  .attachFiles(ImgEmbed)
  .setImage('attachment://welcome-ZeewApi.png')
member.guild.channels.cache.get("Id del canal").send(embed);

/*
v11
  [-] RichEmbed > attachFiles
  > https://discord.js.org/#/docs/main/v11/class/RichEmbed
v12
  [-] MessageEmbed> attachFiles
  > https://discord.js.org/#/docs/main/v12/class/MessageEmbed
*/

```
