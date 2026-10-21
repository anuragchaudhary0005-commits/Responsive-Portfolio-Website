# Responsive-Portfolio-Website
<!DOCTYPE html>
<html lang="en" data-bs-theme="light">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Alex Rivera — Front-end Developer</title>
<meta name="description" content="Portfolio of Alex Rivera, front-end developer.">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Bricolage+Grotesque:wght@500;700;800&family=DM+Sans:wght@400;500&display=swap" rel="stylesheet">
<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet">
<style>
  :root{
    --accent:#2f5bff; --accent-2:#ffb703;
    --bs-body-font-family:'DM Sans',system-ui,sans-serif;
    --bs-body-bg:#f5f7fa; --bs-body-color:#0f1b2d;
    --surface:#fff; --line:#dde3ec;
  }
  [data-bs-theme="dark"]{
    --accent:#7c97ff; --bs-body-bg:#0c1220; --bs-body-color:#e8edf6;
    --surface:#141c2e; --line:#26314a;
  }
  html{scroll-behavior:smooth;scroll-padding-top:72px}
  h1,h2,h3,.navbar-brand{font-family:'Bricolage Grotesque',sans-serif;letter-spacing:-.02em}
  a{color:var(--accent)}
  .navbar{background:color-mix(in srgb,var(--bs-body-bg) 88%,transparent);backdrop-filter:blur(8px);border-bottom:1px solid var(--line)}
  .navbar-brand{font-weight:800}
  .nav-link{font-weight:500}
  .nav-link.active{color:var(--accent)!important}
  .btn-accent{background:var(--accent);color:#fff;border:0;font-weight:500}
  .btn-accent:hover{background:var(--accent);color:#fff;filter:brightness(1.1)}
  .btn-outline-ink{border:1.5px solid var(--bs-body-color);color:var(--bs-body-color)}
  .btn-outline-ink:hover{background:var(--bs-body-color);color:var(--bs-body-bg)}
  :focus-visible{outline:3px solid var(--accent-2);outline-offset:2px}

  .hero{padding:9rem 0 5rem}
  .hero h1{font-size:clamp(2.8rem,9vw,6.5rem);font-weight:800;line-height:.98}
  .hero .role{font-size:clamp(1.1rem,2.5vw,1.5rem);min-height:2em}
  .caret{display:inline-block;width:2px;height:1.1em;background:var(--accent);margin-left:3px;vertical-align:-.15em;animation:blink 1s steps(2) infinite}
  @keyframes blink{50%{opacity:0}}
  .marker{background:linear-gradient(transparent 62%,var(--accent-2) 62%);padding:0 .1em}

  section{padding:5rem 0}
  .section-title{font-size:clamp(1.8rem,4vw,2.6rem);font-weight:700;margin-bottom:2rem}
  .panel{background:var(--surface);border:1px solid var(--line);border-radius:14px}

  .skill-row{margin-bottom:1.1rem}
  .progress{height:8px;background:var(--line);border-radius:8px}
  .progress-bar{background:var(--accent);width:0;transition:width 1.1s ease}

  .project{overflow:hidden;height:100%;display:flex;flex-direction:column}
  .thumb{height:150px;display:flex;align-items:flex-end;padding:1rem;color:#fff;font-family:'Bricolage Grotesque',sans-serif;font-weight:700;font-size:1.3rem}
  .t1{background:linear-gradient(135deg,#2f5bff,#0f1b2d)}
  .t2{background:linear-gradient(135deg,#ffb703,#e4572e)}
  .t3{background:linear-gradient(135deg,#17a589,#0f3d3e)}
  .t4{background:linear-gradient(135deg,#8e44ad,#2f5bff)}
  .t5{background:linear-gradient(135deg,#ef476f,#ffb703)}
  .t6{background:linear-gradient(135deg,#118ab2,#073b4c)}
  .tag{font-size:.78rem;border:1px solid var(--line);border-radius:20px;padding:.1rem .6rem;margin:0 .25rem .25rem 0;display:inline-block}
  .filters .btn{border-radius:20px}
  .filters .btn.active{background:var(--bs-body-color);color:var(--bs-body-bg);border-color:var(--bs-body-color)}

  .timeline{border-left:2px solid var(--line);padding-left:1.25rem}
  .timeline .item{position:relative;margin-bottom:1.5rem}
  .timeline .item::before{content:"";position:absolute;left:-1.6rem;top:.45rem;width:10px;height:10px;border-radius:50%;background:var(--accent)}
  .form-control{background:var(--surface);border-color:var(--line)}
  footer{border-top:1px solid var(--line);padding:2rem 0}
  @media (prefers-reduced-motion:reduce){html{scroll-behavior:auto}.caret{animation:none}.progress-bar{transition:none}}
</style>
</head>
<body data-bs-spy="scroll" data-bs-target="#nav" data-bs-offset="80" tabindex="0">

<nav class="navbar navbar-expand-md fixed-top">
  <div class="container">
    <a class="navbar-brand" href="#top">Alex Rivera</a>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#nav" aria-controls="nav" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="nav">
      <ul class="navbar-nav ms-auto align-items-md-center gap-md-1">
        <li class="nav-item"><a class="nav-link" href="#about">About</a></li>
        <li class="nav-item"><a class="nav-link" href="#projects">Projects</a></li>
        <li class="nav-item"><a class="nav-link" href="#experience">Experience</a></li>
        <li class="nav-item"><a class="nav-link" href="#contact">Contact</a></li>
        <li class="nav-item ms-md-2">
          <button id="themeBtn" class="btn btn-sm btn-outline-ink" type="button" aria-label="Switch color theme">Dark mode</button>
        </li>
      </ul>
    </div>
  </div>
</nav>

<header class="hero" id="top">
  <div class="container">
    <div class="row">
      <div class="col-lg-10">
        <p class="mb-2 text-body-secondary">Hi, I'm Alex — based in Lisbon, working worldwide.</p>
        <h1>I build fast, <span class="marker">accessible</span> websites.</h1>
        <p class="role mt-4"><span id="typed"></span><span class="caret" aria-hidden="true"></span></p>
        <div class="d-flex flex-wrap gap-2 mt-4">
          <a href="#projects" class="btn btn-accent btn-lg">See my work</a>
          <a href="#contact" class="btn btn-outline-ink btn-lg">Get in touch</a>
        </div>
      </div>
    </div>
  </div>
</header>

<section id="about">
  <div class="container">
    <div class="row g-5">
      <div class="col-lg-6">
        <h2 class="section-title">About me</h2>
        <p class="fs-5">I'm a front-end developer with six years of experience turning designs into responsive, accessible interfaces.</p>
        <p>I've shipped products for startups and agencies, from marketing sites to complex dashboards. I care about performance, clean code, and interfaces that work for everyone — on any screen.</p>
        <p>Outside of work I mentor junior developers and cook too much pasta.</p>
        <a href="#" class="btn btn-outline-ink mt-2">Download résumé</a>
      </div>
      <div class="col-lg-6">
        <div class="panel p-4" id="skills">
          <h3 class="h5 mb-4">Skills</h3>
          <div class="skill-row"><div class="d-flex justify-content-between"><span>HTML &amp; CSS</span><span>95%</span></div><div class="progress"><div class="progress-bar" data-w="95"></div></div></div>
          <div class="skill-row"><div class="d-flex justify-content-between"><span>JavaScript</span><span>90%</span></div><div class="progress"><div class="progress-bar" data-w="90"></div></div></div>
          <div class="skill-row"><div class="d-flex justify-content-between"><span>Bootstrap &amp; Sass</span><span>88%</span></div><div class="progress"><div class="progress-bar" data-w="88"></div></div></div>
          <div class="skill-row"><div class="d-flex justify-content-between"><span>React</span><span>80%</span></div><div class="progress"><div class="progress-bar" data-w="80"></div></div></div>
          <div class="skill-row mb-0"><div class="d-flex justify-content-between"><span>Accessibility</span><span>85%</span></div><div class="progress"><div class="progress-bar" data-w="85"></div></div></div>
        </div>
      </div>
    </div>
  </div>
</section>

<section id="projects">
  <div class="container">
    <h2 class="section-title">Selected projects</h2>
    <div class="filters d-flex flex-wrap gap-2 mb-4" role="group" aria-label="Filter projects">
      <button class="btn btn-sm btn-outline-secondary active" data-filter="all">All</button>
      <button class="btn btn-sm btn-outline-secondary" data-filter="web">Websites</button>
      <button class="btn btn-sm btn-outline-secondary" data-filter="app">Web apps</button>
      <button class="btn btn-sm btn-outline-secondary" data-filter="ui">UI kits</button>
    </div>
    <div class="row g-4" id="grid">
      <div class="col-md-6 col-lg-4" data-cat="web"><article class="panel project"><div class="thumb t1">Brightside Café</div><div class="p-3"><p>Ordering site for a local café, with a menu that loads in under a second.</p><span class="tag">HTML</span><span class="tag">Bootstrap</span><span class="tag">JS</span></div></article></div>
      <div class="col-md-6 col-lg-4" data-cat="app"><article class="panel project"><div class="thumb t2">TaskTide</div><div class="p-3"><p>A drag-and-drop task board that syncs across devices.</p><span class="tag">React</span><span class="tag">Firebase</span></div></article></div>
      <div class="col-md-6 col-lg-4" data-cat="ui"><article class="panel project"><div class="thumb t3">Pebble UI</div><div class="p-3"><p>An open-source component library built on Bootstrap's Sass variables.</p><span class="tag">Sass</span><span class="tag">Bootstrap</span></div></article></div>
      <div class="col-md-6 col-lg-4" data-cat="web"><article class="panel project"><div class="thumb t4">Northwind Studio</div><div class="p-3"><p>Portfolio site for an architecture studio with an image-led layout.</p><span class="tag">HTML</span><span class="tag">CSS</span></div></article></div>
      <div class="col-md-6 col-lg-4" data-cat="app"><article class="panel project"><div class="thumb t5">Fitlog</div><div class="p-3"><p>Workout tracker with charts of weekly progress.</p><span class="tag">JS</span><span class="tag">Chart.js</span></div></article></div>
      <div class="col-md-6 col-lg-4" data-cat="ui"><article class="panel project"><div class="thumb t6">Dashkit</div><div class="p-3"><p>Admin dashboard templates with light and dark themes.</p><span class="tag">Bootstrap</span><span class="tag">Sass</span></div></article></div>
    </div>
  </div>
</section>

<section id="experience">
  <div class="container">
    <h2 class="section-title">Experience</h2>
    <div class="row"><div class="col-lg-8">
      <div class="timeline">
        <div class="item"><h3 class="h5 mb-0">Senior Front-end Developer, Lumen Labs</h3><small class="text-body-secondary">2022 – Present</small><p class="mt-2 mb-0">Lead a team of four building the customer dashboard. Cut load time by 40%.</p></div>
        <div class="item"><h3 class="h5 mb-0">Front-end Developer, Pixel &amp; Co.</h3><small class="text-body-secondary">2019 – 2022</small><p class="mt-2 mb-0">Built more than 30 responsive client sites with Bootstrap and vanilla JavaScript.</p></div>
        <div class="item"><h3 class="h5 mb-0">Junior Developer, Webworks</h3><small class="text-body-secondary">2018 – 2019</small><p class="mt-2 mb-0">Maintained marketing sites and learned the craft from great mentors.</p></div>
      </div>
    </div></div>
  </div>
</section>

<section id="contact">
  <div class="container">
    <div class="row g-5">
      <div class="col-lg-5">
        <h2 class="section-title">Let's work together</h2>
        <p>Have a project in mind? Send a message and I'll reply within two days.</p>
        <p class="mb-1"><a href="mailto:alex@example.com">alex@example.com</a></p>
        <p><a href="#">GitHub</a> · <a href="#">LinkedIn</a></p>
      </div>
      <div class="col-lg-7">
        <form id="form" class="panel p-4 needs-validation" novalidate>
          <div class="row g-3">
            <div class="col-md-6"><label for="name" class="form-label">Name</label><input id="name" class="form-control" required><div class="invalid-feedback">Enter your name.</div></div>
            <div class="col-md-6"><label for="email" class="form-label">Email</label><input id="email" type="email" class="form-control" required><div class="invalid-feedback">Enter a valid email address.</div></div>
            <div class="col-12"><label for="msg" class="form-label">Message</label><textarea id="msg" rows="4" class="form-control" required minlength="10"></textarea><div class="invalid-feedback">Write at least 10 characters.</div></div>
            <div class="col-12"><button class="btn btn-accent" type="submit">Send message</button></div>
          </div>
          <div id="ok" class="alert alert-success mt-3 mb-0 d-none" role="status">Message ready to send — your email app should open now.</div>
        </form>
      </div>
    </div>
  </div>
</section>

<footer><div class="container d-flex flex-wrap justify-content-between gap-2 small text-body-secondary"><span>© <span id="yr"></span> Alex Rivera</span><a href="#top">Back to top</a></div></footer>

<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"></script>
<script>
(function(){
  var root=document.documentElement, btn=document.getElementById('themeBtn');
  function setTheme(t){root.setAttribute('data-bs-theme',t);btn.textContent=t==='dark'?'Light mode':'Dark mode';try{localStorage.setItem('theme',t)}catch(e){}}
  var saved=null;try{saved=localStorage.getItem('theme')}catch(e){}
  setTheme(saved||(matchMedia('(prefers-color-scheme: dark)').matches?'dark':'light'));
  btn.addEventListener('click',function(){setTheme(root.getAttribute('data-bs-theme')==='dark'?'light':'dark')});

  // Typed roles
  var roles=['Front-end developer','Bootstrap specialist','Accessibility advocate'],el=document.getElementById('typed'),r=0,c=0,del=false;
  if(matchMedia('(prefers-reduced-motion: reduce)').matches){el.textContent=roles[0]}
  else(function tick(){
    var w=roles[r];c+=del?-1:1;el.textContent=w.slice(0,c);
    var d=del?35:70;
    if(!del&&c===w.length){del=true;d=1400}
    else if(del&&c===0){del=false;r=(r+1)%roles.length;d=300}
    setTimeout(tick,d);
  })();

  // Skill bars fill on view
  var io=new IntersectionObserver(function(es){es.forEach(function(e){
    if(e.isIntersecting){e.target.querySelectorAll('.progress-bar').forEach(function(b){b.style.width=b.dataset.w+'%'});io.unobserve(e.target)}
  })},{threshold:.3});
  io.observe(document.getElementById('skills'));

  // Project filter
  var fb=document.querySelectorAll('[data-filter]'),cards=document.querySelectorAll('#grid [data-cat]');
  fb.forEach(function(b){b.addEventListener('click',function(){
    fb.forEach(function(x){x.classList.remove('active')});b.classList.add('active');
    cards.forEach(function(c){c.classList.toggle('d-none',b.dataset.filter!=='all'&&c.dataset.cat!==b.dataset.filter)});
  })});

  // Contact form (replace mailto with your form service when you go live)
  var f=document.getElementById('form');
  f.addEventListener('submit',function(e){
    e.preventDefault();f.classList.add('was-validated');
    if(!f.checkValidity())return;
    var n=encodeURIComponent(document.getElementById('name').value),m=encodeURIComponent(document.getElementById('msg').value);
    document.getElementById('ok').classList.remove('d-none');
    location.href='mailto:alex@example.com?subject=Portfolio%20message%20from%20'+n+'&body='+m;
  });
  document.getElementById('yr').textContent=new Date().getFullYear();
})();
</script>
</body>
</html>
