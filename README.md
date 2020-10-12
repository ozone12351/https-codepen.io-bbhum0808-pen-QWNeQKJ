//embotteamcodehtml//

<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8">
        <title>embot</title>
<link rel="stylesheet" href="style.css">
<script src="https://code.jquery.com/jquery-3.4.1.js"></script>
<script src="https://kit.fontawesome.com/a076d05399.js"></script>
<style>
body {
  background: url("https://scontent.fbkk12-1.fna.fbcdn.net/v/t1.0-9/120702975_965767257258756_8431111857745245457_n.jpg?_nc_cat=101&_nc_sid=730e14&_nc_eui2=AeHzKa17OVHsjlsr-yWTA11VvOuteIknnUa86614iSedRnftoKk_mBjBt7uVOb4YKjMSMq9SmsHU8ghJ8XRQH3mK&_nc_ohc=5gECMokDmmYAX_UrMVk&_nc_ht=scontent.fbkk12-1.fna&oh=146d128cf16a040065265b6af2b9e384&oe=5F9FAB56");
  background-size: 1100px 750px;
  background-repeat: no-repeat;
}
</style>

    </head>

    <body>
<div class="alert hide">
<span class="fas fa-exclamation-circle"></span>
<span class="msg" style="color:white;">Warning This is a warning alert!</span>
<span class="close-btn">
<span class="fas fa-times"></span>

</div>
<img src="https://scontent.fbkk12-2.fna.fbcdn.net/v/t1.0-9/120664436_965764997258982_9039700573932307943_o.jpg?_nc_cat=104&_nc_sid=730e14&_nc_eui2=AeEBZjcqzXxpI1baWgftPEN1q6Cpna6ZpHSroKmdrpmkdMuwtB1hGxDy99kxkPKFDeLY-VPeKT5Tg4HfxVRSRPsR&_nc_ohc=O_M3qBCOHx0AX8zoxak&_nc_ht=scontent.fbkk12-2.fna&oh=344d03b32070fbed51a3cb0389d2cf5b&oe=5F9FA0E2" alt="logo" width="200" height="200" style="position: relative; right :370px">
<h3><span style="color: #a61c12">
1.First, protect yourself from an Earthquake. ...<br>
2.Get to high ground as far inland as possible.<br>
3.Be alert to signs of a tsunami, such as a sudden rise or draining of ocean waters.<br>
4.Listen to emergency information and alerts.<br>
5.Evacuate: DO NOT wait! ...<br>
6.If you are in a boat, go out to sea.
</h3>



<script>
/* see user position */
const successCallback = (position) => {
let USlocation = console.log(position);
};
const errorCallback = (error) => {
console.error(error);
};
navigator.geolocation.getCurrentPosition(successCallback, errorCallback)

let x = Math.abs(13.903367999002882,100.53809833168926)

let SamutPrakan = Math.abs(13.501113,100.275901)

/* nonthaburi check */
if(x >  SamutPrakan){

    $('.alert').addClass("show");
        $('.alert').removeClass("hide");
        $('.alert').addClass("showAlert");
        setTimeout(function(){
          $('.alert').removeClass("show");
          $('.alert').addClass("hide");
        },5000);
 $('.close-btn').click(function(){
        $('.alert').removeClass("show");
        $('.alert').addClass("hide");
      });
};
</script>
    </body>
</html>
//embotteamcodecss//
@import url('https://fonts.googleapis.com/css?family=Poppins:400,500,600,700&display=swap');
*{
  margin: 0;
  padding: 0;
  user-select: none;
  box-sizing: border-box;
  font-family: 'Poppins', sans-serif;
}
html,body{
  height: 100%;
}
body{
  display: grid;
  place-items: center;
  overflow: hidden;
}
.alert{
  background: #ffa29b;
  padding: 20px 40px;
  min-width: 420px;
  position: absolute;
  right: 0;
  top: 10px;
  border-radius: 4px;
  border-left: 8px solid #ff0202;
  overflow: hidden;
  opacity: 0;
  pointer-events: none;
}
.alert.showAlert{
  opacity: 1;
  pointer-events: auto;
}
.alert.show{
  animation: show_slide 1s ease forwards;
}
@keyframes show_slide {
  0%{
    transform: translateX(100%);
  }
  40%{
    transform: translateX(-10%);
  }
  80%{
    transform: translateX(0%);
  }
  100%{
    transform: translateX(-10px);
  }
}
.alert.hide{
  animation: hide_slide 1s ease forwards;
}
@keyframes hide_slide {
  0%{
    transform: translateX(-10px);
  }
  40%{
    transform: translateX(0%);
  }
  80%{
    transform: translateX(-10%);
  }
  100%{
    transform: translateX(100%);
  }
}
.alert .fa-exclamation-circle{
  position: absolute;
  left: 20px;
  top: 50%;
  transform: translateY(-50%);
  color: #ce1b00;
  font-size: 30px;
}
.alert .msg{
  padding: 0 20px;
  font-size: 18px;
  color: #ce1b00;
}
.alert .close-btn{
  position: absolute;
  right: 0px;
  top: 50%;
  transform: translateY(-50%);
  background: #ff8680;
  padding: 20px 18px;
  cursor: pointer;
}
.alert .close-btn:hover{
  background: #ff6666;
}
.alert .close-btn .fas{
  color: #ce0700;
  font-size: 22px;
  line-height: 40px;
}

