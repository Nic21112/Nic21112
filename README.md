
<html><meta charset='UTF-8'/><meta content='width=device-width, initial-scale=1, user-scalable=1, minimum-scale=1, maximum-scale=5' name='viewport'/><meta content='IE=edge' http-equiv='X-UA-Compatible'/><link href="https://feeldreams.github.io/hayoloh/style.css" rel="stylesheet" type="text/css" /><script src="https://feeldreams.github.io/hayoloh/script.js"></script>
<link rel="preconnect" href="https://fonts.googleapis.com"><link rel="preconnect" href="https://fonts.gstatic.com" crossorigin><link href="https://fonts.googleapis.com/css2?family=Josefin+Sans:wght@400;700&display=swap" rel="stylesheet"><script src="https://cdn.jsdelivr.net/npm/sweetalert2@11.0.19/dist/sweetalert2.all.min.js"></script><script src="https://kit.fontawesome.com/4f3ce16e3e.js" crossorigin="anonymous"></script>
<head>
<title>Script HTML</title>
<!-- 
  Made with love by Rayys!
     Blog: https://PalingIT.com
     Instagram: @rayyarrr
     TikTok: @rayy4r
     Email: rayyar0703@gmail.com
  Thanks to all <3
  
  DM ke IG: @rayyarrr apabila masih bingung
  untuk cara edit scriptnya!
-->
</head>
<style>
:root {
--warna-bg: rgba(0, 0, 0, .5); 
--warna-teks: #fff;
--warna-bingkai: #fff;
--bingkai: 8px;
--bingkai-kiri: 2px solid var(--warna-bingkai);
--bingkai-kanan: 2px solid var(--warna-bingkai);
--gaya-font: 'Josefin Sans', sans-serif;
}
</style>
<body>
	
   <!-- Ganti Audio di sini --><audio id="linkmp3">https://feeldreams.github.io/papapa.mp3</audio>
   
   <div id="bodyblur">
     <!-- Wallpaper --><img src="https://feeldreams.github.io/wp3.jpeg" id="wallpaper"/>
   </div>

   <div id='Content'>
   	
     <div id="suratin" onClick="memulai();audio.play();">
       <!-- Tombol Surat --><img src="https://rayyscoding.github.io/envelope.png"/>
     </div>
     <p id="ket">Klik Suratnya!</p>

     <div><blockquote id='bq'>
       <div>
         <!-- Stiker untuk Konten -->
         <img src="https://feeldreams.github.io/bunga.gif" id="fotoakhir"/>
         <img src="https://feeldreams.github.io/peach1.gif" id="fotoakhir2"/>
         <img src="https://feeldreams.github.io/weee.gif" id="fotoakhir3"/>
       </div>

       <!-- Konten Pertanyaan -->
       <p id="kalimat">Kamu Mau Gak Jadi Pacar Aku? 🤭❤️</p>
       <p id="kalimatb"></p>
       <p id="kalimatc"></p>

       <!-- Konten Jawaban -->
       <p id="kalimat2">Yeaayy! 😆</p>
       <p id="kalimatb2">Sekarang, Kamu adalah Pacarku ❤️</p>
       <p id="kalimatc2">Eitss.. 🏃 Tapi kita akan PUTUS dalam waktu: <b id="ctimer" style="font-size:24px">7</b></p>

       <!-- Konten Jawaban 2 -->
       <p id="kalimat3">Tapi Boong😜</p>
       <p id="kalimatb3">Kamu beneran jadi pacar aku kok, wkwk🤣❤️</p>
       <p id="kalimatc3">📅 </p>
     </blockquote></div>

     <!-- Tombol Multifungsi -->
     <div id="Tombol">
       <a id="By" onClick="multifungsi()">
         <b id="tmbl">Mau</b>
       </a>
       
       <a id="Bn" onClick="ditolak()">Gamau</a><a id="Bn2" onClick="ditolak2()"></a>
     </div>
     
   </div>

<!-- Jangan Edit Bagian Ini --><script>
  ftom=0;jikapr=1;ftganti=0;flag=1;flagg=1;fungsi=0;Bn2.innerHTML=Bn.innerHTML;function showDiv() {pesanwhatsapp = "Aku mau kok jadi pacarmu ><";Bn2.style.display="none";Content.style = "opacity:1;margin-top:15vh;";ket.style="margin-top:30px";}
  function memulai(){suratin.style="transition:all 1s ease;transform:scale(.1);opacity:0";ket.style="transition:all 1s ease;transform:scale(.1);opacity:0";setTimeout(mulaikonten,300)}
  function mulaikonten() {otomatis();suratin.style="display:none";ket.style="display:none";Content.style = "opacity:1;margin-top:4vh";bodyblur.style="opacity:.6;animation:none";wallpaper.style="transform: scale(2);opacity:1;";fotoakhir.style="display:inline-flex;";setTimeout(ftmuncul,200);bq.style = "position:relative;opacity:1;visibility:visible;transform: scale(1);border-radius:var(--bingkai);margin-top:0";fungsi=1;setTimeout(tombol,500);}
  
  function ftmuncul(){
    if(ftganti==0){fotoakhir.style="display:inline-flex;opacity:1;transform:scale(1)";}
    if(ftganti==1){fotoakhir.src = fotoakhir2.src;fotoakhir.style="display:inline-flex;opacity:1;transition:all .7s ease;transform:scale(1);";}
    if(ftganti==2){fotoakhir.src = fotoakhir3.src;fotoakhir.style="display:inline-flex;opacity:1;transition:all .7s ease;transform:scale(1);";}
  }
  function fthilang(){fotoakhir.style="display:inline-flex;opacity:1;transition:all .7s ease;transform:scale(.1)";}
  function jjfoto(){fotoakhir.style.animation="rto .8s infinite alternate";}
  
  function tombol(){Tombol.style="opacity:1;transform: scale(1);";Bn.style="margin:12px 0 12px 12px";ftom=1;}
  function multifungsi(){if(ftom==1){diterima();} if(ftom==5){menuju();}}
  async function menuju(){await swals.fire('OK!', 'Kirim pesan ke WhatsApp aku, ya!', 'success');window.location = "https://api.whatsapp.com/send?phone=&text=" + pesanwhatsapp;Tombol.style="margin-top:15px;opacity:1;transform: scale(1);";} setTimeout(showDiv,100);

  const swalst = Swal.mixin({timer: 2777, allowOutsideClick: false, showConfirmButton: false, timerProgressBar: true, imageHeight: 100,}); audio = new Audio('' + linkmp3.innerHTML);const swals = Swal.mixin({allowOutsideClick: false, cancelButtonColor: '#FF0040', imageWidth: 100, imageHeight: 100,}); const style = document.createElement('style'); var today = new Date();var dd = String(today.getDate()).padStart(2, '0');var mm = String(today.getMonth() + 1).padStart(2, '0');var yyyy = today.getFullYear();const monthNames = ["Januari", "Februari", "Maret", "April", "Mei", "Juni", "Juli", "Agustus", "September", "Oktober", "November", "Desember"];today = dd + ' ' + monthNames[today.getMonth()] + ' ' + yyyy;
   const body = document.querySelector("body");function createHeart() {const heart = document.createElement("div"); heart.className = "fas fa-heart"; heart.style.left = (Math.random() * 90)+"vw"; heart.style.animationDuration = (Math.random()*3)+2+"s"; body.appendChild(heart);} setInterval(function name(params) {var heartArr = document.querySelectorAll(".fa-heart"); if (heartArr.length > 100) {heartArr[0].remove()}},100);
</script>
<!-- Sampai Sini -->
</body>
</html>
