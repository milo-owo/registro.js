# registro.js

var registros = [];

function agregarRegistro(){
    let in_usuario = document.getElementById("in_usuario").value;
    let in_contrasena = document.getElementById("in_contrasena").value;
    let obj = {
        usuario: in_usuario,
        contrasena: in_contrasena
    }
    registros.push(obj);
}

function filtrarPorContrasena(arreglo,filtro){
    let newArray = [];
    for(let i = 0; i < arreglo.length; i++){
        if(arreglo[i].contrasena.length <= filtro){
            newArray.push(arreglo[i]);
        }
    }
    console.log(newArray);
    return newArray
}

module.exports.registros = registros;
module.exports.filtrarPorContrasena = filtrarPorContrasena;
module.exports.agregarRegistro = agregarRegistro;
