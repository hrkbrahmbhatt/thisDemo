 var login_attempts=3;
function validate()
{
    if(   document.getElementById("username").value == "admin"
       && document.getElementById("password").value == "admin123" )
    {
       location.href="index1.html";
    }
    else
 {
  if(login_attempts==0)
  {
   alert("No Login Attempts Available");
 document.getElementById("button").style.background='#cc0000';
       document.getElementById("button").disabled=true;
  }
  else
  {
   login_attempts=login_attempts-1;
   alert("Login Failed Now Only "+login_attempts+" Login Attempts Available");
    document.getElementById("button").style.background='#cc0000';
   if(login_attempts==0)
   {
    document.getElementById("username").disabled=true;
    document.getElementById("password").disabled=true;
    document.getElementById("form").disabled=true;
       document.getElementById("button").style.background='#cc0000';
       document.getElementById("button").disabled=true;
   }
  }
 }
 
 return false;
}	
</script>
