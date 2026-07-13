
<html lang="pt-BR"

<title>Convite Especial ❤️</title>

<style>
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family:Arial, Helvetica, sans-serif;
}

body{
    background:linear-gradient(135deg,#ffdde1,#ee9ca7);
    height:100vh;
    display:flex;
    justify-content:center;
    align-items:center;
    overflow:hidden;
}

.card{
    background:white;
    width:90%;
    max-width:700px;
    padding:40px;
    border-radius:20px;
    text-align:center;
    box-shadow:0 15px 35px rgba(0,0,0,.2);
}

h1{
    color:#e91e63;
    margin-bottom:25px;
}

p{
    font-size:20px;
    line-height:1.7;
    margin-bottom:20px;
}

button{
    margin:10px;
    padding:15px 35px;
    font-size:20px;
    border:none;
    border-radius:12px;
    cursor:pointer;
    transition:.3s;
}

.sim{
    background:#4CAF50;
    color:white;
}

.nao{
    background:#f44336;
    color:white;
}

button:hover{
    transform:scale(1.08);
}

#pagina2,#final{
    display:none;
}

.emoji{
    position:fixed;
    font-size:30px;
    animation:cair 4s linear forwards;
    pointer-events:none;
}

@keyframes cair{
    from{
        transform:translateY(-100px) rotate(0deg);
        opacity:1;
    }
    to{
        transform:translateY(110vh) rotate(720deg);
        opacity:0;
    }
}

.final-msg{
    font-size:35px;
    color:#d81b60;
    margin-top:20px;
}
</style>
</head>

<body>

<div class="card" id="pagina1">

<h1>💌 Convite Especial</h1>

<p>
Olá, tudo bem?!<br><br>

Estamos entrando em contato, pois <b>Gabriel lindo</b> está convidando <b>Anita linda</b> para uma noite especial em Gramado.
</p>

<p><b>Gostaríamos de saber se a senhorita está preparada?</b></p>

<button class="sim" onclick="irPagina2()">SIM</button>
<button class="nao" onclick="escolhaErrada()">NÃO</button>

</div>

<div class="card" id="pagina2">

<h1>❤️ Meu Convite ❤️</h1>

<p>
Já que está preparada, eu quero convidar meu amor,
<b>Anita Grotto</b>,
para passar uma noite linda na cidade do amor,
<b>Gramado</b>,
no dia <b>24/07</b>
e apreciar uma deliciosa sequência de fondue.
</p>

<p><b>Aceita meu convite especial?</b></p>

<button class="sim" onclick="aceitou()">CLARO</button>

<button style="background:#ff9800;color:white;"
onclick="aceitou()">
COM CERTEZA
</button>

</div>

<div class="card" id="final">

<h1>❤️ Eu sabia!! ❤️</h1>

<p class="final-msg">
Mal posso esperar para viver essa noite contigo! 💕
</p>

</div>

<script>

function escolhaErrada(){

alert("Escolha errada😕.\n\nTenho certeza que tu está pronta sim.");

}

function irPagina2(){

document.getElementById("pagina1").style.display="none";
document.getElementById("pagina2").style.display="block";

}

function aceitou(){

document.getElementById("pagina2").style.display="none";
document.getElementById("final").style.display="block";

for(let i=0;i<120;i++){

let emoji=document.createElement("div");

emoji.className="emoji";

emoji.innerHTML=Math.random()>0.5?"❤️":"🥳";

emoji.style.left=Math.random()*100+"vw";

emoji.style.animationDelay=(Math.random()*2)+"s";

emoji.style.fontSize=(25+Math.random()*30)+"px";

document.body.appendChild(emoji);

setTimeout(()=>{
emoji.remove();
},4500);

}

}

</script>

</body>
</html>
