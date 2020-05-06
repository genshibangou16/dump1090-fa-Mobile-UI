# Mobile UI for dump1090-fa
Add one file to make dump1090-fa web interface Mobile-Friendly!  
Let's fit your PiAware SkyAware with mobile.  
Installation is super easy, it may take only five minutes.

# Sample
![Screenshot1](https://user-images.githubusercontent.com/64895726/81192960-cd290b00-8ff5-11ea-982f-cfa108585303.jpg)
![Screenshot2](https://user-images.githubusercontent.com/64895726/81194550-bedbee80-8ff7-11ea-88ca-c0a4dfa4511c.jpg)

# Require
dump1090-fa 3.8.1  
I'm using Raspberry Pi (the first), so probably this works on all of your Pi.  
And it can works with both iPhone and Android.

# Installation
It's just two steps!

## 1 Enter your pi with SSH and run wget as the following.
```bash
sudo wget -P /usr/share/dump1090-fa/html https://github.com/genshibangou16/dump1090-fa-Mobile-UI/raw/master/style_mobile.css
```
Of course you can also put it manualy.
Don't put it wrong place.
## 2 Edit `index.html` at `/usr/share/dump1090-fa/html`.
Ex. with nano.
```bash
sudo nano /usr/share/dump1090-fa/html/index.html
```

#### Add the following at the _END_ of `<header>`.
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
Do __NOT__ put ↑ before `<link rel="stylesheet" type="text/css" href="style.css?v=3.8.1" />`, or you can't use PC layout.

# Note
I tried to pack all of features into one CSS file, so there might be some strange point.  
And... what's IE?  
I don't know about it. lol  
Please don't blame for my immaturity, but I welcome your pointing out my misstake and suggesting reform measures.  
Enjoy dumping!
