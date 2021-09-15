# Screenshot Pages

## GoWitness

### Github Links

* [https://github.com/sensepost/gowitness](https://github.com/sensepost/gowitness)
* [https://github.com/sensepost/gowitness/wiki](https://github.com/sensepost/gowitness/wiki)

### Install

* go get -u github.com/sensepost/gowitness

### Install if Above Gives an Error

* try using "pimpmykali"

```bash
sudo go get -u gorm.io/gorm && sudo go get -u github.com/sensepost/gowitness
```

## Aquatone

* look into this alternative

## cutycapt

* [https://tools.kali.org/web-applications/cutycapt](https://tools.kali.org/web-applications/cutycapt)

## Create HTML Page of Screenshots

```bash
#List all pictures of Pictures
ls -1 *.png
#output
10.x.x.10.png
10.x.x.10.png
10.x.x.10.png
    
#Script that puts all images in HTML file for easy viewing
#!/bin/bash
echo "<HTML><BODY><BR>" > webview.html

ls -1 *.png | awk -F : '{ print $1":\n<BR><IMG SRC=\""$1""$2"\" width=600><BR>"}' >> webview.html

echo "</BODY></HTML>" >> webview.html


#Create the script above and use it like this
./nameOfScript.sh
```

