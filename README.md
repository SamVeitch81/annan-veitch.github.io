<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Badger Banter — Sam</title>
  <style>
    :root{
      --bg:#0f1724; --card:#0b1220; --accent:#ffd166; --muted:#9aa8b6; --text:#eef6ff;
      --radius:12px; font-family: Inter, system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
    }
    *{box-sizing:border-box}
    html,body{height:100%}
    body{margin:0;background:linear-gradient(180deg,#061221 0%,#0f1724 100%);color:var(--text);-webkit-font-smoothing:antialiased}
    .wrap{max-width:980px;margin:28px auto;padding:20px}
    header{display:flex;align-items:center;justify-content:space-between;gap:12px;margin-bottom:18px}
    .logo{font-weight:800;letter-spacing:0.6px;font-size:1.05rem;color:var(--accent)}
    nav a{color:var(--muted);text-decoration:none;margin-left:14px;font-size:0.95rem}
    main{display:grid;grid-template-columns:1fr 380px;gap:20px}
    @media (max-width:920px){main{grid-template-columns:1fr}}
    .panel{background:linear-gradient(180deg,rgba(255,255,255,0.02),transparent);padding:18px;border-radius:12px;border:1px solid rgba(255,255,255,0.03)}
    .chat{display:flex;flex-direction:column;gap:12px;max-height:66vh;overflow:auto;padding-right:6px}
    .bubble{padding:12px 14px;border-radius:14px;max-width:78%;line-height:1.4}
    .left{align-self:flex-start;background:rgba(255,255,255,0.03);border:1px solid rgba(255,255,255,0.02)}
    .right{align-self:flex-end;background:linear-gradient(90deg,#1f8a70,#2ab7a9);color:#022;box-shadow:0 6px 18px rgba(0,0,0,0.35)}
    .meta{font-size:0.82rem;color:var(--muted);margin-bottom:6px}
    .badger-name{font-weight:700;color:var(--accent);margin-right:8px}
    .images{display:grid;grid-template-columns:repeat(3,1fr);gap:10px;margin-top:12px}
    .images img{width:100%;height:110px;object-fit:cover;border-radius:10px;cursor:pointer;border:2px solid rgba(255,255,255,0.03);transition:transform .18s ease, box-shadow .18s}
    .images img:focus, .images img:hover{transform:translateY(-6px);box-shadow:0 10px 30px rgba(0,0,0,0.5);outline:none}
    .caption{font-size:0.85rem;color:var(--muted);margin-top:8px}
    .aside .card{margin-bottom:14px}
    .small{font-size:0.9rem;color:var(--muted)}
    .cta{display:inline-block;padding:8px 12px;background:var(--accent);color:#022;border-radius:10px;font-weight:700;text-decoration:none}
    footer{margin-top:18px;color:var(--muted);font-size:0.85rem;text-align:center}
    /* lightbox */
    .lightbox{position:fixed;inset:0;display:none;align-items:center;justify-content:center;background:rgba(2,6,23,0.75);z-index:60}
    .lightbox.open{display:flex}
    .lightbox img{max-width:92%;max-height:86%;border-radius:10px;box-shadow:0 30px 80px rgba(2,6,23,0.9)}
    .close-btn{position:absolute;top:22px;right:22px;background:#222;padding:8px;border-radius:8px;border:1px solid rgba(255,255,255,0.04);color:var(--muted);cursor:pointer}
    .note{font-size:0.9rem;color:var(--muted)}
    /* little bounce */
    .badge {display:inline-block;padding:6px 10px;background
