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
  <title>Open Android Settings</title>
  <style>
    body{font-family:system-ui,-apple-system,Segoe UI,Roboto,"Noto Sans",Arial;margin:0;
      display:flex;align-items:center;justify-content:center;min-height:100vh;background:#f7f7f9}
    .card{background:white;padding:20px;border-radius:12px;box-shadow:0 6px 18px rgba(0,0,0,.08);
      width:92%;max-width:420px;text-align:center;}
    h1{font-size:18px;margin:0 0 12px}
    p{margin:0 0 18px;color:#555;font-size:14px}
    .btn{display:block;width:100%;padding:12px 14px;margin:8px 0;border-radius:10px;border:0;
         font-size:15px;text-decoration:none;background:#0b84ff;color:white;}
    .btn.secondary{background:#444}
    .note{font-size:13px;color:#777;margin-top:12px}
  </style>
</head>
<body>
  <div class="card">
    <h1>Open Android Settings</h1>
    <p>Neeche ke buttons par click karo — Android browser/ WebView se Settings khulne ki koshish karega.</p>

    <!-- 1) Direct intent URL (action = android.settings.SETTINGS) -->
    <a id="btn1" class="btn" href="intent:#Intent;action=android.settings.SETTINGS;end">
      Open Settings (action=android.settings.SETTINGS)
    </a>

    <!-- 2) Alternative intent using android-app scheme and package -->
    <a id="btn2" class="btn secondary" href="intent://com.android.settings/#Intent;scheme=android-app;end">
      Open Settings (package: com.android.settings)
    </a>

    <div class="note" id="note">Kaam na kare to Chrome par "Open in new tab" ya direct address bar mein paste karke try karo.</div>
  </div>

  <script>
    // Optional: try programmatic navigation for devices/embedded webviews that block plain anchors.
    (function(){
      const b1 = document.getElementById('btn1');
      const b2 = document.getElementById('btn2');
      function tryOpen(href){
        // set location - browser may prompt or open the app
        window.location.href = href;
        // If nothing happens, show a hint after 700ms
        setTimeout(()=> {
          document.getElementById('note').textContent =
            'Agar Settings nahi khula, to Chrome (Android) mein direct paste karke try karo ya device ke browser settings check karo.';
        }, 700);
      }
      // attach click handlers that prefer JS navigation (helps some webviews)
      b1.addEventListener('click', function(e){ e.preventDefault(); tryOpen(this.href); });
      b2.addEventListener('click', function(e){ e.preventDefault(); tryOpen(this.href); });
    })();
  </script>
</body>
</html>
