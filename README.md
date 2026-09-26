<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Mi Web</title>

<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>

<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:wght@400;500;600;700&family=DM+Sans:wght@400;500;600&display=swap" rel="stylesheet">

<style>

*{
    box-sizing:border-box;
    margin:0;
    padding:0;
}

html{
    scroll-behavior:smooth;
}

body{
    font-family:"DM Sans",sans-serif;
    color:#181818;
    background:#f5f3ef;
    background-size:cover;
    background-position:center;
    background-attachment:fixed;
    background-repeat:no-repeat;
    min-height:100vh;
}

/* CAPA SUAVE SOBRE EL FONDO GENERAL */
body::before{
    content:"";
    position:fixed;
    inset:0;
    background:rgba(245,243,239,.55);
    z-index:-1;
    pointer-events:none;
}

/* -------------------------------- */
/* CABECERA */
/* -------------------------------- */

header{
    position:fixed;
    top:0;
    left:0;
    width:100%;
    z-index:1000;

    padding:22px 5%;

    display:flex;
    justify-content:space-between;
    align-items:center;

    background:rgba(245,243,239,.88);
    backdrop-filter:blur(10px);
    -webkit-backdrop-filter:blur(10px);
}

.logo{
    font-family:"Cormorant Garamond",serif;
    font-size:30px;
    font-weight:600;
}

nav{
    display:flex;
    align-items:center;
    gap:30px;
}

nav a{
    color:#181818;
    text-decoration:none;
    font-size:14px;
    cursor:pointer;
    transition:opacity .2s ease;
}

nav a:hover{
    opacity:.55;
}

/* BOTÓN MENÚ MÓVIL */

.menu-toggle{
    display:none;
    border:0;
    background:none;
    font-size:27px;
    cursor:pointer;
    color:#181818;
}

/* -------------------------------- */
/* CONTENEDOR */
/* -------------------------------- */

main{
    width:100%;
}

/* -------------------------------- */
/* PORTADA */
/* -------------------------------- */

.portada{
    min-height:100vh;
    padding:150px 7% 100px;

    display:grid;
    grid-template-columns:1fr 1fr;
    gap:70px;
    align-items:center;
}

.portada-texto h1{
    font-family:"Cormorant Garamond",serif;
    font-size:clamp(55px,7vw,105px);
    line-height:.9;
    font-weight:500;
    margin-bottom:30px;
}

.portada-texto p{
    max-width:620px;
    font-size:18px;
    line-height:1.7;
}

.portada-imagen{
    width:100%;
}

.portada-imagen img{
    display:block;
    width:100%;
    max-height:700px;
    object-fit:cover;
}

/* -------------------------------- */
/* SECCIONES */
/* -------------------------------- */

.seccion{
    padding:120px 7%;
    min-height:650px;

    background:rgba(245,243,239,.70);
    background-size:cover;
    background-position:center;
    background-repeat:no-repeat;
}

.seccion-contenido{
    max-width:1200px;
    margin:auto;
}

.seccion h2{
    font-family:"Cormorant Garamond",serif;
    font-size:clamp(50px,7vw,90px);
    font-weight:500;
    line-height:1;
    margin-bottom:40px;
}

.seccion-texto{
    max-width:800px;
    font-size:18px;
    line-height:1.8;
}

.seccion-imagen{
    margin-top:60px;
}

.seccion-imagen img{
    width:100%;
    max-height:650px;
    object-fit:cover;
    display:block;
}

/* -------------------------------- */
/* SECCIONES OCULTABLES */
/* -------------------------------- */

.oculta-navegacion{
    display:none !important;
}

/* -------------------------------- */
/* GALERÍA */
/* -------------------------------- */

#galeria{
    transition:opacity .5s ease;
}

.galeria-grid{
    display:grid;
    grid-template-columns:repeat(3,1fr);
    gap:25px;
}

.galeria-item{
    overflow:hidden;
    aspect-ratio:4/3;
}

.galeria-item img{
    width:100%;
    height:100%;
    object-fit:cover;
    display:block;

    opacity:1;
    transition:opacity .5s ease,transform .5s ease;
}

.galeria-item img:hover{
    transform:scale(1.02);
}

/* -------------------------------- */
/* COLABORADORES */
/* -------------------------------- */

#colaboradores{
    background:rgba(245,243,239,.70);
    background-size:cover;
    background-position:center;
}

.colaboradores-grid{
    display:flex;
    flex-direction:column;
    gap:60px;
}

.colaboradores-fila{
    display:grid;
    gap:25px;
    width:100%;
}

.colaborador{
    text-align:center;
}

.colaborador-imagen{
    width:100%;
    aspect-ratio:1/1;
    overflow:hidden;
    margin-bottom:18px;
}

.colaborador-imagen img{
    width:100%;
    height:100%;
    object-fit:cover;
    display:block;
    transition:transform .4s ease;
}

.colaborador-imagen a{
    display:block;
    width:100%;
    height:100%;
}

.colaborador-imagen img:hover{
    transform:scale(1.04);
}

.colaborador-nombre{
    font-family:"Cormorant Garamond",serif;
    font-size:25px;
}

/* -------------------------------- */
/* CONTACTO */
/* -------------------------------- */

.contacto{
    padding:120px 7%;
    background:rgba(245,243,239,.94);
}

.contacto-contenido{
    max-width:900px;
    margin:auto;
}

.contacto h2{
    font-family:"Cormorant Garamond",serif;
    font-size:clamp(50px,7vw,90px);
    font-weight:500;
    margin-bottom:50px;
}

.contacto-dato{
    margin-bottom:22px;
    font-size:18px;
}

.contacto-dato a{
    color:#181818;
    text-decoration:none;
}

.contacto-dato a:hover{
    text-decoration:underline;
}

.redes{
    display:flex;
    flex-wrap:wrap;
    gap:20px;
    margin-top:35px;
}

.redes a{
    color:#181818;
    text-decoration:none;
    border-bottom:1px solid #181818;
    padding-bottom:4px;
}

/* -------------------------------- */
/* FOOTER */
/* -------------------------------- */

footer{
    padding:50px 7%;
    background:#181818;
    color:#f5f3ef;
}

footer p{
    font-size:14px;
}

/* -------------------------------- */
/* RESPONSIVE */
/* -------------------------------- */

@media(max-width:900px){

    header{
        padding:18px 5%;
    }

    .menu-toggle{
        display:block;
    }

    nav{
        position:absolute;
        top:100%;
        left:0;
        width:100%;

        display:none;
        flex-direction:column;
        align-items:flex-start;
        gap:0;

        padding:15px 5% 25px;

        background:rgba(245,243,239,.97);
        backdrop-filter:blur(10px);
    }

    nav.menu-abierto{
        display:flex;
    }

    nav a{
        width:100%;
        padding:14px 0;
        font-size:16px;
    }

    .portada{
        grid-template-columns:1fr;
        padding-top:140px;
    }

    .galeria-grid{
        grid-template-columns:1fr;
    }

    .colaboradores-fila{
        grid-template-columns:repeat(3,1fr) !important;
    }
}

@media(max-width:500px){

    .portada{
        padding:130px 6% 80px;
        gap:45px;
    }

    .portada-texto h1{
        font-size:58px;
    }

    .portada-texto p{
        font-size:16px;
    }

    .seccion,
    .contacto{
        padding:90px 6%;
    }

    .seccion h2,
    .contacto h2{
        font-size:55px;
    }

    .seccion-texto{
        font-size:16px;
    }

    .colaboradores-fila{
        grid-template-columns:repeat(2,1fr) !important;
        gap:18px;
    }

    .colaborador-nombre{
        font-size:21px;
    }
}

</style>
</head>


<body>

<!-- ====================================================== -->
<!-- INICIO — ZONA DE CONFIGURACIÓN -->
<!-- ====================================================== -->

<script>

const CONFIG = {

    /* -------------------------------- */
    /* CABECERA */
    /* -------------------------------- */

    cabecera:{
        on:true,

        logo:"Nuestra Web Pensat i Fet",

        menuInicio:"Inicio",
        menuHistoria:"Historia",
        menuProyecto:"Proyecto",
        menuGaleria:"Galería",
        menuColaboradores:"Colaboradores",
        menuContacto:"Contacto"
    },


    /* -------------------------------- */
    /* PORTADA */
    /* -------------------------------- */

    portada:{
        on:true,

        titulo:"Un espacio para colaborar",

        texto:"Esto es una prueba para anunciantes, los fondos cambian cada vez que entras, los colaboradores cambian tambien de posicion cada vez que entras, es rotativo, he creado 5 grupos, 2,3,4,5,6 colaboradores por fila, facilmente editable si pulsas la imagen de bar tolo te manda a otra web que tambien es editable, he de mejorarla, ya te comentare.Arriba tienes botones directos a historia,proyecto, etc , la galeria tiene fotos de internet, 3 fotos que cambian aleatoriamente cada 30 segundos de una lista que he configurado, se pueden subir las que quieras, cambiarlas etc",

        imagenOn:true,

        imagen:"https://i.ibb.co/3yXfNxj9/sierra-final-limpio.png"
    },


    /* -------------------------------- */
    /* HISTORIA */
    /* -------------------------------- */

    historia:{
        on:true,

        titulo:"Historia",

        texto:"Aqui contaremos algo de la falla ",

        imagenOn:true,

        imagen:"https://images.unsplash.com/photo-1497366754035-f200968a6e72?auto=format&fit=crop&w=1200&q=80"
    },


    /* -------------------------------- */
    /* PROYECTO */
    /* -------------------------------- */

    proyecto:{
        on:true,

        titulo:"Proyecto",

        texto:"Aqui contariamos algo bla bla bla todo es editable en el codigo",

        imagenOn:true,

        imagen:"https://images.unsplash.com/photo-1497366811353-6870744d04b2?auto=format&fit=crop&w=1200&q=80"
    },


    /* -------------------------------- */
    /* GALERÍA */
    /* -------------------------------- */

    galeria:{

        on:true,

        titulo:"Galería",

        imagen1:"https://images.unsplash.com/photo-1497366216548-37526070297c?auto=format&fit=crop&w=1000&q=80",

        imagen2:"https://images.unsplash.com/photo-1497366754035-f200968a6e72?auto=format&fit=crop&w=1000&q=80",

        imagen3:"https://images.unsplash.com/photo-1497366811353-6870744d04b2?auto=format&fit=crop&w=1000&q=80",

        imagen4:"https://images.unsplash.com/photo-1500530855697-b586d89ba3ee?auto=format&fit=crop&w=1000&q=80",

        imagen5:"https://images.unsplash.com/photo-1497366754035-f200968a6e72?auto=format&fit=crop&w=1000&q=80",

        imagen6:"https://images.unsplash.com/photo-1497366216548-37526070297c?auto=format&fit=crop&w=1000&q=80",

        imagen7:"https://images.unsplash.com/photo-1497366811353-6870744d04b2?auto=format&fit=crop&w=1000&q=80",

        imagen8:"https://images.unsplash.com/photo-1500530855697-b586d89ba3ee?auto=format&fit=crop&w=1000&q=80",

        imagen9:"https://images.unsplash.com/photo-1518005020951-eccb494ad742?auto=format&fit=crop&w=1000&q=80",


        /*
            TIEMPO DE ALEATORIZACIÓN

            10000  = 10 segundos
            30000  = 30 segundos
            60000  = 1 minuto
            120000 = 2 minutos
            300000 = 5 minutos
        */

        tiempoAleatorizacion:30000
    },


    /* -------------------------------- */
    /* FONDOS */
    /* -------------------------------- */

    fondos:{

        /*
            TODAS LAS ZONAS UTILIZAN ESTA MISMA LISTA.

            Cada zona selecciona aleatoriamente
            una imagen diferente al cargar la web.

            Si una zona está en false,
            utilizará automáticamente el fondo
            seleccionado para "web".
        */

        imagenes:[

            "https://i.ibb.co/C5DTQS1W/fondo-rojo.jpg",

            "https://i.ibb.co/v6t8xykW/fondo-raro.webp",

            "https://i.ibb.co/CpNc88mN/fondo-verde.jpg",

            "https://i.ibb.co/ns3Yh9JJ/fondo.webp",

            "https://i.ibb.co/v6t8xykW/fondo-raro.webp"
        ],


        web:{
            on:true
        },

        galeria:{
            on:true
        },

        historia:{
            on:true
        },

        proyecto:{
            on:true
        },

        colaboradores:{
            on:true
        }
    },


    /* -------------------------------- */
    /* COLABORADORES */
    /* -------------------------------- */

    colaboradores:{

        on:true,

        grupo2:{
            on:true,
            columnas:2,
            aleatorio:false
        },

        grupo3:{
            on:true,
            columnas:3,
            aleatorio:true
        },

        grupo4:{
            on:true,
            columnas:4,
            aleatorio:true
        },

        grupo5:{
            on:true,
            columnas:5,
            aleatorio:true
        },

        grupo6:{
            on:false,
            columnas:6,
            aleatorio:true
        },


        lista:[

            {
                grupo:2,
                on:true,
                nombre:"Colaborador 1",
                imagen:"https://i.ibb.co/ycBjBjLw/colaboradores-hueso-humo-corto-original.png",
                enlace:"#"
            },

            {
                grupo:2,
                on:true,
                nombre:"Colaborador 2",
                imagen:"https://i.ibb.co/ycBjBjLw/colaboradores-hueso-humo-corto-original.png",
                enlace:"#"
            },

            {
                grupo:3,
                on:true,
                nombre:"Bar Tolo",
                imagen:"https://i.ibb.co/b5Mz3SJf/image-20260925-220449.jpg",
                enlace:"https://aqua-kirby-16.tiiny.site"
            },

            {
                grupo:3,
                on:true,
                nombre:"Colaborador 4",
                imagen:"https://i.ibb.co/ycBjBjLw/colaboradores-hueso-humo-corto-original.png",
                enlace:"#"
            },

            {
                grupo:3,
                on:true,
                nombre:"Colaborador 5",
                imagen:"https://i.ibb.co/ycBjBjLw/colaboradores-hueso-humo-corto-original.png",
                enlace:"#"
            },

            {
                grupo:4,
                on:true,
                nombre:"Bar Tolo",
                imagen:"https://i.ibb.co/b5Mz3SJf/image-20260925-220449.jpg",
                enlace:"https://aqua-kirby-16.tiiny.site"
            },

            {
                grupo:4,
                on:true,
                nombre:"Colaborador 7",
                imagen:"https://i.ibb.co/ycBjBjLw/colaboradores-hueso-humo-corto-original.png",
                enlace:"#"
            },

            {
                grupo:4,
                on:true,
                nombre:"Colaborador 8",
                imagen:"https://i.ibb.co/ycBjBjLw/colaboradores-hueso-humo-corto-original.png",
                enlace:"#"
            },

            {
                grupo:4,
                on:true,
                nombre:"Colaborador 9",
                imagen:"https://i.ibb.co/ycBjBjLw/colaboradores-hueso-humo-corto-original.png",
                enlace:"#"
            },

            {
                grupo:4,
                on:true,
                nombre:"Colaborador 10",
                imagen:"https://i.ibb.co/ycBjBjLw/colaboradores-hueso-humo-corto-original.png",
                enlace:"#"
            },

            {
                grupo:4,
                on:true,
                nombre:"Colaborador 11",
                imagen:"https://i.ibb.co/ycBjBjLw/colaboradores-hueso-humo-corto-original.png",
                enlace:"#"
            },

            {
                grupo:4,
                on:true,
                nombre:"Colaborador 12",
                imagen:"https://i.ibb.co/ycBjBjLw/colaboradores-hueso-humo-corto-original.png",
                enlace:"#"
            },

            {
                grupo:4,
                on:true,
                nombre:"Colaborador 13",
                imagen:"https://i.ibb.co/ycBjBjLw/colaboradores-hueso-humo-corto-original.png",
                enlace:"#"
            },

            {
                grupo:5,
                on:true,
                nombre:"Bar Tolo",
                imagen:"https://i.ibb.co/b5Mz3SJf/image-20260925-220449.jpg",
                enlace:"https://aqua-kirby-16.tiiny.site"
            },

            {
                grupo:5,
                on:true,
                nombre:"Colaborador 15",
                imagen:"https://i.ibb.co/ycBjBjLw/colaboradores-hueso-humo-corto-original.png",
                enlace:"#"
            },

            {
                grupo:5,
                on:true,
                nombre:"Colaborador 16",
                imagen:"https://i.ibb.co/ycBjBjLw/colaboradores-hueso-humo-corto-original.png",
                enlace:"#"
            },

            {
                grupo:5,
                on:true,
                nombre:"Colaborador 17",
                imagen:"https://i.ibb.co/ycBjBjLw/colaboradores-hueso-humo-corto-original.png",
                enlace:"#"
            },

            {
                grupo:5,
                on:true,
                nombre:"Colaborador 18",
                imagen:"https://i.ibb.co/ycBjBjLw/colaboradores-hueso-humo-corto-original.png",
                enlace:"#"
            },

            {
                grupo:6,
                on:true,
                nombre:"Colaborador 19",
                imagen:"https://i.ibb.co/ycBjBjLw/colaboradores-hueso-humo-corto-original.png",
                enlace:"#"
            },

            {
                grupo:6,
                on:true,
                nombre:"Colaborador 20",
                imagen:"https://i.ibb.co/ycBjBjLw/colaboradores-hueso-humo-corto-original.png",
                enlace:"#"
            },

            {
                grupo:6,
                on:true,
                nombre:"Colaborador 21",
                imagen:"https://i.ibb.co/ycBjBjLw/colaboradores-hueso-humo-corto-original.png",
                enlace:"#"
            },

            {
                grupo:6,
                on:true,
                nombre:"Colaborador 22",
                imagen:"https://i.ibb.co/ycBjBjLw/colaboradores-hueso-humo-corto-original.png",
                enlace:"#"
            },

            {
                grupo:6,
                on:true,
                nombre:"Colaborador 23",
                imagen:"https://i.ibb.co/ycBjBjLw/colaboradores-hueso-humo-corto-original.png",
                enlace:"#"
            },

            {
                grupo:6,
                on:true,
                nombre:"Colaborador 24",
                imagen:"https://i.ibb.co/ycBjBjLw/colaboradores-hueso-humo-corto-original.png",
                enlace:"#"
            }
        ]
    },


    /* -------------------------------- */
    /* CONTACTO */
    /* -------------------------------- */

    contacto:{

        on:true,

        telefono:"963498903",

        email:"aqui va el correo",

        direccion:"Carrer de Clarachet, 6, Benicalap, 46015 València, Valencia",

        ubicacionGoogle:{
            on:true,
            texto:"Ver ubicación en Google Maps",
            enlace:"https://maps.app.goo.gl/EfA1WLu4D2hDqhFP6"
        },

        redes:{

            red1:{
                on:true,
                nombre:"Instagram",
                enlace:"https://www.instagram.com/fallasierramartes/"
            },

            red2:{
                on:true,
                nombre:"Facebook",
                enlace:"https://www.facebook.com/fallasierramartes?locale=es_ES"
            },

            red3:{
                on:true,
                nombre:"YouTube",
                enlace:"https://youtube.com/"
            }
        }
    },


    /* -------------------------------- */
    /* FOOTER */
    /* -------------------------------- */

    footer:{
        on:true,
        texto:"© 2026 Web Pensat i Fet"
    }

};


/* ====================================================== */
/* FIN — ZONA DE CONFIGURACIÓN */
/* ====================================================== */


/* ====================================================== */
/* VARIABLES INTERNAS */
/* ====================================================== */

let fondosSeleccionados = {};

let intervaloGaleria = null;


/* ====================================================== */
/* FUNCIONES GENERALES */
/* ====================================================== */

function obtenerElemento(id){

    return document.getElementById(id);

}


function mezclarArray(array){

    const copia = [...array];

    for(let i=copia.length-1;i>0;i--){

        const j=Math.floor(Math.random()*(i+1));

        [copia[i],copia[j]]=[copia[j],copia[i]];
    }

    return copia;
}


function mostrarElemento(id){

    const elemento=obtenerElemento(id);

    if(elemento){
        elemento.style.display="";
    }

}


function ocultarElemento(id){

    const elemento=obtenerElemento(id);

    if(elemento){
        elemento.style.display="none";
    }

}


/* ====================================================== */
/* FONDOS */
/* ====================================================== */

function cargarFondos(){

    const fondos=CONFIG.fondos.imagenes;

    if(!Array.isArray(fondos) || fondos.length===0){

        fondosSeleccionados.web="";

        return;
    }


    function fondoAleatorio(){

        return fondos[Math.floor(Math.random()*fondos.length)];

    }


    fondosSeleccionados.web=
        CONFIG.fondos.web.on
        ? fondoAleatorio()
        : fondos[0];


    fondosSeleccionados.galeria=
        CONFIG.fondos.galeria.on
        ? fondoAleatorio()
        : fondosSeleccionados.web;


    fondosSeleccionados.historia=
        CONFIG.fondos.historia.on
        ? fondoAleatorio()
        : fondosSeleccionados.web;


    fondosSeleccionados.proyecto=
        CONFIG.fondos.proyecto.on
        ? fondoAleatorio()
        : fondosSeleccionados.web;


    fondosSeleccionados.colaboradores=
        CONFIG.fondos.colaboradores.on
        ? fondoAleatorio()
        : fondosSeleccionados.web;


    if(fondosSeleccionados.web){

        document.body.style.backgroundImage=
            `url("${fondosSeleccionados.web}")`;
    }

}


function aplicarFondosSecciones(){

    const galeria=obtenerElemento("galeria");

    const historia=obtenerElemento("historia");

    const proyecto=obtenerElemento("proyecto");

    const colaboradores=obtenerElemento("colaboradores");


    if(galeria && fondosSeleccionados.galeria){

        galeria.style.backgroundImage=
            `url("${fondosSeleccionados.galeria}")`;
    }


    if(historia && fondosSeleccionados.historia){

        historia.style.backgroundImage=
            `url("${fondosSeleccionados.historia}")`;
    }


    if(proyecto && fondosSeleccionados.proyecto){

        proyecto.style.backgroundImage=
            `url("${fondosSeleccionados.proyecto}")`;
    }


    if(colaboradores && fondosSeleccionados.colaboradores){

        colaboradores.style.backgroundImage=
            `url("${fondosSeleccionados.colaboradores}")`;
    }

}


/* ====================================================== */
/* CABECERA */
/* ====================================================== */

function cargarCabecera(){

    const header=obtenerElemento("cabecera");

    if(!header) return;


    if(!CONFIG.cabecera.on){

        header.style.display="none";

        return;
    }


    const logo=obtenerElemento("logo");

    const navInicio=obtenerElemento("navInicio");

    const navHistoria=obtenerElemento("navHistoria");

    const navProyecto=obtenerElemento("navProyecto");

    const navGaleria=obtenerElemento("navGaleria");

    const navColaboradores=obtenerElemento("navColaboradores");

    const navContacto=obtenerElemento("navContacto");


    if(logo){

        logo.textContent=CONFIG.cabecera.logo;
    }


    if(navInicio){

        navInicio.textContent=CONFIG.cabecera.menuInicio;
    }


    if(navHistoria){

        navHistoria.textContent=CONFIG.cabecera.menuHistoria;
    }


    if(navProyecto){

        navProyecto.textContent=CONFIG.cabecera.menuProyecto;
    }


    if(navGaleria){

        navGaleria.textContent=CONFIG.cabecera.menuGaleria;
    }


    if(navColaboradores){

        navColaboradores.textContent=CONFIG.cabecera.menuColaboradores;
    }


    if(navContacto){

        navContacto.textContent=CONFIG.cabecera.menuContacto;
    }

}


/* ====================================================== */
/* PORTADA */
/* ====================================================== */

function cargarPortada(){

    const portada=obtenerElemento("portada");

    if(!portada) return;


    if(!CONFIG.portada.on){

        portada.style.display="none";

        return;
    }


    const titulo=obtenerElemento("portadaTitulo");

    const texto=obtenerElemento("portadaTexto");

    const imagen=obtenerElemento("portadaImagen");

    const contenedorImagen=obtenerElemento("portadaImagenContenedor");


    if(titulo){

        titulo.textContent=CONFIG.portada.titulo;
    }


    if(texto){

        texto.textContent=CONFIG.portada.texto;
    }


    if(contenedorImagen){

        if(CONFIG.portada.imagenOn && CONFIG.portada.imagen){

            contenedorImagen.style.display="";
        }
        else{

            contenedorImagen.style.display="none";
        }
    }


    if(imagen && CONFIG.portada.imagen){

        imagen.src=CONFIG.portada.imagen;
    }

}


/* ====================================================== */
/* HISTORIA */
/* ====================================================== */

function cargarHistoria(){

    const seccion=obtenerElemento("historia");

    if(!seccion) return;


    if(!CONFIG.historia.on){

        seccion.style.display="none";

        return;
    }


    const titulo=obtenerElemento("historiaTitulo");

    const texto=obtenerElemento("historiaTexto");

    const imagen=obtenerElemento("historiaImagen");

    const contenedorImagen=obtenerElemento("historiaImagenContenedor");


    if(titulo){

        titulo.textContent=CONFIG.historia.titulo;
    }


    if(texto){

        texto.textContent=CONFIG.historia.texto;
    }


    if(imagen){

        imagen.src=CONFIG.historia.imagen;
    }


    if(contenedorImagen){

        contenedorImagen.style.display=
            CONFIG.historia.imagenOn
            ? ""
            : "none";
    }

}


/* ====================================================== */
/* PROYECTO */
/* ====================================================== */

function cargarProyecto(){

    const seccion=obtenerElemento("proyecto");

    if(!seccion) return;


    if(!CONFIG.proyecto.on){

        seccion.style.display="none";

        return;
    }


    const titulo=obtenerElemento("proyectoTitulo");

    const texto=obtenerElemento("proyectoTexto");

    const imagen=obtenerElemento("proyectoImagen");

    const contenedorImagen=obtenerElemento("proyectoImagenContenedor");


    if(titulo){

        titulo.textContent=CONFIG.proyecto.titulo;
    }


    if(texto){

        texto.textContent=CONFIG.proyecto.texto;
    }


    if(imagen){

        imagen.src=CONFIG.proyecto.imagen;
    }


    if(contenedorImagen){

        contenedorImagen.style.display=
            CONFIG.proyecto.imagenOn
            ? ""
            : "none";
    }

}


/* ====================================================== */
/* GALERÍA */
/* ====================================================== */

function obtenerImagenesGaleria(){

    const imagenes=[];

    Object.keys(CONFIG.galeria).forEach(clave=>{

        if(clave.startsWith("imagen")){

            const valor=CONFIG.galeria[clave];

            if(typeof valor==="string" && valor.trim()!==""){

                imagenes.push(valor);
            }
        }
    });

    return imagenes;
}


function actualizarGaleria(){

    const contenedor=obtenerElemento("galeriaGrid");

    if(!contenedor) return;


    const imagenes=obtenerImagenesGaleria();

    if(imagenes.length===0){

        contenedor.innerHTML="";

        return;
    }


    const seleccionadas=mezclarArray(imagenes).slice(
        0,
        Math.min(3,imagenes.length)
    );


    const elementos=[
        obtenerElemento("galeriaImagen1"),
        obtenerElemento("galeriaImagen2"),
        obtenerElemento("galeriaImagen3")
    ];


    elementos.forEach((img,index)=>{

        if(!img) return;


        if(seleccionadas[index]){

            img.style.opacity="0";


            setTimeout(()=>{

                img.src=seleccionadas[index];

                img.onload=()=>{

                    img.style.opacity="1";
                };

            },300);

        }
        else{

            img.style.display="none";
        }

    });

}


function cargarGaleria(){

    const seccion=obtenerElemento("galeria");

    if(!seccion) return;


    if(!CONFIG.galeria.on){

        seccion.style.display="none";

        return;
    }


    const titulo=obtenerElemento("galeriaTitulo");

    if(titulo){

        titulo.textContent=CONFIG.galeria.titulo;
    }


    actualizarGaleria();


    if(intervaloGaleria){

        clearInterval(intervaloGaleria);

        intervaloGaleria=null;
    }


    const imagenes=obtenerImagenesGaleria();

    if(
        imagenes.length>3 &&
        Number(CONFIG.galeria.tiempoAleatorizacion)>0
    ){

        intervaloGaleria=setInterval(

            actualizarGaleria,

            Number(CONFIG.galeria.tiempoAleatorizacion)

        );
    }

}


/* ====================================================== */
/* COLABORADORES */
/* ====================================================== */

function cargarColaboradores(){

    const seccion=obtenerElemento("colaboradores");

    const contenedor=obtenerElemento("colaboradoresGrid");


    if(!seccion || !contenedor) return;


    if(!CONFIG.colaboradores.on){

        seccion.style.display="none";

        return;
    }


    contenedor.innerHTML="";


    for(let numeroGrupo=2;numeroGrupo<=6;numeroGrupo++){

        const configuracion=
            CONFIG.colaboradores["grupo"+numeroGrupo];


        if(!configuracion || !configuracion.on){

            continue;
        }


        let lista=
            CONFIG.colaboradores.lista.filter(

                colaborador=>
                    colaborador.grupo===numeroGrupo &&
                    colaborador.on===true
            );


        if(lista.length===0){

            continue;
        }


        if(configuracion.aleatorio){

            lista=mezclarArray(lista);
        }


        const fila=document.createElement("div");

        fila.className="colaboradores-fila";


        fila.style.gridTemplateColumns=
            `repeat(${configuracion.columnas},1fr)`;


        lista.forEach(colaborador=>{

            const elemento=document.createElement("div");

            elemento.className="colaborador";


            const contenedorImagen=
                document.createElement("div");

            contenedorImagen.className="colaborador-imagen";


            if(
                colaborador.enlace &&
                colaborador.enlace!=="#"
            ){

                const enlace=document.createElement("a");

                enlace.href=colaborador.enlace;

                enlace.target="_blank";

                enlace.rel="noopener noreferrer";


                const imagen=
                    document.createElement("img");

                imagen.src=colaborador.imagen;

                imagen.alt=colaborador.nombre;

                imagen.loading="lazy";


                enlace.appendChild(imagen);

                contenedorImagen.appendChild(enlace);

            }
            else{

                const imagen=
                    document.createElement("img");

                imagen.src=colaborador.imagen;

                imagen.alt=colaborador.nombre;

                imagen.loading="lazy";


                contenedorImagen.appendChild(imagen);
            }


            const nombre=
                document.createElement("div");

            nombre.className="colaborador-nombre";

            nombre.textContent=colaborador.nombre;


            elemento.appendChild(contenedorImagen);

            elemento.appendChild(nombre);

            fila.appendChild(elemento);

        });


        contenedor.appendChild(fila);
    }

}


/* ====================================================== */
/* CONTACTO */
/* ====================================================== */

function cargarContacto(){

    const seccion=obtenerElemento("contacto");

    if(!seccion) return;


    if(!CONFIG.contacto.on){

        seccion.style.display="none";

        return;
    }


    const telefono=obtenerElemento("contactoTelefono");

    const email=obtenerElemento("contactoEmail");

    const direccion=obtenerElemento("contactoDireccion");

    const ubicacion=obtenerElemento("contactoUbicacion");

    const redes=obtenerElemento("redes");


    if(telefono){

        telefono.textContent=CONFIG.contacto.telefono;

        const numero=
            CONFIG.contacto.telefono.replace(
                /[^\d+]/g,
                ""
            );

        telefono.href="tel:"+numero;
    }


    if(email){

        email.textContent=CONFIG.contacto.email;

        email.href=
            "mailto:"+CONFIG.contacto.email;
    }


    if(direccion){

        direccion.textContent=
            CONFIG.contacto.direccion;
    }


    if(ubicacion){

        if(
            CONFIG.contacto.ubicacionGoogle.on &&
            CONFIG.contacto.ubicacionGoogle.enlace
        ){

            ubicacion.style.display="";

            ubicacion.textContent=
                CONFIG.contacto.ubicacionGoogle.texto;

            ubicacion.href=
                CONFIG.contacto.ubicacionGoogle.enlace;

            ubicacion.target="_blank";

            ubicacion.rel=
                "noopener noreferrer";

        }
        else{

            ubicacion.style.display="none";
        }
    }


    if(redes){

        redes.innerHTML="";


        Object.keys(CONFIG.contacto.redes)
        .forEach(clave=>{

            const red=
                CONFIG.contacto.redes[clave];


            if(!red.on) return;


            const enlace=
                document.createElement("a");

            enlace.href=red.enlace;

            enlace.textContent=red.nombre;

            enlace.target="_blank";

            enlace.rel="noopener noreferrer";


            redes.appendChild(enlace);
        });
    }

}


/* ====================================================== */
/* FOOTER */
/* ====================================================== */

function cargarFooter(){

    const footer=obtenerElemento("footer");

    if(!footer) return;


    if(!CONFIG.footer.on){

        footer.style.display="none";

        return;
    }


    const texto=obtenerElemento("footerTexto");

    if(texto){

        texto.textContent=
            CONFIG.footer.texto;
    }

}


/* ====================================================== */
/* NAVEGACIÓN */
/* ====================================================== */

function cerrarMenuMovil(){

    const nav=obtenerElemento("nav");

    if(nav){

        nav.classList.remove("menu-abierto");
    }

}


function cerrarSeccionesNavegables(){

    [
        "historia",
        "proyecto",
        "galeria"
    ].forEach(id=>{

        const elemento=obtenerElemento(id);

        if(elemento){

            elemento.classList.add(
                "oculta-navegacion"
            );
        }

    });

}


function mostrarSeccion(id){

    const elemento=obtenerElemento(id);

    if(!elemento) return;


    const yaEstabaAbierta=
        !elemento.classList.contains(
            "oculta-navegacion"
        );


    cerrarSeccionesNavegables();


    if(!yaEstabaAbierta){

        elemento.classList.remove(
            "oculta-navegacion"
        );


        setTimeout(()=>{

            elemento.scrollIntoView({
                behavior:"smooth",
                block:"start"
            });

        },50);

    }

}


function volverInicio(){

    cerrarSeccionesNavegables();

    cerrarMenuMovil();


    window.scrollTo({
        top:0,
        behavior:"smooth"
    });

}


function configurarNavegacion(){

    const navInicio=obtenerElemento("navInicio");

    const navHistoria=obtenerElemento("navHistoria");

    const navProyecto=obtenerElemento("navProyecto");

    const navGaleria=obtenerElemento("navGaleria");

    const navColaboradores=
        obtenerElemento("navColaboradores");

    const navContacto=
        obtenerElemento("navContacto");


    if(navInicio){

        navInicio.addEventListener(
            "click",
            volverInicio
        );
    }


    if(navHistoria){

        navHistoria.addEventListener(
            "click",
            ()=>{

                mostrarSeccion("historia");

                cerrarMenuMovil();
            }
        );
    }


    if(navProyecto){

        navProyecto.addEventListener(
            "click",
            ()=>{

                mostrarSeccion("proyecto");

                cerrarMenuMovil();
            }
        );
    }


    if(navGaleria){

        navGaleria.addEventListener(
            "click",
            ()=>{

                mostrarSeccion("galeria");

                cerrarMenuMovil();
            }
        );
    }


    if(navColaboradores){

        navColaboradores.addEventListener(
            "click",
            ()=>{

                cerrarSeccionesNavegables();

                cerrarMenuMovil();


                const seccion=
                    obtenerElemento(
                        "colaboradores"
                    );


                if(seccion){

                    seccion.scrollIntoView({
                        behavior:"smooth",
                        block:"start"
                    });
                }

            }
        );
    }


    if(navContacto){

        navContacto.addEventListener(
            "click",
            ()=>{

                cerrarSeccionesNavegables();

                cerrarMenuMovil();


                const seccion=
                    obtenerElemento("contacto");


                if(seccion){

                    seccion.scrollIntoView({
                        behavior:"smooth",
                        block:"start"
                    });
                }

            }
        );
    }


    const menuToggle=
        obtenerElemento("menuToggle");


    if(menuToggle){

        menuToggle.addEventListener(
            "click",
            ()=>{

                const nav=
                    obtenerElemento("nav");

                if(nav){

                    nav.classList.toggle(
                        "menu-abierto"
                    );
                }

            }
        );
    }

}


function ocultarSeccionesNavegables(){

    cerrarSeccionesNavegables();

}


/* ====================================================== */
/* INICIALIZACIÓN */
/* ====================================================== */

/*
    IMPORTANTE:

    Este código se encuentra al principio del BODY
    porque así lo hemos configurado.

    Sin embargo, las funciones NO se ejecutan
    inmediatamente.

    Esperamos a DOMContentLoaded para asegurarnos
    de que todos los elementos HTML ya existen.
*/

document.addEventListener(
    "DOMContentLoaded",
    function(){

        cargarFondos();

        aplicarFondosSecciones();

        cargarCabecera();

        cargarPortada();

        cargarHistoria();

        cargarProyecto();

        cargarGaleria();

        cargarColaboradores();

        cargarContacto();

        cargarFooter();

        configurarNavegacion();

        ocultarSeccionesNavegables();

    }
);

</script>


<!-- ====================================================== -->
<!-- CABECERA -->
<!-- ====================================================== -->

<header id="cabecera">

    <div class="logo" id="logo">
        Mi Web
    </div>


    <button
        class="menu-toggle"
        id="menuToggle"
        aria-label="Abrir menú"
        type="button"
    >
        ☰
    </button>


    <nav id="nav">

        <a id="navInicio">Inicio</a>

        <a id="navHistoria">Historia</a>

        <a id="navProyecto">Proyecto</a>

        <a id="navGaleria">Galería</a>

        <a id="navColaboradores">Colaboradores</a>

        <a id="navContacto">Contacto</a>

    </nav>

</header>


<!-- ====================================================== -->
<!-- CONTENIDO -->
<!-- ====================================================== -->

<main>


    <!-- PORTADA -->

    <section
        class="portada"
        id="portada"
    >

        <div class="portada-texto">

            <h1 id="portadaTitulo">
                Una historia que continúa
            </h1>

            <p id="portadaTexto">
                Un espacio creado para compartir nuestra historia,
                nuestros proyectos y las personas que forman parte
                de ellos.
            </p>

        </div>


        <div
            class="portada-imagen"
            id="portadaImagenContenedor"
        >

            <img
                id="portadaImagen"
                src=""
                alt="Imagen de portada"
            >

        </div>

    </section>


    <!-- HISTORIA -->

    <section
        class="seccion oculta-navegacion"
        id="historia"
    >

        <div class="seccion-contenido">

            <h2 id="historiaTitulo">
                Historia
            </h2>

            <p
                class="seccion-texto"
                id="historiaTexto"
            >
            </p>


            <div
                class="seccion-imagen"
                id="historiaImagenContenedor"
            >

                <img
                    id="historiaImagen"
                    src=""
                    alt="Historia"
                >

            </div>

        </div>

    </section>


    <!-- PROYECTO -->

    <section
        class="seccion oculta-navegacion"
        id="proyecto"
    >

        <div class="seccion-contenido">

            <h2 id="proyectoTitulo">
                Proyecto
            </h2>

            <p
                class="seccion-texto"
                id="proyectoTexto"
            >
            </p>


            <div
                class="seccion-imagen"
                id="proyectoImagenContenedor"
            >

                <img
                    id="proyectoImagen"
                    src=""
                    alt="Proyecto"
                >

            </div>

        </div>

    </section>


    <!-- GALERÍA -->

    <section
        class="seccion oculta-navegacion"
        id="galeria"
    >

        <div class="seccion-contenido">

            <h2 id="galeriaTitulo">
                Galería
            </h2>


            <div
                class="galeria-grid"
                id="galeriaGrid"
            >

                <div class="galeria-item">

                    <img
                        id="galeriaImagen1"
                        src=""
                        alt="Galería 1"
                    >

                </div>


                <div class="galeria-item">

                    <img
                        id="galeriaImagen2"
                        src=""
                        alt="Galería 2"
                    >

                </div>


                <div class="galeria-item">

                    <img
                        id="galeriaImagen3"
                        src=""
                        alt="Galería 3"
                    >

                </div>

            </div>

        </div>

    </section>


    <!-- COLABORADORES -->

    <section
        class="seccion"
        id="colaboradores"
    >

        <div class="seccion-contenido">

            <h2>
                Colaboradores
            </h2>


            <div
                class="colaboradores-grid"
                id="colaboradoresGrid"
            >
            </div>

        </div>

    </section>


    <!-- CONTACTO -->

    <section
        class="contacto"
        id="contacto"
    >

        <div class="contacto-contenido">

            <h2>
                Contacto
            </h2>


            <div class="contacto-dato">

                <a
                    id="contactoTelefono"
                    href="#"
                >
                </a>

            </div>


            <div class="contacto-dato">

                <a
                    id="contactoEmail"
                    href="#"
                >
                </a>

            </div>


            <div
                class="contacto-dato"
                id="contactoDireccion"
            >
            </div>


            <div class="contacto-dato">

                <a
                    id="contactoUbicacion"
                    href="#"
                >
                </a>

            </div>


            <div
                class="redes"
                id="redes"
            >
            </div>

        </div>

    </section>


</main>


<!-- ====================================================== -->
<!-- FOOTER -->
<!-- ====================================================== -->

<footer id="footer">

    <p id="footerTexto">
        © 2026 solo una prueba para que veas
    </p>

</footer>


</body>
</html>
