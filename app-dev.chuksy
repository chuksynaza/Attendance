<!DOCTYPE html>
<html lang='en'>
<head>
  <!-- Meta -->
  <meta charset='utf-8'>
  <meta name='viewport' content='width=device-width, initial-scale=1.0'>
  <meta name='description' content='Attendance Application'>
  <meta name='author' content='Chuksy'>
  <meta name='keywords' content='MaTt, Attendance'>
  <!--End of Meta-->
  <!--Title-->
  <title>MaTt | Attendance Tracking App</title>
  <!--End of Title-->
  <!--External Top Scripts-->
  <script src='assets/js/jquery-1.11.2.min.js'></script>
  <!--End of External Top Scripts-->
  <!--Internal Top Scripts-->

  <!--End of Internal Top Scripts-->
  <!-- External Css -->
  <link href='assets/css/bootstrap.min.css' rel='stylesheet'>
  <link href='assets/css/font-awesome.min.css' rel='stylesheet'>
  <!--End of External CSS -->
  <style>
    body
    {
      -webkit-user-select: none;
      padding: 0px;
      margin: 0px;
      /*min-height:700px;*/
      height:100%;
      cursor:default;
      overflow-x: hidden;
    }
    .vmemb
    {

      max-width:inherit;
      max-height:500px;
      -webkit-user-select: initial;
    }
    .vmemb-table td, .vmemb-table th, .vmemb-table tr
    {
     vertical-align: middle;
   }

   .vmemb-table thead
   {

   }
   .vmemb-table th
   {
     text-align: center;
   }
   .vmemb-cent
   {
    text-align: center;
  }
  .vmemb-but .fa
  {
    font-size: 20px;
  }
  .vmemb-but
  {
    border:none;
    padding:0px;
    margin-top: 3px;
  }
  .vmemb-check
  {
    width:25px;
    height: 20px;
  }
</style>

<style type="text/css">
  body{
   background:#202020;
   font:bold 12px Arial, Helvetica, sans-serif;
   margin:0;
   padding:0;
   min-width:960px;
   color:#bbbbbb; 
   overflow-y: hidden;
 }

 

 #theclock a { 
  text-decoration:none; 
  color:#00c6ff;
}

#theclock h1 {
  font: 4em normal Arial, Helvetica, sans-serif;
  padding: 20px;  margin: 0;
  text-align:center;
}

#theclock h1 small{
  font: 0.2em normal  Arial, Helvetica, sans-serif;
  text-transform:uppercase; letter-spacing: 0.2em; line-height: 5em;
  display: block;
}

#theclock h2 {
  font-weight:700;
  color:#bbb;
  font-size:20px;
}

#theclock h2, #theclock p {
  margin-bottom:10px;
}

@font-face {
  font-family: 'BebasNeueRegular';
  src: url('assets/fonts/BebasNeue-webfont.eot');
  src: url('assets/fonts/BebasNeue-webfont.eot?#iefix') format('embedded-opentype'),
  url('assets/fonts/BebasNeue-webfont.woff') format('woff'),
  url('assets/fonts/BebasNeue-webfont.ttf') format('truetype'),
  url('assets/fonts/BebasNeue-webfont.svg#BebasNeueRegular') format('svg');
  font-weight: normal;
  font-style: normal;

}


#theclock .clock { margin:0 auto; padding:30px; border:1px solid #333; color:#fff; }

#theclock #Date { font-family:'BebasNeueRegular', Arial, Helvetica, sans-serif; font-size:36px; text-align:center; text-shadow:0 0 5px #00c6ff; }

#theclock ul {width:500px; margin:0 auto; padding:0px; list-style:none; text-align:center;}
#theclock ul li { display:inline; font-size:10em; text-align:center; font-family:'BebasNeueRegular', Arial, Helvetica, sans-serif; text-shadow:0 0 5px #00c6ff; }

#theclock #point { position:relative; -moz-animation:mymove 1s ease infinite; -webkit-animation:mymove 1s ease infinite; padding-left:10px; padding-right:10px; }

@-webkit-keyframes mymove 
{
  0% {opacity:1.0; text-shadow:0 0 20px #00c6ff;}
  50% {opacity:0; text-shadow:none; }
  100% {opacity:1.0; text-shadow:0 0 20px #00c6ff; }  
}


@-moz-keyframes mymove 
{
  0% {opacity:1.0; text-shadow:0 0 20px #00c6ff;}
  50% {opacity:0; text-shadow:none; }
  100% {opacity:1.0; text-shadow:0 0 20px #00c6ff; }  
}

</style>


<script>

function page_switch(page, thiss)
{
 if(page == 'A')
 {
   $('.tab').removeClass('active');
   $(thiss).parents('.tab').addClass('active');
   $('.page').hide();
   $('.page-welcome').show();
 }
 else if(page == 'B')
 {
   $('.tab').removeClass('active');
   $(thiss).parents('.tab').addClass('active');
   $('.page').hide();
   $('.page-design-parameters').show();

 }
}

function continuetoapp()
{
  $('.pga').remove();
  $('ul, main').show();
}



function runninglate()
{
  $('#theclock .clock').css({'color':'#fc0000'});
}

</script>


<script type="text/javascript">
  var monthNames = [ "January", "February", "March", "April", "May", "June", "July", "August", "September", "October", "November", "December" ]; 
  var dayNames= ["Sunday","Monday","Tuesday","Wednesday","Thursday","Friday","Saturday"];
  var biodata;

  var markreturn = "<b class = 'mark-report text-danger '> PLEASE RUN AS AN ADMINISTRATOR </b>";
  $(document).ready(function() {
// Create two variable with the names of the months and days in an array


// Create a newDate() object
var newDate = new Date();
// Extract the current date from Date object
newDate.setDate(newDate.getDate());
// Output the day, date, month and year    
$('#Date').html(dayNames[newDate.getDay()] + " " + newDate.getDate() + ' ' + monthNames[newDate.getMonth()] + ' ' + newDate.getFullYear());

setInterval( function() {
  // Create a newDate() object and extract the seconds of the current time on the visitor's
  var seconds = new Date().getSeconds();
  // Add a leading zero to seconds value
  $("#sec").html(( seconds < 10 ? "0" : "" ) + seconds);
},1000);

setInterval( function() {
  // Create a newDate() object and extract the minutes of the current time on the visitor's
  var minutes = new Date().getMinutes();
  // Add a leading zero to the minutes value
  $("#min").html(( minutes < 10 ? "0" : "" ) + minutes);
},1000);

setInterval( function() {
  // Create a newDate() object and extract the hours of the current time on the visitor's
  var hours = new Date().getHours();
  // Add a leading zero to the hours value
  $("#hours").html(( hours < 10 ? "0" : "" ) + hours);
}, 1000);

setTimeout("runninglate()", 2700000);
}); 



  var path = require('path');
  var nwPath = process.execPath;
  var nwDir = path.dirname(nwPath);

  var fs = require('fs');

  var d = new Date();
  var attendancepath = nwDir + '/AppData/Attendance' + '-Date-' + dayNames[d.getDay()] + '-' + monthNames[d.getMonth()] + '-' + d.getFullYear() + '-Time-' + d.getHours() + '-' + d.getMinutes() + '-' + d.getSeconds() + '.chuksy';

  var studentsattendance =  JSON.stringify({"day": dayNames[d.getDay()], "month": dayNames[d.getDay()], "year": monthNames[d.getMonth()], "hour": d.getHours(), "minute": d.getMinutes(), "second": d.getSeconds(), "attendance":[]});

  var biodatapath = nwDir + '/BioData/Biodata.chuksy';

  fs.appendFile(attendancepath, studentsattendance, function(err) {
   if(err) {
    alert("Please close and run as an administrator [Error: 4011]");
    $('.markreturn').html(markreturn);
    $('.markreturn').show();
  }
  else
  {
    var biodataFile = fs.readFileSync(biodatapath);
    biodata = JSON.parse(biodataFile);
    //alert(JSON.stringify(biodata));
  }
});


  function getFormData($form){
    var unindexed_array = $form.serializeArray();
    var indexed_array = {};

    $.map(unindexed_array, function(n, i){
      indexed_array[n['name']] = n['value'];
    });

    return indexed_array;
  }

  function appendObject(obj){

    var configFile = fs.readFileSync(attendancepath);
    var config = JSON.parse(configFile);
    config.attendance.push(obj);
    var configJSON = JSON.stringify(config);
    fs.writeFileSync(attendancepath, configJSON);



    var regg = $('.regno').val();

    markreturn = "<b class = 'mark-report text-warning'> WELCOME, " + regg + " YOU ARE NOT REGISTERED FOR THIS PROGRAM </b>";

    $.each(biodata.students, function(i, v) {

     if (v.regno == regg) {
       markreturn = "<b class = 'mark-report text-success'> WELCOME, " + v.surname.toUpperCase() + ' ' + v.firstname.toUpperCase() + ' ' + v.othernames.toUpperCase() + " </b>";
       return;
     }
   });

    var uimg = nwDir + '/User-Images/' + regg + '.jpg';
    if (fs.existsSync(uimg)) {
      $('.userimg').attr('src', uimg);
    }
    else
    {
      $('.userimg').attr('src', uimg);
    }


    $('.markreturn').html(markreturn);
    $('.markreturn').show();

    $('.attendance').each(function()
    {
      this.reset();
    });
    $('.regno').focus();
  }

  function process_attendance()
  {

    var dm = new Date();

    $('.marktime').val(dm.getHours() + '-' + dm.getMinutes() + '-' + dm.getSeconds());

    var details = JSON.stringify($('.attendance').serializeArray());

   //document.write(JSON.stringify(formdetails));

   formdetails = getFormData($('.attendance'));
   //document.write(JSON.stringify(formdetails));
   appendObject(formdetails);

 }

</script>

</head>

<body id='home' onload = "">
  <div class = 'containter pga' style = 'display:none;'>

  </div>

  <main >
    <div class = 'container-fluid'>



     <!--Gear Design Parameters-->
     <div class = 'page page-mark-attendance' style=''>
      <div class = 'row'>


        <br/>
        <div id = 'theclock'>
          <div class="container">
            <div class="clock">
              <div id="Date"></div>

              <ul>
                <li id="hours"> </li>
                <li id="point">:</li>
                <li id="min"> </li>
                <li id="point">:</li>
                <li id="sec"> </li>
              </ul>

            </div>
          </div>
        </div>

        <br/>

        <h3 class = 'text-center'>
          WELCOME, PLEASE SIGN IN
        </h3>
        <br/>
        <br/>
        <div class = 'container'>
          <div class = 'row'>
            <div class = 'col-sm-6'>
              <form onsubmit = "process_attendance(); return false;" class = 'attendance'>
                <input type = 'hidden' class = 'marktime' name = 'time'/>
                <div class = 'col-sm-1'>
                </div> 
                <div class = ''>
                  <div class="input-group">
                    <span class="input-group-addon" id="sizing-addon1">Registration Number:</span>
                    <input type="number" autofocus="true" class="form-control regno" placeholder="Enter Registration Number" minlength="7" maxlength="7" min="1000000" max="9999999" required="true" aria-describedby="sizing-addon1" name = 'regno'>
                  </div>


                </div>

                <div class = 'col-sm-1'>
                </div>
                <br/>
                <br/>
                <br/>
                <br/>
                <br/>


                <div class = 'col-sm-3'>
                </div>
                <div class = 'col-sm-6'>
                  <button type="submit" class="btn btn-default btn-lg btn-block">
                    <i class="fa fa-plus-circle"></i> Mark Present
                  </button>

                </div>

                <div class = 'col-sm-3'>
                </div>
              </form>
            </div>
            <div class = 'col-sm-6'>
              <div class = 'row'>
                <div class = 'col-sm-4'>
                </div>
                <div class = 'col-sm-4'>
                  <img src="assets/images/demo.png" class="img-rounded userimg" style = 'margin-left: auto; margin-right: auto; height:100px; width:150px;'>
                </div>

                <div class = 'col-sm-4'>
                </div>
              </div>
              <br/>
              <br/>

              <div class = 'row'>
                <div class = 'col-sm-1'>
                </div>
                <div class = 'col-sm-10'>
                 <div class='well well-sm markreturn' style = 'display: none;'>  </div>


               </div>

               <div class = 'col-sm-1'>
               </div>
             </div>



           </div>
         </div>
       </div>

     </div>

   </div>

 </div>
 <!-- End of Gear Design Parameters -->

</div>
</main>

<!--External Bottom Scripts-->
<script src='assets/js/bootstrap.min.js'></script>
<!--End of External Bottom Scripts-->
<!--Internal Bottom Scripts-->

<!--End of Internal Bottom Scripts-->

<b class = 'text-muted' style = 'position:fixed; bottom:10px; right:10px; font-size: 15.5px;'> <i>Developed by ChuksyLabs</i> </b>
</body>
</html>
