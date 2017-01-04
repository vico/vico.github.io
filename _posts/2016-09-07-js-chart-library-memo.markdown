---
layout: post
title:  "JS Chart library memo"
date:   2016-09-08 12:38:00 +0900
comments: false
categories: javascript charts visualization
---

[Plot.ly](https://plot.ly/javascript/) [postMessage API](https://github.com/plotly/postMessage-API) for update graph: http://help.plot.ly/postMessage-API/



Elegant design: [metricgraphics](http://metricsgraphicsjs.org/)

Cute and simple: [chartjs](http://www.chartjs.org/)

Good charts: [nvd3](http://nvd3.org/livecode/index.html) [c3js](http://c3js.org/)

Stream data chart: [cubism](http://square.github.io/cubism/)



Data exploration charts: [dc](https://dc-js.github.io/dc.js/)

Chart for React.js [recharts](http://recharts.org/)



Design note for chart library: https://bost.ocks.org/mike/chart/

Comparison: [jsgraphs](http://www.jsgraphs.com/)

{% if page.comments %}
<div id="disqus_thread"></div>
<script>

/**
*  RECOMMENDED CONFIGURATION VARIABLES: EDIT AND UNCOMMENT THE SECTION BELOW TO INSERT DYNAMIC VALUES FROM YOUR PLATFORM OR CMS.
*  LEARN WHY DEFINING THESE VARIABLES IS IMPORTANT: https://disqus.com/admin/universalcode/#configuration-variables*/
var disqus_config = function () {
this.page.url = "http://blog.tranvinhcuong.me{{ page.url}}";  // Replace PAGE_URL with your page's canonical URL variable
this.page.identifier = "{{page.id}}";
};
(function() { // DON'T EDIT BELOW THIS LINE
var d = document, s = d.createElement('script');
s.src = '//cuongmemo.disqus.com/embed.js';
s.setAttribute('data-timestamp', +new Date());
(d.head || d.body).appendChild(s);
})();
</script>
<noscript>Please enable JavaScript to view the <a href="https://disqus.com/?ref_noscript">comments powered by Disqus.</a></noscript>
{% endif %}
