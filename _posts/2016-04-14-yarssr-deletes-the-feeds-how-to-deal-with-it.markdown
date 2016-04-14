---
published: true
title: Yarssr deletes the feeds, how to deal with it
layout: post
---
Intermittently, after OS reboot, yarssr seems to lose all the feeds. This can be observed by checking ~/.yarssr/config, it should be zero bytes.
This is highly inconvenient, and I haven't found a permanent fix. What I am doing as a workaround is a daily backup of the config files. 
{% highlight shell %}
0 5 * * * tar rvf /home/manu/.yarssr/yarssr-backup.tar -C /home/manu/.yarssr/ . 2>&1 1>/dev/null
{% endhighlight %}

That at least avoids the annoyance of losing everything. I don't think I'll ever have the time to resolve this bug. It is easier to do
{% highlight shell %} 
# tar xvf ~/.yarssr/yarssr-back.tar
{% endhighlight %} 

I've experienced this in the past with other solutions, as it is a little bit hard to reproduce and find the root cause.