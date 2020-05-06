# Mobile UI for dump1090-fa
Add one file to make dump1090-fa web interface Mobile-Friendly!
<br>
Let's fit your PiAware SkyAware with mobile.

# Require
dump1090-fa 3.8.1
<br>
I'm using Raspberry Pi (the first), so probably this works on all of your Pi.

# Installation
Just two steps!
## 1 Enter your pi with SSH and run wget as the following.
```bash
sudo wget -P /usr/share/dump1090-fa/html https://github.com/genshibangou16/dump1090-fa-Mobile-UI/raw/master/style_mobile.css
```
## 2 Edit `index.html` at `/usr/share/dump1090-fa/html`.
Ex. with nano.
```bash
sudo nano /usr/share/dump1090-fa/html/index.html
```
Add ↓ at the _end_ of `<header>`.
```html
<meta name="viewport" content="width=device-width,initial-scale=1">
<script>
        document.documentElement.style.setProperty('--vh', `${window.innerHeight * 0.01}px`);
        window.addEventListener('resize', () => {
                document.documentElement.style.setProperty('--vh', `${window.innerHeight * 0.01}px`);
        });
</script>
<link rel="stylesheet" type="text/css" href="style_mobile.css" media="screen and (max-width: 600px)" />
```
