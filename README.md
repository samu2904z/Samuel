<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Para ti 🌻</title>

<style>
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
}

body{
    overflow:hidden;
    font-family:Georgia,"Times New Roman",serif;
}

/* =========================
   INICIO
========================= */

#inicio{
    position:fixed;
    inset:0;
    z-index:100;
    display:flex;
    justify-content:center;
    align-items:center;
    text-align:center;
    cursor:pointer;
    background:linear-gradient(135deg,#171126,#392052,#6b3f69);
    transition:1.2s ease;
}

#inicio.oculto{
    opacity:0;
    pointer-events:none;
}

.inicio-contenido{
    color:white;
}

.girasol-inicio{
    position:relative;
    width:140px;
    height:140px;
    margin:auto;
    animation:flotar 3s ease-in-out infinite;
}

.petalo-inicio{
    position:absolute;
    width:42px;
    height:70px;
    left:49px;
    top:35px;
    border-radius:50%;
    background:linear-gradient(#fff05b,#f1ad00);
    transform-origin:21px 35px;
}

.petalo-inicio:nth-child(1){transform:rotate(0deg) translateY(-30px)}
.petalo-inicio:nth-child(2){transform:rotate(45deg) translateY(-30px)}
.petalo-inicio:nth-child(3){transform:rotate(90deg) translateY(-30px)}
.petalo-inicio:nth-child(4){transform:rotate(135deg) translateY(-30px)}
.petalo-inicio:nth-child(5){transform:rotate(180deg) translateY(-30px)}
.petalo-inicio:nth-child(6){transform:rotate(225deg) translateY(-30px)}
.petalo-inicio:nth-child(7){transform:rotate(270deg) translateY(-30px)}
.petalo-inicio:nth-child(8){transform:rotate(315deg) translateY(-30px)}

.centro-inicio{
    position:absolute;
    width:48px;
    height:48px;
    left:46px;
    top:46px;
    border-radius:50%;
    background:radial-gradient(circle,#63360d,#180b02);
    z-index:5;
}

#inicio h1{
    margin-top:30px;
    font-size:34px;
}

#inicio p{
    margin-top:10px;
    opacity:.8;
}

@keyframes flotar{
    0%,100%{transform:translateY(0)}
    50%{transform:translateY(-12px)}
}


/* =========================
   ESCENA
========================= */

#escena{
    position:fixed;
    inset:0;
    opacity:0;
    visibility:hidden;
    transition:1.5s ease;

    background:
        linear-gradient(
            to bottom,
            #5b3c88 0%,
            #b86d9c 25%,
            #f3a66d 48%,
            #ffd18b 63%,
            #7ca86d 82%,
            #365b3d 100%
        );
}

#escena.visible{
    opacity:1;
    visibility:visible;
}


/* SOL */

.sol{
    position:absolute;
    width:135px;
    height:135px;
    left:50%;
    top:14%;
    transform:translateX(-50%);
    border-radius:50%;
    background:#fff0a8;
    box-shadow:
        0 0 40px #ffe99b,
        0 0 100px rgba(255,220,120,.7);
}


/* MONTAÑAS */

.montana{
    position:absolute;
    bottom:24%;
    width:0;
    height:0;
    border-left:230px solid transparent;
    border-right:230px solid transparent;
    border-bottom:270px solid rgba(62,66,91,.65);
}

.m1{left:-120px}

.m2{
    left:25%;
    transform:scale(1.25);
    border-bottom-color:rgba(65,65,92,.7);
}

.m3{
    right:-130px;
    transform:scale(.9);
}


/* PASTO */

.pasto{
    position:absolute;
    bottom:0;
    width:100%;
    height:28%;
    background:linear-gradient(to bottom,#58794e,#365c3e);
}


/* TEXTO */

.mensaje-superior{
    position:absolute;
    top:7%;
    width:100%;
    z-index:10;
    text-align:center;
    color:white;
    text-shadow:0 2px 10px rgba(0,0,0,.4);
}

.mensaje-superior h2{
    font-size:28px;
    margin-bottom:10px;
}

.mensaje-superior p{
    font-size:17px;
}


/* =========================
   CORAZÓN
========================= */

.corazon{
    position:absolute;
    width:min(600px,90vw);
    height:min(520px,75vh);
    left:50%;
    top:53%;
    transform:translate(-50%,-50%);
    z-index:20;

    filter:
        drop-shadow(0 0 15px rgba(255,222,54,.55))
        drop-shadow(0 0 35px rgba(255,210,40,.25));
}

.corazon svg{
    width:100%;
    height:100%;
    overflow:visible;
}


/* FLORES */

.flor{
    transform-box:fill-box;
    transform-origin:center;
}

.petalo{
    fill:url(#amarillo);
}

.centro{
    fill:url(#centro);
}


/* brillo */

.brillo{
    animation:pulso 3s ease-in-out infinite;
    transform-origin:center;
}

@keyframes pulso{
    0%,100%{
        opacity:.35;
    }
    50%{
        opacity:.75;
    }
}


/* LUCES */

.luz{
    position:absolute;
    width:5px;
    height:5px;
    border-radius:50%;
    background:#fff7a8;
    box-shadow:0 0 12px #fff3a0;
    animation:subir 5s ease-in-out infinite;
}

.luz:nth-of-type(1){left:10%;bottom:20%}
.luz:nth-of-type(2){left:22%;bottom:35%;animation-delay:1s}
.luz:nth-of-type(3){left:75%;bottom:30%;animation-delay:2s}
.luz:nth-of-type(4){left:88%;bottom:18%;animation-delay:3s}
.luz:nth-of-type(5){left:65%;bottom:40%;animation-delay:1.5s}
.luz:nth-of-type(6){left:35%;bottom:25%;animation-delay:2.5s}
.luz:nth-of-type(7){left:52%;bottom:18%;animation-delay:4s}

@keyframes subir{
    0%,100%{
        transform:translateY(0);
        opacity:.2;
    }

    50%{
        transform:translateY(-60px);
        opacity:1;
    }
}


/* =========================
   CARTA
========================= */

#carta{
    position:fixed;
    inset:0;
    z-index:200;

    display:flex;
    justify-content:center;
    align-items:center;

    padding:25px;

    background:
        radial-gradient(
            circle at center,
            #fff6cf,
            #f6d98a 55%,
            #e7b95c
        );

    opacity:0;
    visibility:hidden;
    transition:1.5s ease;
    overflow:auto;
}

#carta.visible{
    opacity:1;
    visibility:visible;
}

.contenido-carta{
    width:min(720px,92%);
    padding:55px 50px;

    background:rgba(255,255,255,.9);

    border:2px solid rgba(218,167,46,.35);
    border-radius:25px;

    box-shadow:
        0 20px 60px rgba(91,59,15,.25);

    text-align:center;
    color:#654719;
}

.contenido-carta h1{
    font-size:34px;
    color:#b87900;
    margin-bottom:30px;
}

.contenido-carta p{
    font-size:20px;
    line-height:1.8;
    margin-bottom:20px;
}

.firma{
    margin-top:30px;
    font-size:25px;
    color:#a56a00;
    font-style:italic;
}


/* =========================
   MÓVIL
========================= */

@media(max-width:600px){

    .mensaje-superior h2{
        font-size:22px;
    }

    .mensaje-superior p{
        font-size:14px;
        padding:0 20px;
    }

    .corazon{
        width:95vw;
        height:70vh;
        top:53%;
    }

    .contenido-carta{
        padding:35px 25px;
    }

    .contenido-carta h1{
        font-size:26px;
    }

    .contenido-carta p{
        font-size:17px;
    }
}
</style>
</head>

<body>


<!-- =========================
     INICIO
========================= -->

<div id="inicio">

    <div class="inicio-contenido">

        <div class="girasol-inicio">

            <div class="petalo-inicio"></div>
            <div class="petalo-inicio"></div>
            <div class="petalo-inicio"></div>
            <div class="petalo-inicio"></div>
            <div class="petalo-inicio"></div>
            <div class="petalo-inicio"></div>
            <div class="petalo-inicio"></div>
            <div class="petalo-inicio"></div>

            <div class="centro-inicio"></div>

        </div>

        <h1>Para ti 🌻</h1>
        <p>Haz clic para entrar</p>

    </div>

</div>


<!-- =========================
     ESCENA
========================= -->

<section id="escena">

    <div class="sol"></div>

    <div class="montana m1"></div>
    <div class="montana m2"></div>
    <div class="montana m3"></div>

    <div class="pasto"></div>


    <div class="mensaje-superior">
        <h2>🌻 Para alguien muy especial 🌻</h2>

        <p>
            Hay flores que simplemente florecen...
            y otras que hacen florecer el corazón.
        </p>
    </div>


    <div class="luz"></div>
    <div class="luz"></div>
    <div class="luz"></div>
    <div class="luz"></div>
    <div class="luz"></div>
    <div class="luz"></div>
    <div class="luz"></div>


    <!-- =========================
         CORAZÓN DE MUCHÍSIMAS FLORES
    ========================= -->

    <div class="corazon">

        <svg viewBox="0 0 600 520">

            <defs>

                <!-- Silueta perfecta del corazón -->

                <clipPath id="clipCorazon">

                    <path d="
                        M300 475
                        C275 445 80 325 55 185
                        C35 75 150 25 225 75
                        C260 98 282 125 300 150
                        C318 125 340 98 375 75
                        C450 25 565 75 545 185
                        C520 325 325 445 300 475
                        Z
                    "/>

                </clipPath>


                <!-- Flor amarilla -->

                <radialGradient id="amarillo"
                                cx="35%"
                                cy="25%"
                                r="80%">

                    <stop offset="0%" stop-color="#fff98a"/>
                    <stop offset="45%" stop-color="#ffe342"/>
                    <stop offset="100%" stop-color="#e8a800"/>

                </radialGradient>


                <radialGradient id="centro">

                    <stop offset="0%" stop-color="#8b5510"/>
                    <stop offset="65%" stop-color="#4e2707"/>
                    <stop offset="100%" stop-color="#241000"/>

                </radialGradient>

            </defs>


            <!-- Todo lo que se dibuja aquí queda encerrado
                 dentro de la silueta del corazón -->

            <g clip-path="url(#clipCorazon)">

                <!-- fondo amarillo para eliminar huecos -->

                <rect
                    x="0"
                    y="0"
                    width="600"
                    height="520"
                    fill="#f5c51c"
                />


                <!-- Las flores se generan automáticamente -->

                <g id="flores"></g>

            </g>


            <!-- brillo exterior -->

            <path
                class="brillo"
                d="
                    M300 475
                    C275 445 80 325 55 185
                    C35 75 150 25 225 75
                    C260 98 282 125 300 150
                    C318 125 340 98 375 75
                    C450 25 565 75 545 185
                    C520 325 325 445 300 475
                    Z
                "
                fill="none"
                stroke="rgba(255,240,120,.75)"
                stroke-width="5"
            />

        </svg>

    </div>

</section>


<!-- =========================
     CARTA
========================= -->

<section id="carta">

    <div class="contenido-carta">

        <h1>🌻 Feliz día de las flores amarillas 🌻</h1>

        <p>
            Cada girasol que ves aquí es un pequeño
            latido de mi corazón.
        </p>

        <p>
            Así como el sol ilumina los campos,
            tú tienes esa forma especial de
            iluminar mis días.
        </p>

        <p>
            Quiero que cuando veas estas flores
            recuerdes lo especial que eres para mí
            y la sonrisa tan bonita que provocas en mí.
        </p>

        <div class="firma">
            Eres el sol que hace florecer
            cada uno de mis días. 💛
        </div>

    </div>

</section>


<script>

/* ==========================================
   GENERAR CIENTOS DE FLORES
   DENTRO DE LA SILUETA DEL CORAZÓN
========================================== */

const contenedor = document.getElementById("flores");

const ancho = 600;
const alto = 520;

/*
   Flores muy juntas.
   Al estar dentro del clipPath,
   automáticamente toman la forma
   exacta del corazón.
*/

for(let y = 45; y < alto; y += 28){

    for(let x = 35; x < ancho; x += 28){

        const flor = document.createElementNS(
            "http://www.w3.org/2000/svg",
            "g"
        );

        flor.setAttribute(
            "transform",
            `translate(${x} ${y}) rotate(${Math.random()*25-12})`
        );

        flor.setAttribute(
            "class",
            "flor"
        );


        /* 8 pétalos */

        for(let i = 0; i < 8; i++){

            const petalo =
                document.createElementNS(
                    "http://www.w3.org/2000/svg",
                    "ellipse"
                );

            petalo.setAttribute("class","petalo");

            petalo.setAttribute("cx","0");
            petalo.setAttribute("cy","-8");

            petalo.setAttribute("rx","7");
            petalo.setAttribute("ry","13");

            petalo.setAttribute(
                "transform",
                `rotate(${i*45})`
            );

            flor.appendChild(petalo);
        }


        /* centro */

        const centro =
            document.createElementNS(
                "http://www.w3.org/2000/svg",
                "circle"
            );

        centro.setAttribute("class","centro");

        centro.setAttribute("cx","0");
        centro.setAttribute("cy","0");

        centro.setAttribute("r","6");

        flor.appendChild(centro);


        contenedor.appendChild(flor);
    }
}


/* ==========================================
   TRANSICIONES
========================================== */

const inicio =
    document.getElementById("inicio");

const escena =
    document.getElementById("escena");

const carta =
    document.getElementById("carta");


inicio.addEventListener("click",()=>{

    inicio.classList.add("oculto");


    setTimeout(()=>{

        escena.classList.add("visible");

    },700);


    /*
       Después de 10 segundos
       aparece la carta.
    */

    setTimeout(()=>{

        escena.style.opacity="0";

        setTimeout(()=>{

            escena.style.display="none";

            carta.classList.add("visible");

        },1300);

    },10000);

});

</script>

</body>
</html>
