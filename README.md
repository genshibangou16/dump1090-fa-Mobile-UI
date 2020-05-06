# Mobile UI for dump1090-fa
Add one file to make dump1090-fa web interface Mobile-Friendly!
<br>
Let's fit your PiAware SkyAware with mobile.

# Installation
sudo wget -P /usr/share/dump1090-fa/html

        <meta name="viewport" content="width=device-width,initial-scale=1">
        <script>
            document.documentElement.style.setProperty('--vh', `${window.innerHeight * 0.01}px`);
            window.addEventListener('resize', () => {
                document.documentElement.style.setProperty('--vh', `${window.innerHeight * 0.01}px`);
            });
        </script>
        <link rel="stylesheet" type="text/css" href="style_mobile.css" media="screen and (max-width: 600px)" />
