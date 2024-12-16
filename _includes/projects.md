<h2 id="publications" style="margin: 2px 0px -15px;">Projects</h2>

<div class="publications">
  <ol class="bibliography">

{% for link in site.data.publications.main %}

<li>
<!-- 전체 컨테이너 -->
<div class="pub-row" style="display: flex; flex-direction: column; margin-bottom: 30px;">

<!-- 제목 -->
<div class="col-sm-12" style="margin-bottom: 10px;">
  <div class="title" style="font-size: 18px; font-weight: bold; width: 100%; text-align: left;">
    <a href="{{ link.pdf }}" style="display: block; text-align: left; ">{{ link.title }}</a>
  </div>
  <div class="author" style="font-size: 14px; color: #555;">{{ link.authors }}</div>
  <div class="periodical" style="font-size: 14px; font-style: italic; color: #777;">{{ link.conference }}</div>
</div>
<!-- 하단 내용 (이미지 + 설명) -->
<div class="pub-content" style="display: flex; align-items: flex-start;">
  <!-- 이미지 -->
  <div class="col-sm-3" style="padding-right: 15px; padding-left: 15px;">
    {% if link.image %}
    <img src="{{ link.image }}" class="teaser img-fluid z-depth-1" 
          style="width: 100%; max-width: 800px; height: auto; max-height: 500px; object-fit: cover;">
    {% endif %}
  </div>

  <!-- 설명 -->
  <div class="col-sm-9" style="padding-left: 20px; font-size: 14px; color: #333;">
    {% if link.notes %}
      <div class="notes">
        <ul style="list-style-type: disc; padding-left: 20px; margin-top: 0; margin-bottom: 0;">
          {% for note in link.notes %}
            <li style="margin-bottom: 5px; line-height: 1.5;">{{ note }}</li>
          {% endfor %}
        </ul>
      </div>
    {% endif %}
    <div class="links" style="margin-top: 10px;">
      {% if link.pdf %}
      <a href="{{ link.pdf }}" class="btn btn-sm z-depth-0" role="button" target="_blank" 
          style="font-size:12px;">PDF</a>
      {% endif %}
      {% if link.code %}
      <a href="{{ link.code }}" class="btn btn-sm z-depth-0" role="button" target="_blank" 
          style="font-size:12px;">Code</a>
      {% endif %}
      {% if link.page %}
      <a href="{{ link.page }}" class="btn btn-sm z-depth-0" role="button" target="_blank" 
          style="font-size:12px;">Project Page</a>
      {% endif %}
      {% if link.bibtex %}
      <a href="{{ link.bibtex }}" class="btn btn-sm z-depth-0" role="button" target="_blank" 
          style="font-size:12px;">BibTex</a>
      {% endif %}
    </div>
  </div>
</div>

</div>
</li>

{% endfor %}

  </ol>
</div>




<!-- <h2 id="publications" style="margin: 2px 0px -15px;">Projects</h2>

<div class="publications">
<ol class="bibliography">

{% for link in site.data.publications.main %}

<li>
<div class="pub-row">
  <div class="col-sm-12" style="position: relative;padding-right: 15px;padding-left: 20px;">
      <div class="title"><a href="{{ link.pdf }}">{{ link.title }}</a></div>
      <div class="author">{{ link.authors }}</div>
      <div class="periodical"><em>{{ link.conference }}</em></div>
  </div>
</div>
<div class="pub-row" style="display: flex;">
  <div class="col-sm-3 abbr" style="position: relative;padding-right: 15px;padding-left: 15px;">
    {% if link.image %} 
    <img src="{{ link.image }}" class="teaser img-fluid z-depth-1" style="width: 80%; height: auto; max-height: 500px; margin-bottom: 100px;">
    {% endif %}
  </div>
  <div class="col-sm-9" style="position: relative;padding-right: 15px;padding-left: 20px;">
    <div class="links">
      {% if link.pdf %} 
      <a href="{{ link.pdf }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">PDF</a>
      {% endif %}
      {% if link.code %} 
      <a href="{{ link.code }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Code</a>
      {% endif %}
      {% if link.page %} 
      <a href="{{ link.page }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Project Page</a>
      {% endif %}
      {% if link.bibtex %} 
      <a href="{{ link.bibtex }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">BibTex</a>
      {% endif %}
      {% if link.notes %} 
      <div>
        {{ link.notes }}
      </div>
      {% endif %}
      {% if link.others %} 
      {{ link.others }}
      {% endif %}
    </div>
  </div>
</div>
</li>
<br>

{% endfor %}

</ol>
</div> -->
