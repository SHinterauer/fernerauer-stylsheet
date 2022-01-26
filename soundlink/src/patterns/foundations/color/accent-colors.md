---
title: Accent Colors
styles: base/variables.scss
maturity: ready
control: exclude
colors: 
  - name: $onyx-80
    hex: '#41415D'
    rgb: rgb(65,65,93)
  - name: $onyx-60
    hex: '#686882'
    rgb: rgb(104,104,130)
  - name: $onyx-40
    hex: '#8F8F9B'
    rgb: rgb(143,143,155)
  - name: $clay-80
    hex: '#DDAA45'
    rgb: rgb(221,170,69)
  - name: $clay-60
    hex: '#E9B859'
    rgb: rgb(233,184,89)
  - name: $clay-40
    hex: '#FFD178'
    rgb: rgb(255,209,120)
  - name: $white
    hex: '#ffffff'
    rgb: rgb(0,0,0)
  - name: $red
    hex: '#E28570'
    rgb: rgb(226,133,112)
  - name: $light-green
    hex: '#97C65C'
    rgb: rgb(151,198,92)
---
<style>
.set {
  display: flex;
  flex-wrap: wrap;
  margin: 0 -1rem;
  margin-top: 0;
  padding: 0;
  list-style: none;
}
li {
  flex: 1 0 20%;
  margin: 1rem;
}
.color {
  width: 100%;
  min-width: 160px;
  height: 80px;
  color: white;
  border: 1px solid whitesmoke;
  margin-bottom: 1rem;
}
p {
  margin: 0;
}
</style>
<ul class="set">
{% for item in page.colors %} 
  <li>
    <div class="color" style="background:{{ item.hex }}"></div> 
    <p>{{ item.name }}</p>
    {% if item.hex %}<p>{{ item.hex }}</p>{% endif %}
    {% if item.rgb %}<p>{{ item.rgb }}</p>{% endif %}
  </li>
{% endfor %}
</ul>