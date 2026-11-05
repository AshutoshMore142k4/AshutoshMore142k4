<!doctype html>
<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width,initial-scale=1">
<title>Profile card</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600&display=swap" rel="stylesheet">
<style>
:root{
  --bg:#f5f5f7; --fg:#1d1d1f; --mut:#6e6e73; --hair:rgba(0,0,0,.08); --acc:#34c759; --track:rgba(0,0,0,.06);
  --l0:#007aff; --l1:#af52de; --l2:#ffcc00; --lo:rgba(0,0,0,.14);
}
@media (prefers-color-scheme:dark){:root:not([data-theme="light"]){
  --bg:#1c1c1e; --fg:#f5f5f7; --mut:#98989d; --hair:rgba(255,255,255,.10); --acc:#30d158; --track:rgba(255,255,255,.08);
  --l0:#0a84ff; --l1:#bf5af2; --l2:#ffd60a; --lo:rgba(255,255,255,.18);
}}
:root[data-theme="dark"]{
  --bg:#1c1c1e; --fg:#f5f5f7; --mut:#98989d; --hair:rgba(255,255,255,.10); --acc:#30d158; --track:rgba(255,255,255,.08);
  --l0:#0a84ff; --l1:#bf5af2; --l2:#ffd60a; --lo:rgba(255,255,255,.18);
}
*{box-sizing:border-box;margin:0;padding:0}
body{background:transparent;display:grid;place-items:center;min-height:100vh;padding:16px;
  font-family:Inter,-apple-system,BlinkMacSystemFont,"SF Pro Display","Segoe UI",system-ui,sans-serif;
  -webkit-font-smoothing:antialiased}
.card{width:100%;max-width:1040px;display:grid;grid-template-columns:1.15fr 1.2fr .65fr;
  background:var(--bg);color:var(--fg);border:1px solid var(--hair);border-radius:28px;
  letter-spacing:-.011em}
.col{padding:30px 32px 32px}
.col+.col{border-left:1px solid var(--hair)}
h2{font-size:13px;font-weight:500;color:var(--mut);letter-spacing:0;margin-bottom:14px}
ul{list-style:none}
.ach li{display:flex;align-items:baseline;gap:10px;font-size:15px;line-height:1.3;padding:5px 0;white-space:nowrap}
.ach li::before{content:"";flex:none;width:6px;height:6px;border-radius:50%;background:var(--acc);transform:translateY(-2px)}
.ach b{font-weight:600;letter-spacing:-.014em}
.ach span{color:var(--mut)}
.nums{display:flex;gap:34px;margin-bottom:18px}
.n{font-size:40px;font-weight:600;letter-spacing:-.035em;line-height:1;font-variant-numeric:tabular-nums}
.k{font-size:12.5px;color:var(--mut);margin-top:7px;letter-spacing:0}
.bar{display:flex;gap:3px;height:8px;border-radius:4px;overflow:hidden}
.bar i{display:block;min-width:4px}
.l0{background:var(--l0)}.l1{background:var(--l1)}.l2{background:var(--l2)}.lo{background:var(--lo)}
.leg{display:flex;flex-wrap:wrap;gap:6px 14px;margin-top:12px;font-size:12.5px}
.leg span{white-space:nowrap;display:inline-flex;align-items:center;gap:6px;letter-spacing:0}
.leg u{width:8px;height:8px;border-radius:50%;display:block}
.leg em{font-style:normal;color:var(--mut);font-variant-numeric:tabular-nums}
.oss li{display:flex;align-items:center;gap:11px;font-size:15px;font-weight:500;letter-spacing:-.012em;padding:7px 0}
.oss svg{width:20px;height:20px;fill:var(--fg);flex:none}
@media (max-width:760px){
  .card{grid-template-columns:1fr}
  .col+.col{border-left:0;border-top:1px solid var(--hair)}
  .ach li{white-space:normal}
}
</style>
</head>
<body>
<main class="card">
  <section class="col">
    <h2>Achievements</h2>
    <ul class="ach">
      <li><b>Founder</b><span>11Startups</span></li>
      <li><b>Top 1,000 semifinalist</b><span>AWS 10,000 AIdeas</span></li>
      <li><b>350+ npm downloads</b><span>codereportcard</span></li>
      <li><b>100+ active users</b><span>GrindSDE</span></li>
      <li><b>800+ LeetCode solved</b><span>rating ~1678</span></li>
    </ul>
  </section>
  <section class="col">
    <h2>GitHub</h2>
    <div class="nums">
      <div><div class="n">85</div><div class="k">repositories</div></div>
      <div><div class="n">14</div><div class="k">active in 90 days</div></div>
    </div>
    <div class="bar"><i class="l0" style="flex:42"></i><i class="l1" style="flex:26"></i><i class="l2" style="flex:11"></i><i class="lo" style="flex:21"></i></div>
    <div class="leg">
      <span><u class="l0"></u>TypeScript<em>42%</em></span>
      <span><u class="l1"></u>Python<em>26%</em></span>
      <span><u class="l2"></u>JavaScript<em>11%</em></span>
    </div>
  </section>
  <section class="col">
    <h2>Open source</h2>
    <ul class="oss">
      <li><svg viewBox="0 0 24 24" aria-hidden="true"><path d="M12.48 10.92v3.28h7.84c-.24 1.84-.853 3.187-1.787 4.133-1.147 1.147-2.933 2.4-6.053 2.4-4.827 0-8.6-3.893-8.6-8.72s3.773-8.72 8.6-8.72c2.6 0 4.507 1.027 5.907 2.347l2.307-2.307C18.747 1.44 16.133 0 12.48 0 5.867 0 .307 5.387.307 12s5.56 12 12.173 12c3.573 0 6.267-1.173 8.373-3.36 2.16-2.16 2.84-5.213 2.84-7.667 0-.76-.053-1.467-.173-2.053H12.48z"/></svg>Google</li>
      <li><svg viewBox="0 0 24 24" aria-hidden="true"><path d="M17.3041 3.541h-3.6718l6.696 16.918H24Zm-10.6082 0L0 20.459h3.7442l1.3693-3.5527h7.0052l1.3693 3.5528h3.7442L10.5363 3.5409Zm-.3712 10.2232 2.2914-5.9456 2.2914 5.9456Z"/></svg>Anthropic</li>
      <li><svg viewBox="0 0 24 24" aria-hidden="true"><path d="M20.702 2.29c-2.494-1.554-5.778-1.187-8.706.654C9.076 1.104 5.79.736 3.3 2.29c-3.941 2.463-4.42 8.806-1.07 14.167 2.47 3.954 6.333 6.269 9.77 6.226 3.439.043 7.301-2.273 9.771-6.226 3.347-5.361 2.872-11.704-1.069-14.167zM4.042 15.328a12.838 12.838 0 01-1.546-3.541 10.12 10.12 0 01-.336-3.338c.15-1.98.956-3.524 2.27-4.345 1.315-.822 3.052-.87 4.903-.137.281.113.556.24.825.382A15.11 15.11 0 007.5 7.54c-2.035 3.255-2.655 6.878-1.945 9.765a13.247 13.247 0 01-1.514-1.98zm17.465-3.541a12.866 12.866 0 01-1.547 3.54 13.25 13.25 0 01-1.513 1.984c.635-2.589.203-5.76-1.353-8.734a.39.39 0 00-.563-.153l-4.852 3.032a.397.397 0 00-.126.546l.712 1.139a.395.395 0 00.547.126l3.145-1.965c.101.306.203.606.28.916.296 1.086.41 2.214.335 3.337-.15 1.982-.956 3.525-2.27 4.347a4.437 4.437 0 01-2.25.65h-.101a4.432 4.432 0 01-2.25-.65c-1.314-.822-2.121-2.365-2.27-4.347-.074-1.123.039-2.251.335-3.337a13.212 13.212 0 014.05-6.482 10.148 10.148 0 012.849-1.765c1.845-.733 3.586-.685 4.9.137 1.316.822 2.122 2.365 2.271 4.345a10.146 10.146 0 01-.33 3.334z"/></svg>GoDaddy</li>
    </ul>
  </section>
</main>
</body>
</html>
