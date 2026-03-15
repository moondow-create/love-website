<!DOCTYPE html><html>
<head><meta name="viewport" content="width=device-width, initial-scale=1">
<title>Rohit ❤️ Punya</title><style>

body{
margin:0;
font-family:Georgia, serif;
background:#fff0f5;
color:#333;
text-align:center;
overflow-x:hidden;
}

#intro{
height:100vh;
display:flex;
flex-direction:column;
justify-content:center;
align-items:center;
background:linear-gradient(#ffd6e0,#fff0f5);
}

h1{
font-size:48px;
color:#ff2e63;
}

button{
padding:15px 40px;
border:none;
background:#ff4d6d;
color:white;
font-size:18px;
border-radius:40px;
cursor:pointer;
}

button:hover{
background:#ff2e63;
}

#letter{
max-width:650px;
margin:auto;
font-size:22px;
line-height:1.7;
display:none;
padding:20px;
}

.slide{
width:85%;
max-width:450px;
border-radius:20px;
display:none;
box-shadow:0 15px 35px rgba(0,0,0,0.2);
margin-top:30px;
}

.gallery{
display:flex;
flex-wrap:wrap;
justify-content:center;
gap:20px;
margin-top:40px;
}

.photo{
width:250px;
border-radius:15px;
box-shadow:0 15px 30px rgba(0,0,0,0.2);
transition:.4s;
}

.photo:hover{
transform:scale(1.1) rotate(2deg);
}

.timeline{
margin-top:60px;
}

.timeline p{
font-size:20px;
}

.heart{
position:fixed;
bottom:-40px;
color:#ff4d6d;
font-size:20px;
animation:float 6s linear infinite;
}

@keyframes float{
0%{transform:translateY(0);opacity:1;}
100%{transform:translateY(-120vh);opacity:0;}
}

</style></head><body><div id="intro"><h1>Rohit ❤️ Punya</h1><p>5 Years of Love</p><button onclick="start()">Open Our Love Story</button>

</div><div id="letter"></div><div><img src="photo1.jpg" class="slide">
<img src="photo2.jpg" class="slide">
<img src="photo3.jpg" class="slide">
<img src="photo4.jpg" class="slide">
<img src="photo5.jpg" class="slide"></div><h2>Our Beautiful Memories</h2><div class="gallery"><img src="photo1.jpg" class="photo">
<img src="photo2.jpg" class="photo">
<img src="photo3.jpg" class="photo">
<img src="photo4.jpg" class="photo">
<img src="photo5.jpg" class="photo"></div><div class="timeline"><h2>Our Story</h2><p>💫 The day Rohit met Punya</p>
<p>💫 Our first picture together</p>
<p>💫 Falling in love</p>
<p>💫 5 amazing years together</p>
<p>💫 Forever to go ❤️</p></div><div style="margin-top:60px"><h2>Punya, will you stay with Rohit forever?</h2><button onclick="alert('I love you Punya ❤️')">YES</button>

<button id="no">NO</button>

</div><iframe width="0" height="0"
src="https://www.youtube.com/embed/jnT6XUeY9r4?autoplay=1&loop=1"
allow="autoplay">
</iframe><script>

const text = `

Punya,

Five years ago,
my life changed when I met you.

You became my happiness,
my strength,
and the most beautiful part of my life.

Every memory with you
is a treasure I will always keep.

No matter where life takes us,
I promise I will always choose you.

Forever yours,
Rohit ❤️
`

let i=0

function type(){

if(i<text.length){

document.getElementById("letter").innerHTML+=text.charAt(i)

i++

setTimeout(type,40)

}

}

function start(){

document.getElementById("intro").style.display="none"

document.getElementById("letter").style.display="block"

type()

showSlides()

}

let slideIndex=0

function showSlides(){

let slides=document.getElementsByClassName("slide")

for(let i=0;i<slides.length;i++){

slides[i].style.display="none"

}

slideIndex++

if(slideIndex>slides.length){

slideIndex=1

}

slides[slideIndex-1].style.display="block"

setTimeout(showSlides,3000)

}

function createHeart(){

const heart=document.createElement("div")

heart.classList.add("heart")

heart.innerHTML="❤"

heart.style.left=Math.random()*100+"vw"

heart.style.fontSize=10+Math.random()*30+"px"

document.body.appendChild(heart)

setTimeout(()=>{

heart.remove()

},6000)

}

setInterval(createHeart,400)

const noBtn=document.getElementById("no")

noBtn.addEventListener("mouseover",()=>{

const x=Math.random()*window.innerWidth

const y=Math.random()*window.innerHeight

noBtn.style.position="absolute"

noBtn.style.left=x+"px"

noBtn.style.top=y+"px"

})

</script></body>
</html>
