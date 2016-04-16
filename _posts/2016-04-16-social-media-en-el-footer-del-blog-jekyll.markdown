---
published: true
title: Social media en el footer del Blog Jekyll
layout: post
---
### Te muestro como agregar al footer de tu blog links a tus sitios de social media. Los ejemplos son sólamente para GitHub y Linkedin... pero usando SVG!!!! 

### En esta continuación de [GitHub pages desde linea de comando][2] vamos a agregar iconos y links al footer de social media


1. Especificar tus usuarios a _config.yml, por ejemplo los mios son:
{% highlight text %}
github_username:  emmanuel-galindo
linkedin_username: emmanuelgalindo
{% endhighlight %}

2. Dimensionar los SVG en tu CSS customizado (css/custom.css en mi caso), y otra clase mas que uso en mi ejemplo asi no se ve tan feo

{% highlight text %}
/** Icons */
.icon > svg {display: inline-block;width: 16px;height: 16px;vertical-align: middle;}
.icon > svg path { fill: #828282; }

.social-media-list {list-style: none;margin-left: 0;}
{% endhighligtht %}

3. Modificar _includes/footer.html. Por ejemplo, el mio actualmente es:

{% highlight html %}
{% raw %}

<footer class="footer">
  <div class="p2 wrap">
    <div class="measure mt1 center">
      <ul class="social-media-list">
      {% if site.github_username %}
      <li>
      <a href="https://github.com/{{ site.github_username }}">
      <span class="icon icon--github">
      <svg viewBox="0 0 16 16">
      <path fill="#828282" d="M7.999,0.431c-4.285,0-7.76,3.474-7.76,7.761 c0,3.428,2.223,6.337,5.307,7.363c0.388,0.071,0.53-0.168,0.53-0.374c0-0.184-0.007-0.672-0.01-1.32 c-2.159,0.469-2.614-1.04-2.614-1.04c-0.353-0.896-0.862-1.135-0.862-1.135c-0.705-0.481,0.053-0.472,0.053-0.472 c0.779,0.055,1.189,0.8,1.189,0.8c0.692,1.186,1.816,0.843,2.258,0.645c0.071-0.502,0.271-0.843,0.493-1.037 C4.86,11.425,3.049,10.76,3.049,7.786c0-0.847,0.302-1.54,0.799-2.082C3.768,5.507,3.501,4.718,3.924,3.65 c0,0,0.652-0.209,2.134,0.796C6.677,4.273,7.34,4.187,8,4.184c0.659,0.003,1.323,0.089,1.943,0.261 c1.482-1.004,2.132-0.796,2.132-0.796c0.423,1.068,0.157,1.857,0.077,2.054c0.497,0.542,0.798,1.235,0.798,2.082 c0,2.981-1.814,3.637-3.543,3.829c0.279,0.24,0.527,0.713,0.527,1.437c0,1.037-0.01,1.874-0.01,2.129 c0,0.208,0.14,0.449,0.534,0.373c3.081-1.028,5.302-3.935,5.302-7.362C15.76,3.906,12.285,0.431,7.999,0.431z"/>
      </svg>
      </span>

      <span class="username">{{ site.github_username }}</span>
      </a>
      </li>
      {% endif %}
      {% if site.linkedin_username %}
      <li>
      <a href="https://www.linkedin.com/in/{{ site.linkedin_username }}">
      <span class="icon  icon--linkedin">
      <svg viewBox="0 0 57 57">
      <path fill="#828282" d="M49.265,4.667H7.145c-2.016,0-3.651,1.596-3.651,3.563v42.613c0,1.966,1.635,3.562,3.651,3.562h42.12   c2.019,0,3.654-1.597,3.654-3.562V8.23C52.919,6.262,51.283,4.667,49.265,4.667z M18.475,46.304h-7.465V23.845h7.465V46.304z    M14.743,20.777h-0.05c-2.504,0-4.124-1.725-4.124-3.88c0-2.203,1.67-3.88,4.223-3.88c2.554,0,4.125,1.677,4.175,3.88   C18.967,19.052,17.345,20.777,14.743,20.777z M45.394,46.304h-7.465V34.286c0-3.018-1.08-5.078-3.781-5.078   c-2.062,0-3.29,1.389-3.831,2.731c-0.197,0.479-0.245,1.149-0.245,1.821v12.543h-7.465c0,0,0.098-20.354,0-22.459h7.465v3.179   c0.992-1.53,2.766-3.709,6.729-3.709c4.911,0,8.594,3.211,8.594,10.11V46.304z"/>
      </svg>
      </span>

      <span class="username">{{ site.linkedin_username }}</span>
      </a>
      </li>
      {% endif %}
      </ul>
</div>
</div>
</footer>
{% endraw %}
{% endhighlight %}

Otra alternativa a los SVG, es usar la libreria de [Font Awesome][1]

[1]: http://fontawesome.io/examples/
[2]: http://emmanuel-galindo.github.io/2016/04/15/github-pages-desde-linea-de-comando.html
