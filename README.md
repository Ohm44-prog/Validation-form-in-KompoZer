# Validation-form-in-KompoZer

<!DOCTYPE html PUBLIC "-//W3C//DTD HTML 4.01//EN" "http://www.w3.org/TR/html4/strict.dtd">
<html><head>

  
  <meta content="text/html; charset=ISO-8859-1" http-equiv="content-type"><title>form</title>
  

  
  
  <style type="text/css">
h1 {
  font-size: 2.5em;
  font-weight: bold;
  text-align: center;
  font-family: Lucida Bright;
  color: #0507ff;
  font-style: italic;
  background-color: #03eefd;
}
body {
  font-family: Segoe UI Variable Text Semibold;
  font-size: 1.1em;
  background-color: #07f0ff;
}
input {
  background-color: transparent;
}
textarea {
  background-color: transparent;
}
select {
  background-color: transparent;
}
</style>
  
  <script>
function validateForm()
{
  var x=document.form.fname.value
  if (x==null || x=="")
  {
    alert("Please enter the first name");
    document.form.fname.focus();
    return false;
  }

  var y=document.form.mname.value;
  if (y==null || y=="")
  {
    alert("Please enter your middle name");
    document.form.mname.focus();
    return false;
  }

  var z=document.form.lname.value;
  if (z==null || z=="")
  {
  alert("Please enter proper last name");
  document.form.lname.focus();
  return false
  }

  var w=document.form.Address.value;
  if(w=="")
  {
    alert("Please enter address");
    document.form.Address.focus();
    return false;
  }
  
  var a=document.form.no.value;
  if (isNaN(a) || a==null || a=="" || a.length!==10)
  {
  alert("Please enter number properly!");
  document.form.no.focus();
  return false;
  }
  
  if ((document.form.hobby[0].checked==false) && (document.form.hobby[1].checked==false) && (document.form.hobby[2].checked==false) && (document.form.hobby[3].checked==false) && (document.form.hobby[4].checked==false) && (document.form.hobby[5].checked==false))
  {
  alert("Please Select one or more hobby!");
  return false;
  }

  if((document.form.gender[0].checked==false) && (document.form.gender[1].checked==false))
  {
    alert("Please chose your gender!");
    return false;
  }
  if (document.form.city.selectedIndex=="0")
  {
    alert("Please Select your city!");
    return false;
  }
  return true;
}

  </script></head><body>
<form onsubmit="return validateForm()" method="post" action="form.html" name="form">
  <div style="text-align: center; color: rgb(5, 7, 255);">
  <h1>REGISTRATION FORM</h1>
  </div>
  <br>
  <div style="text-align: center;">FIRST NAME <input name="fname"><br>
  <br>
MIDDLE NAME <input name="mname"><br>
  <br>
LAST NAME <input name="lname"><br>
  <br>
ADDRESS <textarea cols="40" rows="5" name="Address"></textarea><br>
  <br>
MOBILE NUMBER <input maxlength="10" name="no"><br>
  <br>
HOBBIES <br>
Football<input name="hobby" value="h1" type="checkbox">
Basketball<input name="hobby" value="h2" type="checkbox">
Chess<input name="hobby" value="h3" type="checkbox">
Singing<input name="hobby" value="h4" type="checkbox">
Sleeping<input name="hobby" value="h5" type="checkbox">
Coding<input name="hobby" value="h6" type="checkbox">
  <br>
<br>
GENDER <br>
Male <input name="gender" value="male" type="radio">Female <input name="gender" value="female" type="radio"><br>
  <br>
CITY
  <select name="city">
  <option selected="selected">select a city</option>
  <option>vadodara</option>
  <option>anand</option>
  <option>ahmedabad</option>
  <option>surat</option>
  </select>
  <br>
  <br>
  <div style="text-align: left;"><input value="submit" name="submit" type="submit"> </div>
  <div style="text-align: right;"> <input name="reset" value="reset" type="reset"><br>
  </div>
  </div>
  <br>
  <br>
  <br>
  <br>
  <br>
</form>

</body></html>
