---
layout: post
title: "Japanese equinox dates calculation"
date: 2016-11-26 14:45:00 +0900
comments: true
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

{% if page.comments %}
<div id="disqus_thread"></div>
<script>

/**
*  RECOMMENDED CONFIGURATION VARIABLES: EDIT AND UNCOMMENT THE SECTION BELOW TO INSERT DYNAMIC VALUES FROM YOUR PLATFORM OR CMS.
*  LEARN WHY DEFINING THESE VARIABLES IS IMPORTANT: https://disqus.com/admin/universalcode/#configuration-variables*/
var disqus_config = function () {
this.page.url = "{{ site.baseurl }}{% post_url 2016-11-26-calculate-equinox-date-using-python %}";  // Replace PAGE_URL with your page's canonical URL variable
this.page.identifier = "2016-11-26-calculate-equinox-date-using-python"; // Replace PAGE_IDENTIFIER with your page's unique identifier variable
};
(function() { // DON'T EDIT BELOW THIS LINE
var d = document, s = d.createElement('script');
s.src = '//EXAMPLE.disqus.com/embed.js';
s.setAttribute('data-timestamp', +new Date());
(d.head || d.body).appendChild(s);
})();
</script>
<noscript>Please enable JavaScript to view the <a href="https://disqus.com/?ref_noscript">comments powered by Disqus.</a></noscript>
{% endif %}
