<h1>SpeedyClub-Dev</h1>
<br>
<h2>Crear Un Usuario Nuevo</h2>

Post    
https://us-central1-clubspeedy-dev.cloudfunctions.net/api/crearUsuario   

Campos obligatorios 

identificacion;
email;
password;
nombres;
avatar;
municipio;
telefono;
termino;
codigoLider;
codigoPasajero;
codigoTransportador;
codigo1;
habilitado;
cambioUsuario;
habilitadoPasajero;
habilitadoLider;
habilitadoTransportador;
habilitadoMotoSpeedy;
habilitadoCarroSpeedy;
habilitadoCarroCarrera;
habilitadoCarroMensajeria;
habilitadoMotoCarrera;
habilitadoMotoMensajeria;
historicoPasajero;
historicoMotoSpeedy;
historicoCarroSpeedy;
saldoMotoSpeedy;
saldoMotoCarroSpeedy;
motoOcupada;
carroOcupado;
usuarioIdLider;
   

ok: false,
message: 'El código líder no existe'

ok: false,
message: 'Este código de lider ya está en uso'

ok: false,
message: 'Error al registrar al usuario',

ok: false,
message: 'Ya existe esta identificación en la base de datos'

ok: false,
message: 'Ya existe este email en la base de datos.',

Creacion Exitosa
ok: true,
message: 'usuario ' + nombres + ' Agregado Exitosamente'

<h2>#Login De Usuario</h2>
Post    
https://us-central1-clubspeedy-dev.cloudfunctions.net/api/login

Campo Obligatorio
    
email;
password;

ok: false,
message: 'Usuario incorrecto'

ok: false,
message: 'Credenciales Incorrectas'

Login Exitoso
true,
usuario
    
<h2>#Editar usuario desde la app</h2>
Post    
https://us-central1-clubspeedy-dev.cloudfunctions.net/api/editApp
Campos obligatorios:
email;
nombres;
municipio;
telefono;

ok: false,
message: 'Usuario ' + email + ' no existe en nuestra base de datos'

ok: false,
message: 'Error al registrar el usuario, este email No existe o tiene un formato incorrecto.'

ok: false,
message: 'Error al Actualizar usuario 001',

Mensaje de actualizacion Exitosa
ok: true,
message: 'Usuario ' + email + ' Actualizado Exitosamente',
   
<h2>Editar Usuario Web</h2>
Edicion de perfil del usuario desde la web
Post 

https://us-central1-clubspeedy-dev.cloudfunctions.net/api/editWeb

Campos Obligatorios

identificacion;
email;
password;
nombres;
municipio;
telefono;
codigoLider;
codigoPasajero;
codigoTransportador;
codigo1;
habilitado;
cambioUsuario;
habilitadoPasajero;
habilitadoLider;
saldoMotoSpeedy;
saldoCarroSpeedy;

ok: false,
message: 'Usuario ' + email + ' no existe en nuestra base de datos'
    
ok: false,
message: 'Error al Actulizar usuario '

ok: false,
message: 'Error al registrar el usuario, este email No existe o tiene un formato incorrecto.'


Actualizacion Exitosa
ok: true,
message: 'Usuario ' + email + ' Actualizado Exitosamente',

<h2>Editar Estado de notificacion</h2>
Cambio el estado el view de una notificacion
Post
https://us-central1-clubspeedy-dev.cloudfunctions.net/api/editarEstadoNotificacion

Campos obligatorios
identificacion;
idNotificacion;

ok: false,
message: 'No existe este usuario en la base de datos.

ok: false,
messaje: 'Error al actualizar el cambiar el estado del usuario'

Cambio Exitoso
ok: true,
messaje: 'Cambios de estado Exitosamente',

<h2>Eliminacion de Usuario </h2>
Elimina usuario de la base de datos y lo crea en la coleccion usuario eliminado
Post

https://us-central1-clubspeedy-dev.cloudfunctions.net/api/userDeleteWeb

Campos Oblogatorios
email;

ok: false,
message: 'No existe este usuario en la base de datos'

ok: false,
message: 'Error al intentar eliminar usuario'   

ok: false,
message: 'Usuario No Existe'

Eliminacion Exitosa
ok: true,
message: 'usuario Eliminado',

<h2>Listar Usuarios</h2>
Listar todos los usuarios de la base de datos
   
https://us-central1-clubspeedy-dev.cloudfunctions.net/api/usuarios 
GET 

<h2>Finalizar Solicitud Transportador</h2>

https://us-central1-clubspeedy-dev.cloudfunctions.net/api/finalizarSolicitudTransportador
post

Campos Obligatorios
email;
latitude;
longitude;

ok: false,
message: 'No se encontró sus usuario en la base de datos.'

ok: false,
message: 'Error al guardar cambios.'
     
ok: false,
messsage: 'No se pudo actualizar la posición.'

Finalizacion Exitosa
ok: true,
message: 'Posicion actualizada.'

    
<h2>Eliminar posicion</h2>

https://us-central1-clubspeedy-dev.cloudfunctions.net/api/eliminarPosicion
post

Campos obligatorios
email;

ok: false,
message: 'No se encontró su usuario en la base de datos.'

ok: false,
message: 'Error al eliminar su posición en el sistema de Speedy. Su posición sigue activa.'

Eliminacion Exitosa
ok: true,
message: 'Su posición en el mapa fué eliminada hasta que vuelva a iniciar sesión.'
    
    
<h2>Editar Saldo Web</h2>

https://us-central1-clubspeedy-dev.cloudfunctions.net/api/editSaldo
post

Campos obligatorios
email;
tipo;
nuevoSaldo;

ok: false,
message: 'Error al registrar el usuario, este email No existe o tiene un formato incorrecto.'
    
ok: false,
message: 'Error al IntentarActulizar Usuario ',


Edicion Exitosa
ok: true,
 message: 'Usuario ' + email + ' Saldo Actualizado Exitosamente',


<h2>Editar Posicion</h2>

https://us-central1-clubspeedy-dev.cloudfunctions.net/api/editarPosicion
post
    
Campos Obligatorios
email;
latitude;
longitude;

ok: false,
message: 'Error al actualizar la posicion del usuario',

ok: false,
message: 'Usuario ' + email + ' no existe en nuestra base de datos'

ok: false,
message: 'Error al registrar el usuario, este email No existe o tiene un formato incorrecto.'

Actulizacion Exitosa
ok: true,
message: 'Posicion actualizada',

<h2>Cambiar Usuario</h2>

https://us-central1-clubspeedy-dev.cloudfunctions.net/api/cambiarUsuarioTransportador
post

Campo Obligatorio
email;

ok: false,
message: 'Usuario ' + email + ' no existe en nuestra base de datos'

ok: false,
message: 'Error al actualizar el cambio del usuario',

ok: false,
message: 'Error al registrar el usuario, este email No existe o tiene un formato incorrecto.'


Cambio Exitoso devuelve el usuari
ok: true,
message: 'cambio actualizada',
usuario 


<h2>Enviar mensaje a un usuario</h2>

https://us-central1-clubspeedy-dev.cloudfunctions.net/api/enviarMensajeUno
post

Campo Obligatorio

const email = req.body.email;
const mensaje = req.body.mensaje;

ok: false,
message: 'No existe este usuario en la base de datos.'

ok: false,
messaje: 'Error al intentar enviar notificacion a el usuario',

Mensaje Enviado Exitosamente
ok: true,
messaje: 'Notificacion Enviada Exitosamente',

<h2>Enviar mensaje a todos los usuarios</h2>

https://us-central1-clubspeedy-dev.cloudfunctions.net/api/enviarMensajeTodos
post

Campo Obligatorio    
const mensaje = req.body.mensaje;

ok: false,
message: 'Error al buscar usuario',

ok: false,
mensaje: 'Error al buscar email'

MensajeEnviado Exitosamente
ok: true
mensaje: 'Mensaje Enviado Con Exito'

<h2>Crear Comision</h2>

https://us-central1-clubspeedy-dev.cloudfunctions.net/api/crearCampoComision
get

ok: false,
mensaje: 'Error al buscar los usuarios',


comision generada con Exito
ok: true,
message: 'Terminó el proceso de habilitar por comisión.',
ahora

<h2>Des-habilitacion de todos los transportador por  comision</h2>

https://us-central1-clubspeedy-dev.cloudfunctions.net/api/deshabilitarComisionFalse
get

ok: false,
mensaje: 'Error al buscar los usuarios'

Des-habilitados todos con exito
ok: true,
message: 'Terminó el proceso de deshabilitado por comisión.',

<h2>Pago individual comision</h2>
https://us-central1-clubspeedy-dev.cloudfunctions.net/api/pagoIndividualComision
post

Campos obligatorios

email;
comision;
fecha;
tipo;

ok: false,
message: 'No se encontró este usuario en al abase de datos.'

ok: false,
message: 'Error al subir la comisión.'

pago Exitoso
ok: true,
message: 'Pago de la comisión efectuado correctamente.'
<h2>Total comision</h2>
https://us-central1-clubspeedy-dev.cloudfunctions.net/api/totalComision
post

Campo obligatorio
email;

Operacion Exitosa
ok: true,
arraySolicitudes

<h2>Ver Usuario Debajo de un lider</h2>

https://us-central1-clubspeedy-dev.cloudfunctions.net/api/verUsuariosDebajo
post

Campo obligatorio
codigo;

ok: false,
mensaje: 'Error al buscar los usuarios'


operacion Exitosa
ok: true,
message: 'Terminó el proceso de deshabilitado por comisión.',
asociados


<h2>Ver Usuario Arriba de un lider</h2>

https://us-central1-clubspeedy-dev.cloudfunctions.net/api/verUsuariosArriba
post

Campo obligatorio
codigo;

ok: false,
mensaje: 'Error al buscar los usuarios'


operacion Exitosa
ok: true,
message: 'Terminó el proceso de ver usuario arriba de un lider',
asociados

<h2>Tranferir usuarios antes de eliminar un lider</h2>

https://us-central1-clubspeedy-dev.cloudfunctions.net/api/transferirAsociado
post    

emailOrigen;
emailDestino;
email;

ok: false,
message: 'No se encontró este lider de origen.'

ok: false,
message: 'No se encontró este lider destino.'

ok: false,
message: 'No se encontró este usuario.'

ok: false,
message: 'Error al tranferir usuario.'

operacion exitosa
ok: true,
message: 'Pago de la comisión efectuado correctamente.' 

<h2>Valor total actual de comision y numero de usuarios en total</h2>

https://us-central1-clubspeedy-dev.cloudfunctions.net/api/sumatoriaComision
get    
  

ok: false,
message: 'No se encontró este usuarios para calcular comisiones.'
    

operacion exitosa
ok: true,
saldoAcumulado: saldoAcumulado,
contadorUsuarios: contadorUsuarios,

<h2>Tomar solicitudes elimnadas y volverla a activar por telefono celular</h2>

https://us-central1-clubspeedy-dev.cloudfunctions.net/api/aceptarSolicitudWeb
post

Campos Obligatorios
idSolicitud:;
emailTransportador;
avatarTransportador;
nombreTransportador;
demanda;
motoOcupada;
carroOcupado;

ok: false,
message: 'Este transportador esta ocupado o no esta disponible'

ok: false,
message: 'No existe esta solicitud en la base de datos.'

ok: false,
message: 'No es posible RE-ASIGNAR la solicitud que ya ha sido aceptada por otro transportador.'

ok: false,
message: 'No existe este transportador en la base de datos.'

ok: false,
message: 'Saldo MotoSpeedy Insuficiente, Su Saldo Actual: $' + transportador.saldoMotoSpeedy

ok: false,
message: 'Saldo CarroSpeedy Insuficiente, Su Saldo Actual: $' + transportador.saldoMotoSpeedy

ok: false,
message: 'Fallo al Actualizar transportador'

ok: false,
message: 'Error al tomar la solicitud CarroSpeedy'

ok: false,
messaje: 'Error al actualizar la solicitud CarroSpeedy',
error
    

operacion exitosa
ok: true,
message: 'Solicitud Recuperada y aceptada'

<h2>Tomar solicitudes eliminadas y descartalas y enviarlaa desiertas definitivamnete</h2>

https://us-central1-clubspeedy-dev.cloudfunctions.net/api/solicitudDesierta
post

Campos Obligatorios
idSolicitud:;
    

ok: false,
message: 'No existe la solicitud a operar.'

ok: false,
message: 'La solicitud no se puede operar en el estado en que se encuentra, debe estar en estado "ELIMINADA".'

ok: false,
message: 'No tiene permisos para cambiar de estado la solicitud.'
    

operacion exitosa
ok: true,
message: 'Solicitud se ha Desertado exitosamente.'


https://us-central1-clubspeedy-dev.cloudfunctions.net/api/solicitudDesierta
post

Campos Obligatorios
idSolicitud:;
    

ok: false,
message: 'No existe la solicitud a operar.'

ok: false,
message: 'La solicitud no se puede operar en el estado en que se encuentra, debe estar en estado "ELIMINADA".'

ok: false,
message: 'No tiene permisos para cambiar de estado la solicitud.'
    

operacion exitosa
ok: true,
message: 'Solicitud se ha Desertado exitosamente.'

++++



<h2>lista solictudes eliminadas</h2>

Lista cual de solicitudes del coleccion solicitudes son elimindas y devuelve un arreglo con la mismas

Get
https://us-central1-clubspeedy-dev.cloudfunctions.net/api/getSolicitudesEliminadas

    
Mensaje listado correcto
ok: false,
message: 'No existen solicitudes en la base de datos.'

Mensaje correcto
ok: true,
solicitudesEliminadas: solicitudesEliminadas,


#Login solo de lider

https://us-central1-clubspeedy-dev.cloudfunctions.net/api/loginLider

##Campo obligatorios
email;
password;

Mensaje Login Correcto
status 200
ok: true,
mensaje: Login Correcto

Mensaje Login Incorrecto
status 400
ok: false,
mensaje: Email  No existe

Mensaje Login Incorrecto
status 400
ok: false,
mensaje: Login Incorrecto, Verifique Contraseña

#Creacion de usuario Pasajero
##No puede haber un pasajero con identificacion, o email;
##Igual no puedo haber pasajero sin un lider previamente registrado enla BD

Post
https://us-central1-clubspeedy-dev.cloudfunctions.net/api/crearUsuarioPasajero
<br>
Campos Obligatorios:
identificacion;
email;
password;
nombres;
avatar;
municipio;
codigoLider;
codigoPasajero;
telefono;

mensajes registro incorrecto

ok: false,
message: ' No Existe Este Codigo de Lider en la Base De Datos, no se puede registra pasajero sin lider 004'

ok: false,
error: 'Error al registrar el usuario LIDER EN LA COLECCION 006'

ok: false,
error: 'Error al registrar el usuario ya existe 009'

Mensaje Registro Correcto
ok: true,
error: 'registra Pasajero Exitoso 013'

#Creacion de usuario Transportador
##No puede haber un transportador con id, email, igual
##No puede registrar sin codigo o con codigo lider incorrecto:
##Es decir que no exista en la base de datos de lideres
  
Post
https://us-central1-clubspeedy-dev.cloudfunctions.net/api/crearUsuarioTransportador

Campos Obligatorios:  
email;
password;
nombres;
avatar;
municipio;
codigoLider;
codigoTransportador;
telefono;

Mensaje De Error

ok: false,
message: 'No existe el códido lider, verificar código  '

ok: false,
message: 'Error al registrar el usuario '

ok: false,
message: 'Error al registrar el usuario, email ya existe'

ok: false,
message: 'YA EXISTE UN USUARIO CON ESTA IDENTIFICACION EN LA LISTA DE TRANSPORTADOR '

ok: false,
message: 'YA ESTA REGISTRADO UN USUARIO CON ESA IDENTIFICACION '

ok: false,
message: 'USUARIO YA EXISTE EN LA LISTA DE LIDER '
    
Mensaje de Registro Exitoso
ok: true,
message: 'Usuario registrado con éxito  '


#Lista de lideres
Get
Listado de todos los lideres
https://us-central1-clubspeedy-dev.cloudfunctions.net/api/getLideres

#Lista de Pasajeros
Get
Listado de todos los Pasajeros
https://us-central1-clubspeedy-dev.cloudfunctions.net/api/getPasajeros

#lista de Transportadores
Get
Listado de todos los Transportadores
https://us-central1-clubspeedy-dev.cloudfunctions.net/api/getTransportadores

    
    

    
  
  
# Editar Usuario App
## Edicion de perfil del usuario desde la app
Post  
    
https://us-central1-clubspeedy-dev.cloudfunctions.net/api/editApp

Campos Oblogatorios

email;
nombres;
municipio;
telefono;

ok: false,
message: 'Usuario ' + email + ' no existe en nuestra base de datos'

ok: false,
message: 'Error al Actulizar usuario '

ok: false,
message: 'Error al registrar el usuario, este email No existe o tiene un formato incorrecto'

Edicion Exitosa
ok: true,
message: 'Usuario ' + email + ' Actualizado Exitosamente',



   


    



   


# Editar Ubicacion
## Editar ubicacion del usuario

https://us-central1-clubspeedy-dev.cloudfunctions.net/api/editarPosicion 
POST 

Campos Obligatorios

email;
latitude;
longitude;

# Crear Solicitud
## Creacion de solicitud

https://us-central1-clubspeedy-dev.cloudfunctions.net/api/crearSolicitud
POST

Campos Obligatorios
    
emailPasajero;
tipo;
descripcionOrigen;
descripcionDestino;
nombrePasajero;
nombreTransportador;
descripcion;
oferta;
municipio;
demanda;    
distancia;
codigo;
posicionOrigenLat;
posicionOrigenLon;
posicionDestinoLat;
posicionDestinoLon;
avatarPasajero;
avatarTransportador;
usuarioIdusuario;

ok: false,
message: 'No se encontró sus usuario en la base de datos'

ok: false,
message: 'Error al guardar cambios.'



Actualizacion Exitosa
ok: true,
message: 'Posicion actualizada'
    
    
    



   


    

    







