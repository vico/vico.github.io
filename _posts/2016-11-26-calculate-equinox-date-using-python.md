---
layout: post
title: "Japanese equinox dates calculation"
date: 2016-11-26 14:45:00 +0900
categories: python calendar
---

The calculation is all done by library [PyEphem](http://rhodesmill.org/pyephem/) library.
For Japanese date, need to convert the date to JST timezone to get correct date.

{% highlight python %}
import pytz
import ephem

equinox = ephem.next_autumnal_equinox(str('2008')).datetime()
local_tz = pytz.timezone('Asia/Tokyo')
equinox = equinox.replace(tzinfo=pytz.utc).astimezone(local_tz).date() # 2008-09-23
{% endhighlight %}

Same for Vernal Equinox which can be calculated by using `ephem.next_spring_equinox`.
