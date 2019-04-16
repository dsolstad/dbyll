---
layout: post
title: The Status of phpGolf
categories: [phpgolf]
tags: [codegolf, php]
description: Sample placeholder post.
---

As the former creator and maintainer of phpGolf.org, people ask me what happened to the php code golfing site and why it is down. The reason was basically that the server owner wanted to change to another hosting vendor. Since I was out of the country for a year, without proper access to my developing infrastructure, and limited amount of spare time, it just never got back online. If the site was to get back now, it would require another dedicated person to rewrite the old code, polish the design, dockerize it, and basically carry the whole thing. The source can be found on <a href="https://github.com/phpGolf">GitHub</a>, except for the challenges, but I can provide those for anyone interested. 

![_config.yml]({{ site.baseurl }}/images/phpGolf.jpg)

I will now show off two of the most impressive work from the public challenges. They were submitted in 2012 by the talented primo, whom had the top score on all challenges. The encoding used to calculate the filesize was ISO-8859-1.

## Cantor's Enumeration

Challenge description: Print out the 100 first numbers in <a href="https://pastebin.com/4nub2H0r">Cantor's Enumeration</a>.

![_config.yml]({{ site.baseurl }}/images/cantor.png)

Leading submission with 57 byte:
{% highlight php %}
<?for($f=µ;$ö++.$µ++-49;--$$f?--$$f:$f^=C)echo"$ö / $µ
";
{% endhighlight %}

Shown in hex:
![_config.yml]({{ site.baseurl }}/images/primo-cantor-hex.png)

By comparrison, this was the next shortest submission from the user JWvdVeer with 76 bytes:
{% highlight php %}
<?for(;$x++.$y++^49;$b--?${$a%2?x:y}-=2:--${(1&$b=++$a)?y:x})echo"$x / $y
";
{% endhighlight %}

## Pathing

The challenge description were as follows:

* The constant MAP will contain one random map.
* Your program should output, to standard out, one single number,
the shortest distance from . to X. (alas, how many moves are the absolute 
minimum to get from the spot marked with '.' to the spot marked with 'X')
* Do not include the starting position, but include the end position.
* The map will always be closed, i.e. they will have a wall that reaches all the way around.
* The map are of random size, but no map will be greater than 50*50.
* The map may not always be square, but will always be rectangular.
* You may only move up, down, left or right. No diagonals.

Example input value (Given in the MAP constant on runtime):

```####################################
####################################
####################################
####### ############################
######  .###########################
######   ##############X ###########
#####     ##############  ##########
##### #  ############  ## ##########
#####       #######    #   #########
#######     ##### #      ###########
########  #####           ##########
########   #### ####   #############
########  #  #  ####   #############
########         ###################
#########        ###################
####################################
```

Example answer: 36

This was the leading submission with only 118 bytes.

{% highlight php %}
<?for(;^$f=$m[strpos($m=~MAP,Ñ)+$c=~($Ü%2*strpos($m,õ))*~-($Ü&2)+$p=$a[$Ü++/5-3]];)${$$f|$$c?z:$a[]=$c}=$$p+1;echo$z;
{% endhighlight %}

And as shown in hex:
![_config.yml]({{ site.baseurl }}/images/primo-pathing-hex.png)


I will follow up with a post about tips and tricks for golfing in php later on, which will explain some of the weird things going on here.

