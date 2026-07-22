<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Opening App Store...</title>
  <style>
    body {
      font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif;
      text-align: center;
      padding: 50px 20px;
      color: #333;
    }
    .btn {
      display: inline-block;
      margin-top: 20px;
      padding: 14px 28px;
      background-color: #007AFF;
      color: #ffffff;
      text-decoration: none;
      border-radius: 10px;
      font-weight: bold;
      font-size: 16px;
    }
  </style>
  <script>
    window.addEventListener("DOMContentLoaded", function () {
      var ua = navigator.userAgent || navigator.vendor || window.opera;

      // === PASTE YOUR ACTUAL LINKS HERE (Make sure https:// is included) ===
      var iosUrl = "https://apps.apple.com/tw/app/leap-taxi-app/id6475029322?l=en-GB"; 
      var androidUrl = "https://play.google.com/store/apps/details?id=product.customer.leaptaxi";
      var fallbackUrl = "https://leapsd.africa/riders/"; 

      var targetUrl = fallbackUrl;

      if (/android/i.test(ua)) {
        targetUrl = androidUrl;
      } else if (/iPad|iPhone|iPod/.test(ua) && !window.MSStream) {
        targetUrl = iosUrl;
      }

      // Set fallback button link
      document.getElementById("redirect-btn").href = targetUrl;

      // Auto-redirect
      window.location.replace(targetUrl);
    });
  </script>
</head>
<body>
  <h2>Redirecting to the App Store...</h2>
  <p>If you are not redirected automatically, tap the button below:</p>
  <a id="redirect-btn" href="#" class="btn">Open App Store</a>
</body>
</html>
