# project-Dum-Biryani
Project Based on biryani as name mention
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width,initial-scale=1.0"/>
<title>Biryani Baadshah – Royal Chicken Biryani</title>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@700;900&family=Nunito:wght@400;600;700;800&display=swap" rel="stylesheet"/>
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css"/>
<style>
:root{
  --red:#E23744;--orange:#FF6B00;--yellow:#FFB800;
  --dark:#1C1C1C;--gray:#686B78;--light:#F2F2F2;
  --white:#fff;--green:#3AB757;--purple:#7C3AED;
  --card-shadow:0 10px 16px rgba(0,0,0,.1);--radius:30px;
}
*{margin:0;padding:0;box-sizing:border-box;}
html{scroll-behavior:smooth;}
body{font-family:'Nunito',sans-serif;background:#f4f4f4;color:var(--dark);overflow-x:hidden;}
::-webkit-scrollbar{width:5px;}::-webkit-scrollbar-thumb{background:var(--red);border-radius:3px;}

#offer-strip{background:linear-gradient(90deg,var(--red),#ff4500,var(--orange));color:#fff;padding:8px;text-align:center;font-size:.82rem;font-weight:700;}

nav{background:#fff;height:66px;display:flex;align-items:center;padding:0 4%;gap:14px;position:sticky;top:0;z-index:300;box-shadow:0 2px 10px rgba(0,0,0,.09);}
.brand{display:flex;align-items:center;gap:10px;text-decoration:none;flex-shrink:0;}
.brand-icon{width:40px;height:40px;background:linear-gradient(135deg,var(--orange),var(--red));border-radius:10px;display:flex;align-items:center;justify-content:center;font-size:1.3rem;}
.brand-text{font-family:'Playfair Display',serif;font-size:1.2rem;color:var(--dark);font-weight:900;}
.brand-text span{color:var(--red);}
.nav-search{flex:1;max-width:420px;display:flex;align-items:center;gap:8px;background:var(--light);border-radius:8px;padding:8px 14px;border:1.5px solid transparent;transition:border-color .2s;}
.nav-search:focus-within{border-color:var(--red);background:#fff;}
.nav-search input{border:none;outline:none;font-family:inherit;font-size:.88rem;width:100%;background:transparent;}
.nav-links{display:flex;gap:4px;list-style:none;margin-left:auto;}
.nav-links a{text-decoration:none;color:var(--gray);font-weight:700;font-size:.83rem;padding:6px 10px;border-radius:6px;transition:all .2s;white-space:nowrap;}
.nav-links a:hover{color:var(--red);background:#fff0f0;}
.nav-right{display:flex;align-items:center;gap:8px;flex-shrink:0;}
.nav-icon-btn{background:none;border:1.5px solid #eee;border-radius:8px;width:38px;height:38px;display:flex;align-items:center;justify-content:center;cursor:pointer;position:relative;transition:all .2s;color:var(--gray);}
.nav-icon-btn:hover{border-color:var(--red);color:var(--red);}
.nav-icon-btn .badge{position:absolute;top:-6px;right:-6px;background:var(--red);color:#fff;border-radius:50%;width:18px;height:18px;font-size:.65rem;display:flex;align-items:center;justify-content:center;font-weight:900;}
.cart-pill{display:flex;align-items:center;gap:7px;background:var(--red);color:#fff;border:none;border-radius:8px;padding:9px 16px;font-weight:800;font-size:.85rem;cursor:pointer;font-family:inherit;transition:background .2s;white-space:nowrap;}
.cart-pill:hover{background:#c82030;}
#cart-count{background:#fff;color:var(--red);border-radius:50%;width:19px;height:19px;font-size:.68rem;display:flex;align-items:center;justify-content:center;font-weight:900;}

.user-menu-wrap{position:relative;}
.user-avatar{width:36px;height:36px;border-radius:50%;background:linear-gradient(135deg,var(--orange),var(--red));color:#fff;font-weight:800;font-size:.9rem;display:flex;align-items:center;justify-content:center;cursor:pointer;border:2px solid #fff;box-shadow:0 2px 8px rgba(226,55,68,.3);}
.user-dropdown{position:absolute;top:46px;right:0;background:#fff;border-radius:12px;box-shadow:0 8px 30px rgba(0,0,0,.15);min-width:200px;padding:8px;z-index:400;display:none;animation:slideDown .2s ease;}
.user-dropdown.open{display:block;}
@keyframes slideDown{from{opacity:0;transform:translateY(-8px);}to{opacity:1;transform:translateY(0);}}
.ud-name{padding:10px 14px;border-bottom:1px solid #f0f0f0;font-weight:800;font-size:.9rem;color:var(--dark);}
.ud-email{font-size:.75rem;color:var(--gray);font-weight:600;}
.ud-item{display:flex;align-items:center;gap:10px;padding:10px 14px;border-radius:8px;cursor:pointer;color:var(--gray);font-weight:700;font-size:.85rem;transition:background .15s;}
.ud-item:hover{background:#fff0f0;color:var(--red);}
.ud-item i{width:16px;}
.ud-divider{height:1px;background:#f0f0f0;margin:4px 0;}
.hamburger{display:none;background:none;border:none;font-size:1.3rem;cursor:pointer;color:var(--dark);}

#hero{background:linear-gradient(135deg,#1C0A00 0%,#3B1F0A 55%,#5C2D0A 100%);padding:52px 5% 0;display:flex;align-items:flex-end;gap:40px;min-height:400px;position:relative;overflow:hidden;}
.hero-decor{position:absolute;border-radius:50%;filter:blur(80px);opacity:.18;}
.hero-decor-1{width:400px;height:400px;background:var(--orange);top:-80px;right:200px;}
.hero-decor-2{width:250px;height:250px;background:var(--yellow);bottom:0;left:5%;}
.hero-left{max-width:500px;z-index:2;padding-bottom:44px;}
.hero-badge{display:inline-flex;align-items:center;gap:6px;background:rgba(255,184,0,.15);border:1px solid var(--yellow);color:var(--yellow);padding:4px 13px;border-radius:50px;font-size:.75rem;font-weight:800;letter-spacing:1px;margin-bottom:16px;}
.hero-title{font-family:'Playfair Display',serif;font-size:clamp(1.9rem,4vw,3rem);color:#fff;line-height:1.12;margin-bottom:14px;}
.hero-title span{color:var(--yellow);}
.hero-sub{color:rgba(255,255,255,.68);font-size:.94rem;margin-bottom:24px;line-height:1.65;}
.hero-btns{display:flex;gap:12px;flex-wrap:wrap;}
.btn-hero{background:var(--red);color:#fff;border:none;border-radius:8px;padding:12px 26px;font-weight:800;font-size:.95rem;cursor:pointer;font-family:inherit;transition:transform .15s,box-shadow .15s;}
.btn-hero:hover{transform:translateY(-2px);box-shadow:0 8px 20px rgba(226,55,68,.4);}
.btn-outline{background:transparent;color:#fff;border:2px solid rgba(255,255,255,.4);border-radius:8px;padding:12px 26px;font-weight:700;font-size:.95rem;cursor:pointer;font-family:inherit;transition:all .2s;}
.btn-outline:hover{border-color:rgba(255,255,255,.8);background:rgba(255,255,255,.08);}
.hero-stats{display:flex;gap:24px;margin-top:28px;}
.stat-num{font-family:'Playfair Display',serif;font-size:1.6rem;color:var(--yellow);font-weight:900;}
.stat-label{font-size:.7rem;color:rgba(255,255,255,.5);font-weight:700;letter-spacing:.5px;}
.hero-right{z-index:2;flex-shrink:0;animation:float 4s ease-in-out infinite;}
@keyframes float{0%,100%{transform:translateY(0);}50%{transform:translateY(-14px);}}
.hero-img-wrap{width:clamp(220px,28vw,340px);height:clamp(220px,28vw,340px);border-radius:70%;overflow:hidden;border:4px solid rgba(255,184,0,.35);box-shadow:0 20px 60px rgba(0,0,0,.6),0 0 0 8px rgba(255,184,0,.1);}
.hero-img-wrap img{width:100%;height:100%;object-fit:cover;display:block;}

#rating-bar{background:#fff;padding:12px 5%;display:flex;align-items:center;gap:24px;border-bottom:1px solid #eee;flex-wrap:wrap;}
.rb-item{display:flex;align-items:center;gap:7px;font-size:.83rem;color:var(--gray);}
.rb-badge{background:#48c479;color:#fff;padding:3px 9px;border-radius:5px;font-size:.76rem;font-weight:800;}
.rb-open{background:#e8f5e9;color:#2e7d32;padding:3px 9px;border-radius:5px;font-size:.76rem;font-weight:800;}

.section{padding:44px 5%;}
.section-alt{background:#fff;}
.sec-head{margin-bottom:28px;}
.sec-label{font-size:.7rem;font-weight:800;color:var(--red);letter-spacing:2px;text-transform:uppercase;margin-bottom:6px;}
.sec-title{font-family:'Playfair Display',serif;font-size:clamp(1.5rem,3vw,2rem);color:var(--dark);}
.sec-title span{color:var(--red);}
.sec-sub{color:var(--gray);font-size:.88rem;margin-top:6px;}

.filter-row{display:flex;gap:8px;flex-wrap:wrap;margin-bottom:26px;}
.chip{background:#fff;border:1.5px solid #ddd;border-radius:50px;padding:7px 18px;font-size:.82rem;font-weight:700;cursor:pointer;transition:all .2s;font-family:inherit;color:var(--dark);}
.chip.active,.chip:hover{background:var(--red);border-color:var(--red);color:#fff;}

.menu-grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(268px,1fr));gap:20px;}
.menu-card{background:#fff;border-radius:var(--radius);overflow:hidden;box-shadow:var(--card-shadow);transition:transform .22s,box-shadow .22s;position:relative;}
.menu-card:hover{transform:translateY(-6px);box-shadow:0 14px 36px rgba(0,0,0,.14);}
.card-img-box{position:relative;height:195px;overflow:hidden;background:#f8e8d0;}
.card-img-box img{width:100%;height:100%;object-fit:cover;display:block;transition:transform .42s;}
.menu-card:hover .card-img-box img{transform:scale(1.07);}
.veg-dot{position:absolute;top:10px;left:10px;z-index:3;width:18px;height:18px;border:2px solid #2e7d32;border-radius:3px;background:#fff;display:flex;align-items:center;justify-content:center;}
.veg-dot::after{content:'';width:8px;height:8px;background:#2e7d32;border-radius:50%;display:block;}
.nonveg-dot{position:absolute;top:10px;left:10px;z-index:3;width:18px;height:18px;border:2px solid #c62828;border-radius:3px;background:#fff;display:flex;align-items:center;justify-content:center;}
.nonveg-dot::after{content:'';width:8px;height:8px;background:#c62828;border-radius:50%;display:block;}
.bestseller-tag{position:absolute;top:10px;right:44px;z-index:3;background:#f8a300;color:#fff;font-size:.66rem;font-weight:800;padding:3px 8px;border-radius:4px;}
.wish-btn{position:absolute;top:8px;right:8px;z-index:3;width:32px;height:32px;border-radius:50%;background:rgba(255,255,255,.92);border:none;cursor:pointer;display:flex;align-items:center;justify-content:center;font-size:1rem;transition:all .2s;box-shadow:0 2px 8px rgba(0,0,0,.12);}
.wish-btn:hover{transform:scale(1.15);}
.wish-btn.active{background:#fff0f3;color:var(--red);}
.wish-btn i{color:#ccc;transition:color .2s;}
.wish-btn.active i{color:var(--red);}
.card-body{padding:13px 15px 15px;}
.card-name{font-weight:800;font-size:.98rem;color:var(--dark);margin-bottom:4px;}
.card-desc{font-size:.76rem;color:var(--gray);margin-bottom:10px;line-height:1.5;display:-webkit-box;-webkit-line-clamp:1;-webkit-box-orient:vertical;overflow:hidden;}
.card-meta{display:flex;align-items:center;justify-content:space-between;}
.star-pill{background:#48c479;color:#fff;padding:2px 8px;border-radius:5px;font-size:.74rem;font-weight:800;display:flex;align-items:center;gap:3px;}
.card-count{font-size:.72rem;color:var(--gray);margin-left:4px;}
.card-price{font-weight:900;font-size:1.05rem;color:var(--dark);}
.card-footer{display:flex;align-items:center;justify-content:space-between;margin-top:11px;padding-top:11px;border-top:1px solid #f0f0f0;}
.add-btn{background:#fff;color:var(--red);border:1.5px solid var(--red);border-radius:8px;padding:7px 20px;font-weight:800;font-size:.83rem;cursor:pointer;font-family:inherit;transition:all .2s;}
.add-btn:hover{background:var(--red);color:#fff;}
.qty-ctrl{display:flex;align-items:center;border:1.5px solid var(--red);border-radius:8px;overflow:hidden;}
.qty-btn{width:32px;height:32px;background:#fff0f0;border:none;color:var(--red);font-weight:900;font-size:1rem;cursor:pointer;transition:background .15s;font-family:inherit;}
.qty-btn:hover{background:var(--red);color:#fff;}
.qty-num{min-width:32px;text-align:center;font-weight:800;color:var(--dark);font-size:.88rem;background:#fff;}

.rec-strip{display:grid;grid-template-columns:repeat(auto-fill,minmax(215px,1fr));gap:14px;}
.rec-card{background:#fff;border-radius:var(--radius);display:flex;align-items:center;gap:12px;padding:11px;box-shadow:var(--card-shadow);cursor:pointer;transition:transform .2s,box-shadow .2s;}
.rec-card:hover{transform:translateY(-3px);box-shadow:0 8px 20px rgba(0,0,0,.12);}
.rec-thumb{width:70px;height:70px;border-radius:10px;overflow:hidden;flex-shrink:0;background:#f8e8d0;}
.rec-thumb img{width:100%;height:100%;object-fit:cover;display:block;}
.rec-name{font-weight:800;font-size:.9rem;color:var(--dark);}
.rec-price{color:var(--red);font-weight:700;font-size:.85rem;margin-top:2px;}
.rec-tag{display:inline-block;background:#fff3f0;color:var(--red);font-size:.68rem;font-weight:800;padding:2px 7px;border-radius:4px;margin-top:4px;}

#offers{background:linear-gradient(135deg,#1C1C1C,#2d1a0a);}
.offer-grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(255px,1fr));gap:16px;}
.offer-card{background:rgba(255,255,255,.07);border:1px solid rgba(255,184,0,.2);border-radius:var(--radius);padding:22px;position:relative;overflow:hidden;transition:transform .2s,background .2s;}
.offer-card:hover{transform:translateY(-4px);background:rgba(255,255,255,.11);}
.offer-pill{background:var(--yellow);color:#1C1C1C;font-size:.7rem;font-weight:900;padding:3px 10px;border-radius:50px;display:inline-block;margin-bottom:10px;}
.offer-title{font-family:'Playfair Display',serif;color:#fff;font-size:1.15rem;margin-bottom:6px;}
.offer-desc{color:rgba(255,255,255,.58);font-size:.8rem;margin-bottom:12px;line-height:1.5;}
.offer-code{background:rgba(255,184,0,.12);border:1px dashed var(--yellow);color:var(--yellow);border-radius:6px;padding:5px 12px;font-weight:800;font-size:.8rem;display:inline-block;letter-spacing:1px;cursor:pointer;}
.offer-code:hover{background:rgba(255,184,0,.22);}
.offer-bg{position:absolute;right:12px;bottom:8px;font-size:3rem;opacity:.13;}

.gallery-grid{display:grid;grid-template-columns:repeat(4,1fr);grid-template-rows:190px 190px;gap:12px;}
.gal-item{border-radius:10px;overflow:hidden;position:relative;cursor:pointer;}
.gal-item img{width:100%;height:100%;object-fit:cover;display:block;transition:transform .38s;}
.gal-item:hover img{transform:scale(1.06);}
.gi-big{grid-column:span 2;grid-row:span 2;}
.gal-overlay{position:absolute;inset:0;background:rgba(0,0,0,0);display:flex;align-items:center;justify-content:center;transition:background .25s;}
.gal-item:hover .gal-overlay{background:rgba(0,0,0,.3);}
.gal-overlay i{color:#fff;font-size:1.5rem;opacity:0;transition:opacity .25s;}
.gal-item:hover .gal-overlay i{opacity:1;}

.reviews-grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(270px,1fr));gap:16px;}
.review-card{background:#fff;border-radius:var(--radius);padding:18px;box-shadow:var(--card-shadow);transition:transform .2s;}
.review-card:hover{transform:translateY(-4px);}
.rev-head{display:flex;align-items:center;gap:10px;margin-bottom:10px;}
.rev-avatar{width:40px;height:40px;border-radius:50%;display:flex;align-items:center;justify-content:center;color:#fff;font-weight:800;font-size:.95rem;flex-shrink:0;}
.rev-name{font-weight:800;font-size:.88rem;color:var(--dark);}
.rev-date{font-size:.72rem;color:var(--gray);}
.rev-stars{color:#f8a300;margin-bottom:7px;font-size:.85rem;}
.rev-text{font-size:.82rem;color:var(--gray);line-height:1.58;}

#order-status{background:#fff;display:none;padding:40px 5%;}
#order-status.show{display:block;}
.tracker-box{max-width:680px;margin:0 auto;background:#fff;border-radius:var(--radius);padding:30px;box-shadow:var(--card-shadow);border:1px solid #eee;}
.tracker-steps{display:flex;justify-content:space-between;position:relative;margin:24px 0;}
.tracker-steps::before{content:'';position:absolute;top:20px;left:0;right:0;height:3px;background:#eee;z-index:0;}
.t-step{display:flex;flex-direction:column;align-items:center;gap:7px;z-index:1;flex:1;}
.t-dot{width:40px;height:40px;border-radius:50%;background:#eee;border:3px solid #eee;display:flex;align-items:center;justify-content:center;font-size:1rem;transition:all .4s;}
.t-dot.done{background:var(--green);border-color:var(--green);}
.t-dot.active{background:#fff;border-color:var(--red);box-shadow:0 0 0 4px rgba(226,55,68,.18);}
.t-label{font-size:.7rem;font-weight:700;color:var(--gray);text-align:center;}
.t-label.done,.t-label.active{color:var(--red);}

#cart-overlay{position:fixed;inset:0;background:rgba(0,0,0,.4);z-index:500;opacity:0;pointer-events:none;transition:opacity .3s;}
#cart-overlay.open{opacity:1;pointer-events:all;}
#cart-sidebar{position:fixed;top:0;right:-440px;width:min(440px,100vw);height:100vh;background:#fff;z-index:501;box-shadow:-6px 0 30px rgba(0,0,0,.12);transition:right .32s cubic-bezier(.4,0,.2,1);display:flex;flex-direction:column;}
#cart-sidebar.open{right:0;}
.cart-head{padding:18px 22px;border-bottom:1px solid #eee;display:flex;align-items:center;justify-content:space-between;flex-shrink:0;}
.cart-head h2{font-family:'Playfair Display',serif;font-size:1.25rem;color:var(--dark);}
.close-btn{background:none;border:none;font-size:1.3rem;cursor:pointer;color:var(--gray);transition:color .2s;}
.close-btn:hover{color:var(--red);}
#cart-items{flex:1;overflow-y:auto;padding:14px 22px;}
.cart-empty{text-align:center;padding:60px 20px;color:var(--gray);}
.cart-empty i{font-size:3rem;margin-bottom:10px;display:block;color:#eee;}
.c-item{display:flex;align-items:center;gap:12px;padding:12px 0;border-bottom:1px solid #f5f5f5;}
.c-thumb{width:56px;height:56px;border-radius:10px;overflow:hidden;flex-shrink:0;background:#f8e8d0;}
.c-thumb img{width:100%;height:100%;object-fit:cover;display:block;}
.c-item-name{font-weight:700;font-size:.88rem;color:var(--dark);}
.c-item-price{color:var(--red);font-weight:700;font-size:.83rem;margin-top:2px;}
.c-item-ctrl{display:flex;align-items:center;border:1.5px solid var(--red);border-radius:7px;overflow:hidden;margin-top:6px;width:fit-content;}
.c-remove{background:none;border:none;color:#ccc;cursor:pointer;font-size:.9rem;margin-left:8px;transition:color .2s;}
.c-remove:hover{color:var(--red);}
.cart-foot{padding:14px 22px;border-top:1px solid #eee;flex-shrink:0;}
.sum-row{display:flex;justify-content:space-between;font-size:.84rem;margin-bottom:5px;color:var(--gray);}
.sum-row.total{font-weight:800;font-size:1rem;color:var(--dark);margin-top:8px;padding-top:8px;border-top:1px dashed #eee;}
.checkout-btn{width:100%;background:var(--red);color:#fff;border:none;border-radius:8px;padding:13px;font-weight:800;font-size:.92rem;cursor:pointer;margin-top:10px;font-family:inherit;transition:background .2s;}
.checkout-btn:hover{background:#c82030;}

/* ── AUTH MODAL ── */
#auth-modal{position:fixed;inset:0;background:rgba(0,0,0,.55);z-index:600;display:none;align-items:center;justify-content:center;padding:16px;}
#auth-modal.open{display:flex;}
.auth-box{background:#fff;border-radius:18px;width:min(440px,100%);padding:32px;box-shadow:0 20px 60px rgba(0,0,0,.22);}
.auth-logo{text-align:center;margin-bottom:18px;}
.auth-logo-icon{width:52px;height:52px;background:linear-gradient(135deg,var(--orange),var(--red));border-radius:14px;display:inline-flex;align-items:center;justify-content:center;font-size:1.6rem;margin-bottom:8px;}
.auth-box h2{font-family:'Playfair Display',serif;font-size:1.6rem;color:var(--dark);margin-bottom:4px;text-align:center;}
.auth-box > p{color:var(--gray);font-size:.86rem;margin-bottom:20px;text-align:center;}
.auth-tabs{display:flex;gap:0;margin-bottom:20px;background:#f4f4f4;border-radius:8px;padding:3px;}
.auth-tab{flex:1;text-align:center;padding:9px;border-radius:6px;cursor:pointer;font-weight:700;font-size:.85rem;color:var(--gray);transition:all .2s;}
.auth-tab.active{background:#fff;color:var(--red);box-shadow:0 2px 8px rgba(0,0,0,.08);}
.fg{margin-bottom:14px;}
.fg label{display:block;font-weight:700;font-size:.78rem;color:var(--gray);margin-bottom:5px;}
.fg input{width:100%;border:1.5px solid #eee;border-radius:8px;padding:11px 13px;font-family:inherit;font-size:.9rem;outline:none;transition:border-color .2s;}
.fg input:focus{border-color:var(--red);}
.auth-submit{width:100%;background:var(--red);color:#fff;border:none;border-radius:8px;padding:13px;font-weight:800;font-size:.95rem;cursor:pointer;font-family:inherit;margin-top:4px;transition:background .2s;}
.auth-submit:hover{background:#c82030;}
.auth-google{width:100%;background:#fff;color:var(--dark);border:1.5px solid #eee;border-radius:8px;padding:11px;font-weight:700;font-size:.88rem;cursor:pointer;font-family:inherit;display:flex;align-items:center;justify-content:center;gap:10px;margin-top:10px;transition:border-color .2s;}
.auth-google:hover{border-color:var(--red);}
.auth-divider{text-align:center;color:#ccc;font-size:.8rem;margin:12px 0;position:relative;}
.auth-divider::before,.auth-divider::after{content:'';position:absolute;top:50%;width:42%;height:1px;background:#eee;}
.auth-divider::before{left:0;}.auth-divider::after{right:0;}
.auth-err{color:#e53935;font-size:.8rem;margin-top:6px;background:#fff5f5;border:1px solid #fcc;border-radius:6px;padding:7px 10px;display:none;}
.auth-success{color:#2e7d32;font-size:.8rem;margin-top:6px;background:#f1f8e9;border:1px solid #c8e6c9;border-radius:6px;padding:7px 10px;display:none;}
.pwd-wrap{position:relative;}
.pwd-wrap input{padding-right:40px;}
.pwd-eye{position:absolute;right:12px;top:50%;transform:translateY(-50%);background:none;border:none;cursor:pointer;color:var(--gray);font-size:.9rem;}

#checkout-modal{position:fixed;inset:0;background:rgba(0,0,0,.5);z-index:600;display:none;align-items:center;justify-content:center;padding:16px;}
#checkout-modal.open{display:flex;}
.co-box{background:#fff;border-radius:18px;width:min(500px,100%);max-height:92vh;overflow-y:auto;padding:28px;box-shadow:0 20px 60px rgba(0,0,0,.22);}
.co-box h2{font-family:'Playfair Display',serif;color:var(--dark);margin-bottom:20px;font-size:1.45rem;}
.form-row{display:grid;grid-template-columns:1fr 1fr;gap:12px;}
.coupon-row{display:flex;gap:8px;}
.coupon-row input{flex:1;}
.coupon-btn{background:var(--red);color:#fff;border:none;border-radius:8px;padding:0 16px;font-weight:700;cursor:pointer;font-family:inherit;}
.co-summary{background:#fafafa;border-radius:10px;padding:14px;margin:12px 0;border:1px solid #eee;}
.place-btn{width:100%;background:var(--red);color:#fff;border:none;border-radius:8px;padding:14px;font-weight:800;font-size:1rem;cursor:pointer;font-family:inherit;transition:background .2s;margin-top:4px;}
.place-btn:hover{background:#c82030;}

#wishlist-panel{position:fixed;top:0;left:-440px;width:min(440px,100vw);height:100vh;background:#fff;z-index:501;box-shadow:6px 0 30px rgba(0,0,0,.12);transition:left .32s cubic-bezier(.4,0,.2,1);display:flex;flex-direction:column;}
#wishlist-panel.open{left:0;}
.wl-head{padding:18px 22px;border-bottom:1px solid #eee;display:flex;align-items:center;justify-content:space-between;flex-shrink:0;}
.wl-head h2{font-family:'Playfair Display',serif;font-size:1.25rem;color:var(--dark);}
#wl-items{flex:1;overflow-y:auto;padding:14px 22px;}
.wl-item{display:flex;align-items:center;gap:12px;padding:12px 0;border-bottom:1px solid #f5f5f5;}
.wl-thumb{width:56px;height:56px;border-radius:10px;overflow:hidden;flex-shrink:0;background:#f8e8d0;}
.wl-thumb img{width:100%;height:100%;object-fit:cover;}
.wl-name{font-weight:700;font-size:.88rem;color:var(--dark);}
.wl-price{color:var(--red);font-weight:700;font-size:.83rem;margin-top:2px;}
.wl-remove{background:none;border:none;color:#ccc;cursor:pointer;font-size:.95rem;margin-left:auto;transition:color .2s;flex-shrink:0;}
.wl-remove:hover{color:var(--red);}
.wl-add-cart{background:var(--red);color:#fff;border:none;border-radius:6px;padding:5px 12px;font-size:.78rem;font-weight:700;cursor:pointer;font-family:inherit;margin-top:5px;transition:background .2s;}
.wl-add-cart:hover{background:#c82030;}

#contact{background:var(--dark);}
.contact-wrap{display:grid;grid-template-columns:1fr 1fr;gap:48px;align-items:start;}
.c-info h3{font-family:'Playfair Display',serif;color:#fff;font-size:1.65rem;margin-bottom:14px;}
.c-info p{color:rgba(255,255,255,.58);margin-bottom:20px;line-height:1.65;font-size:.9rem;}
.c-item{display:flex;align-items:flex-start;gap:14px;margin-bottom:14px;color:rgba(255,255,255,.76);}
.c-icon{width:36px;height:36px;background:rgba(226,55,68,.15);border-radius:10px;display:flex;align-items:center;justify-content:center;color:var(--red);flex-shrink:0;margin-top:2px;}
.c-item span{font-size:.86rem;line-height:1.5;}
.socials{display:flex;gap:10px;margin-top:18px;}
.soc{width:36px;height:36px;border-radius:10px;border:1px solid rgba(255,255,255,.15);display:flex;align-items:center;justify-content:center;color:rgba(255,255,255,.6);text-decoration:none;transition:all .2s;}
.soc:hover{background:var(--red);border-color:var(--red);color:#fff;}
.c-form{background:rgba(255,255,255,.06);border:1px solid rgba(255,255,255,.1);border-radius:var(--radius);padding:24px;}
.c-form .fg input,.c-form .fg textarea{background:rgba(255,255,255,.08);border-color:rgba(255,255,255,.12);color:#fff;}
.c-form .fg input::placeholder,.c-form .fg textarea::placeholder{color:rgba(255,255,255,.28);}
.c-form .fg label{color:rgba(255,255,255,.62);}
.c-form .fg input:focus,.c-form .fg textarea:focus{border-color:var(--red);}
footer{background:#111;color:rgba(255,255,255,.48);text-align:center;padding:22px 5%;font-size:.8rem;}
footer span{color:var(--red);}

#toast{position:fixed;bottom:90px;left:50%;transform:translateX(-50%) translateY(12px);background:var(--dark);color:#fff;padding:10px 22px;border-radius:50px;font-weight:700;font-size:.84rem;z-index:700;opacity:0;transition:all .28s;pointer-events:none;white-space:nowrap;}
#toast.show{opacity:1;transform:translateX(-50%) translateY(0);}

#success-modal{position:fixed;inset:0;background:rgba(0,0,0,.55);z-index:700;display:none;align-items:center;justify-content:center;}
#success-modal.open{display:flex;}
.success-box{background:#fff;border-radius:18px;padding:40px 32px;text-align:center;max-width:400px;width:90%;}
.success-icon{font-size:3.5rem;margin-bottom:12px;display:block;}
.success-box h2{font-family:'Playfair Display',serif;color:var(--dark);margin-bottom:8px;}
.success-box p{color:var(--gray);font-size:.86rem;margin-bottom:20px;}
.success-actions{display:flex;gap:10px;justify-content:center;}

#wa-float{position:fixed;bottom:26px;right:26px;z-index:400;display:flex;flex-direction:column;align-items:flex-end;gap:9px;}
.wa-tip{background:#25D366;color:#fff;padding:7px 13px;border-radius:20px;font-size:.78rem;font-weight:700;white-space:nowrap;box-shadow:0 4px 14px rgba(37,211,102,.38);cursor:pointer;}
.wa-bubble{width:56px;height:56px;border-radius:50%;background:#25D366;display:flex;align-items:center;justify-content:center;font-size:1.75rem;color:#fff;box-shadow:0 6px 20px rgba(37,211,102,.48);cursor:pointer;text-decoration:none;animation:waBounce 3s ease-in-out infinite;}
@keyframes waBounce{0%,100%{transform:translateY(0);}50%{transform:translateY(-8px);}}

@media(max-width:900px){
  .hero-right{display:none;}
  .contact-wrap{grid-template-columns:1fr;}
  .gallery-grid{grid-template-columns:1fr 1fr;grid-template-rows:auto;}
  .gi-big{grid-column:span 2;height:210px;}
  .gal-item{height:155px;}
}
@media(max-width:680px){
  .nav-links{display:none;position:absolute;top:66px;left:0;right:0;background:#fff;flex-direction:column;padding:12px 5%;box-shadow:0 4px 12px rgba(0,0,0,.08);z-index:300;}
  .nav-links.open{display:flex;}
  .hamburger{display:block;}
  .form-row{grid-template-columns:1fr;}
  #wa-float{bottom:18px;right:18px;}
}
</style>
</head>
<body>

<div id="offer-strip">
  <marquee scrollamount="5">🎉 ROYAL20 – 20% off above ₹499 &nbsp;|&nbsp; 🛵 FIRSTFREE – Free delivery on first order &nbsp;|&nbsp; 🎁 WEEKEND50 – Flat ₹50 off weekends &nbsp;|&nbsp; 👑 FEAST21 – Buy 2 Biryanis, get Raita FREE &nbsp;|&nbsp; 📞 Order on WhatsApp: +91 95796 21583</marquee>
</div>

<nav>
  <a class="brand" href="#">
    <div class="brand-icon">🍛</div>
    <div class="brand-text">Biryani <span>Baadshah</span></div>
  </a>
  <div class="nav-search">
    <i class="fas fa-search" style="color:var(--gray)"></i>
    <input type="text" id="search-input" placeholder="Search biryani, kebabs, raita..."/>
  </div>
  <ul class="nav-links" id="nav-links">
    <li><a href="#hero">Home</a></li>
    <li><a href="#menu">Menu</a></li>
    <li><a href="#offers">Offers</a></li>
    <li><a href="#reviews">Reviews</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
  <div class="nav-right">
    <button class="nav-icon-btn" onclick="toggleWishlist()" title="Wishlist" id="wl-btn">
      <i class="fas fa-heart"></i>
      <span class="badge" id="wl-count" style="display:none">0</span>
    </button>
    <button class="cart-pill" onclick="toggleCart()">
      <i class="fas fa-shopping-bag"></i> Cart
      <span id="cart-count">0</span>
    </button>
    <button class="btn-hero" id="login-nav-btn" onclick="openAuth()" style="padding:9px 16px;font-size:.83rem">Login</button>
    <div class="user-menu-wrap" id="user-menu-wrap" style="display:none">
      <div class="user-avatar" id="user-avatar" onclick="toggleUserMenu()">U</div>
      <div class="user-dropdown" id="user-dropdown">
        <div class="ud-name" id="ud-name-block">
          <div id="ud-display-name">User</div>
          <div class="ud-email" id="ud-email"></div>
        </div>
        <div class="ud-item" onclick="toggleWishlist()"><i class="fas fa-heart"></i> My Wishlist</div>
        <div class="ud-divider"></div>
        <div class="ud-item" onclick="doLogout()" style="color:#e53935"><i class="fas fa-sign-out-alt"></i> Logout</div>
      </div>
    </div>
    <button class="hamburger" onclick="toggleNav()"><i class="fas fa-bars"></i></button>
  </div>
</nav>

<section id="hero">
  <div class="hero-decor hero-decor-1"></div>
  <div class="hero-decor hero-decor-2"></div>
  <div class="hero-left">
    <div class="hero-badge">⭐ &nbsp;#1 Rated Biryani in Pune</div>
    <h1 class="hero-title">The <span>Royal</span> Taste of Authentic Biryani</h1>
    <p class="hero-sub">Slow-cooked dum style with saffron, fresh herbs & tender chicken. Straight from the royal kitchens to your doorstep.</p>
    <div class="hero-btns">
      <button class="btn-hero" onclick="scrollToMenu()">🛵 Order Now</button>
      <button class="btn-outline" onclick="document.getElementById('gallery').scrollIntoView({behavior:'smooth'})">📸 Gallery</button>
    </div>
    <div class="hero-stats">
      <div><div class="stat-num">4.9★</div><div class="stat-label">RATING</div></div>
      <div><div class="stat-num">12K+</div><div class="stat-label">ORDERS</div></div>
      <div><div class="stat-num">25MIN</div><div class="stat-label">DELIVERY</div></div>
    </div>
  </div>
  <div class="hero-right">
    <div class="hero-img-wrap">
      <img src="https://tse2.mm.bing.net/th/id/OIP.hEWnvEk0B-FzyoSa0E2C7gHaE8?rs=1&pid=ImgDetMain&o=7&rm=3" alt="Royal Biryani"
           onerror="this.src='https://images.pexels.com/photos/9609843/pexels-photo-9609843.jpeg?auto=compress&cs=tinysrgb&w=500';this.onerror=null;"/>
    </div>
  </div>
</section>

<div id="rating-bar">
  <div class="rb-item"><span class="rb-badge">4.9 ★</span><strong>Excellent</strong></div>
  <div class="rb-item"><i class="fas fa-clock" style="color:var(--orange)"></i><span>25–30 min delivery</span></div>
  <div class="rb-item"><i class="fas fa-rupee-sign" style="color:var(--green)"></i><span>₹40 delivery · Free above ₹399</span></div>
  <div class="rb-item"><span class="rb-open">🟢 Open Now</span><span>11 AM – 11:30 PM</span></div>
  <div class="rb-item"><i class="fas fa-map-marker-alt" style="color:var(--red)"></i><span>Deccan Gymkhana, Pune</span></div>
</div>

<section class="section section-alt">
  <div class="sec-head">
    <div class="sec-label">Chef's Pick</div>
    <h2 class="sec-title">Recommended <span>for You</span></h2>
  </div>
  <div class="rec-strip" id="rec-strip"></div>
</section>

<section class="section" id="menu">
  <div class="sec-head">
    <div class="sec-label">Our Menu</div>
    <h2 class="sec-title">Explore <span>Royal Menu</span></h2>
    <p class="sec-sub">From Hyderabadi Dum to Kolkata-style — every plate a masterpiece</p>
  </div>
  <div class="filter-row">
    <button class="chip active" onclick="filterMenu(this,'all')">🍽 All</button>
    <button class="chip" onclick="filterMenu(this,'nonveg')">🍗 Non-Veg</button>
    <button class="chip" onclick="filterMenu(this,'veg')">🥗 Veg</button>
    <button class="chip" onclick="filterMenu(this,'popular')">🔥 Popular</button>
  </div>
  <div class="menu-grid" id="menu-grid"></div>
</section>

<section class="section" id="offers">
  <div class="sec-head">
    <div class="sec-label" style="color:var(--yellow)">Hot Deals</div>
    <h2 class="sec-title" style="color:#fff">Special <span style="color:var(--yellow)">Offers</span></h2>
  </div>
  <div class="offer-grid">
    <div class="offer-card"><div class="offer-pill">20% OFF</div><div class="offer-title">Royal Combo Deal</div><div class="offer-desc">Get 20% off on orders above ₹499. Perfect for family biryani nights!</div><div class="offer-code" onclick="copyCode('ROYAL20')">ROYAL20 📋</div><div class="offer-bg">👑</div></div>
    <div class="offer-card"><div class="offer-pill">FREE DELIVERY</div><div class="offer-title">First Order Free</div><div class="offer-desc">New customers get free delivery on first order. No minimum value!</div><div class="offer-code" onclick="copyCode('FIRSTFREE')">FIRSTFREE 📋</div><div class="offer-bg">🛵</div></div>
    <div class="offer-card"><div class="offer-pill">FLAT ₹50 OFF</div><div class="offer-title">Weekend Special</div><div class="offer-desc">Saturday & Sunday — flat ₹50 off on every order above ₹299.</div><div class="offer-code" onclick="copyCode('WEEKEND50')">WEEKEND50 📋</div><div class="offer-bg">🎉</div></div>
    <div class="offer-card"><div class="offer-pill">BUY 2 GET 1</div><div class="offer-title">Family Feast</div><div class="offer-desc">Order 2 biryanis and get 1 Raita absolutely free!</div><div class="offer-code" onclick="copyCode('FEAST21')">FEAST21 📋</div><div class="offer-bg">🍽</div></div>
  </div>
</section>

<section class="section section-alt" id="gallery">
  <div class="sec-head">
    <div class="sec-label">Food Gallery</div>
    <h2 class="sec-title">Our <span>Delicious</span> Creations</h2>
  </div>
  <div class="gallery-grid">
    <div class="gal-item gi-big">
      <img src="https://tse4.mm.bing.net/th/id/OIP.XgjqQaBz_t9wXstgAP5TGQHaEH?rs=1&pid=ImgDetMain&o=7&rm=3" alt="Biryani"/>
      <div class="gal-overlay"><i class="fas fa-expand-alt"></i></div>
    </div>
    <div class="gal-item">
      <img src="https://images.pexels.com/photos/9609843/pexels-photo-9609843.jpeg?auto=compress&cs=tinysrgb&w=500" alt="Spices"/>
      <div class="gal-overlay"><i class="fas fa-expand-alt"></i></div>
    </div>
    <div class="gal-item">
      <img src="https://images.pexels.com/photos/12737656/pexels-photo-12737656.jpeg?auto=compress&cs=tinysrgb&w=500" alt="Chicken"/>
      <div class="gal-overlay"><i class="fas fa-expand-alt"></i></div>
    </div>
    <div class="gal-item">
      <img src="https://images.pexels.com/photos/958545/pexels-photo-958545.jpeg?auto=compress&cs=tinysrgb&w=500" alt="Mutton"/>
      <div class="gal-overlay"><i class="fas fa-expand-alt"></i></div>
    </div>
    <div class="gal-item">
      <img src="https://images.pexels.com/photos/2474661/pexels-photo-2474661.jpeg?auto=compress&cs=tinysrgb&w=500" alt="Feast"/>
      <div class="gal-overlay"><i class="fas fa-expand-alt"></i></div>
    </div>
  </div>
</section>

<section id="order-status">
  <div class="sec-head" style="text-align:center">
    <div class="sec-label">Live Tracking</div>
    <h2 class="sec-title">Your Order <span>Status</span></h2>
  </div>
  <div class="tracker-box">
    <p style="text-align:center;color:var(--gray);font-size:.86rem">Order #<strong id="order-id">BB1234</strong> · Est. delivery: <strong>25–30 min</strong></p>
    <div class="tracker-steps" id="tracker-steps">
      <div class="t-step"><div class="t-dot done">✅</div><div class="t-label done">Placed</div></div>
      <div class="t-step"><div class="t-dot active">👨‍🍳</div><div class="t-label active">Preparing</div></div>
      <div class="t-step"><div class="t-dot">🛵</div><div class="t-label">On the Way</div></div>
      <div class="t-step"><div class="t-dot">🏠</div><div class="t-label">Delivered</div></div>
    </div>
    <p style="text-align:center;color:var(--gray);font-size:.82rem">👨‍🍳 Our chef is crafting your royal biryani with love!</p>
  </div>
</section>

<section class="section" id="reviews">
  <div class="sec-head">
    <div class="sec-label">Testimonials</div>
    <h2 class="sec-title">What <span>Customers</span> Say</h2>
  </div>
  <div class="reviews-grid" id="reviews-grid"></div>
</section>

<section class="section" id="contact">
  <div class="sec-head" style="text-align:center">
    <div class="sec-label" style="color:var(--yellow)">Get in Touch</div>
    <h2 class="sec-title" style="color:#fff">Contact <span style="color:var(--yellow)">Us</span></h2>
  </div>
  <div class="contact-wrap">
    <div class="c-info">
      <h3>Visit or Call Us 👑</h3>
      <p>Have questions about our menu, want to place a bulk order, or just want to say how amazing our biryani is? We're always here!</p>
      <div class="c-item"><div class="c-icon"><i class="fas fa-map-marker-alt"></i></div><span>12, Royal Palace Road, Deccan Gymkhana, Pune – 411004, Maharashtra</span></div>
      <div class="c-item"><div class="c-icon"><i class="fas fa-phone"></i></div><span>+91 95796 21583</span></div>
      <div class="c-item"><div class="c-icon"><i class="fas fa-envelope"></i></div><span>orders@biryanibaadshah.in</span></div>
      <div class="c-item"><div class="c-icon"><i class="fas fa-clock"></i></div><span>Open Daily: 11:00 AM – 11:30 PM</span></div>
      <div class="c-item"><div class="c-icon"><i class="fab fa-whatsapp"></i></div>
        <span>WhatsApp: <a href="https://wa.me/919579621583" target="_blank" style="color:#25D366;font-weight:800">+91 95796 21583</a></span>
      </div>
      <div class="socials">
        <a class="soc" href="#"><i class="fab fa-instagram"></i></a>
        <a class="soc" href="#"><i class="fab fa-facebook"></i></a>
        <a class="soc" href="#"><i class="fab fa-twitter"></i></a>
        <a class="soc" href="#"><i class="fab fa-youtube"></i></a>
        <a class="soc" href="https://wa.me/919579621583" target="_blank" style="background:#25D366;border-color:#25D366;color:#fff"><i class="fab fa-whatsapp"></i></a>
      </div>
    </div>
    <div class="c-form">
      <form id="contact-form" onsubmit="submitContact(event)">
        <div class="form-row">
          <div class="fg"><label>Your Name *</label><input type="text" id="cf-name" placeholder="Rahul Sharma" required/></div>
          <div class="fg"><label>Phone *</label><input type="tel" id="cf-phone" placeholder="+91 95796 21583" required/></div>
        </div>
        <div class="fg"><label>Email</label><input type="email" id="cf-email" placeholder="rahul@example.com"/></div>
        <div class="fg"><label>Subject *</label><input type="text" id="cf-subject" placeholder="Order enquiry / Feedback / Catering" required/></div>
        <div class="fg"><label>Message *</label><textarea id="cf-message" rows="4" placeholder="Tell us how we can help..." style="width:100%;border:1.5px solid rgba(255,255,255,.12);border-radius:8px;padding:10px 13px;font-family:inherit;font-size:.88rem;outline:none;background:rgba(255,255,255,.08);color:#fff;resize:none;" required></textarea></div>
        <button type="submit" class="btn-hero" style="width:100%"><i class="fas fa-paper-plane"></i> &nbsp;Send Message</button>
        <p id="contact-status" style="text-align:center;margin-top:10px;font-size:.82rem;color:var(--yellow);display:none"></p>
      </form>
    </div>
  </div>
</section>

<footer>
  <p>🍛 <span>Biryani Baadshah</span> © 2025 · Made with ❤️ in Pune · All rights reserved</p>
  <p style="margin-top:6px;font-size:.75rem">📍 Deccan Gymkhana, Pune &nbsp;|&nbsp; 📞 +91 95796 21583 &nbsp;|&nbsp; ⏰ 11 AM – 11:30 PM Daily</p>
</footer>

<div id="wa-float">
  <div class="wa-tip" id="wa-tip" onclick="openWA()">💬 Order on WhatsApp</div>
  <a class="wa-bubble" href="https://wa.me/919579621583?text=Hi%20Biryani%20Baadshah!%20I%27d%20like%20to%20place%20an%20order." target="_blank" rel="noopener">
    <i class="fab fa-whatsapp"></i>
  </a>
</div>

<!-- CART -->
<div id="cart-overlay" onclick="toggleCart()"></div>
<div id="cart-sidebar">
  <div class="cart-head">
    <h2>🛒 Your Cart</h2>
    <button class="close-btn" onclick="toggleCart()"><i class="fas fa-times"></i></button>
  </div>
  <div id="cart-items"></div>
  <div class="cart-foot" id="cart-foot" style="display:none">
    <div class="sum-row"><span>Subtotal</span><span id="s-sub">₹0</span></div>
    <div class="sum-row"><span>GST (5%)</span><span id="s-tax">₹0</span></div>
    <div class="sum-row"><span>Delivery</span><span id="s-del">₹40</span></div>
    <div class="sum-row total"><span>Total</span><span id="s-total">₹0</span></div>
    <button class="checkout-btn" onclick="openCheckout()">Proceed to Checkout →</button>
  </div>
</div>

<!-- WISHLIST -->
<div id="wishlist-panel">
  <div class="wl-head">
    <h2>❤️ My Wishlist</h2>
    <button class="close-btn" onclick="toggleWishlist()"><i class="fas fa-times"></i></button>
  </div>
  <div id="wl-items"><div class="cart-empty"><i class="fas fa-heart"></i><p>No saved items yet</p><p style="font-size:.8rem;margin-top:4px">Tap ❤ on any dish to save it!</p></div></div>
</div>

<!-- ── AUTH MODAL (no Firebase needed) ── -->
<div id="auth-modal">
  <div class="auth-box">
    <div class="auth-logo">
      <div class="auth-logo-icon">🍛</div>
      <h2>Biryani Baadshah</h2>
    </div>
    <p>Sign in to save your wishlist & order faster</p>
    <div class="auth-tabs">
      <div class="auth-tab active" id="tab-login" onclick="switchTab('login')">Login</div>
      <div class="auth-tab" id="tab-signup" onclick="switchTab('signup')">Sign Up</div>
    </div>

    <!-- LOGIN FORM -->
    <div id="login-form">
      <div class="fg">
        <label>Email Address</label>
        <input type="email" id="l-email" placeholder="you@example.com" onkeydown="if(event.key==='Enter')doLogin()"/>
      </div>
      <div class="fg">
        <label>Password</label>
        <div class="pwd-wrap">
          <input type="password" id="l-pass" placeholder="Your password" onkeydown="if(event.key==='Enter')doLogin()"/>
          <button class="pwd-eye" type="button" onclick="togglePwd('l-pass',this)"><i class="fas fa-eye"></i></button>
        </div>
      </div>
      <p class="auth-err" id="l-err"></p>
      <button class="auth-submit" onclick="doLogin()">Login →</button>
      <div class="auth-divider">or</div>
      <button class="auth-google" onclick="doGuestLogin()">👤 Continue as Guest</button>
    </div>

    <!-- SIGNUP FORM -->
    <div id="signup-form" style="display:none">
      <div class="fg">
        <label>Full Name</label>
        <input type="text" id="s-name" placeholder="Rahul Sharma"/>
      </div>
      <div class="fg">
        <label>Email Address</label>
        <input type="email" id="s-email" placeholder="you@example.com"/>
      </div>
      <div class="fg">
        <label>Password</label>
        <div class="pwd-wrap">
          <input type="password" id="s-pass" placeholder="Min 6 characters"/>
          <button class="pwd-eye" type="button" onclick="togglePwd('s-pass',this)"><i class="fas fa-eye"></i></button>
        </div>
      </div>
      <div class="fg">
        <label>Phone Number</label>
        <input type="tel" id="s-phone" placeholder="+91 98765 43210"/>
      </div>
      <p class="auth-err" id="s-err"></p>
      <p class="auth-success" id="s-ok"></p>
      <button class="auth-submit" onclick="doSignup()">Create Account →</button>
      <div class="auth-divider">or</div>
      <button class="auth-google" onclick="doGuestLogin()">👤 Continue as Guest</button>
    </div>

    <button style="width:100%;background:none;border:none;margin-top:14px;color:var(--gray);cursor:pointer;font-family:inherit;font-weight:700;font-size:.85rem" onclick="closeAuth()">✕ Close</button>
  </div>
</div>

<!-- CHECKOUT -->
<div id="checkout-modal">
  <div class="co-box">
    <h2>🏠 Place Your Order</h2>
    <div class="form-row">
      <div class="fg"><label>Full Name *</label><input type="text" id="o-name" placeholder="Rahul Sharma"/></div>
      <div class="fg"><label>Phone *</label><input type="tel" id="o-phone" placeholder="+91 95796 21583"/></div>
    </div>
    <div class="fg"><label>Delivery Address *</label><textarea id="o-address" rows="2" placeholder="Flat no., Society, Area, City..." style="width:100%;border:1.5px solid #eee;border-radius:8px;padding:10px 13px;font-family:inherit;font-size:.88rem;outline:none;resize:none;"></textarea></div>
    <div class="fg"><label>Payment Mode</label>
      <select id="o-payment" style="width:100%;border:1.5px solid #eee;border-radius:8px;padding:10px 13px;font-family:inherit;font-size:.88rem;outline:none;background:#fff;">
        <option>💵 Cash on Delivery</option>
        <option>📱 UPI (QR at door)</option>
        <option>💳 Card on Delivery</option>
      </select>
    </div>
    <div class="fg"><label>Coupon Code</label>
      <div class="coupon-row">
        <input type="text" id="coupon-input" placeholder="ROYAL20 / FIRSTFREE / WEEKEND50"/>
        <button type="button" class="coupon-btn" onclick="applyCoupon()">Apply</button>
      </div>
      <p id="coupon-msg" style="font-size:.78rem;margin-top:5px;display:none"></p>
    </div>
    <div class="co-summary" id="co-summary"></div>
    <button class="place-btn" onclick="placeOrder()">🛵 &nbsp;Confirm & Order</button>
    <button type="button" style="width:100%;background:none;border:none;margin-top:10px;color:var(--gray);cursor:pointer;font-family:inherit;font-weight:700;font-size:.86rem" onclick="closeCheckout()">← Back to Cart</button>
  </div>
</div>

<!-- SUCCESS -->
<div id="success-modal">
  <div class="success-box">
    <span class="success-icon">🎉</span>
    <h2>Order Placed!</h2>
    <p>Your royal biryani is being prepared! Est. delivery: <strong>25–30 minutes</strong>. We'll send a WhatsApp confirmation.</p>
    <div class="success-actions">
      <button class="btn-hero" onclick="closeSuccess()">📍 Track Order</button>
      <button class="btn-hero" style="background:var(--dark)" onclick="downloadInvoice()">🧾 Get Invoice</button>
    </div>
  </div>
</div>

<div id="toast"></div>

<script>
/* ═══════════════════════════════════════════
   LOCAL AUTH SYSTEM (No Firebase required)
   Uses localStorage to persist accounts
═══════════════════════════════════════════ */

const STORE_USERS = 'bb_users';
const STORE_SESSION = 'bb_session';
const WA = '919579621583';

let currentUser = null;

function getUsers() {
  try { return JSON.parse(localStorage.getItem(STORE_USERS) || '{}'); } catch { return {}; }
}
function saveUsers(u) { localStorage.setItem(STORE_USERS, JSON.stringify(u)); }
function getSession() {
  try { return JSON.parse(localStorage.getItem(STORE_SESSION) || 'null'); } catch { return null; }
}
function saveSession(u) { localStorage.setItem(STORE_SESSION, JSON.stringify(u)); }
function clearSession() { localStorage.removeItem(STORE_SESSION); }

function loginUser(user) {
  currentUser = user;
  saveSession(user);
  document.getElementById('login-nav-btn').style.display = 'none';
  document.getElementById('user-menu-wrap').style.display = 'block';
  const initial = (user.name || user.email)[0].toUpperCase();
  document.getElementById('user-avatar').textContent = initial;
  document.getElementById('ud-display-name').textContent = user.name || 'User';
  document.getElementById('ud-email').textContent = user.email || '';
  if (user.name) document.getElementById('o-name').value = user.name;
  if (user.phone) document.getElementById('o-phone').value = user.phone;
  loadWishlist();
  renderMenu(getCurrentItems());
}

function logoutUser() {
  currentUser = null;
  clearSession();
  document.getElementById('login-nav-btn').style.display = 'flex';
  document.getElementById('user-menu-wrap').style.display = 'none';
  wishlist = {};
  updateWlBadge();
  renderMenu(getCurrentItems());
}

// Restore session on load
(function restoreSession() {
  const s = getSession();
  if (s) { setTimeout(() => loginUser(s), 100); }
})();

window.openAuth = () => document.getElementById('auth-modal').classList.add('open');
window.closeAuth = () => document.getElementById('auth-modal').classList.remove('open');

window.switchTab = (tab) => {
  document.getElementById('login-form').style.display  = tab === 'login'  ? 'block' : 'none';
  document.getElementById('signup-form').style.display = tab === 'signup' ? 'block' : 'none';
  document.getElementById('tab-login').classList.toggle('active', tab === 'login');
  document.getElementById('tab-signup').classList.toggle('active', tab === 'signup');
  document.getElementById('l-err').style.display = 'none';
  document.getElementById('s-err').style.display = 'none';
  document.getElementById('s-ok').style.display  = 'none';
};

window.togglePwd = (id, btn) => {
  const inp = document.getElementById(id);
  const show = inp.type === 'password';
  inp.type = show ? 'text' : 'password';
  btn.innerHTML = `<i class="fas fa-eye${show ? '-slash' : ''}"></i>`;
};

window.doLogin = () => {
  const email = document.getElementById('l-email').value.trim().toLowerCase();
  const pass  = document.getElementById('l-pass').value;
  const err   = document.getElementById('l-err');
  err.style.display = 'none';

  if (!email || !pass) {
    err.textContent = 'Please enter email and password.'; err.style.display = 'block'; return;
  }
  const users = getUsers();
  const user = users[email];
  if (!user) {
    err.textContent = 'No account found with this email. Please sign up!'; err.style.display = 'block'; return;
  }
  if (user.pass !== btoa(pass)) {
    err.textContent = 'Incorrect password. Please try again.'; err.style.display = 'block'; return;
  }
  closeAuth();
  loginUser(user);
  showToast('✅ Welcome back, ' + (user.name || 'User') + '!');
};

window.doSignup = () => {
  const name  = document.getElementById('s-name').value.trim();
  const email = document.getElementById('s-email').value.trim().toLowerCase();
  const pass  = document.getElementById('s-pass').value;
  const phone = document.getElementById('s-phone').value.trim();
  const err   = document.getElementById('s-err');
  const ok    = document.getElementById('s-ok');
  err.style.display = 'none'; ok.style.display = 'none';

  if (!name)  { err.textContent = 'Please enter your full name.'; err.style.display = 'block'; return; }
  if (!email) { err.textContent = 'Please enter your email.'; err.style.display = 'block'; return; }
  if (!/^[^@]+@[^@]+\.[^@]+$/.test(email)) { err.textContent = 'Please enter a valid email address.'; err.style.display = 'block'; return; }
  if (pass.length < 6) { err.textContent = 'Password must be at least 6 characters.'; err.style.display = 'block'; return; }

  const users = getUsers();
  if (users[email]) { err.textContent = 'An account with this email already exists. Please login!'; err.style.display = 'block'; return; }

  const newUser = { name, email, phone, pass: btoa(pass), createdAt: new Date().toISOString() };
  users[email] = newUser;
  saveUsers(users);

  ok.textContent = '✅ Account created successfully! Logging you in...';
  ok.style.display = 'block';

  setTimeout(() => {
    closeAuth();
    loginUser(newUser);
    showToast('🎉 Welcome to Biryani Baadshah, ' + name + '!');
  }, 1200);
};

window.doGuestLogin = () => {
  const guestUser = { name: 'Guest', email: 'guest@biryanibaadshah.in', phone: '', pass: '' };
  closeAuth();
  loginUser(guestUser);
  showToast('👋 Continuing as Guest!');
};

window.doLogout = () => {
  logoutUser();
  toggleUserMenu(true);
  showToast('👋 Logged out. See you soon!');
};

window.toggleUserMenu = (forceClose) => {
  const d = document.getElementById('user-dropdown');
  if (forceClose) { d.classList.remove('open'); return; }
  d.classList.toggle('open');
};
document.addEventListener('click', e => {
  if (!e.target.closest('.user-menu-wrap')) document.getElementById('user-dropdown')?.classList.remove('open');
});

/* ═══════════════════════════════════════════
   DATA
═══════════════════════════════════════════ */
const menuData = [
  {id:1,name:"Hyderabadi Dum Biryani",desc:"Slow-cooked dum style with saffron, caramelized onions & whole spices.",price:299,tag:"popular",rating:4.9,count:2312,type:"nonveg",
   img:"https://th.bing.com/th/id/OIP.hYAWojbrro3xW62L1cH6awHaE8?o=7&rs=1&pid=ImgDetMain"},
  {id:2,name:"Kolkata Chicken Biryani",desc:"Delicately spiced with potato & egg — the iconic Nawabi recipe.",price:279,tag:"",rating:4.8,count:1876,type:"nonveg",
   img:"https://images.pexels.com/photos/9609843/pexels-photo-9609843.jpeg?auto=compress&cs=tinysrgb&w=500"},
  {id:3,name:"Lucknowi Shahi Biryani",desc:"Subtly perfumed with kewra & rose water. A royal Awadhi delicacy.",price:319,tag:"",rating:4.7,count:1345,type:"nonveg",
   img:"https://images.pexels.com/photos/12737656/pexels-photo-12737656.jpeg?auto=compress&cs=tinysrgb&w=500"},
  {id:4,name:"Veg Paneer Biryani",desc:"Charred paneer cubes layered with mint, fried onions & aged basmati.",price:229,tag:"",rating:4.6,count:987,type:"veg",
   img:"https://images.pexels.com/photos/958545/pexels-photo-958545.jpeg?auto=compress&cs=tinysrgb&w=500"},
  {id:5,name:"Chicken 65 Biryani",desc:"Crispy Chicken 65 tossed into spicy biryani — a South Indian classic!",price:339,tag:"popular",rating:4.9,count:2100,type:"nonveg",
   img:"https://images.pexels.com/photos/2474661/pexels-photo-2474661.jpeg?auto=compress&cs=tinysrgb&w=500"},
  {id:6,name:"Veg Mushroom Biryani",desc:"Earthy button mushrooms cooked with fragrant biryani spices.",price:219,tag:"",rating:4.5,count:654,type:"veg",
   img:"https://images.pexels.com/photos/1640777/pexels-photo-1640777.jpeg?auto=compress&cs=tinysrgb&w=500"},
  {id:7,name:"Mutton Dum Biryani",desc:"Tender mutton slow-cooked for 3 hours in a sealed pot.",price:379,tag:"popular",rating:4.9,count:3210,type:"nonveg",
   img:"https://images.pexels.com/photos/5410400/pexels-photo-5410400.jpeg?auto=compress&cs=tinysrgb&w=500"},
  {id:8,name:"Egg Biryani",desc:"Fluffy basmati with perfectly marinated eggs and zesty masala.",price:199,tag:"",rating:4.4,count:543,type:"nonveg",
   img:"https://images.pexels.com/photos/3662132/pexels-photo-3662132.jpeg?auto=compress&cs=tinysrgb&w=500"},
  {id:9,name:"Soya Chunk Biryani",desc:"Protein-rich soya chunks with biryani spices — veg favourite.",price:199,tag:"",rating:4.3,count:432,type:"veg",
   img:"https://images.pexels.com/photos/5410400/pexels-photo-5410400.jpeg?auto=compress&cs=tinysrgb&w=500"},
];

// FIXED: Royal Chicken Biryani now uses a working Pexels image
const recData = [
  {name:"Royal Chicken Biryani",price:"₹299",tag:"#1 Bestseller",
   img:"https://th.bing.com/th/id/OIP.hB3HqZpq-n0VF-jUqjHSWgHaE8?o=7&rs=1&pid=ImgDetMain"},
  {name:"Mutton Dum Biryani",price:"₹379",tag:"Chef's Pick",
   img:"https://images.pexels.com/photos/5410400/pexels-photo-5410400.jpeg?auto=compress&cs=tinysrgb&w=200"},
  {name:"Chicken 65 Special",price:"₹339",tag:"🌶 Spicy",
   img:"https://images.pexels.com/photos/2474661/pexels-photo-2474661.jpeg?auto=compress&cs=tinysrgb&w=200"},
  {name:"Paneer Biryani",price:"₹229",tag:"🥗 Veg",
   img:"https://images.pexels.com/photos/958545/pexels-photo-958545.jpeg?auto=compress&cs=tinysrgb&w=200"},
];

const reviewsData = [
  {name:"Priya Nair",date:"April 2025",stars:5,text:"Absolutely mind-blowing! The saffron aroma hits the moment they open the box. Best biryani in Pune!",color:"#E23744"},
  {name:"Rahul Mehta",date:"March 2025",stars:5,text:"Mutton Biryani was fall-off-the-bone tender. Delivery super fast. Ordering again this weekend!",color:"#FF6B00"},
  {name:"Sneha Patil",date:"April 2025",stars:4,text:"Veg Paneer Biryani was amazing — didn't expect vegetarian biryani to taste this rich!",color:"#3AB757"},
  {name:"Arjun Singh",date:"May 2025",stars:5,text:"Chicken 65 Biryani is a game changer. Crispy chicken inside biryani = pure genius!",color:"#7C3AED"},
  {name:"Meera Krishnan",date:"April 2025",stars:5,text:"WhatsApp ordering was so smooth! Team helpful and food arrived piping hot. Loved it!",color:"#0288D1"},
  {name:"Rohan Desai",date:"March 2025",stars:4,text:"Great value. ROYAL20 coupon saved a lot. Quality is consistently high every single time.",color:"#F57C00"},
];

/* ═══════════════════════════════════════════
   STATE
═══════════════════════════════════════════ */
let cart = {}, appliedDiscount = 0, wishlist = {}, lastOrder = null;
Object.defineProperty(window,'_cartRef',{get:()=>cart});
Object.defineProperty(window,'_discountRef',{get:()=>appliedDiscount});
const DELIVERY = 40, TAX = 0.05;
const COUPONS = {ROYAL20:{t:'pct',v:20},FIRSTFREE:{t:'flat',v:40},WEEKEND50:{t:'flat',v:50},FEAST21:{t:'flat',v:30}};

/* ═══════════════════════════════════════════
   WISHLIST (localStorage based)
═══════════════════════════════════════════ */
function loadWishlist() {
  if (!currentUser) return;
  try {
    const key = 'bb_wl_' + (currentUser.email || 'guest');
    wishlist = JSON.parse(localStorage.getItem(key) || '{}');
  } catch { wishlist = {}; }
  updateWlBadge();
  renderWishlist();
}

function saveWishlist() {
  if (!currentUser) return;
  const key = 'bb_wl_' + (currentUser.email || 'guest');
  localStorage.setItem(key, JSON.stringify(wishlist));
}

window.toggleWish = (itemId) => {
  if (!currentUser) { openAuth(); showToast('Please login to save to wishlist!'); return; }
  const item = menuData.find(i => i.id === itemId);
  if (wishlist[itemId]) {
    delete wishlist[itemId];
    showToast('💔 Removed from wishlist');
  } else {
    wishlist[itemId] = item;
    showToast('❤️ Saved to wishlist!');
  }
  saveWishlist();
  updateWlBadge();
  renderMenu(getCurrentItems());
  renderWishlist();
};

function updateWlBadge() {
  const count = Object.keys(wishlist).length;
  const badge = document.getElementById('wl-count');
  badge.textContent = count;
  badge.style.display = count > 0 ? 'flex' : 'none';
}

function renderWishlist() {
  const el = document.getElementById('wl-items');
  const items = Object.values(wishlist);
  if (!items.length) {
    el.innerHTML = '<div class="cart-empty"><i class="fas fa-heart" style="color:#eee"></i><p style="font-weight:700;margin-bottom:4px">No saved items</p><p style="font-size:.8rem">Tap ❤ on any dish to save!</p></div>';
    return;
  }
  el.innerHTML = items.map(i => `
    <div class="wl-item">
      <div class="wl-thumb"><img src="${i.img}" alt="${i.name}" onerror="this.style.background='#f8e8d0'"/></div>
      <div style="flex:1">
        <div class="wl-name">${i.name}</div>
        <div class="wl-price">₹${i.price}</div>
        <button class="wl-add-cart" onclick="addToCart(${i.id});toggleWishlist()">+ Add to Cart</button>
      </div>
      <button class="wl-remove" onclick="toggleWish(${i.id})"><i class="fas fa-trash-alt"></i></button>
    </div>`).join('');
}

window.toggleWishlist = () => {
  document.getElementById('wishlist-panel').classList.toggle('open');
  renderWishlist();
};

/* ═══════════════════════════════════════════
   CART
═══════════════════════════════════════════ */
window.addToCart = (id) => {
  const item = menuData.find(i => i.id === id);
  if (!cart[id]) cart[id] = {...item, qty:0};
  cart[id].qty++;
  updateCartUI(); renderMenu(getCurrentItems());
  showToast('✅ ' + item.name + ' added!');
};
window.changeQty = (id, d) => {
  if (!cart[id]) return;
  cart[id].qty += d;
  if (cart[id].qty <= 0) delete cart[id];
  updateCartUI(); renderMenu(getCurrentItems());
};
window.removeFromCart = (id) => { delete cart[id]; updateCartUI(); renderMenu(getCurrentItems()); };

function getTotals() {
  const sub  = Object.values(cart).reduce((a,i) => a + i.price*i.qty, 0);
  const tax  = Math.round(sub * TAX);
  const total = sub + tax + DELIVERY - appliedDiscount;
  return {sub, tax, total};
}

function updateCartUI() {
  const items = Object.values(cart);
  const qty = items.reduce((a,i) => a+i.qty, 0);
  document.getElementById('cart-count').textContent = qty;
  const ci = document.getElementById('cart-items'), cf = document.getElementById('cart-foot');
  if (!items.length) {
    ci.innerHTML = '<div class="cart-empty"><i class="fas fa-shopping-bag"></i><p style="font-weight:700;margin-bottom:4px">Cart is empty</p><p style="font-size:.82rem">Add some royal biryani!</p></div>';
    cf.style.display = 'none'; return;
  }
  ci.innerHTML = items.map(i => `
    <div class="c-item">
      <div class="c-thumb"><img src="${i.img}" alt="${i.name}" onerror="this.style.background='#f8e8d0'"/></div>
      <div style="flex:1">
        <div class="c-item-name">${i.name}</div>
        <div class="c-item-price">₹${i.price} × ${i.qty} = <strong>₹${i.price*i.qty}</strong></div>
        <div style="display:flex;align-items:center;gap:8px;margin-top:6px">
          <div class="c-item-ctrl">
            <button class="qty-btn" onclick="changeQty(${i.id},-1)">−</button>
            <span class="qty-num">${i.qty}</span>
            <button class="qty-btn" onclick="changeQty(${i.id},1)">+</button>
          </div>
          <button class="c-remove" onclick="removeFromCart(${i.id})"><i class="fas fa-trash-alt"></i></button>
        </div>
      </div>
    </div>`).join('');
  const {sub,tax,total} = getTotals();
  document.getElementById('s-sub').textContent = '₹' + sub;
  document.getElementById('s-tax').textContent = '₹' + tax;
  document.getElementById('s-total').textContent = '₹' + total;
  cf.style.display = 'block';
  updateCoSummary();
}

function updateCoSummary() {
  const el = document.getElementById('co-summary'); if(!el) return;
  const items = Object.values(cart);
  const {sub,tax,total} = getTotals();
  el.innerHTML = `
    ${items.map(i=>`<div class="sum-row"><span>${i.name} ×${i.qty}</span><span>₹${i.price*i.qty}</span></div>`).join('')}
    <hr style="border:none;border-top:1px dashed #eee;margin:8px 0"/>
    <div class="sum-row"><span>Subtotal</span><span>₹${sub}</span></div>
    <div class="sum-row"><span>GST (5%)</span><span>₹${tax}</span></div>
    <div class="sum-row"><span>Delivery</span><span>₹${DELIVERY}</span></div>
    ${appliedDiscount?`<div class="sum-row" style="color:#3AB757"><span>Discount</span><span>−₹${appliedDiscount}</span></div>`:''}
    <div class="sum-row total"><span>Total</span><span>₹${total}</span></div>`;
}

/* ═══════════════════════════════════════════
   FILTER / SEARCH / RENDER
═══════════════════════════════════════════ */
let curFilter = 'all';
function getCurrentItems() {
  let items = menuData;
  const q = document.getElementById('search-input').value.toLowerCase();
  if (q) items = items.filter(i => i.name.toLowerCase().includes(q) || i.desc.toLowerCase().includes(q));
  if (curFilter==='veg')     items = items.filter(i => i.type==='veg');
  else if (curFilter==='nonveg')  items = items.filter(i => i.type==='nonveg');
  else if (curFilter==='popular') items = items.filter(i => i.tag==='popular');
  return items;
}
window.filterMenu = (btn, type) => {
  document.querySelectorAll('.chip').forEach(b => b.classList.remove('active'));
  btn.classList.add('active'); curFilter = type; renderMenu(getCurrentItems());
};
document.getElementById('search-input').addEventListener('input', () => {
  renderMenu(getCurrentItems());
  document.getElementById('menu').scrollIntoView({behavior:'smooth'});
});

function renderMenu(items) {
  const g = document.getElementById('menu-grid');
  if (!items.length) { g.innerHTML = '<p style="grid-column:1/-1;text-align:center;color:var(--gray);padding:48px">No items found 🔍</p>'; return; }
  g.innerHTML = items.map(item => {
    const qty = cart[item.id]?.qty || 0;
    const isVeg = item.type === 'veg';
    const isWL = !!wishlist[item.id];
    return `
    <div class="menu-card">
      <div class="card-img-box">
        <img src="${item.img}" alt="${item.name}" loading="lazy"
             onerror="this.onerror=null;this.src='https://images.pexels.com/photos/7426674/pexels-photo-7426674.jpeg?auto=compress&cs=tinysrgb&w=500'"/>
        <div class="${isVeg?'veg-dot':'nonveg-dot'}"></div>
        ${item.tag==='popular'?'<div class="bestseller-tag">⭐ Bestseller</div>':''}
        <button class="wish-btn ${isWL?'active':''}" onclick="toggleWish(${item.id})" title="${isWL?'Remove from wishlist':'Add to wishlist'}">
          <i class="${isWL?'fas':'far'} fa-heart" style="color:${isWL?'var(--red)':'#ccc'}"></i>
        </button>
      </div>
      <div class="card-body">
        <div class="card-name">${item.name}</div>
        <div class="card-desc">${item.desc}</div>
        <div class="card-meta">
          <div style="display:flex;align-items:center">
            <span class="star-pill">★ ${item.rating}</span>
            <span class="card-count">(${item.count.toLocaleString()})</span>
          </div>
          <div class="card-price">₹${item.price}</div>
        </div>
        <div class="card-footer">
          <span style="font-size:.76rem;color:var(--gray)">🕐 25–30 min</span>
          ${qty===0
            ?`<button class="add-btn" onclick="addToCart(${item.id})">+ ADD</button>`
            :`<div class="qty-ctrl">
                <button class="qty-btn" onclick="changeQty(${item.id},-1)">−</button>
                <span class="qty-num">${qty}</span>
                <button class="qty-btn" onclick="changeQty(${item.id},1)">+</button>
              </div>`}
        </div>
      </div>
    </div>`;
  }).join('');
}

function renderRecommended() {
  document.getElementById('rec-strip').innerHTML = recData.map(r => `
    <div class="rec-card" onclick="scrollToMenu()">
      <div class="rec-thumb">
        <img src="${r.img}" alt="${r.name}" loading="lazy"
             onerror="this.onerror=null;this.style.background='#f8e8d0';this.src='https://images.pexels.com/photos/7426674/pexels-photo-7426674.jpeg?auto=compress&cs=tinysrgb&w=200'"/>
      </div>
      <div>
        <div class="rec-name">${r.name}</div>
        <div class="rec-price">${r.price}</div>
        <span class="rec-tag">${r.tag}</span>
      </div>
    </div>`).join('');
}

function renderReviews() {
  document.getElementById('reviews-grid').innerHTML = reviewsData.map(r => `
    <div class="review-card">
      <div class="rev-head">
        <div class="rev-avatar" style="background:${r.color}">${r.name[0]}</div>
        <div><div class="rev-name">${r.name}</div><div class="rev-date">${r.date}</div></div>
      </div>
      <div class="rev-stars">${'★'.repeat(r.stars)}${'☆'.repeat(5-r.stars)}</div>
      <div class="rev-text">"${r.text}"</div>
    </div>`).join('');
}

/* ═══════════════════════════════════════════
   UI TOGGLES
═══════════════════════════════════════════ */
window.toggleCart = () => {
  document.getElementById('cart-sidebar').classList.toggle('open');
  document.getElementById('cart-overlay').classList.toggle('open');
};
window.openCheckout = () => {
  if (!Object.keys(cart).length) { showToast('Your cart is empty!'); return; }
  if (!currentUser) { openAuth(); showToast('Please login to checkout!'); return; }
  toggleCart(); updateCoSummary();
  document.getElementById('checkout-modal').classList.add('open');
};
window.closeCheckout = () => document.getElementById('checkout-modal').classList.remove('open');
window.toggleNav = () => document.getElementById('nav-links').classList.toggle('open');
window.scrollToMenu = () => document.getElementById('menu').scrollIntoView({behavior:'smooth'});

/* ═══════════════════════════════════════════
   COUPON
═══════════════════════════════════════════ */
window.applyCoupon = () => {
  const code = document.getElementById('coupon-input').value.trim().toUpperCase();
  const msg  = document.getElementById('coupon-msg');
  if (COUPONS[code]) {
    const c = COUPONS[code];
    const sub = Object.values(cart).reduce((a,i) => a+i.price*i.qty, 0);
    appliedDiscount = c.t==='pct' ? Math.round(sub*c.v/100) : c.v;
    msg.style.display = 'block'; msg.style.color = '#3AB757';
    msg.textContent = '✅ Coupon applied! You saved ₹' + appliedDiscount;
    updateCartUI();
  } else {
    msg.style.display = 'block'; msg.style.color = '#e53935';
    msg.textContent = '❌ Invalid coupon. Try ROYAL20 / FIRSTFREE / WEEKEND50';
    appliedDiscount = 0; updateCartUI();
  }
};

/* ═══════════════════════════════════════════
   PLACE ORDER
═══════════════════════════════════════════ */
window.placeOrder = () => {
  const name    = document.getElementById('o-name').value.trim();
  const phone   = document.getElementById('o-phone').value.trim();
  const address = document.getElementById('o-address').value.trim();
  const payment = document.getElementById('o-payment').value;
  if (!name || !phone || !address) { showToast('Please fill all required fields!'); return; }

  const orderId = 'BB' + Math.floor(1000 + Math.random()*9000);
  const now     = new Date();
  const {sub, tax, total} = getTotals();

  lastOrder = {
    orderId, name, phone, address, payment,
    items: Object.values(cart).map(i => ({name:i.name, qty:i.qty, price:i.price})),
    subtotal:sub, tax, delivery:DELIVERY, discount:appliedDiscount, total,
    date: now.toLocaleDateString('en-IN',{day:'2-digit',month:'short',year:'numeric'}),
    time: now.toLocaleTimeString('en-IN',{hour:'2-digit',minute:'2-digit'})
  };

  const waMsg = `🍛 *New Order – Biryani Baadshah*\n\n*Order ID:* ${orderId}\n*Name:* ${name}\n*Phone:* ${phone}\n*Address:* ${address}\n*Payment:* ${payment}\n\n*Items:*\n${lastOrder.items.map(i=>`• ${i.name} ×${i.qty} = ₹${i.price*i.qty}`).join('\n')}\n\n*Subtotal:* ₹${sub}\n*GST:* ₹${tax}\n*Delivery:* ₹${DELIVERY}${appliedDiscount?`\n*Discount:* −₹${appliedDiscount}`:''}\n*Total: ₹${total}*\n\n✅ Please confirm my order!`;
  window.open('https://wa.me/' + WA + '?text=' + encodeURIComponent(waMsg), '_blank');

  document.getElementById('order-id').textContent = orderId;
  closeCheckout();
  cart = {}; appliedDiscount = 0;
  updateCartUI(); renderMenu(getCurrentItems());
  document.getElementById('success-modal').classList.add('open');
};

window.closeSuccess = () => {
  document.getElementById('success-modal').classList.remove('open');
  const os = document.getElementById('order-status');
  os.classList.add('show'); os.scrollIntoView({behavior:'smooth'});
  simulateTracker();
};

window.downloadInvoice = () => {
  document.getElementById('success-modal').classList.remove('open');
  if (lastOrder) generateInvoice(lastOrder);
};

function generateInvoice(order) {
  const rows = order.items.map(i=>`<tr><td>${i.name}</td><td style="text-align:center">${i.qty}</td><td style="text-align:right">₹${i.price}</td><td style="text-align:right">₹${i.price*i.qty}</td></tr>`).join('');
  const win = window.open('','_blank');
  win.document.write(`<!DOCTYPE html><html><head><meta charset="UTF-8"/><title>Invoice ${order.orderId}</title>
  <link href="https://fonts.googleapis.com/css2?family=Nunito:wght@400;700;800&family=Playfair+Display:wght@700&display=swap" rel="stylesheet"/>
  <style>*{margin:0;padding:0;box-sizing:border-box;}body{font-family:'Nunito',sans-serif;background:#f4f4f4;padding:20px;}
  .page{max-width:700px;margin:0 auto;background:#fff;padding:40px 48px;border-radius:16px;}
  .hd{display:flex;justify-content:space-between;align-items:flex-start;border-bottom:3px solid #E23744;padding-bottom:22px;margin-bottom:26px;}
  .logo{font-family:'Playfair Display',serif;font-size:1.7rem;color:#1C1C1C;}.logo span{color:#E23744;}
  .im h2{color:#E23744;text-align:right;font-family:'Playfair Display',serif;}
  .sum-row{display:flex;justify-content:space-between;padding:6px 0;font-size:.86rem;}
  .sum-row.total{font-weight:800;font-size:1rem;border-top:2px solid #E23744;margin-top:6px;padding-top:8px;}
  table{width:100%;border-collapse:collapse;margin:16px 0;}
  th{background:#f8f8f8;padding:9px 12px;text-align:left;font-size:.76rem;color:#686B78;}
  td{padding:9px 12px;border-bottom:1px solid #f5f5f5;font-size:.86rem;}
  .foot{text-align:center;margin-top:20px;color:#686B78;font-size:.78rem;}
  .btn{padding:10px 24px;border:none;border-radius:8px;font-weight:800;cursor:pointer;font-family:'Nunito',sans-serif;margin:4px;}
  @media print{.no-print{display:none;}}
  </style></head><body><div class="page">
  <div class="hd"><div><div class="logo">Biryani <span>Baadshah</span></div><p style="font-size:.78rem;color:#686B78;margin-top:6px">📍 Deccan Gymkhana, Pune</p></div>
  <div class="im"><h2>INVOICE</h2><p style="font-size:.82rem;text-align:right">Order: <strong>${order.orderId}</strong></p><p style="font-size:.82rem;text-align:right">${order.date} · ${order.time}</p></div></div>
  <p><strong>Name:</strong> ${order.name} &nbsp;|&nbsp; <strong>Phone:</strong> ${order.phone}</p>
  <p style="margin-top:4px"><strong>Address:</strong> ${order.address}</p>
  <table><thead><tr><th>Item</th><th>Qty</th><th style="text-align:right">Price</th><th style="text-align:right">Amount</th></tr></thead><tbody>${rows}</tbody></table>
  <div class="sum-row"><span>Subtotal</span><span>₹${order.subtotal}</span></div>
  <div class="sum-row"><span>GST (5%)</span><span>₹${order.tax}</span></div>
  <div class="sum-row"><span>Delivery</span><span>₹${order.delivery}</span></div>
  ${order.discount?`<div class="sum-row" style="color:#3AB757"><span>Discount</span><span>−₹${order.discount}</span></div>`:''}
  <div class="sum-row total"><span>Total Payable</span><span>₹${order.total}</span></div>
  <div class="foot"><p>Thank you for ordering from <strong style="color:#E23744">Biryani Baadshah</strong> 🍛</p></div>
  <div class="no-print" style="text-align:center;margin-top:20px">
    <button class="btn" style="background:#E23744;color:#fff" onclick="window.print()">🖨 Print</button>
    <button class="btn" style="background:#f0f0f0" onclick="window.close()">✕ Close</button>
  </div></div></body></html>`);
  win.document.close();
}

/* ═══════════════════════════════════════════
   ORDER TRACKER
═══════════════════════════════════════════ */
function simulateTracker() {
  const steps = document.querySelectorAll('.t-step');
  let step = 1;
  const iv = setInterval(() => {
    step++;
    if (step >= steps.length) { clearInterval(iv); return; }
    steps.forEach((s,i) => {
      const d = s.querySelector('.t-dot'), l = s.querySelector('.t-label');
      if (i < step)      { d.className='t-dot done';   l.className='t-label done'; }
      else if (i===step) { d.className='t-dot active'; l.className='t-label active'; }
    });
  }, 8000);
}

/* ═══════════════════════════════════════════
   CONTACT FORM
═══════════════════════════════════════════ */
window.submitContact = async (e) => {
  e.preventDefault();
  const st = document.getElementById('contact-status');
  const data = {
    name:    document.getElementById('cf-name').value.trim(),
    phone:   document.getElementById('cf-phone').value.trim(),
    email:   document.getElementById('cf-email').value.trim(),
    subject: document.getElementById('cf-subject').value.trim(),
    message: document.getElementById('cf-message').value.trim(),
    createdAt: new Date().toISOString()
  };
  st.style.display = 'block';
  st.textContent = '⏳ Sending...';
  try {
    await fbAddDoc(fbCollection(fbDb, 'contacts'), data);
    st.textContent = '✅ Message sent! We\'ll reply within 24 hours.';
    document.getElementById('contact-form').reset();
  } catch(err) {
    console.warn('Contact save error:', err);
    st.textContent = '✅ Message received! We\'ll reply within 24 hours.';
    document.getElementById('contact-form').reset();
  }
};

/* ═══════════════════════════════════════════
   HELPERS
═══════════════════════════════════════════ */
window.showToast = (msg) => {
  const t = document.getElementById('toast');
  t.textContent = msg; t.classList.add('show');
  setTimeout(() => t.classList.remove('show'), 2600);
};
window.copyCode = (code) => {
  navigator.clipboard?.writeText(code).catch(()=>{});
  showToast('📋 "' + code + '" copied!');
};
window.openWA = () => window.open('https://wa.me/' + WA + '?text=Hi%20Biryani%20Baadshah!%20I%27d%20like%20to%20place%20an%20order.','_blank');

setTimeout(() => {
  const tip = document.getElementById('wa-tip');
  if (tip) { tip.style.opacity='0'; tip.style.transition='opacity .5s'; setTimeout(()=>tip.style.display='none',500); }
}, 6000);

/* INIT */
renderRecommended();
renderMenu(menuData);
renderReviews();
updateCartUI();
</script>

<!-- ═══════════════════════════════════════════
     FIREBASE — saves orders & contacts to Firestore
     Login/auth stays in localStorage (unchanged above)
════════════════════════════════════════════ -->
<script type="module">
import { initializeApp, getApps } from "https://www.gstatic.com/firebasejs/10.11.0/firebase-app.js";
import {
  getFirestore, collection, addDoc, serverTimestamp
} from "https://www.gstatic.com/firebasejs/10.11.0/firebase-firestore.js";

const firebaseConfig = {
  apiKey:            "AIzaSyC73_RXR_Thq9qu1PKlDLVBAlJOLek0c9A",
  authDomain:        "my-shop-c0bd5.firebaseapp.com",
  projectId:         "my-shop-c0bd5",
  storageBucket:     "my-shop-c0bd5.firebasestorage.app",
  messagingSenderId: "293130360307",
  appId:             "1:293130360307:web:cdb1ccf442921b6fabee86"
};

let db;
try {
  const app = getApps().length ? getApps()[0] : initializeApp(firebaseConfig);
  db = getFirestore(app);
  console.log('✅ Firebase connected: my-shop-c0bd5');
} catch(e) {
  console.warn('Firebase init error:', e.message);
}

/* Expose Firestore helpers to the main script */
window.fbDb         = db;
window.fbAddDoc     = addDoc;
window.fbCollection = collection;
window.fbTimestamp  = serverTimestamp;

/* ── Patch placeOrder to ALSO save to Firestore ── */
const _origPlaceOrder = window.placeOrder;
window.placeOrder = async function() {
  const name    = document.getElementById('o-name').value.trim();
  const phone   = document.getElementById('o-phone').value.trim();
  const address = document.getElementById('o-address').value.trim();
  const payment = document.getElementById('o-payment').value;
  if (!name || !phone || !address) { window.showToast('Please fill all required fields!'); return; }

  const orderId = 'BB' + Math.floor(1000 + Math.random()*9000);
  const now     = new Date();

  /* Rebuild totals inline (same logic as original) */
  const DELIVERY = 40, TAX = 0.05;
  const cartItems = Object.values(window._cartRef || {});
  const sub  = cartItems.reduce((a,i) => a + i.price*i.qty, 0);
  const tax  = Math.round(sub * TAX);
  const disc = window._discountRef || 0;
  const total = sub + tax + DELIVERY - disc;

  const orderData = {
    orderId, name, phone, address, payment,
    items:    cartItems.map(i => ({name:i.name, qty:i.qty, price:i.price})),
    subtotal: sub, tax, delivery: DELIVERY, discount: disc, total,
    userEmail: window.currentUser?.email || 'guest',
    userName:  window.currentUser?.name  || 'Guest',
    status:    'placed',
    date:      now.toLocaleDateString('en-IN',{day:'2-digit',month:'short',year:'numeric'}),
    time:      now.toLocaleTimeString('en-IN',{hour:'2-digit',minute:'2-digit'}),
    createdAt: serverTimestamp()
  };

  /* Save to Firestore */
  if (db) {
    try {
      await addDoc(collection(db, 'orders'), orderData);
      console.log('✅ Order saved to Firestore:', orderId);
    } catch(err) {
      console.warn('Order save failed:', err.message);
    }
  }

  /* Now run the original placeOrder UI logic */
  _origPlaceOrder();
};
</script>
</body>
</html>
