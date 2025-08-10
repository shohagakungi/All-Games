<!DOCTYPE html>
<html lang="bn">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>All GaMes BD</title>
  <style>
    * { box-sizing: border-box; margin: 0; padding: 0; }
    body {
      font-family: Arial, sans-serif;
      background: #f5f5f5;
      color: #000;
      padding-top: 130px;
      transition: background 0.3s, color 0.3s;
    }
    body.dark { background: #121212; color: #fff; }
    #splash-loader {
      position: fixed; top: 0; left: 0; width: 100%; height: 100%;
      background: #000; color: #fff; display: flex; justify-content: center;
      align-items: center; font-size: 1.5rem; z-index: 9999;
    }
    header {
      position: fixed; top: 0; left: 0; width: 100%;
      background: linear-gradient(90deg, #ff512f, #f09819);
      color: #fff; padding: 15px 20px; z-index: 1000; text-align: center;
      box-shadow: 0 2px 8px rgba(0,0,0,0.2);
    }
    header h1 { font-size: 1.8rem; display: flex; justify-content: center; align-items: center; gap: 10px; }
    .sub-header { margin-top: 8px; font-size: 1rem; font-weight: bold; }
    #dark-mode-toggle {
      position: absolute; top: 15px; right: 15px; font-size: 1.2rem;
      background: #000; color: #ffd700; border: none; padding: 8px; border-radius: 10px; cursor: pointer;
    }
    #search-input {
      width: 90%; margin: 20px auto; padding: 10px; display: block;
      border: 1px solid #ccc; border-radius: 5px;
    }
    .game-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(120px, 1fr)); gap: 15px; padding: 10px; }
    .game-item {
      background:transparent; color:ffff; border-radius: 10px; padding: 10px; text-align: center;
      box-shadow: 0 2px 6px rgba(0,0,0,0.3); transition: transform 0.2s;
    }
    .game-item:hover { transform: scale(1.05); }
    .game-item img { width: 100%; height: 70px; object-fit: contain; margin-bottom: 5px; }
    footer { text-align: center; padding: 20px; background:#212121; color:#fff; margin-top: 30px; }
    
    /* শেয়ার পপআপ */
    #sharePopup {
      display:none; position:fixed; bottom:20px; right:20px; background:#fff;
      border:1px solid #ccc; border-radius:8px; box-shadow:0 4px 10px rgba(0,0,0,0.3);
      z-index:10000; padding:10px; width:200px;
    }
    #sharePopup button {
      width:100%; margin:5px 0; padding:8px; border:none; border-radius:6px; cursor:pointer;
    }
  </style>




</head>
<body>
  <!-- Splash Loader -->
  <div id="splash-loader">⏳ লোড হচ্ছে...</div>

<div style="max-width: 400px; margin: 0 auto; background: #0c1c1f; border-radius: 12px; padding: 20px; color: #fff; font-family: sans-serif; box-shadow: 0 0 15px #000;">
  <h2 style="color: #ffc107; text-align: center; margin-bottom: 20px;">🥇রেজিস্ট্রেশন ধাপসমূহ</h2><p>এই ভাবে রেজিস্ট্রেশন করবেন</p>

  <!-- Step 1 -->
  <div style="margin-bottom: 20px;">
    <h3 style="color: #4fc3f7;">১ম ধাপ: মোবাইল নম্বর লিখুন</h3>
    <input type="text" placeholder="📞 01912345678" disabled style="width: 100%; padding: 10px; border-radius: 6px; border: none; background: #1c3c40; color: #ccc;" />
  </div>

  <!-- Step 2 -->
  <div style="margin-bottom: 20px;">
    <h3 style="color: #4fc3f7;">২য় ধাপ: পাসওয়ার্ড সেট করুন</h3>
    <input type="password" placeholder="🔒 123ABC" disabled style="width: 100%; padding: 10px; border-radius: 6px; border: none; background: #1c3c40; color: #ccc;" />
  </div>

  <!-- Step 3 -->
  <div style="margin-bottom: 20px;">
    <h3 style="color: #4fc3f7;">৩য় ধাপ: পাসওয়ার্ড নিশ্চিত করুন</h3>
    <input type="password" placeholder="🔒 123ABC" disabled style="width: 100%; padding: 10px; border-radius: 6px; border: none; background: #1c3c40; color: red;" />
  </div>

  <!-- Step 4 -->
  <div style="margin-bottom: 20px;">
    <h3 style="color: #4fc3f7;">৪র্থ ধাপ: চেকবক্সে টিক দিন</h3>
    <div style="font-size: 14px;">
      <label><input type="checkbox" checked disabled /> আমি ১৮ বছরের বেশি এবং শর্তাবলী পড়েছি</label><br />
      <label><input type="checkbox" checked disabled /> অফার এবং বোনাস পেতে চাই</label>
    </div>
  </div>

  <!-- Step 5 -->
  <div style="margin-bottom: 20px;">
    <h3 style="color: #4fc3f7;">৫ম ধাপ: রেজিস্টার বোতামে ক্লিক করুন</h3>
    <button disabled style="width: 100%; padding: 12px; background: #ffc107; color: #000; font-weight: bold; border: none; border-radius: 8px;">Register</button>
  </div>

  <!-- Step 6 -->
  <div style="margin-bottom: 10px;">
    <h3 style="color: #4fc3f7;">৬ষ্ঠ ধাপ: Facebook বা Google দিয়ে লগইন করুন (ঐচ্ছিক)</h3>
    <div style="text-align: center;">
      <img src="https://i.ibb.co/QcZx4tS/facebook.png" alt="Facebook" title="Facebook" style="width: 38px; margin: 0 8px;" />
      <img src="https://i.ibb.co/6FzjG3J/google.png" alt="Google" title="Google" style="width: 38px; margin: 0 8px;" />
    </div>
  </div>
</div>

  <header>
    <h1>🎯 All GaMes BD 🇧🇩</h1>
    <p class="sub-header">"🎯 প্রতিদিন বোনাস পান, শুধু অ্যাকাউন্ট খুললেই!"🎁 আজই রেজিস্ট্রেশন করুন এবং ফ্রি বোনাস নিন! সবগুলো গেমে একাউন্ট খুলুন আর বোনাস নি"</p>
    <button id="dark-mode-toggle">🌙</button>
  </header>

  <!-- Popup -->
  <div id="popup" style="display:none; position:fixed; top:0; left:0; width:100%; height:100%; background:rgba(0,0,0,0.7); z-index:1000; justify-content:center; align-items:center;">  
    <div style="background:#fff; color:#000; padding:20px; border-radius:12px; width:90%; max-width:400px; text-align:center; position:relative;">
      <button onclick="closePopup()" style="position:absolute; top:10px; right:10px; background:none; border:none; font-size:20px; cursor:pointer;">❌</button>
      <h2>🎁 রেজিস্ট্রেশন বোনাস</h2>
      <p>এই গেমে রেজিস্ট্রেশন করুন ১৬০ টাকা বোনাস নিন!</p>
      <a href="http://www.bgd3310.com/?r=ays3267" target="_blank" style="display:inline-block; padding:10px 20px; background:green; color:white; border-radius:6px; text-decoration:none;">✅ রেজিস্টার করুন</a>
    </div>    
  </div>

  <!-- Search -->
  <input type="text" id="search-input" placeholder="🔍 গেম খুঁজুন..." />

 
    <!-- এখানে আপনার গেম লিঙ্কগুলো থাকবে (আপনি আগের লিস্ট 그대로 ব্যবহার করবেন) -->
  
  <main class="game-grid" id="gameGrid"> 
  <div class="game-item">
  
 		 <a href="http://www.fb77.wang/?r=ond1556">
  
  		<img src="https://images.6492394993.com/wsd-images-prod/fb77bdtf6/merchant_resource/appdownloadicon/app_download_icon_fb77bdtf6_20250623144519.png">
  
 <p>FB77</p>
  </a>
  </div>
  
  <div class="game-item">
  
 		 <a href="http://www.ck444app.org/?r=eks3611">
  
 		 <img src="https://images.5943920202.com/wsd-images-prod/we999bdtf5/merchant_resource/appdownloadicon/app_download_icon_we999bdtf5_20250730144249.png">
  
  <p>CK444</p>
  </a>
  </div>
  
  <div class="game-item">
  
  		<a href="http://www.bgd3310.com/?r=ays3267">
  
 		 <img src="https://images.6492394993.com/wsd-images-prod/bgd33bdtf6/merchant_resource/appdownloadicon/app_download_icon_bgd33bdtf6_20250425005147.png">
  
  <p>BGD33</p>
  </a>
  </div>
  
  <div class="game-item">
  
  		<a href="http://www.eg-333.me/?r=mth7450">
  
  		<img src="https://images.6492394993.com/wsd-images-prod/eg333bdtf6/merchant_resource/appdownloadicon/app_download_icon_eg333bdtf6_20250401145956.png">
  
  <p>EG333</p>
  </a>
  </div>
  
  <div class="game-item">
  
  		<a href="http://www.l-444.com/?r=ebj5911">
  
  		<img src="https://images.5943920202.com/wsd-images-prod/444bdtf5/merchant_resource/appdownloadicon/app_download_icon_444bdtf5_20250125200220.png">
  
  <p>L444</p>
  </a>
  </div>
  
  <div class="game-item">
  
  		<a href="http://www.ck33com.net/?r=scc2849">
  
  		<img src="https://images.484930494.com/wsd-images-prod/jm555bdtf4/merchant_resource/appdownloadicon/app_download_icon_jm555bdtf4_20250630103125.png">
  
  <p>CK33</p>
  </a>
  </div>
  
  <div class="game-item">
  
  		<a href="http://www.cv-666.info/?r=fmx2522">
  
 		 <img src="https://images.6492394993.com/wsd-images-prod/cv666bdtf6/merchant_resource/appdownloadicon/app_download_icon_cv666bdtf6_20250313162725.png">
  
  <p>CV666</p>
  </a>
  </div>
  
  <div class="game-item">
  
  		<a href="http://wsapp55.winbd18.com/?referralCode=vhh6950">
  
 		 <img src="https://images.239494003.com/wsd-images-prod/winbdtf2/merchant_resource/appdownloadicon/wps_winbdtf2_app_20231019112649.png">
  
  <p>WINBD</p>
  </a>
  </div>
  
  <div class="game-item">
  
  		<a href="http://www.ace365.co/?r=hzz2127">
  
 		 <img src="https://images.6492394993.com/wsd-images-prod/365acbdtf6/merchant_resource/appdownloadicon/app_download_icon_365acbdtf6_20250606181653.png">
  
  <p>ACE365</p>
  </a>
  </div>
  
  <div class="game-item">
  
  		<a href="http://www.bk33vip.com/?r=zkj3854">
  
  		<img src="https://images.5943920202.com/wsd-images-prod/bk33bdtf5/merchant_resource/appdownloadicon/app_download_icon_bk33bdtf5_20250102153419.png">
  
  <p>BK33</p>
  </a>
  </div>
  
  <div class="game-item">
  
 		 <a href="http://www.0qqgg.com/?r=hzu6847">
  
 		 <img src="https://images.6492394993.com/wsd-images-prod/qqggbdtf6/merchant_resource/appdownloadicon/app_download_icon_qqggbdtf6_20250502154703.png">
  
  <p>QQGG</p>
  </a>
  </div>
  
  <div class="game-item">
  
 		 <a href="https://e2bet006.com?refcode=dHiF1C">
  
 		 <img src="game2.png">
  
  <p>E2BET</p>
  </a>
  </div>
  
  <div class="game-item">
  
 		 <a href="http://www.b8bet.cc/?r=urd4915">
  
 		 <img src="https://images.6492394993.com/wsd-images-prod/nbjbdtf6/merchant_resource/appdownloadicon/app_download_icon_nbjbdtf6_20250505142710.png">
  
  <p>B8BET</p>
  </a>
  </div>
  
  <div class="game-item">
  
		  <a href="http://www.asha7.co/?r=ruw8377">
  
 		 <img src="https://images.6492394993.com/wsd-images-prod/as777bdtf6/merchant_resource/appdownloadicon/app_download_icon_as777bdtf6_20250402132955.png">
  
  <p>ASHA777</p>
  </a>
  </div>
  
  <div class="game-item">
  
  		<a href="http://bd9999.98bdbajee.com/?referralCode=dqf1143">
  
 		 <img src="https://images.239494003.com/wsd-images-prod/bajeebdf2/merchant_resource/appdownloadicon/wps_bajeebdf2_app_20231208103106.png">
  
  <p>BDBAJEE</p>
  </a>
  </div>
  
  <div class="game-item">
  
  		<a href="http://www.jeeta6.com/?r=jyn5315">
  
		  <img src="https://images.6440949940.com/wsd-images-prod/bgp88bdtf6/template/wt8820_logo/wps_Jeeta_Logo_-for_dark_background_20250719174051.png">
  
  <p>JEETA</p>
  </a>
  </div>
  
  <div class="game-item">
  
  		<a href="http://www.85nbajee.vip/?r=zox0293">
  
 		 <img src="https://images.6492394993.com/wsd-images-prod/bet15bdtf6/merchant_resource/appdownloadicon/app_download_icon_bet15bdtf6_20250528120310.png">
  
  <p>NBAJEE</p>
  </a>
  </div>
  
  <div class="game-item">
  
  		<a href="http://vip9999.rbajee42.com/?referralCode=qna4983">
  
 		 <img src="https://images.185949949.com/wsd-images-prod/bet11bdtf1/merchant_resource/appdownloadicon/app_download_icon_bet11bdtf1_20250224154438.png">
  
  <p>RBAJEE</p>
  </a>
  </div>
  
  <div class="game-item">
  
 		 <a href="http://vip888.77okbajee.com/?referralCode=cst0361">
  
 		 <img src="https://images.484930494.com/wsd-images-prod/bet09bdtf4/merchant_resource/appdownloadicon/app_download_icon_bet09bdtf4_20241024115233.png">
  
  <p>OKBAJEE</p>
  </a>
  </div>
  
  <div class="game-item">
  
  		<a href="http://vip999.86xbajee.club/?referralCode=pbo7260">
  
		  <img src="https://images.185949949.com/wsd-images-prod/bet10bdtf1/merchant_resource/appdownloadicon/app_download_icon_bet10bdtf1_20250115180334.png">
  
  <p>XBAJEE</p>
  </a>
  </div>
  
  <div class="game-item">
  
 		 <a href="http://rich88.6rwin4.com/?referralCode=nyx7708">
  
  		<img src="https://images.185949949.com/wsd-images-prod/6rwincom/merchant_resource/appdownloadicon/app_download_icon_6rwincom_20250411153035.png">
  
  <p>6RWIN</p>
  </a>
  </div>
  
  <div class="game-item">
  
		  <a href="http://www.7c777333.com/?r=mye1915">
  
 		 <img src="https://images.6492394993.com/wsd-images-prod/7c7bdtf6/merchant_resource/appdownloadicon/app_download_icon_7c7bdtf6_20250408183733.png">
  
  <p>7C777</p>
  </a>
  </div>
  
  <div class="game-item">
  
  		<a href="http://rich88.16l777.com/?referralCode=kmw5548">
  
  		<img src="https://images.191829838.com/wsd-images-prod/6l777bdtf1/merchant_resource/appdownloadicon/app_download_icon_6l777bdtf1_20250619235112.png">
  
  <p>6L777</p>
  </a>
  </div>
  
  <div class="game-item">
  
  		<a href="http://www.7p7773.com/?r=tja0828">
  
  		<img src="https://images.6492394993.com/wsd-images-prod/7p777bdtf6/merchant_resource/appdownloadicon/app_download_icon_7p777bdtf6_20250505164013.png">
  
  <p>7P777</p>
  </a>
  </div>
  
  <div class="game-item">
  
  		<a href="http://rich88.5z77744.com/?referralCode=jau3231">
  
  		<img src="https://images.191829838.com/wsd-images-prod/5z777bdtf1/merchant_resource/appdownloadicon/app_download_icon_5z777bdtf1_20250619234924.png">
  
  <p>5Z777</p>
  </a>
  </div>
  
  <div class="game-item">
  
 		 <a href="https://www.897909.com?refer_code=GME1IS4610">
  
 		 <img src="https://www.897909.com/static/svg/bb88_logo_animation2.gif">
  
  <p>BABU88</p>
  </a>
  </div>
  
  <div class="game-item">
  
 		 <a href="http://a71vip.a71-6.com/?referralCode=umj8489">
  
 		 <img src="https://images.191829838.com/wsd-images-prod/a71bdtf1/merchant_resource/appdownloadicon/app_download_icon_a71bdtf1_20250619172723.png">
  
  <p>A71</p>
  </a>
  </div>
  
  <div class="game-item">
  
 		 <a href="http://130662.wicket71.co/?referralCode=yin3049">
  
 		 <img src="https://images.484930494.com/wsd-images-prod/wicket71f4/merchant_resource/appdownloadicon/app_download_icon_wicket71f4_20240626011624.png">
  
  <p>WICKET71</p>
  </a>
  </div>
  
  <div class="game-item">
  
 		 <a href="https://www.jaya9.bet?refer_code=GMZO1H0149">
  
 		 <img src="https://jaya9bangladesh.com/static/image/layout/download-app.png">
  
  <p>JAYA9</p>
  </a>
  </div>
  
  <div class="game-item">
  
  		<a href="https://77bd6.com/?dl=301s67">
  
 		 <img src="https://zx7m061762-a5epdndpczfkd4hq.a02.azurefd.net/siteadmin/upload/img/1930969810145161217.avif">
  
  <p>77BD</p>
  </a>
  </div>
  
  <div class="game-item">
  
 		 <a href="https://6599334.com?refer_code=GMWSAP1873">
  
 		 <img src="https://dhoni88.co/static/image/layout/download-app.svg">
  
  <p>Dhoni88</p>
  </a>
  </div>
  
  <div class="game-item">
  
 		 <a href="http://www.pjok.love/?r=iuq1760">
  
 		 <img src="https://images.6492394993.com/wsd-images-prod/pjokbdtf6/merchant_resource/appdownloadicon/app_download_icon_pjokbdtf6_20250704124158.png ">
  
  <p>PJOK</p>
  </a>
  </div>
  
  <div class="game-item">
  
 		 <a href="https://betjili.cricket/?refcode=MoHJLh">
  
 		 <img src="https://betjiliaffiliates.com/wp-content/uploads/2024/02/BETJILI-Logo.png">
  
  <p>BETJILI</p>
  </a>
  </div>
  
  <div class="game-item">
  
 		 <a href="http://www.jt999.app/?r=kch8675">
  
 		 <img src="https://images.6440949940.com/wsd-images-prod/sun88bdtf6/merchant_resource/appdownloadicon/app_download_icon_sun88bdtf6_20250701124412.png">
  
  <p>JT999</p>
  </a>
  </div>
  </main>
  
 

  			<!-- শেয়ার বাটন --> 			
  <div class="actions" style="text-align:center; margin:20px;">
    <button onclick="toggleSharePopup()">📤 বন্ধুদের শেয়ার করুন</button>
    <div id="sharePopup">
      <button onclick="shareFacebook()">📘 ফেসবুক</button>
      <button onclick="shareWhatsApp()">💬 হোয়াটসঅ্যাপ</button>
      <button onclick="shareMessenger()">📨 মেসেঞ্জার</button>
      <button onclick="shareTelegram()">📢 টেলিগ্রাম</button>
      <button onclick="copyLink()">🔗 কপি লিংক</button>
    </div>
  </div>


  <footer><p>&copy; 2025 All GaMes BD</p></footer>



<script>
  // পপআপ ওপেন ফাংশন
  function showPopup() {
    document.getElementById('popup').style.display = 'flex';
  }

  // পপআপ ক্লোজ ফাংশন
  function closePopup() {
    document.getElementById('popup').style.display = 'none';
  }

  // পেজ লোড হওয়ার ৫ সেকেন্ড পর পপআপ দেখাবে
  window.addEventListener('load', () => {
    setTimeout(showPopup, 5000); 
  });

  
    // লোডিং রিমুভ
    window.addEventListener('load', () => { document.getElementById('splash-loader')?.remove(); });

    // ডার্ক মোড
    document.getElementById('dark-mode-toggle').addEventListener('click', () => { document.body.classList.toggle('dark'); });

    // সার্চ
    const searchInput = document.getElementById('search-input');
    searchInput.addEventListener('input', () => {
      const filter = searchInput.value.toLowerCase();
      document.querySelectorAll('.game-item').forEach(item => {
        item.style.display = item.innerText.toLowerCase().includes(filter) ? 'block' : 'none';
      });
    });

    // ✅ শেয়ার ফাংশন
   // ✅ নির্দিষ্ট লিঙ্ক সেট করুন
   const pageUrl = "https://xmod.top/p/ll-a-es";
   
   function toggleSharePopup() {
   const popup = document.getElementById('sharePopup');
   popup.style.display = 'block';
   setTimeout(() => { popup.style.display = 'none'; }, 7000); // ৩ সেকেন্ড পর অটো বন্ধ
   }
   
   function shareFacebook() { 
   window.open(`https://www.facebook.com/sharer/sharer.php?u=${encodeURIComponent(pageUrl)}`, '_blank'); 
   }
   
   function shareWhatsApp() { 
   window.open(`https://wa.me/?text=${encodeURIComponent(pageUrl)}`, '_blank'); 
   }
   
   function shareMessenger() { 
   window.open(`fb-messenger://share/?link=${encodeURIComponent(pageUrl)}`, '_blank'); 
   }
   
   function shareTelegram() { 
   window.open(`https://t.me/share/url?url=${encodeURIComponent(pageUrl)}&text=দেখে নিন এই সাইটটি!`, '_blank'); 
   }
   
   function copyLink() { 
   navigator.clipboard.writeText(pageUrl).then(() => alert('✅ লিংক কপি হয়েছে!')); 
   }
    // 🔥 উন্নত অ্যাড ব্লকার
    function removeAds() {
      document.querySelectorAll('iframe, .ads, [id*="ad"], script[src*="ad"], div[class*="sponsor"]').forEach(ad => ad.remove());
    }
    setInterval(removeAds, 500);
    const observer = new MutationObserver(removeAds);
    observer.observe(document.body, { childList: true, subtree: true });
  </script>

<!-- কমেন্ট সেকশন শুরু -->
<div style="max-width:600px; margin:20px auto; background:#fff; border-radius:10px; padding:20px; box-shadow:0 0 10px rgba(0,0,0,0.2);">
  <h2 style="text-align:center; color:#333;">💬 আপনার মতামত শেয়ার করুন</h2>
  
  <input id="username" type="text" placeholder="👤 আপনার নাম লিখুন" 
    style="width:100%; padding:10px; border:1px solid #ccc; border-radius:6px; margin-bottom:10px;" />
  <textarea id="comment" placeholder="✍️ আপনার কমেন্ট লিখুন..." 
    style="width:100%; padding:10px; border:1px solid #ccc; border-radius:6px; resize:none; height:80px; margin-bottom:10px;"></textarea>
  <button onclick="postComment()" 
    style="background:#28a745; color:#fff; border:none; border-radius:6px; padding:12px 20px; cursor:pointer; font-size:1rem;">📨 সাবমিট</button>

  <div id="comments-list" style="margin-top:30px;"></div>
</div>
<!-- কমেন্ট সেকশন শেষ -->

<!-- Firebase SDK -->
<script src="https://www.gstatic.com/firebasejs/9.23.0/firebase-app.js"></script>
<script src="https://www.gstatic.com/firebasejs/9.23.0/firebase-database.js"></script>

<script>
  // Firebase Config - অবশ্যই আপনার ডাটাবেজ URL সঠিক বসাবেন
  const firebaseConfig = {
    apiKey: "AIzaSyCIrtegCaN6yXPZz-mfPnNmx2270jU35Rk",
    authDomain: "all-games-bd.firebaseapp.com",
    databaseURL: "https://all-games-bd-default-rtdb.firebaseio.com/",
    projectId: "all-games-bd",
    storageBucket: "all-games-bd.firebasestorage.app",
    messagingSenderId: "23078465078",
    appId: "1:23078465078:web:dc640d78325ffb7a333297"
  };

  // Initialize Firebase
  const app = firebase.initializeApp(firebaseConfig);
  const db = firebase.database();

  // কমেন্ট পোস্ট ফাংশন
  function postComment(parentId = null) {
    const name = document.getElementById("username").value.trim();
    const text = document.getElementById("comment").value.trim();

    if (!name || !text) {
      alert("⚠️ নাম এবং কমেন্ট লিখুন!");
      return;
    }

    const commentRef = db.ref("comments").push();
    commentRef.set({ name, text, parentId, time: Date.now() });

    document.getElementById("comment").value = "";
  }

  // কমেন্ট লোড এবং দেখানো
  db.ref("comments").on("value", snapshot => {
    const data = snapshot.val();
    const container = document.getElementById("comments-list");
    container.innerHTML = "";

    if (data) {
      const commentsArray = Object.entries(data).map(([id, c]) => ({ id, ...c }));
      const parents = commentsArray.filter(c => !c.parentId);

      parents.forEach(p => {
        const replies = commentsArray.filter(r => r.parentId === p.id);
        container.innerHTML += renderComment(p, replies);
      });
    }
  });

  // একেকটি কমেন্ট HTML তৈরী ফাংশন
  function renderComment(comment, replies = []) {
    return `
      <div style="background:#f9f9f9; border:1px solid #ddd; border-radius:6px; padding:10px; margin-bottom:15px;">
        <strong>${comment.name}</strong> 
        <small style="color:#888;">(${new Date(comment.time).toLocaleString()})</small>
        <p style="margin-top:5px;">${comment.text}</p>
        <button onclick="replyTo('${comment.id}')" style="background:#007bff; color:#fff; border:none; padding:4px 8px; border-radius:4px; cursor:pointer;">↩️ রিপ্লাই</button>
        <div style="margin-left:20px; margin-top:10px; border-left:2px solid #007bff; padding-left:8px;">
          ${replies.map(r => `
            <div style="background:#e9f0ff; border:1px solid #c6d8ff; border-radius:4px; padding:8px; margin-bottom:8px;">
              <strong>${r.name}</strong>: ${r.text}
            </div>
          `).join("")}
        </div>
      </div>
    `;
  }

  // রিপ্লাই করার জন্য প্রম্পট
  function replyTo(parentId) {
    const replyText = prompt("✍️ আপনার রিপ্লাই লিখুন:");
    const name = document.getElementById("username").value.trim();

    if (!replyText || !name) {
      alert("⚠️ নাম এবং রিপ্লাই লিখুন!");
      return;
    }

    db.ref("comments").push().set({ name, text: replyText, parentId, time: Date.now() });
  }
</script>



</body>
</html>
