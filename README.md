     Hello YYE NICHE WALA COPY PASTE KARNA HAI 
          👇👇👇👇👇

        `intent:#Intent;action=android.settings.SETTINGS;end`



    AUR UPAR WALA KAAM NA KARE TO NICHE WALA 
                 👇👇👇👇
                 
          intent://com.android.settings/#Intent;scheme=android-app;end


<!doctype html>
<html lang="hi">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Open Settings</title>
  <style>
    body{
      margin:0;
      display:flex;
      justify-content:center;
      align-items:center;
      min-height:100vh;
      background:#f5f5f5;
    }
    a{
      display:flex;
      justify-content:center;
      align-items:center;
      background:white;
      border-radius:50%;
      width:120px;
      height:120px;
      box-shadow:0 6px 20px rgba(0,0,0,0.15);
      transition:transform 0.2s ease, box-shadow 0.2s ease;
    }
    a:hover{
      transform:scale(1.05);
      box-shadow:0 8px 25px rgba(0,0,0,0.2);
    }
    img{
      width:70%;
      height:70%;
    }
  </style>
</head>
<body>
  <!-- Direct intent link -->
  <a href="intent:#Intent;action=android.settings.SETTINGS;end" id="settingsLink">
    <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/6/6e/Android_Settings_icon.svg/1024px-Android_Settings_icon.svg.png" alt="Settings" />
  </a>

  <script>
    // JS fallback: programmatically open intent
    document.getElementById('settingsLink').addEventListener('click', function(e){
      e.preventDefault();
      window.location.href = this.href;
    });
  </script>
</body>
</html>
