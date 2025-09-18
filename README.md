<!DOCTYPE html>
<html lang="ar">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>موقع التطبيقات</title>
<style>
body { font-family: Arial, sans-serif; background: #f0f0f0; margin: 0; padding: 20px; }
h1 { text-align: center; margin-bottom: 20px; }
.accordion { background-color: #0078D7; color: white; cursor: pointer; padding: 15px; width: 100%; border: none; text-align: right; outline: none; font-size: 18px; margin-bottom: 5px; border-radius: 5px;}
.active, .accordion:hover { background-color: #005a9e; }
.panel { padding: 0 15px; display: none; background-color: white; border-radius: 5px; margin-bottom: 10px; }
.sub-app { display: block; background-color: #e7e7e7; border: none; padding: 10px; margin: 5px 0; text-align: right; cursor: pointer; border-radius: 5px;}
.sub-app:hover { background-color: #d0d0d0; }
#app-details { background-color: white; padding: 15px; border-radius: 5px; margin-top: 20px;}
#app-details img { max-width: 100%; height: auto; border-radius: 5px; margin-bottom: 10px;}
a.download { display: inline-block; margin-top: 10px; padding: 10px 15px; background: #0078D7; color: white; text-decoration: none; border-radius: 5px;}
a.download:hover { background: #005a9e; }
</style>
</head>
<body>
<h1>موقع التطبيقات</h1>

<!-- الخانات الرئيسية -->
<button class="accordion">هـ1ك دلتا ايفون</button>
<div class="panel">
  <button class="sub-app" data-title="دلتا ايفون 1" data-desc="وصف دلتا ايفون 1" data-img="https://via.placeholder.com/300x150" data-link="#">دلتا ايفون 1</button>
  <button class="sub-app" data-title="دلتا ايفون 2" data-desc="وصف دلتا ايفون 2" data-img="https://via.placeholder.com/300x150" data-link="#">دلتا ايفون 2</button>
</div>

<button class="accordion">هـ1ك دلتا اندرويد</button>
<div class="panel">
  <button class="sub-app" data-title="دلتا اندرويد 1" data-desc="وصف دلتا اندرويد 1" data-img="https://via.placeholder.com/300x150" data-link="#">دلتا اندرويد 1</button>
  <button class="sub-app" data-title="دلتا اندرويد 2" data-desc="وصف دلتا اندرويد 2" data-img="https://via.placeholder.com/300x150" data-link="#">دلتا اندرويد 2</button>
</div>

<button class="accordion">هـ1ك كوديكس ايفون</button>
<div class="panel">
  <button class="sub-app" data-title="كوديكس ايفون 1" data-desc="وصف كوديكس ايفون 1" data-img="https://via.placeholder.com/300x150" data-link="#">كوديكس ايفون 1</button>
  <button class="sub-app" data-title="كوديكس ايفون 2" data-desc="وصف كوديكس ايفون 2" data-img="https://via.placeholder.com/300x150" data-link="#">كوديكس ايفون 2</button>
</div>

<button class="accordion">هـ1ك كوديكس اندرويد</button>
<div class="panel">
  <button class="sub-app" data-title="كوديكس اندرويد 1" data-desc="وصف كوديكس اندرويد 1" data-img="https://via.placeholder.com/300x150" data-link="#">كوديكس اندرويد 1</button>
  <button class="sub-app" data-title="كوديكس اندرويد 2" data-desc="وصف كوديكس اندرويد 2" data-img="https://via.placeholder.com/300x150" data-link="#">كوديكس اندرويد 2</button>
</div>

<button class="accordion">هـ1ك كرنل ايفون</button>
<div class="panel">
  <button class="sub-app" data-title="كرنل ايفون 1" data-desc="وصف كرنل ايفون 1" data-img="https://via.placeholder.com/300x150" data-link="#">كرنل ايفون 1</button>
  <button class="sub-app" data-title="كرنل ايفون 2" data-desc="وصف كرنل ايفون 2" data-img="https://via.placeholder.com/300x150" data-link="#">كرنل ايفون 2</button>
</div>

<button class="accordion">هـ1ك كرنل اندرويد</button>
<div class="panel">
  <button class="sub-app" data-title="كرنل اندرويد 1" data-desc="وصف كرنل اندرويد 1" data-img="https://via.placeholder.com/300x150" data-link="#">كرنل اندرويد 1</button>
  <button class="sub-app" data-title="كرنل اندرويد 2" data-desc="وصف كرنل اندرويد 2" data-img="https://via.placeholder.com/300x150" data-link="#">كرنل اندرويد 2</button>
</div>

<button class="accordion">هـ1كات بيـ،سي</button>
<div class="panel">
  <button class="sub-app" data-title="كات بي سي 1" data-desc="وصف كات بي سي 1" data-img="https://via.placeholder.com/300x150" data-link="#">كات بي سي 1</button>
  <button class="sub-app" data-title="كات بي سي 2" data-desc="وصف كات بي سي 2" data-img="https://via.placeholder.com/300x150" data-link="#">كات بي سي 2</button>
</div>

<div id="app-details"></div>

<script>
let accordions = document.querySelectorAll('.accordion');
accordions.forEach(acc => {
  acc.onclick = () => {
    let panel = acc.nextElementSibling;
    panel.style.display = panel.style.display === 'block' ? 'none' : 'block';
  }
});

let subApps = document.querySelectorAll('.sub-app');
subApps.forEach(btn => {
  btn.onclick = () => {
    let title = btn.getAttribute('data-title');
    let desc = btn.getAttribute('data-desc');
    let img = btn.getAttribute('data-img');
    let link = btn.getAttribute('data-link');
    document.getElementById('app-details').innerHTML =
      `<h2>${title}</h2>
       <img src="${img}" alt="${title}">
       <p>${desc}</p>
       <a class="download" href="${link}" target="_blank">تحميل</a>`;
    window.scrollTo({ top: document.getElementById('app-details').offsetTop, behavior: 'smooth' });
  }
});
</script>

</body>
</html>
