<!DOCTYPE html><html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Ridwan Success Portfolio</title><link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600&display=swap" rel="stylesheet"><style>
*{box-sizing:border-box}
body{
margin:0;
font-family:'Poppins',sans-serif;
background:linear-gradient(135deg,#eef2ff,#f8fafc);
color:#111827;
}

header{
background:#111827;
color:white;
padding:30px 20px;
text-align:center;
}

header h1{margin:0}

.container{
max-width:1100px;
margin:auto;
padding:25px;
}

.bio{
background:white;
padding:25px;
border-radius:16px;
box-shadow:0 8px 20px rgba(0,0,0,0.08);
margin-bottom:30px;
}

.gallery-section{
margin-top:30px;
}

.gallery{
display:grid;
grid-template-columns:repeat(auto-fit,minmax(230px,1fr));
gap:18px;
margin-top:15px;
}

.card{
background:white;
border-radius:14px;
overflow:hidden;
box-shadow:0 6px 16px rgba(0,0,0,0.08);
transition:transform .25s;
}

.card:hover{
transform:translateY(-6px);
}

.card img{
width:100%;
height:200px;
object-fit:cover;
}

.caption{
padding:10px;
font-weight:500;
}

.upload-box{
background:white;
padding:20px;
border-radius:16px;
box-shadow:0 8px 20px rgba(0,0,0,0.08);
margin-bottom:30px;
}

button{
background:#4f46e5;
color:white;
border:none;
padding:10px 18px;
border-radius:8px;
cursor:pointer;
margin-top:10px;
}

button:hover{background:#4338ca}

input,select{
padding:8px;
margin-top:8px;
}

.login{
max-width:400px;
margin:80px auto;
background:white;
padding:30px;
border-radius:16px;
box-shadow:0 8px 20px rgba(0,0,0,0.1);
text-align:center;
}

.hidden{display:none}

footer{
text-align:center;
padding:25px;
opacity:.7;
font-size:14px;
}
</style></head><body><!-- LOGIN PAGE --><div id="loginPage" class="login">
<h2>Login</h2>
<p>Only you should log in to add achievements.</p><input type="password" id="password" placeholder="Enter password"><br> <button onclick="login()">Login</button>

<p style="font-size:12px;margin-top:15px">Default password: <b>1234</b><br>
You can change it in the code later.</p>
</div><!-- MAIN WEBSITE --><div id="mainSite" class="hidden"><header>
<h1>My Success Portfolio</h1>
<p>A collection of my achievements and proud moments</p>
</header><div class="container"><!-- BIOGRAPHY --><div class="bio">
<h2>My Biography</h2>
<p>
Write your biography here.Example: I am Ridwan, a student passionate about learning, competitions, and achieving great things. This website shows my journey of success including academic awards, co‑curriculum activities, and other achievements.

</p>
</div><!-- UPLOAD --><div class="upload-box">
<h2>Add Achievement</h2><input type="file" id="imageUpload" accept="image/*"><br>

<input type="text" id="captionInput" placeholder="Achievement description"><br>

<select id="categorySelect">
<option value="academic">Academic</option>
<option value="cocurricular">Co‑Curriculum</option>
<option value="others">Others</option>
</select>
<br>
<button onclick="addImage()">Add to Gallery</button>
</div><!-- ACADEMIC --><div class="gallery-section">
<h2>Academic</h2>
<div class="gallery" id="academicGallery"></div>
</div><!-- CO CURRICULUM --><div class="gallery-section">
<h2>Co‑Curriculum</h2>
<div class="gallery" id="cocurricularGallery"></div>
</div><!-- OTHERS --><div class="gallery-section">
<h2>Others</h2>
<div class="gallery" id="othersGallery"></div>
</div></div><footer>
© 2026 My Success Journey
</footer></div><script>

function login(){

const pass=document.getElementById('password').value;

if(pass==='1234'){

document.getElementById('loginPage').style.display='none';
document.getElementById('mainSite').classList.remove('hidden');

}
else{
alert('Wrong password');
}
}

function addImage(){

const file=document.getElementById('imageUpload').files[0];
const caption=document.getElementById('captionInput').value;
const category=document.getElementById('categorySelect').value;

if(!file){
alert('Please select an image');
return;
}

const reader=new FileReader();

reader.onload=function(e){

const card=document.createElement('div');
card.className='card';

const img=document.createElement('img');
img.src=e.target.result;

const cap=document.createElement('div');
cap.className='caption';
cap.innerText=caption || 'Achievement';

card.appendChild(img);
card.appendChild(cap);

if(category==='academic'){
document.getElementById('academicGallery').prepend(card);
}

if(category==='cocurricular'){
document.getElementById('cocurricularGallery').prepend(card);
}

if(category==='others'){
document.getElementById('othersGallery').prepend(card);
}

};

reader.readAsDataURL(file);
}

</script><!--
HOW TO TURN THIS INTO A PUBLIC WEBSITE

FASTEST METHOD (5 minutes)

1. Go to https://github.com
2. Create a free account
3. Click "New Repository"
4. Name it: success-portfolio
5. Upload this file as index.html
6. Go to Settings → Pages
7. Enable GitHub Pages

Your public website link will look like:

https://yourusername.github.io/success-portfolio

You can share that link with anyone.

--></body>
</html># success-portfolio
