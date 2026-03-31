<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>NeuroCoin</title>
<link href="https://fonts.googleapis.com/css2?family=Syne:wght@400;600;700;800&family=DM+Sans:wght@300;400;500&display=swap" rel="stylesheet"/>
<style>
:root {
  --bg: #0a0a0f;
  --surface: #13131a;
  --card: #1a1a24;
  --border: #2a2a3a;
  --accent: #7c5cfc;
  --accent2: #00e5a0;
  --accent3: #ff6b6b;
  --gold: #ffd166;
  --text: #f0f0f8;
  --muted: #888899;
  --r: 14px;
}
*{box-sizing:border-box;margin:0;padding:0}
body{font-family:'DM Sans',sans-serif;background:var(--bg);color:var(--text);min-height:100vh;overflow-x:hidden}
h1,h2,h3,.brand{font-family:'Syne',sans-serif}

/* NAV */
#topbar{position:sticky;top:0;z-index:100;background:rgba(10,10,15,0.92);backdrop-filter:blur(12px);border-bottom:1px solid var(--border);padding:12px 20px;display:flex;align-items:center;justify-content:space-between}
.brand{font-size:1.3rem;font-weight:800;background:linear-gradient(135deg,var(--accent),var(--accent2));-webkit-background-clip:text;-webkit-text-fill-color:transparent}
#bal-display{font-size:.85rem;color:var(--accent2);font-weight:600}
#logout-btn{background:none;border:1px solid var(--border);color:var(--muted);padding:6px 14px;border-radius:20px;cursor:pointer;font-size:.8rem;transition:.2s}
#logout-btn:hover{border-color:var(--accent3);color:var(--accent3)}

/* PAGES */
.page{display:none;padding:20px;max-width:480px;margin:0 auto;animation:fadeUp .35s ease}
.page.active{display:block}
@keyframes fadeUp{from{opacity:0;transform:translateY(16px)}to{opacity:1;transform:none}}

/* CARDS */
.card{background:var(--card);border:1px solid var(--border);border-radius:var(--r);padding:20px;margin-bottom:16px}
.card-title{font-family:'Syne',sans-serif;font-size:1rem;font-weight:700;margin-bottom:14px;display:flex;align-items:center;gap:8px}

/* FORM */
input,select{width:100%;background:var(--surface);border:1px solid var(--border);border-radius:10px;color:var(--text);padding:12px 14px;font-size:.95rem;font-family:'DM Sans',sans-serif;outline:none;transition:.2s;margin-bottom:12px}
input:focus,select:focus{border-color:var(--accent)}
input::placeholder{color:var(--muted)}
label{font-size:.82rem;color:var(--muted);display:block;margin-bottom:4px}

/* BUTTONS */
.btn{width:100%;padding:13px;border:none;border-radius:10px;font-family:'Syne',sans-serif;font-weight:700;font-size:1rem;cursor:pointer;transition:.2s;letter-spacing:.3px}
.btn-primary{background:linear-gradient(135deg,var(--accent),#5a3de8);color:#fff}
.btn-primary:hover{transform:translateY(-1px);box-shadow:0 8px 24px rgba(124,92,252,.35)}
.btn-success{background:linear-gradient(135deg,var(--accent2),#00b87a);color:#000}
.btn-danger{background:linear-gradient(135deg,var(--accent3),#e04040);color:#fff}
.btn-outline{background:none;border:1px solid var(--border);color:var(--text)}
.btn-outline:hover{border-color:var(--accent);color:var(--accent)}
.btn-sm{width:auto;padding:7px 16px;font-size:.82rem;border-radius:8px}

/* BOTTOM NAV */
#bottom-nav{position:fixed;bottom:0;left:0;right:0;background:rgba(13,13,20,0.97);backdrop-filter:blur(12px);border-top:1px solid var(--border);display:flex;z-index:100}
.nav-item{flex:1;display:flex;
