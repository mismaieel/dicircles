Using imagemagick command line to generate circular images :

convert kareem.jpg \( +clone -threshold -1 -negate -fill white -draw "circle `identify -format %w kareem.jpg | awk '{print $1/2}'`, `identify -format %h kareem.jpg | awk '{print $1/2}'` `identify -format %w kareem.jpg | awk '{print $1/2}'`, 0" \) -alpha Off -compose copy_opacity -composite kareem.png
