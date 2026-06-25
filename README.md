<!DOCTYPE html>
<html lang="zh-Hant">
<head>
<meta charset="UTF-8">
<title>金牌燒烤 菜單</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Noto+Serif+TC:wght@500;700;900&family=Noto+Sans+TC:wght@400;500;700;900&display=swap" rel="stylesheet">
<style>
  :root{
    --marble-bg: #f3efe6;
    --marble-vein: #e2d9c4;
    --charcoal: #2b2622;
    --gold-1: #c89a3f;
    --gold-2: #a6781f;
    --gold-light: #e8c878;
    --maroon: #7a1f1f;
    --line: #d8cba8;
  }
  *{box-sizing:border-box;}
  body{
    margin:0;
    background: var(--marble-bg);
    font-family:"Noto Sans TC", sans-serif;
    color: var(--charcoal);
    display:flex;
    justify-content:center;
    padding:24px;
  }
  .poster{
    width:1000px;
    background:
      radial-gradient(circle at 20% 10%, rgba(255,255,255,0.6), transparent 40%),
      radial-gradient(circle at 80% 90%, rgba(255,255,255,0.5), transparent 45%),
      linear-gradient(135deg, #f6f2ea 0%, #efe8d8 40%, #f3efe6 70%, #ece4d2 100%);
    border: 10px solid transparent;
    border-image: linear-gradient(135deg, var(--gold-1), var(--gold-light), var(--gold-2)) 1;
    position:relative;
    padding:40px 50px 30px;
    box-shadow: 0 20px 60px rgba(0,0,0,0.25);
  }
  .poster::before{
    content:"";
    position:absolute;
    inset:18px;
    border:2px solid var(--gold-2);
    pointer-events:none;
    opacity:0.6;
  }

  /* ===== Header ===== */
  .header{
    text-align:center;
    padding-bottom:18px;
    margin-bottom:22px;
    position:relative;
  }
  .medal{
    width:74px;
    height:74px;
    margin:0 auto 6px;
    position:relative;
  }
  .medal svg{width:100%;height:100%;}
  .title{
    font-family:"Noto Serif TC", serif;
    font-weight:900;
    font-size:54px;
    letter-spacing:10px;
    color: var(--maroon);
    text-shadow: 0 1px 0 #fff, 0 3px 8px rgba(122,31,31,0.18);
    margin:6px 0 4px;
  }
  .title .accent{
    color: var(--gold-2);
  }
  .subtitle{
    font-size:14px;
    letter-spacing:8px;
    color: var(--gold-2);
    font-weight:700;
    text-transform:uppercase;
  }
  .divider{
    width:240px;
    height:3px;
    margin:14px auto 0;
    background: linear-gradient(90deg, transparent, var(--gold-1), var(--gold-2), var(--gold-1), transparent);
  }

  /* ===== Columns ===== */
  .columns{
    display:flex;
    gap:34px;
  }
  .col{
    flex:1;
    min-width:0;
  }
  .section{
    margin-bottom:22px;
  }
  .section-title{
    display:flex;
    align-items:center;
    gap:10px;
    font-family:"Noto Serif TC", serif;
    font-weight:700;
    font-size:21px;
    color:#fff;
    background: linear-gradient(90deg, var(--maroon), #9a2c2c 60%, var(--maroon));
    padding:6px 16px;
    border-radius:3px;
    margin-bottom:10px;
    box-shadow: 0 2px 4px rgba(0,0,0,0.15);
  }
  .section-title .ico{font-size:18px;}
  ul.items{
    list-style:none;
    margin:0;
    padding:0;
  }
  ul.items li{
    display:flex;
    align-items:baseline;
    justify-content:space-between;
    padding:5px 4px;
    font-size:15.5px;
    border-bottom:1px dotted var(--line);
  }
  ul.items li:last-child{border-bottom:none;}
  .name{
    color:var(--charcoal);
    font-weight:500;
  }
  .note{
    font-size:12px;
    color:#8a7a55;
    margin-left:4px;
    font-weight:400;
  }
  .price{
    font-weight:700;
    color: var(--gold-2);
    white-space:nowrap;
    margin-left:12px;
  }
  .sub-item{
    padding-left:14px;
  }
  .sub-item .name{font-size:14px;color:#5c5347;}

  /* ===== Footer ===== */
  .footer{
    margin-top:26px;
    padding-top:20px;
    border-top:2px solid var(--gold-1);
    display:flex;
    align-items:center;
    justify-content:space-between;
    gap:30px;
  }
  .footer-info{
    flex:1;
  }
  .footer-info .line{
    font-size:15px;
    margin:5px 0;
    display:flex;
    align-items:center;
    gap:8px;
    font-weight:500;
  }
  .footer-info .line.phone{
    font-size:18px;
    font-weight:900;
    color: var(--maroon);
  }
  .footer-info .label{
    color:var(--gold-2);
    font-weight:700;
  }
  .qr-block{
    text-align:center;
    flex-shrink:0;
  }
  .qr-block img{
    width:110px;
    height:110px;
    border:4px solid #fff;
    outline:2px solid var(--gold-1);
    border-radius:6px;
    display:block;
    box-shadow:0 4px 10px rgba(0,0,0,0.15);
  }
  .qr-block .cap{
    margin-top:6px;
    font-size:12px;
    font-weight:700;
    color: var(--gold-2);
  }
</style>
</head>
<body>
<div class="poster">

  <div class="header">
    <div class="medal">
      <svg viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg">
        <polygon points="35,0 45,0 30,45 18,38" fill="#7a1f1f"/>
        <polygon points="65,0 55,0 70,45 82,38" fill="#a6781f"/>
        <circle cx="50" cy="60" r="38" fill="#e8c878" stroke="#a6781f" stroke-width="3"/>
        <circle cx="50" cy="60" r="29" fill="#fff8e6" stroke="#c89a3f" stroke-width="2"/>
        <text x="50" y="70" font-family="Noto Serif TC, serif" font-size="30" font-weight="900" fill="#a6781f" text-anchor="middle">金</text>
      </svg>
    </div>
    <div class="title"><span class="accent">金牌</span>燒烤</div>
    <div class="subtitle">GOLD MEDAL BARBEQUE</div>
    <div class="divider"></div>
  </div>

  <div class="columns">
    <!-- LEFT COLUMN -->
    <div class="col">

      <div class="section">
        <div class="section-title"><span class="ico">🍢</span>小點類</div>
        <ul class="items">
          <li><span class="name">功夫米血</span><span class="price">30元</span></li>
          <li><span class="name">百頁豆腐</span><span class="price">30元</span></li>
          <li><span class="name">酥烤豆包</span><span class="price">30元</span></li>
          <li><span class="name">新竹貢丸</span><span class="price">30元</span></li>
          <li><span class="name">古早味豆乾</span><span class="price">30元</span></li>
          <li><span class="name">Q彈甜不辣</span><span class="price">30元</span></li>
          <li><span class="name">香烤鑫鑫腸</span><span class="price">30元</span></li>
          <li><span class="name">酥香黑輪片</span><span class="price">30元</span></li>
          <li><span class="name">古早味米腸</span><span class="price">35元</span></li>
          <li><span class="name">黑豬肉香腸</span><span class="price">55元</span></li>
          <li><span class="name">燒烤麻吉<span class="note">（醬烤、煉乳）</span></span><span class="price">55元</span></li>
        </ul>
      </div>

      <div class="section">
        <div class="section-title"><span class="ico">🍗</span>雞肉類</div>
        <ul class="items">
          <li><span class="name">醬烤雞心</span><span class="price">55元</span></li>
          <li><span class="name">香酥雞皮</span><span class="price">55元</span></li>
          <li><span class="name">酥烤七里香</span><span class="price">55元</span></li>
          <li><span class="name">嫩烤蜜汁雞</span><span class="price">60元</span></li>
          <li><span class="name">炙燒雞軟骨</span><span class="price">60元</span></li>
          <li><span class="name">蜜汁香烤翅</span><span class="price">60元</span></li>
          <li><span class="name">黃金雞腿排</span><span class="price">75元</span></li>
        </ul>
      </div>

      <div class="section">
        <div class="section-title"><span class="ico">🐂</span>牛肉類</div>
        <ul class="items">
          <li><span class="name">黑胡椒牛肉</span><span class="price">65元</span></li>
          <li><span class="name">牛五花蔥捲</span><span class="price">75元</span></li>
          <li><span class="name">炙燒骰子牛</span><span class="price">75元</span></li>
          <li><span class="name">嫩烤紐約客</span><span class="price">80元</span></li>
        </ul>
      </div>

    </div>

    <!-- RIGHT COLUMN -->
    <div class="col">

      <div class="section">
        <div class="section-title"><span class="ico">🐖</span>豬肉類</div>
        <ul class="items">
          <li><span class="name">醬烤蜜汁豬</span><span class="price">55元</span></li>
          <li><span class="name">炙烤松阪豬</span><span class="price">60元</span></li>
          <li><span class="name">香烤肥腸串</span><span class="price">65元</span></li>
          <li><span class="name">培根鳳梨捲</span><span class="price">65元</span></li>
          <li><span class="name">煙燻蔥肉捲</span><span class="price">70元</span></li>
          <li><span class="name">豬五花蔥捲</span><span class="price">70元</span></li>
          <li><span class="name">香蔥豬肉串</span><span class="price">70元</span></li>
        </ul>
      </div>

      <div class="section">
        <div class="section-title"><span class="ico">🦑</span>海鮮類</div>
        <ul class="items">
          <li><span class="name">鮮美花枝串</span><span class="price">60元</span></li>
          <li><span class="name">Q彈干貝串</span><span class="price">65元</span></li>
          <li><span class="name">甜烤蝦仁串</span><span class="price">75元</span></li>
          <li><span class="name">深海章魚腳</span><span class="price">90元</span></li>
          <li><span class="name">醬烤大魷魚</span><span class="price">150元</span></li>
          <li><span class="name">極品懶人蝦<span class="note">（免剝殼）</span></span></li>
          <li class="sub-item"><span class="name">小份（5尾）</span><span class="price">60元</span></li>
          <li class="sub-item"><span class="name">大份（10尾）</span><span class="price">100元</span></li>
        </ul>
      </div>

      <div class="section">
        <div class="section-title"><span class="ico">🐑</span>羊肉類</div>
        <ul class="items">
          <li><span class="name">香烤原味羊</span><span class="price">60元</span></li>
          <li><span class="name">香烤孜然羊</span><span class="price">65元</span></li>
        </ul>
      </div>

      <div class="section">
        <div class="section-title"><span class="ico">🥦</span>時蔬類</div>
        <ul class="items">
          <li><span class="name">青椒</span><span class="price">40元</span></li>
          <li><span class="name">香菇</span><span class="price">40元</span></li>
          <li><span class="name">櫛瓜</span><span class="price">40元</span></li>
          <li><span class="name">四季豆</span><span class="price">40元</span></li>
          <li><span class="name">杏鮑菇</span><span class="price">40元</span></li>
          <li><span class="name">花椰菜</span><span class="price">40元</span></li>
        </ul>
      </div>

    </div>
  </div>

  <div class="footer">
    <div class="footer-info">
      <div class="line phone">📞 直接來電訂購：0958-025-220</div>
      <div class="line"><span class="label">📍 店址</span>臺中市西屯區黎明路三段53-1號（宏香火雞肉旁）</div>
      <div class="line"><span class="label">💬</span>加入官方LINE，掌握優惠資訊</div>
    </div>
    <div class="qr-block">
      <img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAJ0AAACeCAYAAAAosgh4AAAAAXNSR0IArs4c6QAAAARnQU1BAACxjwv8YQUAAAAJcEhZcwAAEnQAABJ0Ad5mH3gAAF9WSURBVHhe1X15nBXFtf+3uu+9szHMsAwwCERAQEBEkVVkEUURNEZjNJofKm4hilvc4zOK+mLU5xZcoyYoghugqCAqoihEBAyg7AzrsMOwznaX7vP7o/vUVNetvnMH9X1evjP1ud3Vp06dOrX0qepaBMVXE0RTAAIQKQApAATAAhAByIYHx3OC/HvLfyZ8eqE8M0EAJAC4HjmE7wAI1/MX/iMNHEPdHXz6lPcLG6AIAAsCrqQ0gWABcEHChQABZENQBOTLL8jxk2MDZPkx+2m3XJAABLEMHsfgtQAo6uvHl1y4IEEQEJ7OhAsyppTBz3ydCc9Pxk2AgFNHrooj0x/x+BDfC0BwHpD/KwCL+XB6XUAkAaRAiPjPzPCiFYBrezwtLj+273zdUdTjJRxACAhy9xOJJl6+C4AE+QrxhBIgAARBlsfDAgiup0C1APDDDHBBAFw/lK1wBwBHxoi67FPVr9xZ8imxbKxbWw+jgekseeEHcAHhgOD6BTMCC1wL6mgJft75PoF6JlgiT3oOT8IFwYHw5RawPLn99KfJKZXiehVSEADbC+EXOlnutcAeR8CBCwHXk5i8QkA+vYADuJ4sruXAhQMBGxZsWQ68BiZNsgC8chAJZD8J16v8ql7glSsgCUFRCIcOkYXGAAEuEQRHxBXsJ0R67VZjIO+fOK1eoRJCgEgNRxDC8v288ALw7gMC14UPQJaWoLcHX0KCX7KojkwAIM5SkjIJ+C2ILEQyAUoU5OlW+uhpE8H8JS89ngheujzauudhBYK9Xb+Fs4QAUBdPnQJQd8+sqE5CaJQmSBHCdEoAkQOvnliwyEuHcOgwWSiEV+hcWFbm1up/A5yhRBQqj1oQ0wqWDy/jzM8yIVvejDAaHcHK0/BwXEgbFs4rWNmG+TlBrldQZaHjxKxatQrl5eU/i5C60nUQEXr27InS0lK4rgshBDZu3Ig1a9YECt8JJ5yANm3ayPvy8nL88MMPMlNc10X37t3RoUMHSdMQqJm8Zs0arFmzBrZtS/8+ffqgtLRU0q9duxarVq0KLRREhGOPPRY9e/b0arpPt2TJEmzbtg2WZQXSR+S1pK7romfPnujQoYOM23VdzJ8/HxUVFcYK6bpeCzdgwACUlpbKcKtXr8aKFSsQjUbhuq4xL3S/+u4Zqn8aDaXgEKFHz144sXt3r7V36DAREZHr/YwbN44ikQhFo9H/dReJROjtt98mIiLHcYiI6PHHHyfbtuVz27Zp4sSJnsiuJ/TLL79Mtm1LuS3LogkTJngJOkow7/Hjx5MQQsZtWRa9++67AZpHH32UhBBk27bRCSHouuuuk2E43JgxY2Q45s+/HO6ll14KhKuurqYhQ4bIcJZlScf3QgiaOXNmQMa//vWvBEDSCiHqdSrvTGHgvWAD19LP//3Lo38lTyCiuqriV04iQiqVQjKZ/F93qVRKisO12LIsOI4jnzuOE2iJWGbHcaTcYTUZhlrJTvdjMC+Om1sSHSyDyak8uaXjMKrs6q+aToYeluVhx/d6OA4LPz1MU59TeWcKwzDFm+5j6G6ycGoCf05wPGq8PwVsm4d6glD563GR/2qsTx5WLv+aaHSYaBxHGfZQoMbPlY/v1de8Cp1/ffc/N4QQ8P7SkVboGJywgoIC/OIXv8jKHXvssQHXvn37UNehQwc0bdpUxvdjlKKG5Uzas2cPNm3ahA0bNgRcWVkZysrKsH79elRUVMhwXLPLy8uxfv16lJWVYcOGDRBCoGPHjujUqRM6duyIjh07onHjxoF4j1b21q1bS95dunRB586dkZeXJws/AOzevRsbNmzA2rVrsW7dOqxbtw4lJSXo3LkzunTpgq5du6J58+bGgqhClZELdbt27dCtWzd07drV6Lp165bRde/ePeBOOOEEnHDCCejevTsaNWoUiF9F6Oif8I3d4cOH4/nnnzcmqqHK1hP+wgsvYPz48UBI03w04Ax76qmn8NJLL6Xx5XS5rot7770XN998swzjOA5uvvlmzJ8/H5blDcv84Q9/wL/+9S8Z3nVdFBcXp/FtCDjs3XffjVtvvVUWgkQigXPPPRfLli0D/Ar06KOPYsKECYAfdywWw8svv4w+ffrAdV3Yto0nnngCjzzySCCOTCB/VODhhx/GqFGjAiYD64evVej3JgghkEqlcNFFF+Grr77KrqXTGefl5aG0tBStW7dOc6WlpQ1yrVq1kq5ly5YoLCwMxAWl98XQ5YGhgKr35NsZhw8fxq5du7B79+6AY7+9e/eisrIywAcADhw4gL1792L37t3Ys2cPiAgtWrSQrlWrVsjNzZUFheNkmORFCE1xcTFatmyJFi1aoKSkBK1atUIk4rUDbEcdOXJEyr53717s3bsXubm5aN68OVq0aIFmzZohPz9f8mboBcckV2FhIZo2bYrmzZtL16xZs8C16po2bVqva9KkCZo3by7TwVBftGmFjsFCq79sTPKvDs5wdrqfDr2AHS1MQweZoHZSoBUItgX1TApLswq1lagPOn9ksPGgyKraqtnGFQZd/5y32aQVik70/DV1glRknVtqrbYsy6g0rv1qK6DeZxLkaMD8MmWWCaxslpEzNBaLSV7Mm2nD0gwA0WhUXofR/FiouuP4dPl/Clj+mGE26WA6tWyEQf0aFWrT6SDFuN20aRO2bt2a1kPUI+UwqVQKzZo1Q48ePQLPfyxYnjZt2mDo0KFp8pigKiiVSmHOnDlwHAeWZSGVSuG4445DJBKRdNFoFJ988okMr6fRtm2sWLEi4PdzQK0E8+bNw6FDh+C63heknyr+ZDKJuXPn4uDBg1kVZPKHbfr27YuOHTtmLqiq2uTgsI8bb7yRoAz0XXLJJYHnRET3338/CX/AVHX6YC8PdgKgc845Rw5UMh577DHyxZHurbfeCtA8+eSTaTT//Oc/iZQBU9d1KZlMUjKZJMdx6nUsx5/+9CeZViEERaNR+vTTTyVvIqKHHnpI0uiDpDwYy3LpA6Xq/bXXXpsms+7i8Tj17t07Lb0ctzogy4PH7K/L8NFHH0kdkj/IrvK0LIumTp0aoKmsrKRu3bqlpaU+9/e//z3AJ5lM0umnn+7x8WnMg8MNAL/DU6lUwOmDvTzYiZBXYMaa4YNpVFp+5amtjm3biEQi8vWQyemvA06P2pozVBq2d/QwOq3KQ4+LYQqHEJ2ofIVvprDdlK39lS3U9P5cOKpCdzTIprk2wVTAOGMaYlM0FMxTN7YZlj+kYiokXDDUQqn+cjh2nI6wgV8ovdkweX4qcHpM6fqpcHQl4ShgUmY2CWvUqJEcTmjdujVatmyJZDKJPXv2YOfOndi+fTsOHDhgbEkbCi4sUOQtLi5Gq1at0LZtW7Rp0wZt27ZFTk5OoOemg4hQUlKCdu3aoV27dmjdujWaNGkin3Nhq6iowJYtW1BeXo5t27Zh8+bNaNq0Kdq0aYN27drJQXe+5kH3vLy8QHz/aUgrdNkUhJ8KpgxTQUS49NJL8e9//xuLFy/G4sWLsXTpUixduhQ9e/ZEnz590KtXL4wfPz5g/GeLbOivvvpqLFmyBN9++y0WLVqExYsX44wzzgC0QqrjoYcekuEWL16M++67T7ZwjIcffhi9e/dG37590adPHwwdOhR33XUX/v3vf2PRokX49ttvZbx8/fXXX6NPnz6BuP4ToKqJp81KsFL0Gq8im8yCRmfiY4JOV1hYiDZt2qBNmzZyQLq2tha7du3C9u3bsWfPHhw8eDAQJlvo6VALBf82atQIxxxzjBzgbtmyJQoKCgLhdBARioqKAi1048aNZQvHvA8dOoR9+/Zh165d2LVrF3bs2IHCwkKUlJSgZcuWaa5FixZo2bJlYIiGYUqLCv05DDQw5P/RQo9P5ZfW0v1vQhdMR9hzvWAcrb14tNArpF6YEGKL6mC5OVwkEslID23g1RTvfwKOKrd+qkT+VHyOFrodmEqlsirAesEgQ09WL1Am6K2KEAKxWEyjCkL434ihxatXhJ+7w/FjUL+G/0OxefNm/Otf/8I333yDBQsWYP369fIZZ8wvfvEL9OrVC3369EGfPn3Qr18/bNu2DYsWLQo4tqfYviopKUG/fv3Qr18/9O/fHwMGDJCuf//+6N+/PyoqKvDtt9/iX//6FxYsWIB169Yp0pnhui4WL16MhQsXYsGCBfjqq6+wY8eOtMJ88sknY+DAgRgyZAgGDx6MIUOGSDd06FAMHjwYJSUlAd7/p+DQITloR0R08803E5SBv9/85jd1o34+HnjggQBNNu6ss85KGxx+4okn0ujefPPNAI0JY8aMCYS58sor5TOO44477qDc3FzKz8+n3NxcGj16tByE5QHi2tpaOnz4MB05coQqKyvpwIEDNHLkSMrPz6eCggLp8vPzA27KlClUXV1NlZWVVFlZSVVVVWlu9OjRlJeXR/n5+ZSTkyNnDvOMaCKia665hqAMJFuWRTk5OZSfn095eXkUi8XoxRdflOliuePxOFVXV1NNTU3A1dbWSpdKpWQ8ZNC1ZVn0zjvvBGiqqqqoe/fuaXlSn+PZzYxkMknDhg3z4vFpHn7kL97Dox0c/k9AbW0tamtrUV1djdraWsTjcfmMX2s5OTkoLCxEo0aNUFBQgMaNGyOZTKK6uhpVVVXSVVdXB5xlWcjLy0NBQQEKCgqQn5+f5lzXRU1NDaqrqxGPxwOvUF0OBhEhHo+juroaNTU1SCQSAROA7bdYLIa8vDzk5uYGXE5OjnTZfBLUoZsNPxeOqtAdjb2g208wKD1b6MpR5WGe+mwR27ZlprGDz4vH3EwyZoJux5nA8ZhsxbCvGya96DZbNmgILaOhOkA95cEkQbomMoATUVBQEJh3VVJSktE1a9YsMDiaLYgIVVVV2LNnD/bs2SPnk8ViMZSUlMh5aDyTl8OYUFtbi71792LPnj1yfhrPp8vG6FeRqXDoyETbpEkTtGzZUg6rlJaWGodDoIWvqKjA9u3bsWPHDqPbvn07ampqAuGzgRACrVu3xjHHHIO2bdvW69q1a4c2bdoY50VmQt0sEz9NnDihDXyqNfGKK67AeeedZ6y9JriuW+/YFkONUwiBqVOn4uGHH5afnQDg5ptvxu233w7XX6bYuHHjjJkrhMDnn3+O0047LdC63HLLLRg3bpykqQ+6TtivIVB53HnnnRg7diyE3/ImEglceumlWLp0qR5MxpNIJHDjjTfK2c06OJ9effVVDB8+XPpnkpP88cmcnBxMmjQJqVRKypQNeCZ1JnpVbWlSc0Bdueqzli1bomvXrujSpUtWrmvXrmjXrl1GocJw4MABlJWVYd26dVi/fj3Wr1+P/Pz8wLqCVq1ahfJm/yNHjmDdunVyjcSGDRuwf/9+nTwrhMXVEAghUFJSgo4dO6JDhw5o3749OnbsiJycHJ0UUPLDdV3s2rUL5eXl2LJlS5rbunUrysvLUV1drbNIg57HlmWhdevWaNeunfzsl43LtB6iTlN1cYUWOoYuWJifCer3yWzD6FBrM8vGrRXzh1JbGWom6WA6U0uRCXoa9PuGwKQXV/mgr+cDg4jS7FUTMjUeDKYx8ckUjqHKL7S3gIxf0spH9Rc61d5RXTbg2RNhYRraw9IVofI08WewcvRCpvPLFg21AXWoma3yiEQiaTOXVVoAyM3NTaPJBA5notX1n60+Gbr8fO19B08rWhKhM4eFX3IPHjyIFStWpAmt35v89HsVlmVh27ZtgKYYPUw2id+7dy82b94M27ZlSxGLxdC7d28If+rQvn37sGnTJsAgFymtpF4wW7dujWOPPVZmtPBnh3z77beypS0tLcWxxx4rn6u/DD1OIQTWrl2LHTt2yMxLpVLo3LkzCgoKpByVlZX44osvZHjyt6gYOnQohD8dasOGDTJtYTDJs2zZMhQVFcFxHJnfKthmZnodqt6g9cb37durUAKBfqwcHPZxxx13EJSZo9FolIqKiqhRo0YNduoAq+4aNWpEsVgsbfbr5MmTA/L87W9/I19i6V555RUiZSD49ddflwOxBQUFlJubS//zP/9DNTU1VFlZSTU1NfTaa6+lzYZ98MEHA3ySySSdffbZAZo77riDamtrqaqqSg7I/va3v6WcnBw5gHv77bcrEnv4f//v/wX4/P73v9dJ6Prrr6doNEqxWIxisRg1atSIFixYQIlEgmpraymRSNC4ceMoGo1STk4ORaNRKigooNmzZ1MikaB4PE7JZJIefPDBNB3NmDEjEJc+A1sIIeNVt/UIc/pWGSan09ftpgd68L8f9gQxDQ6rJdfy1w0cOnQIlZWVDXbqAKvuKisrkUgkQluGbMBhUqmUHIitqqpCbW0tbNtGbm4uCgoK5OCpqbaGgXlHo1Hk5OQgPz9fDsgCQDweR21tLRKJBJLJJABza2AC07mui2QyiUQigUQigdraWkQiERknD58kk0nE43E5I9u2bUSjUcRiMUQikbTlftmAiJBIJAIzvvWZ4KpzDNtl6E6l91pJNb6667RCpytOKDNbdX/dNRTcpLM7Wqhx87Xa1Ku/2UItGLqfnla14mQTD9PrtqE6y0TtLKm0ljJ0pP9mgklHQoh6Oy4NgV4WgnLVXVv6TnYpf00DaRuo6AlTCwu7hsIUXjeSTcrQlc0yq34MDm8adDXFYYqPwc944FWPCwqN3sPUbUUYKkY8HpfhmF6ddSL8Qq0vQTRB1Yl+r+tPvz5amPKTuaZSyuc8fX+6SZMmYdq0abLWqbVChX5v8iO/e5+bmyu/I+bm5spemv5aICKMGTMGAwcOlHE/++yzuPHGGwN0L7/8Mq655hp5P3/+fLz++uuBjC4tLZV7fNi2jSVLluDVV18NKHf8+PH485//LO9TqRTOO+88zJ49W/rddddd+Otf/yrvAeDVV1/F0qVLpY6KiorQrFmzQKs0efJkLF68WLZMffv2xcUXXyx5kN9Jq6mpCei5pKREpsO2bUyfPh3z588H/HRFo1FcddVV6NSpk6yglZWVqKmpkYWSiHDllVeie/fuMr4vv/wSs2bNkp0tPa/0e5Offq8j/bmAJRwkkimcefYInDF0mNfE8RJE1/FmMfxfAM8GISKaMGEC+RVGupdffjmNTsett96aFo5nc/D9+PHjA2GSySSNGDEiEOauu+6Sz8Pieuqpp9LiUuPTOzDsnn/+eZ0VnXLKKWl0Kh8Tr7vvvltnQ6Qtd/y/ANdx6zoSRADBG8dSW4KfGipvUzxcS03PTFBrNpTwOg3/ptfEowObGxyXHgfbwKoslmHlvP56TSQSgVenKrMaTo1Df8YgpfVU9WpyPxeIAJADlxw46rAUAAgRtDnCBPkphTQpSlW0nqEqVPtMVz5f86tblVe3TfXBUV43q0KlkUrTaFQ7lLS1qCY/hiltak9Y1bda0NlxeD0d0CoC6yjMqdDjNT3LFkIAEDYsYcMWAq7r56nc6DoLcM3ct28f9u3bl6Z8VdGcGBaU97lTE1lRUYF9+/bJe+F/j+QPyJZl4bnnngt8lCciPPjgg7jsssuQTCaln4pIJIL//u//xsSJEwP+OsaNG4dx48YFCs3YsWOlDQUAV111Fe64445AXG3atAnI+MYbb+Avf/mLXJqoQwiBgwcPYuvWrZIHEeG5557D9ddfL+VPJBK45pprsHz5cti2Ddu2sW3bNrl7lA7mddVVV+Gmm26C46+fEH6vVM0DHbofh+vWrRvy8/Nl2nSaVCqFtWvX4siRI2kFVgcRIODtOdym7bFod0wbL4y+rUQYeOYq+dtBFBcXU9OmTTO6Zs2aUZMmTaioqIjOO++8NJvxxRdfpKZNm1JJSQmVlJRQs2bN5GxWtkOeffZZgmbfFBQUUElJCTVv3pyaNWsWcOyXm5trtH9U2ygvL4+aNm1KTZo0oSZNmlBxcTFFIpFAuJycHGratCkVFRVRUVERFRYW0rRp04j8WcA8A/ngwYPSHTp0KOAqKyvp+eefD8QPgJ577jmZVuZVWVlJhw4dosOHD1NVVRWNGzcuLQ3Mh7e5iEajcjBen+Uc5vLy8gIuNzeXioqKaNmyZQH966ipqaGBAwdSLBaj3NxcysnJCXexHMqNRcmO2DT+4Yc8BqbB4TAIv5mGXyMPHjyI/fv3Z3QVFRU4cOAADh06hKqqKp0l4vE49u/fL+fJVVRUIJFI6GQSXLOqq6uxd+9e7Nu3DxUVFQHHfmF81NpZU1OD/fv348CBAzhw4AAOHjwoWwv4r1GW8dChQzh06BCOHDkiW0ZGTk4OioqKpGvcuHHAFRQUBEwC5q+2NiwXz2AuLCxEfn5+xoU63GImk0k5GK/Pcg5zNTU1Acezq/UWUAfHx4PZ8Xg83CUSSCSTcFIOXIVvoNCRwR5x/Q2U+boh0JtnBvNXC0AYrQpWcn2KUV+5QrNf1PDsp0LlHZZeNUwmWdRnJjoTn7BfVVY9nHqvX+vpM4FpVF5h4erjmfbMTzb59hzUQseJ0w1zvceFBkxpVjMtmUzKgmVKGNNmGtTMFlywdAdNaap/Q8DpD8sANS6GGieD06by0X/Vwqdeq+FUnuo1P9Nl1OXmMGpLF6YX8j+fhSEgm/7Qh3DoMAkqlEVy2bJlWLt2LSzLguu6aNeuHU499dQAs6lTp+Kdd95JK0Q6VKU0b94c/fr1CzzfsmULVq1aJe+JCNdff31gcHjOnDmYOHEiLG04R43TFL/qZ9s2Nm7ciHnz5kk/IsJJJ52EXr16BYxuhn7PcF0XN9xwA3r37g3yC4LeShMRvvzyS6xbt07qYM+ePdi8ebNMh+M4GD16NIYMGSLjSqVSmDFjBnbv3i17pNu3b8fu3bsh/AbAdV18/PHHKC8vlzrq3bs3+vfvj5Qy43f27NnYuHGjpDHp7qyzzkLnzp0BP13RaBS33XYb2igHw+hIJBJ45plnsGXLlrRes6qLGTNmYPPmLXxwFf48fjzG//nPXjFTB4eJiO68806CMsvkV7/6lfdcW77XUHzxxRfkl2zprr/+ep0sgKONy4Rp06bJNPEvzzI5GtQ38KrPMhkzZoxOQqR10Gpra6lPnz6BcE8++WSA3nEcOROG03HvvfcGaIiILrjgggCN7kxLEBlhadI7gpkwfPhwL34/vj/zQLzakRBWeLOuwvS6zQY6H9Rjxzn+7phHExcM8an3fB1ms/0U0N8Cequg2s5MY1lWGp36LZzv9XAmE0TNP1WH6rVuJpFmbvA9u2zygrRVdX6xCiDNpgvLLG62fwz08Pq9Cv11yjD5haE+2vqeZwLrIywNuj71As4VSs9MnZ9+T/5YGQxfNMKgPlfl0XnzPWkFrb60qhD+xFKWzfGjdpy6imHf/8A9D4C8xSBCCCxZsgTr169HkyZNUFRUhM6dO6NXr15ySIHdgQMH5NBITU2NXJwRJtjmzZvx+uuvB/w6d+6Mk046SQ5z7Nu3D7FYDLFYLJBgHTt37sS2bdvShkr27dsnt+OPRCKBre5Xr16Nd999N8Bn6NChGDp0aMAvG2zatAlbtmwJHBGgu5UrVyIej8udnjp16oTWrVtj586dcoemaDQaWNTiui4mTpwoZ1TDt7tOPfVUwNet6289QURy2eKQIUPQt29fGQYA3n77baxZs0bet27dGt26dcMxxxwjlxl269YNruti+/btKC8vx/bt21FcXCyHaYR/IODatWuxbdu2NFdeXp7meGHQhg0bkJeXj/a/aINj2rTB6WeciV4nn+wJwzYd78d76NAh2rFjB+3YsYN27txJU6ZMoVatWlGrVq2oZcuW0rFfSUkJXXLJJZRIJIIvdQ1z585N25+3oKCAWrZsSS1atKAWLVpQ8+bN5Z7DYXYF+R/zmzdvHnDq4HCTJk3SDqSbOnVqmn1z//33B2iyxeWXX06NGzeWA8o8cMzXjRs3ppdffpkOHjxIBw4coEOHDtFLL71EjRs3psaNG8tBZn2v3kQiQQMGDAjI+PjjjxMpNmQymaTq6mo6fPiwHESura0N8CEi+tWvfhXgc8MNN8htMHgbjcsuu4zy8/OpUaNGlJ+fT8XFxWmDwzfccIOcla0PKJscb+Uxc+ZMb7uL6kqqqjpC8WSS3JTywZ9LtfDXkKqHjRQUFMj909SazH48qKu/TvRrE6qqqrDbPyRkz5492LdvH2pra+XzsPCHDx+WLRs7tcU7cOBAxiV4ptazIaiursbhw4dl688Dx3x9+PBhRKNRFBUVobi4GI0bN4Zt2zh8+DAOHz4sB5mzmZenw7Zt5OXlobCwUA4ihy1bVGHbttwGg7fRcF0X1dXVqKyslL+6nZdIJOSsbH1A2eRq/a08otGoN2M7Lx/5+QXeYh3fwLMABKYSq+9zKHaD6b3O17rBrxrJDF2J+uuTf9mQVguxLpMexgS9k8Lh1TBqHCpN2D3DpAP9V+fNMMmcDT9k4GmCHo9uU7r+cQAM7sTovNUOkeosZdYMO6YL8uHj5etgeYQAzyDWmaiFwJQBKiiD4Rk2czdMkXqCVH6mGSTZQo2T+agKU+NRr9W4wmbhqunVoU4qYOgFQQU/UzNd1clPAXWQ13VdxJVNhhhq79nkhGF6meOvmQiDnLrrMfBOaS4rK4NlWYhEItiyZQvOPvts2ZuMRqPyRD4damatX78e33//vaxB6gEbLGiHDh1w8skny+ER11+9Pn369NAMEUJg8+bNksfRgOP6/vvv8e677xoVxMo74YQTcNJJJwX8Bw0aJBfQWJaFNWvWYMmSJRll6tKlC377298GCky3bt0CNCqY17Jly/D222/LAmLbNoYMGYJjjjlGD5IRekEVQmDIkCHIycmRhdm2bRQXFwfoTjvtNCQSCUmTSqXw6aefYu/evVLGAQMGoGvXroBfuYS/J0ooHDpMrltnON59990k/IM8bNumX/7yl5RKpeThIEREjzzyCEExUocPH07xeDxggP7lL38J0JicaXBYH1Q1OZ5hofurjg1wxtSpU2VYvUORyf3xj38M8DGBZ8KofPUDVsKgPk8kEnTqqadmlNOyrLSDSUzgwWF2N954Y+B5mEw8WB0mdzKZlJ0dls80A7puINkhlxxyyBsYlh0JIYKtFPkzCbgFsP2DQfhVq9Lyr8lP/TVBbRX01wn/mkDa5AOOX5VDpeVfTpveGqn2SbZQeahxMPSWWpXZJAODZeDnum4jypJD5qPy41/1taz6m+JW73Ud6nHwJFMVpjeFzD8iz6myMZEuNCOTLcJ+pkgZOj8VauJYSKbXMy0TTHHoSmfzwAQ3ZMUbMlQaPWP0Z2r8akZyPGpB4mv1a4SqDzVvVHuJ/VUe/Kt/yWB98nNVZj2NqszqszDe+leUAIQNIWzuMQBqoWOGvKV8aWmp3INOp2nUqBGaNWuG0tJSlJSUoHnz5mmCZwM+y5T3VNu5cydisRhatWqFY445JtS1bds2cJiHScZ9+/Zh69at2LhxIzZv3oyqqip5orbu+MTqjh07osBwdmpDQUTYtWuXHFhdvXo1tm/fnpaJO3fuxKpVq7BmzRqsWbMGK1eulEM9XDBLS0vRvXt3dO3aFccffzy6desm94MTfsu9e/du/PDDD1ixYgVWrFiBlStXokmTJvK06a5du8qP+GpB3bJlC5YtW4bvv/8ey5cvD7hly5Zh6dKl2LdvX6CgWpaFLl26oEePHjjppJNw4oknorq6GsuXL5dnfLBbtmwZli39Dv9eugQ7du2qW3wtP/j77/CKigrauHEjbdy4kdasWUO7du2Sz/g9vX//flq3bh2tW7eO1q9fL2mYDxnsPpMrLCyk9u3bU/v27ekXv/gFtW3bll5++WXaunUrbdq0iTZt2kSbN29Oc1u2bKGtW7fS1q1bafv27fTCCy9IG4i3qCguLqa2bdtSmzZtqHXr1jR69GgqLy+nbdu2BZzud+ZZ3odqCE/G2267zbdNpEmSBn3rCyEsKi5uQq1alVKLFi2padOmNG7cOCIicty6SQx33nknNWnShJo3by5nT0ej0YDNOn78eNq/fz/t27eP9uzZQ3v27KF4PB6wuf7nf/6HioqK5Izt4uJievvtt2n//v1UUVFB+/bto8rKShmG8/Laa6+lwsJCKi4uNrqCgoLAFh4c7tChQ3TgwAE6ePAgHTlyhG688UZq1KiRHPzmAfCioiIqLiqk/II8eugvdXsOZzVdnROXadZHpkIXZhSb3Ouvv65xrh9vvfWWlunpcV1wwQV6MCNGnX+uF8YvdH+89Rb5zCGiFBG55JJDLrl+EXxmwjMyjLAsEvD28VDjH33F5URElKQUm9V0ww03pMnJ8nOh0ztEDDUvHn744TQePKVeBRcaLkCXXnppWjjdvfDCCwEeppkmYemAMsvk3j//2SMOm65OBqNXtUNUe4AR9nrNZEuZwLQsA9tA7ExQZeN7+DKpHZL67ETHcRD1zdOIjIrDOLDgwAZB+H9ybNO3UjwZCGQ7gEWe8eLLZVv+yn3X31ZGsYW4E6O+fjkNqv2mpp9frXyt+qtQwwllGwmdFztVJpXO0Rb9sFNp1Q6ZdEocDGOh4wAcSRqjkAKmgmn0AlEfdCNZj9sEllUHKZWHxwIzwbZtWJb3sdvxhzBTFg9q277jgla3IYcNv6K45E3Ldvyy6gKy55biDPI23IY28K7qXC8o/KumX2idFQaHM013gtw7zgtrGo1g/esdD1vZKFzNEyjLJvVGQp07HCjkYUsQmWjfvn344YcfYPvTVcjfH61Dhw56EEBR4OOPP44777xTClZcXIyTTjopTXEqHMfBPffcg7POOksKvm3bNjlbgnmrEEJgzZo1+PDDD+W9/tx1XXTq1AnnnXeekYfrurBtG07KwX333Y9/L13iFynCLy+8ADeMHYtkIun5kIArBMBtnRD44Ycf8MUXX3hDGa4LW7gAiN+3cF0XXTp1wfAzz4QgggsXdiyKCRMmYNasWYHCc+qpp6JJkyYy/f3790fPnj3TWml+bts2li1bFtjCgohw9913yxnfQgisW7cOP/zwQ6DAPPXUU4HZ1LZtY/DgwWjatKnM6379+qFLly7y3rIsDB48WG7ZIYTAq6++ig8//DDw1WnBggXYvXs34LpwAfzX/ffjoQce8F629dl0H374odzHLCcnhyKRSL3bGJBv3EKxrwYNGiT3U0smk5RIJNIcn0yt4u9//ztZlpW2Xxo7y7LokksuoVQqFRjEVp3jODR9+nR5EjU73lPN20sNlJ+fTyNGjqBn/vYkvf3WGzRt6lv04QfTaOasGfThzA/pg1kzacasWfTRrI/po1kf08yPZ9MHH82k71eupJRLlEg5lHBcqnVcirNLefp47/0ZFI1GCQDZdvCEbPh2TzQapfnz5xMptpO6X6DJAaB77rlH6kvtLKh45hnf7szgYrEYLVmyRPIhIho7dmyARpVRpdPB23Pw4SX3/vk+70GYTafCcRy5f1o8HkfK33+soRD+oRs8uBmNRtOcaYU9+a9Ijld3XANtf3Ey81cd127HcQL2iOPvqeY4Drp374533n0H77//AW668VZcfMnvcOGvL8G5512Ikef8EueOPBfnnTMSvzznHIw6ZwRGnTMCI0ecjfNGjUSPbt1gC0LUFogIQo4lEBO+swTgAuecfTamvz8dnbp1huN48estLpSWWrWT4OvB5HRwK6bz1vVqgsqPw+t86ruHkmfec89PJatXEpWpKQJowoaBjuJwEGSI82gQpvhTTjkF7733HkaNHIWcaBQOAUl4LgEgAUIK3msCfpVnk80BkAKQgoALAUcIxBFHUtTCFUmAXIAIOdEcnDvyXEyf/h66dq/75qqnLxtdMvSwJjC/sLTrCIs/rBCawK9d79rzU62DUEk4clMk/BmGoQrE15kWCTcE2bSqmZbEMcJahqZNm+KFF19Ap06dfBoHjkigApVYWLMaUw/Ow6SDczDx0Kd4/eBsvHZwNiYe/ASv+e71g7Mx6cBsTDr4CV4/+AkmHfwMUw7Mw/v7F+O72i04YCWQsglkEdykixO6dMPTTz4t57OZZMoWHNb0aYrB+ZFNoROGUxgzfm0IgeXv4Aql76/mY9b7hnKBIiIsWbIEzzzzjGxCdcVFIhHMmTPH+EzF0qVLMWfOnIABPGLECPTo0UOGO/nkk/HHP/4xNPHkLyV0tflhOtQKAbJAlgu4hAt/dZ63nNABhHBxxKrCosR6vLH+YyzYshhH4pWoFQLJCBBNpRB1gFQkCkcQCC5scmG7BAsCKeHNHIulLFiWQLOc5ji93WkY0+U89Iy1gy1skEs488wz8Ktf/QqTJ0/WxQwF6z4SieDSSy9Fly5dpLlgmnI/ZcoUfP/999K8+OabbySPMBARnn76abRu3Vr29hcsWJBGo/P44IMPsHDhQpBv5riui2HDhmHYsGEgNwUXwJDTz/BeEcjQkWADccaMGQTFkK1vdkeYGzRoUNrJfM8991wanToCrncqMsFkPKt47733pOxCRAmWoFgkQp/M+oCIiByHqNaN0we131CfOWMoOrU/RWb2oZwP+lDOR6eSPWsg5czsR40+6EONPuxP+TMHUO6sAZQzawDlzjqVcj7sT3kzB1DORwMo56NTKfpRL4p80Jfy3jydfvXxrbSuZhM5LlHCT9Pbb78t08wdAt1IJ3/WD9MIf3PqTz/9NEBDBoP+l7/8ZZpu9Y6L7rJ5FovF6OuvvyZSOjt/+MMf0uhnz54dkIeI0qer69Df4Vy6yTDkwDC9ZjNB3/ILIc25qXYx1Gf11WQGkQO4hGbNSnBc5+M9PwvYKg7gpVVTsfjwKti5NiIUgWVFYAGIOgSChUTEhmMRLIcQSQiIpI0U2UhFI0gJbymnK2KAyIEbiSDVmDB/72K8uGQyDogawD9fgY8A8OSpX2ZOGxlmepjyxDRplqHTMnQ+nI9hbxCmZXNLpa97C6ZA5MBF3TJXMzcFqvHPidaFg2Y7ZCokKlTeLCT/QuGlQr/nhHL8ulwM7rH6dwAAOxJDLJYPgOCC8N3hdfiu/N+I5jhw4YAsgZQlkBIAyEZuTQ4aHShAs/1N0PZQC3Q80hLtDzdDycE8RA8TKOUiSQ6E6wCWBRKAsBwkGyXx1Y4l2FS1TX7p4HUNurx6YVGnMUGrWKqudKj0HIeqOz1e9lNpOB/1eNTVYtAKHYepo4lACBuWEr99/wP3PCCQvrCDC9a+ffuwdu1aHHvssWjXrh3at28P4e+3ZoKpQMI/RfrKK68M1Jpt27Zh586daN++veQ/YsQIdOrUSdLoBUr4A53Lly/Hpk2bsGnTJjmThH83bNgAW5sFu2/fPmzZsgXtO7RH+/Yd0L5DexQVNsUFF/4KRUVFSMLB9D1f44ttC7zWKmLDhYBNAjkJG00O5+Bkpz0uaXcm/l+Xc3Fpt3NxQZfhGHHsqejXsjtKc5ogcaAaieo4KJKCZbkQsCFcARIu7FqBYa374rjGbQEAu3fvxosvvijlg1/Jjj/+eBw5cgRlZWXYuHEjPvvsM6xatUrqwLIsXHrppVJHqn5UTJ06NRBOh8nftm0MGjQIPXv2RKdOndC1a1fU1tbi8OHDMoxt2+jQoQMOHDiANWvWoKysDJ999hnWrVsn896yLLRv3x6VlZVYs3olVq5eBRIWSpo394bUM9l0rr/kTT01OZFI0KOPPkowvPczuYEDB6bZdMlkkuLxuDyIo7a2lpLJZL322Q033ECRSMR44Ab7PfbYY0RaOhKJBCWSCYr7A9HPTXiB1q5dT0RE1ZSk2za/RLEZp1Js5kASswdR5OPB1OztwXTKq6Po0QXP0rrDmyhOwTSQN95JR6iavjuylu6Z/wy1fWsYFb3fn6IfnUaxj4ZSbNYgaj15BE3bOFfOUlm2bJnUjWov80Eitm3LX9XWikajNHPmTE2CdFx00UUB3np+mFwsFqOFCxeS4ziUSCTIdV35MZ/58EEl6uA6D7YzjRBCDrpHbYuEAP0XL/fMxqazLCtwanI0GjXaXQ0F+T2xWCyGqH8QR05OTtpwjApunnlg2HTghurH4BoajUYRjUQRiUYRidjIjapxCVgE2CmCDW8cPa82gg5VzfCnvlfjtv5jcFzhsbBhA67rfWf1s0s4QCPKw0mNOuO2gb/H2BMvQ2FtAVxhAeTAdgWSwkJCeFNXdHC6yF+9z7O21dnb/xsgv/dpWRai0aixNXT8SaTq4DoP/aj0POjuuC6Igiv8Qwud+m4PGxphmITLBuQPGLPdwPYAP9Ohx8OvFtUx1IoheZE3mpsC4MIBnCRIjiRZiDk2LBAckUTMJZQcjuKKEy7AqO6jYFveEenkJuFaArAIQhBIOHBsFwk4cOCiCDm4rutl+M3xoxCNE2yRhI0kYhDIcXg+Sjj49cTXMOhCv/+pIJQP/mH5wDKF6V2lE8JSPvrX0YTqgBlZ/nQV1U+HLpgJiUQiQMfC2v7sBUubTRLWY4Jhuo/qGHwdUIzwJorEAFiIwBF+QfRVYkEgbjtIRZLIrSV0s9vi3B5n4Yiw8P3B7YhTEkdEEgur1mFp9XpsqN2B3e4hfHdkHRbXrMZnO+dj2Z6VKKRcXNR5BNrmNge5LlJCwE65iCmtlq5Lll/t8Jj0mvSPaWoITHxMIKK0Do4qi0nHqp+eF55/etyh7zLXH2zdtGkTZs+eLQsfEaGyshLXXXcd4AtH2tQcaCPgruuiY8eOMiFMv3LlSnz55ZeSjv0ZqVQK3bt3x7BhwwL+Z599NnJycuoKkwL2i8fjmDBhQkBJgnuxAiA3Ccex0axpMwCACxeOcCGEhVgSiNUKHF/SGS1yS7DJ2Ye3/vUmrh18GWoaxfDSosloXJCHA7sO4/zB5+KDpZ8iVggc3HkQ/UtOwXHNjkOHvFK0b9YGm3fugGXHQAJIKfUolUph+PDh6N27d1rvEFqLovsvWbIE3333HYS/JHDgwIE444wzAnQMTn///v0xYsQIWWEty8L777+P5cuXyzgcx8Hzzz+Ptm3bwvGXErZs2RIPPPBAoGC9/vrr2Lx5sxJLWMH2TRAdYR0JHvj74IMPuLhKp07hbgj0zsHLL7+cxlt3l1/uzbjl8DqPMPA+e5ncn+7lmQ8uVVGK/rThZcqZdioVfjiQSt4YRA8tfoHilKTVzg66eebDtKZ6Pa2mbXTxnP+iq5f/Nw16ZzRd+OXtdO6CP9Jli++mi+bcQc/++12qTsRpPx2iC1fcQ/aMvlTwwWD6xaQR9M6GObIjsXDhQnkIS0PBe7+xMy2T/PWvf01QBnVNNFdeeaWkCetw6DOHiYgGDx6cRhfmeJbJ3byHXrYdCb7n62yNW7V2wFBrGWqtVh0Mg8XsX9d8B5FVXIZU+xIAIgKCjZTtYk/8ABKUQA7ZqK11MH/jUpTt3YBGNUD+QRfDuw5AQSKK5IEaxBIR5KWiKIpEEbGASiRwKFENEgTbnxaQslywxKRso8ppUZ0O9ksmk7Kzxfmhj+3BkH7uWKl5orZ6UPSvmlR6XmezGbYJqjgG9XvQC52qDL0ghEFk/YWgThG64vVE86tILZjQwiJkooAQAv7xQEYIAAQHBAduDrB873rsSB1EE6sYPVt0x+aNe3B4+2GMKu2NYcUnY0hRb9zW/xpc1Px0DC/sg+OTLUGHalGJWqxN7kbZ3i2wIhZcOHCFC4tIKpz83jsMlU0vMCpI2WI1U37oHQIG8xbK1HTdRlbtStOrP1S3hsLOodUD6SKAnwe+cDt27MCuXbtg+d3m9evXA0oBEv6A8fLly2XPs7CwEMcdd5zR+NeFUNGsWTOcfPLJgZqmIpVK4bjjjgN8hfDzTZs2Yffu3dLGLC4uRqdOnQLxH3vssejVq5f84H3gwAFvAFNSIG1jF4DgWg6SUUJcACuObMMHm+fjD50uwnWn/RrwpzJF4MIiyw/t4sR+HeAAsHu4qEEttuIQ3l77OXZVVcDOE0jaAo5FiCnRRSIRrFu3DgsXLkTK311TCIEePXqgqKiojtCHmqlckPh68+bNmD9/fqCAtG7dGqeddhoi/uF/+fn5+Oqrr2SBEUJgx44dgN+wcGE++eST0aRJE7j+WbT60kUA6N27N/Ly8mShXb9+fWA/ZSEETj75ZDRvXgILDuKppDeYzSx0m+6BBx6gvLw8atSoERUWFlJeXl7gnS+EoJycHHk6dW5uLo0aNcq4R1p9iMfjVFlZSdXV1VRVVSVPj2ZXVVVFtbW1abbcTTfdRLFYjPL8k6UvueSStK0Q4vG45JNMJmnatGkUiUQIqFvpdc+9/+UxdF2qphTdu/EVypvWl/I+7EM5swZQzntDqNs7l9CUbZ/REaomSjmUTLlU6xK5SSI3ReS6SaJUipIpItcl2kb7afyOf1LJ++dSzkenUc7M/hSdNZBKpwyj98vqPtQvW7YsMBgciUQoNzc37YO/jkQiQSNHjiQo9po+s1oIQW+//bYcFCfl0Dx1trRpQHfRokVERHIWtqpX15+EoToioltuuSUgjxCibusLN0kupShFbvBAOigl2XEc1NTUoKqqKrCHmtoKxeNxeTp1bW1tYE+5hiAWi6GgoAB5eXnIz8+Xp0ezy8/Pl71UFTyTuaamBgn/ZGmVxvV3Cmc+EX+msrkrpYDgrWmwoyCyYEUcbLbL8cDCp/H8ujexlrbjiB1HQhBqIoBjE1LCBQQhZQObxCH8Y/ssvPDdmzggDiJC3od5i2wIsuD46/Hg65NbEx7M5oHWbCGUEQOVh9oSqq9waIO7/DqFkv8cv+Uv3OE4VAjN7tOfq28lb4KDl3D2S3sf8gOOjO9VZejPoDW/2YITrSY+7Lkalypjpl+dr7ziJYCscL/pg/DjIQu2ayFCDpL5CazP241Hvn8Nv5/7MJ5c9zo+r/gKO2u3I0IpAAKVFuEH2o5nyibj2SX/wF6rAiKSQgQEy1e6kK9jXwQlTWohaUihy6Q73e5TTY8wvfIzHaqfKc/1X/1aN6LTCh2/89WaYCpgamKTyaQ8274hUAuvnnj1uRoXDD0xfeBZlZn5xmIx2YOy/OHJXMvL4BQABwQSLlx/1CBlO6iNCIByEEUe4nmERTXL8fjKVzH2swfx+OfPY497EAdQi1k13+H2RY/i5RVTUGkdQZ4bgQ0BBxEQCaQsgu0I2ORIO5L1q6edr/m5jmg0GtpJMIH5qT1eUwHUYcobtROn/po+XQZ5ammUSxAJgPBmJ7z33nuyed22bRvmzp0rAxARevTogd69e8vEN23aFD169EBEOYOeaVVkuucMUP1d10Xnzp0xZMgQSQcAb7zxBj7//HPY/izVPn364Pe//30g/KJFi7B06VJY/j57S5cuxQsvvgDXdSEoCkIKF//qXPxz0mRECwqREC6e3vQaHlz2ClL5hIjremv0EYGLiLfckBwADkTcwqDCHrhx2NVYvHkZ3l39CcrcnUAkhRzXQgpRJCOECKXgWi6AKI7d3QhPDbodZ7Q/AzkAdu3YgZEjR2L58uUyXdFoFHPmzMHgwYOlPr766issWrRIGu3C78hVV1fD9b9/wu/BkvI5sbS0VJ7UGPFnck+bNi1NxyoikQi+/vpr9O/fX38E+GEcx8G0adOwbds2CH96+9SpUwNLGQHgww8/xLnnngvAGyYiWLA4Sn0vE9K2Dpg1axbBNw555u0dd9whnxMRzZkzRy6v+6kdDw6rxqwJ+nPT4LAQgiBAlogShEXHlLakzZvKyCWiBBFN2f0pNX/nDMr5aAA1/qAvFX3Qm/Jm9iX744EkPh5MkZlDKPej06hgxkBqOesc6vzlxdR46mmU/14fyv3oFMr9uB/FPhpIsQ+HUmTmIIrN6kf27D6UP+NU6v/K+bRyz0pvawo/CTfffHNAvmg0SvPmzZPpISK666670tLRkFkmevpVpz+PRCL0zTff6KwC4FMQ9bA6vw8//NAPEbI/nYe6GqA2vwy1Zui1RdTzrfTHQG2W9XuTTAxdHvlKADy9ECHlEpJJ1/skS4STmx6P44s7gBIWHMtGPAKkLAcQSUQohRg5EABqowIVVIkNh7cjng84uTYcO4qka4MsGzFKItdNIeIA0WQUeVUxdC3uiDaNSyFc9dN3OMJeXdFoNO0NYWq11Fegnl8/Bnpeq/z1PAiDDC38jRH1gOrgLL/T9Xd7puujgYmXiafup8qvD5gSeQXNgoAgAiBw+NBhVOz1Djm2HOAXkZa4ovv5+EVNM8QqYxBuDoAIIo5AzAEEebNKbBFHFCnkCsB2CIIsCBKwBAFIoDYniaTlIOrmoNGhfHRMHIPf9f8NGseK4S3+r6us6i+/ClXovU+RIdNVqHxMhVRtMEx0CBkYjsVigVc9DDxhGNRXkW4B+iDfpigsLET37t0DNkNpaalOnoYWLVqgtLQ0IIhJOSosy0J5eTkqKiogDF8zOHx5eTn27NmT1pqxzJZlYdeuXYFn8No32XOFINTU1mLOnDnod+oAAEDMFbig9WDknibwz0XTsXp/ORLRlLd2FQJx20UMLnIdARc2XBEByN9JXHhfMshy4UCgwI2hqCoXPQo649rTf4chx/QFkgQIF5ZlY9OmTdi+fbuUjeVesWIFotEoXH/CRXl5uSe7rwsiwurVq9G0adM0/fC9ZVnYs2dP4FlpaSk6dOgQCFNWVoaKiorQTosQAhs2bMDOnTvlfTKZTJs13r59e7Rp0ybAQ90zUEfoXiaMeDyOyspKmcGu68rxLy4Ec+fOxciRIxGPx2Vhue666/DYY49JPmGJ0u/HjRuHSZMmwfIXd1x55ZX45z//GaC7/fbb8fe//z0tPJTM4zMNdAhYchcvIqBrl+Px5ZdfoEWrVt7mN+Qgabsoq92BFTvXY8f+nUgl4gAIScsBwULMzYG3ABFwhQUSNgQIFrmwhAsghcJYHo4tbo2erY5HaV5rkAs4ArAFsHHzBpx7zrkoKyuTX3XgF5a8vDxYytqQRCIRGHsDgNzcXHNL7kP4s2x4PA4A/vCHP+CJJ56QdEIIXHvttZg8ebLMM9u2MX/+/EBH4o9//CNeeOEFWMr2uLW1tV6HzB/iefTRR3HzzTcH3oS5ubl+GK+/buxI6MhktJM2Y+Tzzz+nnJwcgj86DoBuvvnmAH22uPbaawN8rrzySp3EuOTN5HTjFgBBWARLkLC9ToUAaOzY6yie9E/8SXhfGxx/Pzqnzv4lhxzfLCZKkENxqqEk1fjdEO+Zd0WUJKIUud6OdkmXEo63t11tdQ2N/t1lUj79q0CavEoHoKHLP1WevCmjissvv5yg6Nq27bSORNjecyrvp556KhCGAuUnQ0fCdevey1wb+JprDNdK9blKp/qZ7IFsoIfT76HYa3pLx/f8S9p4nefv7y9H3h5zBODFF/+O22+/HQcOHACigIh4xi474TsLFix/NzqbCBHY3vR1fwKP5dsrwvV+LZ41GhGIWsCe3btxww034I3JU6R8+qtNTVOdzB64ddGf6XpgqPmi6kR9DoWvMAxO6/GZ4lXDBOKEALnethoEyA9ClkcICBGMXBhm86qZrUbOxqVQ7DC9+c8WbAAzH92whqFnytALPl+rDkQgZR81TuOEZ/6Gc845BxMnTsTSpUuxatUqrF27Fhs3bkw7cK2yshICFixEAYoAwpafewQACML+/ftRvnUrtm7ditWrV2Py5Mk464wz8Oo//4E66eqQSXY1k1U6U5j6wLz0a45HH+TnpYQmubiw6YPVUmYBCMtbguiVBj9PAa/AAV6hWrFihdzHzHEctGnTRg5WMrPVq1dj6dKlsiCuXr06MHuBiLBmzRpMnTo1reboUBNjWRbKysoCBXr9+vV46623ZPyWZcmDUziutm3bYsiQIUblq4rle/Ltl++//x7Lli2TNN9++y1yc3Nx0kknwbZtxGIxrFq1StIIfw3Bk08+iYsuusgYH+Oxxx7DlClTYFkWqqqqsG+f30tWFiLrsG0bo0aNQqtWreD6e+bxLGH4urJtG+eccw7atm0r82Pp0qVYuHChzq7BcF0XU6ZMwcKFC+H6HRmOmxGJRHD++eejTZs2cP1vx7169QrQCP/0802bNsHy1xT37X8qhgwa5JW7usFh71183333kV8kCQCdffbZ8h3Ng8Z//etfAzTQBh4banvoju2cTHyYBg3YT1gHL6XkeIQQNH369ACNvok1AHrttdfk8zC797rrrkuTV5XZ5GKxWNosk/Hjx6fRfPzxxwGaJ554Io2X7vTDS0ix6epzat7GYjFasGCBziptNgrvT8fu1tvrZpsHxulgeC2qrzK+Nr3euLXglkRvYcKg03F4hNhzDG754NPptPzM9MvX+jdcUg7w1cOpra8elwmqHnWdqL86X33LCH28i5QZxwydxgROR0PAsulhdRlJMVPY8WuZS0ok4s9u9m1fI7hgqYWCla0XFPVZNhnCYAH1uNSCEYaw52TYpFt9pkKNj6EWMvVeDwvNsM8EtVDB56WG0+NSr00V/Gig81bvw9Kg0vG1SQ9h4cMQmiJWkNp5YAWYjHuGSYFhIMOSO1JqTbawtLldanihtDKq43Aq1Geqshl8rVasbCqZmmF6JvI1fHlUuX8ucDr1DkA2oKPc3FJFaOlhg3fNmjV46KGHZOZZlhVYNshQn7uui1NPPRXnnXceUqkUbH+2yksvvRQQuE+fPvj1r38Nx1/uZts2pk2bhsWLF6dlfib88MMPuPPOOwGfPpVKYeTIkRg+fLgMv3LlSvzzn/+UhSQSiRiNbz2zhw4diieeeEJmFPmn/sGPSy+4JhARevXqhauvvhqkVICpU6di7ty5Ad5PP/00pk6dCsffH+7bb7+Vz35qXH311Rg0aBDg57ceh6oLNa1dunRRqI4C+uAwG671GfKqQczX6oDhLbfUHfpBRPTdd9+lzUQZPXp0gIaI6Pe//z1BMe4zOTU+3Y0fP55IMfQ//PDDNBqTe/fddzWJwpFpAP3666+XMgKg3/3udzoJ3X777ZImUydDTWc0GqUZM2YE+Dz22GNpYXR3ww03ECn6CJP7p8L5559PUJYg3sGbowdmmZD3w6WbaxfXQt0xjVob1PC6sZlMJtNqkmq0q69Y/lXj4V/VMa0uFwwDyLa/l0kmqOEpxH4x+WUD3YRQ/dgfhpaWn4X5/xQIS+tPAeZK5KfVvAK0DpyxJsfPoRUUViQXqEzQ7TDVT4XKX42faXV/ZNmjg6HiqHuvmTKa/eqz5fReMMuj8tVHCljfJnB8vKZChV7BTWAaUxxhaf0xkPaif59M1skcatOxYC1atECfPn1kT00IgU2bNmHNmjUgvwY2a9YMffr0kYUglUrhxBNPlHzCErRt2zZ89NFHUsBIJIKNGzcCinLatWuHXr16gZQOxvfff48NGzZIPq1bt0bfvn1lPMlkUp4anSl+GJ7PmzcPrjZ0oWaS67ro169fYCdNE/r27Yvdu3fL6eXt2rXD1KlTJa9oNIqVK1cGwliWhdNPPx0lJSWBOFUZXddFu3btlFBAz5498Zvf/Aa28lVITVMqlZJ2qIqvvvoKGzduRDQaTZtUAC3dpnsd6vOuXbuiVatWsOAinkx6kwj4sbTp/Ff8gw8+SFBskREjRgQOBnFdN+1gktNPP52qqqokXSKRSNsv+Ntvv61bAqjYMbzfmb4kjukuu+wyIn/wkXnedNNNgfjPP//8gK2i2it8PWvWrDSbUpWFf/X4TU4/GVAH+/OAKRHRlClTCMqgth4n/Jm7X375ZYCHGoeeRt3VB5XGdd2sThE/Wlc3c1iJ0589UfcuC28MYCsHg5iaYuH3PNlF/bPtgWDp18O5/iQCRzlUhLTXJF9bGZa8cVh+xs9NfEzgZxx3GC3z1eNXw6lhuWWG9lpmOl2Xlv/pkelVx37MX5dBv4chzTqN/npn6HRhUOn0dNaZAARveyIoC6MaADURaoS6stVM1P30e12pJugZqttTpu4+I0zmTFBlUu8zZbjqGGTYr1do44iqfFwgTeAKqusgjJ5hyguGakfb/maIetrqgynNOg895gYVOga//zkhqVQqMDuBI1UFys3NNRYA5qPyU8FjeCovvWdq+Su+dHAGA0BeXp7+OCNUWcJk0xWu+6th1IFYvUVnOYUQcn84HaaCwRlskgFKGvSCz+BJrlygVToTTzUf+DmnU9dXps5N2szhhx56CH/+858lsxEjRuDjjz8OKOirr74K7FkH3zBWlaH+Wv6061deeSWQsJNOOgkXXnhhqFKEcrYow7IsfPLJJ1i4cKGUsXPnzvjNb34TiF9VguXPXnn33Xez6tUyX/j7ul144YUBfrzzge1P4deRSqVw0UUXSeNdCIFVq1Zh5syZUl+2beP9998PLN2LRCK48MIL5QwSFVzAAODKK6/ECSecAPi8586dixkzZsgC6bouRo8ejVNOOSXAR88fdRNtTvOECRMCnbRscMEFF+DMM88E+V8rhBAYNWqUf1JmhiWIjIceeoigdSQog9FMRDRv3rx6jW+TMw2Y6lAP+VBdtka/7lQDXuUTxtc0A/qKK65I46u7p59+mqgevfHywoamQT+12jTrZ9KkSfJ5WPwmDBo0SPJQdWGSkf04rWZkmDmcLbgVUWtQKpUKvBa4RtUHNjZVW0bnbWryVf56i6A+C5ODa7Va83Va5quOibEft1YqhOGbL0J4M5g3tzTsTGDe3JlTYTIt2ATh+HW96noj7Ts4FLnqA896Ue1Mnb+KdO2FQFWmLkwkEglMt8kUoQoWMiyzVBrVT1WkCpaLC4X+nP1UPjp0hamFzpQBqrxq5WEZTAWUoRcMvjaBeaey3GTHtHRRlV9PC+tND8fxmuRiP6bltOpx6Uiz6R5++GHcd999MlPZplNRXl6OLVu2yPuysjJMnDhR2ktWSG9SFYSI5KAm07r+CdTHHHOMpJ87dy4efPDBQMLKyspQXl6eMY4OHTqgQ4cOgSEI/iV/oHnTpk0oKysLhD3xxBPRsmVLWYh++ctf4qabbpI0AHDVVVcFVqi1bdsW3bt3D8hz+umn46STTgJCDHnLsvD3v/8d06dPlzLZto0+ffqgWbNmaWGYRgiB++67L7Bi64knnsDtt98eoL/zzjsxdOhQpFIpGVaFfs+45557Aoee9OzZE+3bt0+TB4pOe/fuje7duwNKpe3Xr5+fjw2w6djxzGFSbIOnnnqKIpEIxWIxikQiNGzYMDp06JA8hIQPJMnkkskkTZkyRe7Pxnu0Pf/884H4+CANPqU6lUqlbcdgcg8++KDxpGv2S6VS9Je//CUQRghBb731FjmOE9ifTcdVV10VCHfNNdfIMKlUihzHoRtvvDFt8Ft1fOiHai9FIhH69NNPA7xMTrfReLBedZniVgfjdafzeeqpp2Q+mJzruoGJC5yWqVOn+tL9SJuOS7brnzTNazJd15UHm8RiMXkgSSbHtkkymZTO9Oqw/B1BI/4p1eqAptpy6rD8IQYOp4bnX/3Vxy2gGlanMUH4ryYeHOcwrjL4rTtOK7cMMMQf5jKlm5Epbnaucso3OxM4fSantqJqWjIhTaN6gkxMdBqE0B0NVN6meLJFJnlUJUGLJ0zxmZAproaADIPJ7J8JP0ZPPx/CZUordGwDMUwfvlXjmu/1jMwGJgWb/HTwFKWGxGUCp1Xlk0382eBoKg+3fDqyDf9zQH2zqFBbNb3MAIDlH7Pprf61YCl6ln1t8o3Uvn37YuzYsYhEIkilUnIQUqU75ZRTcMMNN8C2bTiOg86dO8uC0BAFderUCTfffDNsZZ8UXs7G8qxcuRIzZ86UfC3LwpIlSwA/LlMmIcvCM2jQINx5553y9eE4jpyd8lOCiNC1a1f8+tfeZtkMThOnwbKstI29582bhzlz5sjBd9d1cfHFF6Nr164BXjouuugi9OzZM9CRyCZvJk6ciM2bN0vamTNnYv/+/Uj6W+xaloXLL78cHTt2BHw5R44ciSZNmkizwrIsLF++HIsXL4ElHCRTLoaccQZGnnW2ZynqHQkTspnNEOZ/NFCNd56dobuwAUt2PHNYBxvFP0ZeU0dCB8+EYXfJJZfoJKFQ9Xz//fenpU2f3WxagvjWW28FaLLFkCFDCL5+TR0LAIGTtcP0yDOH2d38x1u9B/pG11zj+Lo+p9JmU4tM0HkyL26puPbAbxk4nqONDxpPTocKNX0mZHrGaIicqi75l6/1gV/uTNQHNoHC0mLyc5QJBfBpWOecDn6jqc9JGVjm8Kxj20++mg5F+/IqEBE3qXqPRVVqNooNgx6XyheaclQFhtk/9UHnD63g87NMadKf6ffQBn4RQsPQZTLFr1aUbEwHRpiOdP5hfjp0vbn+5F61bKhw/OgTibq+gSx+Qnh7T2zfvh3l5eVpSmOopZuv1Wf1QS9EanjHcdCxY0e0atVK+rds2RIDBgxIa/HU34qKCqxevTqNt/q7f/9+OVNX+Mvv2rRpg+OOOy4QbuXKldizZ4+0V4855hh06tQpTZnw+RARduzYgXnz5sn02LYtB8+ZRi0orr9lw/r161FeXi7TRkQ48cQT0bRp07Q0ZipoJtk4TZY/UF9eXo61a9fKuBzHQdeuXeXhJKiHDz9TdSX8yrF27Vps3rxZ2ubw98M744wzEbEI8VQS3VVbWd1zmPytFnJycigvL4/y8/MpLy/vqF1ubm7AmfxUF4vF5AFoLE8ymZSnaqsnbKsnbX/00Udps4IfeOCBAJ/PPvuMCgoKKBqNUk5ODtm2TXf7K5SYxnVduvTSS8lWTpXmVVQq3dVXXx2Iiwd7eZCbB81Vu/Piiy+WfBh33HEHRSIRysnJkTr/5JNPAjQPP/xwWlx1A68ennzyyQANtA/+REQvvPAC2bZNsVhMDsRPnDiRSLGhXdeVh82F2cvRaJQ+++wzSU/+/s6Wf4AKDzxPnTqVHMehZKKWEokaiqdSct81xabzfpPJJOLxOGpqalBdXY2ampqjdrX+wSbsTH6q48FmTx6vJbVtW56qrZ6wrZ60rdoZYSDl1Gh9w0BujYRvSzrKqdJMw89NcPzBXnacDuarQ/VLpVKIx+OIx+Np20X8lCB/2hEf9pLyT55GSAvXELA9xzzZNrQsC5FoBJGot6sXp1oWOo73xwrA4KZXdfqzbBFmv7EfF9BMUF/P6jV8/iyP/ssIK0DQaNX0ZiqoKpiGX4X1IRsaHWq6TPo/Gp4M1qfKU/Ijb2s2efZ8sNClK1sXrCHggqA6/RkMBVDNAF0mXTHsH/VXM5nANJFIBPF4HFDsI+anFkKu/fyM76Hw0u0rtXDxtZ5ujhtaGjkMNL7sp7d+juOk9Wh52aQKXVf6G4S02b2cD2G6Vmn0069NvWkpk4jAsiKwlUqbNsvkkUcewZ/+9CfJsG3bthg5ciRgEIRpwqAmQodlWVi7di0+//xzyZf8mavjxo3TyQEl/vnz52PJkiUysTU1Ndi1axccfysGACgqKkKTJk1kAYjH43Lza/ILRlFREYqKigKFqaKiAjU1NZKmUaNGaNKkSSBcRUUFqqurAV/h33//PT799FPJRwiB008/Hb1795Zfa3r27InRo0cH9HHXXXcF9mW2bRszZ87E2WefLTsbc+bMwezZswO6LCws9E8A8nqN8+bNw0cffST5AMDrr7+O0aNHy/tvvvkG06dPD7SmF110Efr27VtXGITA0KFD0w4iYQi/k3T55ZejU6dOSKVSiEajmDVrFr7++usA7SWXXIITT+wJN5VA0kmh74CB3uAwDIPD+syLc845J/D8p8Q777wTiAsATZgwQSdLgz7wOnz4cJ2EHnjggQDNkCFDKJVKBWh4fzrVvfnmmwGa559/Po2GlyAyJk6cSNAGrJ955pkADWmDvmQ4YMW2bZo9e7akNc1wISK64IIL0mTS3euvvy7pwwZwVTANDw6bXKYBeZ6lEjaofOMt/gzsTLNMuFZlWmCRCXqraIK66jysRVTBPLmFU1sWffaqzs+yrLRXFUN9vWaSm3nqNKZXMPuxPcquodBNAbU1ZxNET6sOVe4wVx8PFRyn6qDIyPyEsNIHh+vbVgIGoztbqImoT9lhGaImAloh06E/0/mpijU9Y5jsNdO16R6G8KpcJrl1qDw5jMmPYZIBGfw5vEmusDAMk/ycd2pe6X4AIITSkZNXITAxayjUROkKzAY6nV4RsuFpojHR6ka6fq9CD6/GoXZITBnM9zrUVlx30Hq4eiuoQtcRDPGZ7jPpBkr8el7CKAcpR+z6F5RhLxMdQqlxX3zxBd599105As3P9Ej5meu6OPbYY3HbbbcZezphEEJg8eLFeOWVVwJK5OWHPwdeeuklzJkzR74WS0tL8Y9//CMwrFJWVoYxY8bA8vfia9mypZyuzzR9+vQBMmSeCUSExx57DJMnTw68slUdCyEwYMAAXHDBBSD/WKdZs2Zh0qRJAV4vvPACPvnkEymTKW9UMM3q1asD/ipc10UkEsF//dd/oWfPnrInPWnSJMyYMUMnD0dYR4INRtVIZ2PTNAJenzvxxBMpHo8H+JhmkOgdibAliFD2sBs+fDglEv7hIz5MHYmampoAjbqvW5iRPHbs2EAYUg5YYTdmzBidhMjQcdChnnAohCDbttPiNzl9lsmzzz6bRvNjnUkXQgiKRqM0d+7cQPz33HNPGi073p/uj3fc7hGbOhLZ1MxsWyu1uc7mq4EJalzMj51uPzUUem3ne9OriUJm9ULRGbf2Kt9s9MlQWzcVaprV75v8m2mM0pQWk0xMq+aZTsdp4w4gx2/qSGVCmkSqAtV79dqUkDDoGYt6BDPR69Az1rT8Uc9A11/HoULdi079VQuXypuf6z160yArX2eCWlgypVstzKYMDqvQFFJRTHExLT+jkB5tSlnHoj83pZtjT6V8uUUDbLr/C2CF9OvXD7169YLjf+c74YQTpIErfNukT58+uOaaa2RL2ahRI7z00kuSl2VZ+OabbwK8hRA488wz0bVrV/kd8bTTTkvLpDPOOEMuPkomkxg4cGC9maWCaU477TRUV1dn9eZQOxBlZWV49tlnkfL3cw4bzFXRs2dPDB8+HMlkUjYaJjmnTp0aOHlx6NCh6Nu3b6BAhu3Np6b9ggsuQJfOXUCURMohDDl9mPccIt2m07coOOusswLPiYgmTJgQoAlzql1wyimnSJuOYbLp/va3vwVopk6dmkbzxBNPBGhI2b8ubFB13rx5gf3xVBlVOadMmaIHzWiXMTjubGjDZMwWv/71r9PSUZ/7wx/+oLMx4owzzpB6Qchhc6TpRB/kRmAJYh1cxzXbdP8J0Ht2XAPV5l1vnVzXDazjUJ0K/bWstp58b7puiMnBUMNnAimvSbUXHZYGE0zfXlWwn55+deiHnemVraOOjwOXHDhKfPVqKpsIsgEZBmdNytKVYaJhmDK9IRkBQ8arMqoy6xmtX5vuwyAMBr6aqaZ7VS4Oq8tuQib5oRRonU6Vg8FhddkzI72CNyT0/xmYFMHXYVBnYqiK1TNNL7w/J0wZrKZFzyz213urehpU6IWWod9z46J/Ksxk/zH01jHMj/Ef1ZEIw9q1a/GPf/xDDoSqIH8i6MaNG+UyOvYfOnQoLrzwwoD/ypUrceuttwbC69D9GnoPv8d7wQUXYMSIEbKwua6LCRMmYMWKFbBtG6lUCmeffbZcush8xo4di2HDhsH2F+l8/vnnePvtt7UYgpg3bx7Gjh0Lx5+YSkS44oorMHjw4IDO7r33Xmzfvl0W9s2bN6cdunLLLbfghBNOkAX1kksuwfHHHy+Hc4hIzl4xltX6OhJnnnlm4DkdZUeiV69ecgCXjdA333wzLYw+O2PatGlpNI8++miA5uOPP06jMTmeAcGDynfddVeADxHRpZdemhbu53IPPvggkTKInEwmadiwYQGaW2/1lu6pHSUdppkw2TjeN4bj12fhEBHdeuutaeF4E+v6OkSerD9yLxO9qdabfRPUliVTeIbeKpiad6bhmmb7Z7NmA1UOdXyN/UyvV75W73kgNRuo9Cof1TZif95Gl2nUb7/C79C42nI/fdyQafX4dPBQjapz5mvSB/wxQXVckGXS842fmXBUhU7tCenPVKjC6LZCtlB7TwxWFiskGo1mxZ/lMcmqZ7JKp4fjay5M9UH4r06dj94Lh6InXUYutJay5S7DZD+xfJnAhYd52/7mP3rcUPgJIYyjAA1Bg2w6Zt6hQwece+65GWdgqHAcB506dUpTVjZo06YNLrzwQnnvui5qa2sxffp0kN+T27lzJy6++GKk/MUwJrA/K4+IkJubi2nTpkklW/6edSo6duyI3r17y8Ji2zYWLVqEzZs3w/Vn99YH13XRunVrDBkyRN47jmM84OWss85CcXGxbLlzc3Px5ptvBgrswIED5QAtEaFbt2747W9/C9vf0cnyB77LyspCC58QAvPnz0csFgs0ImeddRZKS0vh+idr6yAizJo1C1u3bpXp6N27N04++WSdNBwNten4/W+yLcKg0/L9W2+9FYgL2v61YfHccccdgTDDhg0z2iP14amnnkqLX3emD/7qYXOmD+Mmd9FFF+lsJNg2MtlHjz/+eBqvyZMny3Am/ZCyTDJMRpMfgLTlhbfddluAjyncww8/rMWuIgubTq8VXLv4mml0ukzQafVWB8qrkuNgOj2sCZTlgCW09ISFUeM00eivM25d+Jqd6VWopo+hhqkPKl0mel1ufoWqYdR42T9MXtabKj/TqrYh+QPMpnQy0godQ03Y0RY2VVDdQTNSMwmpg8Op4XUlZ4Iel658Cnkl6XGoNMxT5a1eq2F1+04Nq/txOLUwqPGa5IRBNjVNYWFUcPymysSOofOzQuxCRmihY4gsjWUTdCF1gU1GeyYwDffWOEOSyWTaDJIwqOnRa6hJDtWuUTMAIT09pmF/lpF/OX5dH6q/Cm5VOTw14GBj/ZevOQ5TuvWKpU5j0p0qE7T89gpegJVE2hLExx57DHfddRcEvBd2x44d8bvf/S594NXA0TX4qVATZ1kWVq1aFZhxSkR46qmncMsttyih6kB+bf3yyy+xcOFCmck1NTU4fPhwsIbJH7NMruuiUaNGKCoqknwty8KUKVOwePFiSdejR4/ACdmu66J58+YoKiqC4ziwbRuLFy/GG2+8ASgynn/++Rg2bJjkU1lZGVgCaQIR4dprr0WPHj0AAAIC3/37OyxYsEAWSNuysHnLFhw+fDitgDKICG3btkXjxo0h/GMAvvrqK0yePBlQCt2ll16KwYMHS3mICOeddx7atGkj0/Gvf/0LS5culZ0UFa7fkdq+fTt27doV0P+YMWPQr19/CGHY6NqlSiK3znD866N+R0KAYDAaf3InhB+Xd//k096sBt/mNDodc7/4gmA1XNabtdO3iYiuuNI/mMSXx+SeUzbjJiJ6Y/LkujB+uAnPPhugee/999L4mNx7779H5KfTCekk/Obi36SF090r/3g1EOa1117zninpeuXV4FJKRiZdm3CnMgOa3WuTeAlkilxKUUrp+FgEB6QWX/JLMwkvOAQgX4meU6/TnPCdeq3Tq37EcXG8/o/r6pylYzKWm4iQE81Rnqpx6BAQ/Jr06VVerr+3lZDpTEddy+DdJ/1tsASnB0DKP1SXW39vEiO/fqx0fQCwLBu27ZkcAoAlBIi8eDxHcFwXluBXvq4ZRUP+W5Jl5fE/S3CLJZBM1Mko49A4sW6IvHeG6hiWv9JLWJZc9RWxeDjN4+Sl2PuzAAdCuH6jBhDxx2SFvXwtek69TnMsvXqt05v8QF6sjpeBXrlwteeudF6j4tsUTgrxeK3kEYxDh7+3BoBUyssIQR4/AEgmvEPayGDfMVxfRo7f8e9Vesmb0+U6XtxE/tHimj4AuK4DJ8mD3N4zIdi5XtkkV8afrj92gOME43cdv4C53LMkkOv5eTReGdAbeG68hfDoVMclO5Xytswg15XHprNOQDq9C+FQBVko9loaITB92nRMmvSGt1GxJy/gbV0XUCrXFiLyn/s1TD73aDiIRy5ArudR97yOp+O6GDPmSpx73nkhBcYAIfD9suV45JFH4LrZGNke35TjYNSoUbhyzJVKXALPTpiAr+cvgG1ZHq3S2gnhtYRXX301zjzrTJBLEJbAl3Pn4uVX/gFLOUBv9Oj/h5GjRoHIhbAsLFm8GM88/bc6dmorSr4+BXDTTTfhlN6npKWfiCAgQOTi+RdexKJFizw7z0+Rqn2XCFeNGYPBQ4d4fITAV1/Owyuv/gPRiA0IbxXbFZePxtBhp8tKGNayZ4QQeG/6dMyc+TFs21+e6BKuve5a9O3X14/fp+Wy4NIhEtTY9/Oa2bRUyFvfU9WXrwy/VNYF9bWhqi7AQ730iQjcrTcIkCU4dCYIwS2Z8GogC+zL79GExy/j8BVK/quwLrD3iLShlwwstTIWnn4iUnYuD4eXj1xpPH6B+P0oVBmzrecBkFfxdHjp995YxNH5EQjXPUKCGgGWl+kePEHrbB6fWN7XQc3k9KjrQAq/MBh7mgavADSW9cWBsHgU1MdDDc/5qobxnmpx+JmciTfriOAzZhiChPFJi9uPF2n557UIBKUyZFZLOtRwQvWo8xT+qdYEwCLfz3X3kaAmAC/71yM2lSqdJhPU8NmA6c06DUe2cejy6PGE8THpAfXQM/T4wsLAII8K1kum8AjhkSmMib4hCOPtWyjcRxSul4D/D4c3FccZtQIQAAAAAElFTkSuQmCC" alt="LINE QR Code">
      <div class="cap">加入官方 LINE</div>
    </div>
  </div>

</div>
</body>
</html>
