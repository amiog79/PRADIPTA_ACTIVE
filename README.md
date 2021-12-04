# PRADIPTA_ACTIVE
<!DOCTYPE html>
<html>
<head>
	<meta charset="utf-8">
	<meta name="viewport" content="width=device-width, initial-scale=1">

	<title>Check if User is Offline/Online</title>

<style>
			body {
			    padding:10px;
			    font-family:arial;
			    font-size:1.2em;
			}
			.error {
			    background-color:#ff5252;
			    color:white;
			    padding:10px;
			    border-radius:5px;
			    margin-top:10px;
			}
			.success {
			    background-color:#00e676;
			    color:white;
			    padding:10px;
			    border-radius:5px;
			    margin-top:10px;
			}


      div{
      	text-align: center;
      	font-size: 50px;
      }

      h2{

      	text-align: center;
      	font-size: 40px;
      	background: blue;
      	color: white;
        box-shadow: 0 18px 24px 0 black;
        transition: 1s;
        box-sizing:60px;
     
      }

		</style>


</head>

<body>
			<h2>Devolop by Pradipta Ghosh</h2>
        <p>This is a simple code example to show you how to find when a user goes offline and when the user comes back online to show some messages to the user when this happens.</p>
        <div id="status"></div>

<script>
	
	let status = document.getElementById("status");
			
            window.addEventListener('load', function(e) {
                if (navigator.onLine) {
                    status.innerHTML = "User is online";
                    status.classList.add("success");
                } else {
                    status.innerHTML = "User is offline";
                    status.classList.remove("success");
                    status.classList.add("error");
                }
            }, false);
            
            window.addEventListener('online', function(e) {
                status.innerHTML = "User is back online";
                status.classList.remove("error");
                status.classList.add("success");
            }, false);
            
            window.addEventListener('offline', function(e) {
                status.innerHTML = "User went offline";
                status.classList.remove("success");
                status.classList.add("error");
            }, false);

</script>

</body>

</html>
