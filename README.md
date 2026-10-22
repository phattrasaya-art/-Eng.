<!DOCTYPE html>
<html lang="th"><head><meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>เกมคำศัพท์ภาษาอังกฤษ ป.2</title>
<link href="https://fonts.googleapis.com/css2?family=Mali:wght@500;700&display=swap" rel="stylesheet">
<style>
:root{--bg:#fff4d6;--card:#fff;--ink:#3b2f4a;--mut:#7a6d8a;--pri:#ff6b9d;--ok:#3cb878;--bad:#ef5b5b;--line:#f0d89a;--on:#ffe27a;color-scheme:light;box-sizing:border-box;padding-top:env(safe-area-inset-top,0px);padding-bottom:env(safe-area-inset-bottom,0px)}
@media (prefers-color-scheme:dark){:root:not([data-theme="light"]){--bg:#241c33;--card:#352b48;--ink:#fff3e0;--mut:#c4b8d8;--line:#4a3e63;--on:#6b5a1f;color-scheme:dark}}
:root[data-theme="dark"]{--bg:#241c33;--card:#352b48;--ink:#fff3e0;--mut:#c4b8d8;--line:#4a3e63;--on:#6b5a1f;color-scheme:dark}
html{scroll-padding-top:env(safe-area-inset-top,0px)}
body{margin:0;background:var(--bg);color:var(--ink);font-family:'Mali','Sarabun','Noto Sans Thai',system-ui,sans-serif;font-weight:500}
main{max-width:640px;margin:0 auto;padding:16px}
h1{font-size:26px;margin:6px 0;text-align:center}h2{text-align:center}
.mut,.cen{text-align:center;color:var(--mut)}.cen{color:var(--ink);font-size:18px}
button{font:inherit;color:inherit;cursor:pointer}
.chips{display:flex;gap:8px;overflow-x:auto;padding:8px 0}
.chip{flex:none;border:2px solid var(--line);background:var(--card);border-radius:20px;padding:6px 14px}
.chip.on{background:var(--on);border-color:#e0b800;font-weight:700}
.menu{display:grid;grid-template-columns:repeat(auto-fit,minmax(170px,1fr));gap:12px;margin-top:8px}
.card{display:flex;flex-direction:column;align-items:center;gap:4px;background:var(--card);border:3px solid var(--line);border-radius:22px;padding:16px 8px;box-shadow:0 4px 0 var(--line)}
.card span{font-size:44px}.card b{font-size:18px}.card small{color:var(--mut);text-align:center}
.top{display:flex;justify-content:space-between;align-items:center;gap:8px}
.back{border:2px solid var(--line);background:var(--card);border-radius:14px;padding:6px 12px}
.pic{font-size:96px;text-align:center;line-height:1.2;margin:10px 0}
.word{display:flex;justify-content:center;gap:6px;font-size:38px;font-weight:700;margin:10px 0;white-space:pre;flex-wrap:wrap}
.word span{min-width:30px;text-align:center}.word .bl{border-bottom:4px solid var(--pri);color:transparent}
.g2,.g3,.g4{display:grid;gap:10px;margin:10px 0}
.g2{grid-template-columns:1fr 1fr}.g3{grid-template-columns:repeat(3,1fr)}.g4{grid-template-columns:repeat(auto-fit,minmax(72px,1fr))}
.opt{background:var(--card);border:3px solid var(--line);border-radius:18px;padding:14px 6px;font-size:22px;font-weight:700;min-height:64px;box-shadow:0 3px 0 var(--line)}
.opt.em{font-size:44px}.opt.on{background:var(--on)}
.opt.ok{background:var(--ok);border-color:var(--ok);color:#fff}.opt.bad{background:var(--bad);border-color:var(--bad);color:#fff}
.opt:disabled:not(.ok):not(.bad){opacity:.45}
.shake{animation:sk .4s}@keyframes sk{25%{transform:translateX(-8px)}75%{transform:translateX(8px)}}
.spk{border:0;background:var(--on);border-radius:50%;width:38px;height:38px;font-size:18px}
.big{display:block;width:100%;margin:10px 0;padding:14px;border:0;border-radius:20px;background:var(--pri);color:#fff;font-size:20px;font-weight:700;box-shadow:0 4px 0 #c94577}
.big.alt{background:#6c8cff;box-shadow:0 4px 0 #4463cc}
.alt2{display:block;margin:6px auto;border:2px solid var(--line);background:var(--card);border-radius:14px;padding:8px 18px}
.msg{text-align:center;font-size:20px;font-weight:700;border-radius:16px;padding:10px;margin-top:10px}
.msg.ok{background:var(--ok);color:#fff}.msg.bad{background:var(--bad);color:#fff}
.end{text-align:center;padding-top:20px}.end .e{font-size:72px}.pic.t{font-size:44px;font-weight:700;padding:18px 0}.chip:disabled{opacity:.5}.inp{width:100%;box-sizing:border-box;font:inherit;font-size:26px;text-align:center;padding:12px;border:3px solid var(--line);border-radius:16px;background:var(--card);color:var(--ink);margin:8px 0}.inp.bad{border-color:var(--bad)}.bar{height:10px;background:var(--line);border-radius:6px;overflow:hidden;margin:8px 0}.bar i{display:block;height:100%;width:100%;background:var(--pri);transition:width .1s linear}
</style></head><body><main id="g"></main>
<script>
const W=`🔴|Red|สีแดง|สี
🔵|Blue|สีน้ำเงิน|สี
🟡|Yellow|สีเหลือง|สี
🟢|Green|สีเขียว|สี
🟣|Purple|สีม่วง|สี
🩷|Pink|สีชมพู|สี
🍎|Apple|แอปเปิล|ผลไม้-ผัก
🍌|Banana|กล้วย|ผลไม้-ผัก
🍊|Orange|ส้ม|ผลไม้-ผัก
🍇|Grape|องุ่น|ผลไม้-ผัก
🍉|Watermelon|แตงโม|ผลไม้-ผัก
🍍|Pineapple|สับปะรด|ผลไม้-ผัก
🍓|Strawberry|สตรอว์เบอร์รี|ผลไม้-ผัก
🥭|Mango|มะม่วง|ผลไม้-ผัก
🥕|Carrot|แครอท|ผลไม้-ผัก
🍅|Tomato|มะเขือเทศ|ผลไม้-ผัก
🌽|Corn|ข้าวโพด|ผลไม้-ผัก
🥦|Broccoli|บรอกโคลี|ผลไม้-ผัก
🐶|Dog|สุนัข|สัตว์
🐱|Cat|แมว|สัตว์
🐰|Rabbit|กระต่าย|สัตว์
🐴|Horse|ม้า|สัตว์
🐮|Cow|วัว|สัตว์
🐷|Pig|หมู|สัตว์
🐑|Sheep|แกะ|สัตว์
🐔|Chicken|ไก่|สัตว์
🦆|Duck|เป็ด|สัตว์
🐦|Bird|นก|สัตว์
🐯|Tiger|เสือ|สัตว์
🦁|Lion|สิงโต|สัตว์
🐘|Elephant|ช้าง|สัตว์
🦒|Giraffe|ยีราฟ|สัตว์
🐵|Monkey|ลิง|สัตว์
🐼|Panda|แพนด้า|สัตว์
🐸|Frog|กบ|สัตว์
🐢|Turtle|เต่า|สัตว์
🐟|Fish|ปลา|สัตว์
🐬|Dolphin|โลมา|สัตว์
👁️|Eye|ตา|ร่างกาย
👂|Ear|หู|ร่างกาย
👃|Nose|จมูก|ร่างกาย
👄|Mouth|ปาก|ร่างกาย
🦷|Tooth|ฟัน|ร่างกาย
✋|Hand|มือ|ร่างกาย
🦶|Foot|เท้า|ร่างกาย
🧠|Brain|สมอง|ร่างกาย
🍚|Rice|ข้าว|อาหาร
🍞|Bread|ขนมปัง|อาหาร
🥛|Milk|นม|อาหาร
🍕|Pizza|พิซซ่า|อาหาร
🍔|Hamburger|แฮมเบอร์เกอร์|อาหาร
🍦|Ice cream|ไอศกรีม|อาหาร
🍪|Cookie|คุกกี้|อาหาร
🍩|Donut|โดนัท|อาหาร
🎂|Cake|เค้ก|อาหาร
🧀|Cheese|ชีส|อาหาร
🚗|Car|รถยนต์|ยานพาหนะ
🚌|Bus|รถบัส|ยานพาหนะ
🚲|Bicycle|จักรยาน|ยานพาหนะ
🚆|Train|รถไฟ|ยานพาหนะ
🏍️|Motorcycle|มอเตอร์ไซค์|ยานพาหนะ
🚕|Taxi|แท็กซี่|ยานพาหนะ
🚚|Truck|รถบรรทุก|ยานพาหนะ
👕|T-shirt|เสื้อยืด|เสื้อผ้า
👖|Jeans|กางเกงยีนส์|เสื้อผ้า
👗|Dress|ชุดเดรส|เสื้อผ้า
👟|Shoes|รองเท้า|เสื้อผ้า
🧦|Socks|ถุงเท้า|เสื้อผ้า
🧢|Cap|หมวกแก๊ป|เสื้อผ้า
🧣|Scarf|ผ้าพันคอ|เสื้อผ้า
✏️|Pencil|ดินสอ|ของใช้
📖|Book|หนังสือ|ของใช้
🖊️|Pen|ปากกา|ของใช้
✂️|Scissors|กรรไกร|ของใช้
🎒|Backpack|กระเป๋าเป้|ของใช้
📏|Ruler|ไม้บรรทัด|ของใช้
🛏️|Bed|เตียง|ของใช้
🪑|Chair|เก้าอี้|ของใช้
📺|Television|โทรทัศน์|ของใช้
🕐|Clock|นาฬิกา|ของใช้
👩‍🏫|Teacher|ครู|อาชีพ
👨‍⚕️|Doctor|หมอ|อาชีพ
👮|Police officer|ตำรวจ|อาชีพ
👨‍🍳|Chef|เชฟ|อาชีพ
👨‍🚒|Firefighter|นักผจญเพลิง|อาชีพ
🧑‍✈️|Pilot|นักบิน|อาชีพ
☀️|Sunny|แดดออก|อากาศ
☁️|Cloudy|มีเมฆ|อากาศ
🌧️|Rainy|ฝนตก|อากาศ
🌈|Rainbow|รุ้ง|อากาศ
❄️|Snowy|หิมะตก|อากาศ
👨|Father|พ่อ|ครอบครัว
👩|Mother|แม่|ครอบครัว
👶|Baby|เด็กทารก|ครอบครัว
👴|Grandfather|ปู่ / ตา|ครอบครัว
👵|Grandmother|ย่า / ยาย|ครอบครัว
👦|Son|ลูกชาย|ครอบครัว
👧|Daughter|ลูกสาว|ครอบครัว
⚽|Football|ฟุตบอล|กีฬา-ดนตรี
🏀|Basketball|บาสเกตบอล|กีฬา-ดนตรี
🎾|Tennis|เทนนิส|กีฬา-ดนตรี
🏊|Swimming|ว่ายน้ำ|กีฬา-ดนตรี
🎸|Guitar|กีตาร์|กีฬา-ดนตรี
🎹|Piano|เปียโน|กีฬา-ดนตรี
🥁|Drum|กลอง|กีฬา-ดนตรี
🎻|Violin|ไวโอลิน|กีฬา-ดนตรี`.split('\n').map(l=>l.split('|'));
`😀|Hello|สวัสดี|ทักทาย
🙋|Hi|หวัดดี|ทักทาย
🌅|Good morning|สวัสดีตอนเช้า|ทักทาย
🌞|Good afternoon|สวัสดีตอนบ่าย|ทักทาย
🌆|Good evening|สวัสดีตอนเย็น|ทักทาย
🌃|Good night|ราตรีสวัสดิ์|ทักทาย
👋|Goodbye|ลาก่อน|ทักทาย
🤝|Nice to meet you|ยินดีที่ได้รู้จัก|ทักทาย
🙏|Thank you|ขอบคุณ|ทักทาย
😔|Sorry|ขอโทษ|ทักทาย
🥺|Please|กรุณา|ทักทาย
🤗|Welcome|ยินดีต้อนรับ|ทักทาย
🙂|How are you|สบายดีไหม|ทักทาย
👍|Fine|สบายดี|ทักทาย
✅|Yes|ใช่|ทักทาย
❌|No|ไม่|ทักทาย
🥳|Happy birthday|สุขสันต์วันเกิด|ทักทาย
|Monday|วันจันทร์|วัน
|Tuesday|วันอังคาร|วัน
|Wednesday|วันพุธ|วัน
|Thursday|วันพฤหัสบดี|วัน
|Friday|วันศุกร์|วัน
|Saturday|วันเสาร์|วัน
|Sunday|วันอาทิตย์|วัน
|January|มกราคม|เดือน
|February|กุมภาพันธ์|เดือน
|March|มีนาคม|เดือน
|April|เมษายน|เดือน
|May|พฤษภาคม|เดือน
|June|มิถุนายน|เดือน
|July|กรกฎาคม|เดือน
|August|สิงหาคม|เดือน
|September|กันยายน|เดือน
|October|ตุลาคม|เดือน
|November|พฤศจิกายน|เดือน
|December|ธันวาคม|เดือน
🌅|Morning|ตอนเช้า|เวลา
🌇|Afternoon|ตอนบ่าย|เวลา
🌆|Evening|ตอนเย็น|เวลา
🌙|Night|กลางคืน|เวลา
📅|Today|วันนี้|เวลา
|Tomorrow|พรุ่งนี้|เวลา
|Yesterday|เมื่อวาน|เวลา
🗓️|Week|สัปดาห์|เวลา
📆|Year|ปี|เวลา
|Month|เดือน|เวลา
⏰|Hour|ชั่วโมง|เวลา
⏱️|Minute|นาที|เวลา
|Second|วินาที|เวลา
🕛|Noon|เที่ยงวัน|เวลา
|Midnight|เที่ยงคืน|เวลา
|Weekend|วันหยุดสุดสัปดาห์|เวลา
|Now|ตอนนี้|เวลา
|Early|เช้า / เร็ว|เวลา
|Late|สาย / ช้า|เวลา
|Always|เสมอ|เวลา
|Never|ไม่เคย|เวลา
0|Zero|ศูนย์|ตัวเลข
11|Eleven|สิบเอ็ด|ตัวเลข
12|Twelve|สิบสอง|ตัวเลข
13|Thirteen|สิบสาม|ตัวเลข
14|Fourteen|สิบสี่|ตัวเลข
15|Fifteen|สิบห้า|ตัวเลข
16|Sixteen|สิบหก|ตัวเลข
17|Seventeen|สิบเจ็ด|ตัวเลข
18|Eighteen|สิบแปด|ตัวเลข
19|Nineteen|สิบเก้า|ตัวเลข
20|Twenty|ยี่สิบ|ตัวเลข
30|Thirty|สามสิบ|ตัวเลข
40|Forty|สี่สิบ|ตัวเลข
50|Fifty|ห้าสิบ|ตัวเลข
60|Sixty|หกสิบ|ตัวเลข
70|Seventy|เจ็ดสิบ|ตัวเลข
80|Eighty|แปดสิบ|ตัวเลข
90|Ninety|เก้าสิบ|ตัวเลข
100|One hundred|หนึ่งร้อย|ตัวเลข
1000|One thousand|หนึ่งพัน|ตัวเลข
|I|ฉัน|สรรพนาม
|You|คุณ|สรรพนาม
|He|เขา (ผู้ชาย)|สรรพนาม
|She|เธอ (ผู้หญิง)|สรรพนาม
|It|มัน|สรรพนาม
|We|เรา|สรรพนาม
|They|พวกเขา|สรรพนาม
|My|ของฉัน|สรรพนาม
|Your|ของคุณ|สรรพนาม
|His|ของเขา (ชาย)|สรรพนาม
|Her|ของเธอ (หญิง)|สรรพนาม
|Our|ของเรา|สรรพนาม
|This|นี่|สรรพนาม
|That|นั่น|สรรพนาม
|These|เหล่านี้|สรรพนาม
|Those|เหล่านั้น|สรรพนาม
|Who|ใคร|สรรพนาม
|What|อะไร|สรรพนาม
|Where|ที่ไหน|สรรพนาม
|When|เมื่อไร|สรรพนาม
|Why|ทำไม|สรรพนาม
|How|อย่างไร|สรรพนาม
|Which|อันไหน|สรรพนาม
|In|ใน|คำบุพบท
|On|บน|คำบุพบท
|Under|ใต้|คำบุพบท
|Behind|ข้างหลัง|คำบุพบท
|Near|ใกล้|คำบุพบท
|Between|ระหว่าง|คำบุพบท
|Next to|ข้าง ๆ|คำบุพบท
|In front of|ข้างหน้า|คำบุพบท
|Above|เหนือ|คำบุพบท
|Below|ด้านล่าง|คำบุพบท
|With|กับ|คำบุพบท
|From|จาก|คำบุพบท
|To|ไปยัง|คำบุพบท
|At|ที่|คำบุพบท
|For|สำหรับ|คำบุพบท
|Inside|ข้างใน|คำบุพบท
|Outside|ข้างนอก|คำบุพบท
|Up|ขึ้น|คำบุพบท
|Down|ลง|คำบุพบท
|Around|รอบ ๆ|คำบุพบท
|Across|ข้าม|คำบุพบท
➡️|Go|ไป|กริยา
|Come|มา|กริยา
🍽️|Eat|กิน|กริยา
🧋|Drink|ดื่ม|กริยา
🛌|Sleep|นอน|กริยา
🚶|Walk|เดิน|กริยา
🏃|Run|วิ่ง|กริยา
🤸|Jump|กระโดด|กริยา
🧘|Sit|นั่ง|กริยา
🧍|Stand|ยืน|กริยา
💃|Dance|เต้น|กริยา
🎤|Sing|ร้องเพลง|กริยา
😁|Smile|ยิ้ม|กริยา
😂|Laugh|หัวเราะ|กริยา
😭|Cry|ร้องไห้|กริยา
📕|Read|อ่าน|กริยา
📝|Write|เขียน|กริยา
🎨|Draw|วาด|กริยา
🎧|Listen|ฟัง|กริยา
👀|Look|มอง|กริยา
🗣️|Speak|พูด|กริยา
|Open|เปิด|กริยา
|Close|ปิด|กริยา
🎮|Play|เล่น|กริยา
|Help|ช่วย|กริยา
🚿|Wash|ล้าง / อาบ|กริยา
🍳|Cook|ทำอาหาร|กริยา
🚴|Ride|ขี่|กริยา
💸|Buy|ซื้อ|กริยา
🧗|Climb|ปีน|กริยา
🤾|Throw|ขว้าง|กริยา
🥎|Catch|จับ / รับ|กริยา
🦵|Kick|เตะ|กริยา
⏰|Wake up|ตื่นนอน|กริยา
🧑‍🎓|Study|เรียน|กริยา
|Teach|สอน|กริยา
❓|Ask|ถาม|กริยา
💬|Answer|ตอบ|กริยา
|Give|ให้|กริยา
|Take|เอา|กริยา
|Make|ทำ / สร้าง|กริยา
❤️|Love|รัก|กริยา
|Like|ชอบ|กริยา
|Want|ต้องการ|กริยา
|Know|รู้|กริยา
🤔|Think|คิด|กริยา
🫂|Hug|กอด|กริยา
⌛|Wait|รอ|กริยา
🛑|Stop|หยุด|กริยา
😊|Happy|มีความสุข|อารมณ์
😢|Sad|เศร้า|อารมณ์
😠|Angry|โกรธ|อารมณ์
🤩|Excited|ตื่นเต้น|อารมณ์
😨|Scared|กลัว|อารมณ์
😴|Sleepy|ง่วง|อารมณ์
😫|Tired|เหนื่อย|อารมณ์
😳|Shy|ขี้อาย|อารมณ์
😐|Bored|เบื่อ|อารมณ์
😲|Surprised|ประหลาดใจ|อารมณ์
😌|Calm|สงบ|อารมณ์
😟|Worried|กังวล|อารมณ์
🥰|Loved|ถูกรัก|อารมณ์
🤒|Sick|ป่วย|อารมณ์
😋|Hungry|หิว|อารมณ์
🥤|Thirsty|กระหายน้ำ|อารมณ์
🦸|Brave|กล้าหาญ|อารมณ์
🤪|Silly|ตลกซน|อารมณ์
😕|Confused|สับสน|อารมณ์
🏦|Bank|ธนาคาร|สถานที่
🏨|Hotel|โรงแรม|สถานที่
✈️|Airport|สนามบิน|สถานที่
🚉|Train station|สถานีรถไฟ|สถานที่
🌳|Park|สวนสาธารณะ|สถานที่
🏖️|Beach|ชายหาด|สถานที่
🏔️|Mountain|ภูเขา|สถานที่
🌊|Sea|ทะเล|สถานที่
🏝️|Island|เกาะ|สถานที่
🌲|Forest|ป่า|สถานที่
🎬|Cinema|โรงภาพยนตร์|สถานที่
🦓|Zoo|สวนสัตว์|สถานที่
🍛|Restaurant|ร้านอาหาร|สถานที่
📚|Library|ห้องสมุด|สถานที่
🏛️|Museum|พิพิธภัณฑ์|สถานที่
🛕|Temple|วัด|สถานที่
🏟️|Stadium|สนามกีฬา|สถานที่
🏢|Office|สำนักงาน|สถานที่
🚒|Fire station|สถานีดับเพลิง|สถานที่
🛍️|Market|ตลาด|สถานที่
🥖|Bakery|ร้านเบเกอรี่|สถานที่
🌾|Farm|ฟาร์ม|สถานที่
🛋️|Sofa|โซฟา|สิ่งของ
💡|Lamp|โคมไฟ|สิ่งของ
🚪|Door|ประตู|สิ่งของ
🪟|Window|หน้าต่าง|สิ่งของ
🔑|Key|กุญแจ|สิ่งของ
☂️|Umbrella|ร่ม|สิ่งของ
👜|Bag|กระเป๋า|สิ่งของ
📱|Phone|โทรศัพท์|สิ่งของ
💻|Computer|คอมพิวเตอร์|สิ่งของ
📷|Camera|กล้องถ่ายรูป|สิ่งของ
🧸|Toy|ของเล่น|สิ่งของ
🪁|Kite|ว่าว|สิ่งของ
🎈|Balloon|ลูกโป่ง|สิ่งของ
🎁|Gift|ของขวัญ|สิ่งของ
🥤|Cup|ถ้วย / แก้ว|สิ่งของ
🥄|Spoon|ช้อน|สิ่งของ
🍴|Fork|ส้อม|สิ่งของ
🥣|Bowl|ชาม|สิ่งของ
🧼|Soap|สบู่|สิ่งของ
🪥|Toothbrush|แปรงสีฟัน|สิ่งของ
🪞|Mirror|กระจก|สิ่งของ
🧹|Broom|ไม้กวาด|สิ่งของ
🪣|Bucket|ถังน้ำ|สิ่งของ
👓|Glasses|แว่นตา|สิ่งของ
⌚|Watch|นาฬิกาข้อมือ|สิ่งของ
👒|Hat|หมวก|สิ่งของ
💍|Ring|แหวน|สิ่งของ
👑|Crown|มงกุฎ|สิ่งของ
💰|Money|เงิน|สิ่งของ
🌸|Flower|ดอกไม้|ธรรมชาติ
🌞|Sun|ดวงอาทิตย์|ธรรมชาติ
🌙|Moon|ดวงจันทร์|ธรรมชาติ
⭐|Star|ดาว|ธรรมชาติ
🔥|Fire|ไฟ|ธรรมชาติ
💧|Water|น้ำ|ธรรมชาติ
🍃|Leaf|ใบไม้|ธรรมชาติ
💨|Wind|ลม|ธรรมชาติ
🏞️|River|แม่น้ำ|ธรรมชาติ
🌴|Tree|ต้นไม้|ธรรมชาติ
🐻|Bear|หมี|สัตว์
🦊|Fox|จิ้งจอก|สัตว์
🐺|Wolf|หมาป่า|สัตว์
🐭|Mouse|หนู|สัตว์
🦓|Zebra|ม้าลาย|สัตว์
🐊|Crocodile|จระเข้|สัตว์
🐍|Snake|งู|สัตว์
🦈|Shark|ฉลาม|สัตว์
🐳|Whale|วาฬ|สัตว์
🐙|Octopus|ปลาหมึกยักษ์|สัตว์
🦀|Crab|ปู|สัตว์
🦋|Butterfly|ผีเสื้อ|สัตว์
🐝|Bee|ผึ้ง|สัตว์
🐜|Ant|มด|สัตว์
🦉|Owl|นกฮูก|สัตว์
🐧|Penguin|เพนกวิน|สัตว์
🐨|Koala|โคอาลา|สัตว์
🦘|Kangaroo|จิงโจ้|สัตว์
🐐|Goat|แพะ|สัตว์
🍋|Lemon|มะนาวเหลือง|ผลไม้-ผัก
🥥|Coconut|มะพร้าว|ผลไม้-ผัก
🍐|Pear|ลูกแพร์|ผลไม้-ผัก
🍑|Peach|ลูกพีช|ผลไม้-ผัก
🥔|Potato|มันฝรั่ง|ผลไม้-ผัก
🧅|Onion|หัวหอมใหญ่|ผลไม้-ผัก
🍜|Noodles|ก๋วยเตี๋ยว|อาหาร
🍟|French fries|มันฝรั่งทอด|อาหาร
🌭|Hot dog|ฮอตดอก|อาหาร
🥪|Sandwich|แซนด์วิช|อาหาร
🍣|Sushi|ซูชิ|อาหาร
🥚|Egg|ไข่|อาหาร
🍫|Chocolate|ช็อกโกแลต|อาหาร
🍬|Candy|ลูกอม|อาหาร
☕|Coffee|กาแฟ|อาหาร
🍵|Tea|ชา|อาหาร
🧃|Juice|น้ำผลไม้|อาหาร
💇|Hair|ผม|ร่างกาย
💪|Arm|แขน|ร่างกาย
☝️|Finger|นิ้วมือ|ร่างกาย
🫀|Heart|หัวใจ|ร่างกาย`.split('\n').forEach(l=>W.push(l.split('|')));
const A=(c,s)=>s.split('\n').forEach(l=>W.push([...l.split('|'),c]));
A('สี',`⚫|Black|สีดำ
⚪|White|สีขาว
🟤|Brown|สีน้ำตาล
🩶|Gray|สีเทา
🥇|Gold|สีทอง
🥈|Silver|สีเงิน
|Beige|สีเบจ
|Cream|สีครีม
|Navy blue|สีกรมท่า
|Colorful|หลากสี`);
A('ผลไม้-ผัก',`🥝|Kiwi|กีวี
🍒|Cherry|เชอร์รี
🫐|Blueberry|บลูเบอร์รี
🍈|Cantaloupe|แคนตาลูป
🥑|Avocado|อะโวคาโด
🍆|Eggplant|มะเขือยาว
🥒|Cucumber|แตงกวา
🥬|Lettuce|ผักกาดหอม
🧄|Garlic|กระเทียม
🍄|Mushroom|เห็ด
🌶️|Chili|พริก
🫑|Bell pepper|พริกหวาน
🎃|Pumpkin|ฟักทอง
🍠|Sweet potato|มันหวาน
🫚|Ginger|ขิง
🌿|Basil|โหระพา
|Durian|ทุเรียน
|Lychee|ลิ้นจี่
|Longan|ลำไย
|Guava|ฝรั่ง
|Papaya|มะละกอ
|Pomegranate|ทับทิม
|Plum|ลูกพลัม
|Rambutan|เงาะ
|Mangosteen|มังคุด
|Spinach|ผักโขม
|Celery|ขึ้นฉ่าย
|Cauliflower|ดอกกะหล่ำ
|Radish|หัวไชเท้า`);
A('สัตว์',`🐹|Hamster|หนูแฮมสเตอร์
🦃|Turkey|ไก่งวง
🦅|Eagle|นกอินทรี
🦜|Parrot|นกแก้ว
🐆|Leopard|เสือดาว
🦌|Deer|กวาง
🦛|Hippopotamus|ฮิปโปโปเตมัส
🦏|Rhinoceros|แรด
🐪|Camel|อูฐ
🐿️|Squirrel|กระรอก
🦇|Bat|ค้างคาว
🦔|Hedgehog|เม่นแคระ
🦦|Otter|นาก
🦎|Lizard|กิ้งก่า
🦑|Squid|ปลาหมึก
🐛|Worm|หนอน
🐞|Ladybug|เต่าทอง
🕷️|Spider|แมงมุม
🐌|Snail|หอยทาก
🦢|Swan|หงส์
🕊️|Dove|นกพิราบ
🐓|Rooster|ไก่ตัวผู้
🐣|Chick|ลูกไก่
🐕|Puppy|ลูกสุนัข
🐈|Kitten|ลูกแมว
🐂|Bull|วัวตัวผู้
🦙|Llama|ลามะ
|Jellyfish|แมงกะพรุน
|Starfish|ปลาดาว
|Seahorse|ม้าน้ำ`);
A('ร่างกาย',`👅|Tongue|ลิ้น
🦴|Bone|กระดูก
🩸|Blood|เลือด
💅|Nail|เล็บ
🫁|Lung|ปอด
🧔|Beard|เครา
|Head|ศีรษะ
|Face|ใบหน้า
|Neck|คอ
|Shoulder|ไหล่
|Elbow|ข้อศอก
|Knee|หัวเข่า
|Leg|ขา
|Back|หลัง
|Chest|หน้าอก
|Stomach|ท้อง
|Thumb|นิ้วโป้ง
|Cheek|แก้ม
|Chin|คาง
|Lip|ริมฝีปาก
|Eyebrow|คิ้ว
|Forehead|หน้าผาก
|Skin|ผิวหนัง
|Toe|นิ้วเท้า
|Wrist|ข้อมือ
|Ankle|ข้อเท้า
|Waist|เอว
|Palm|ฝ่ามือ
|Muscle|กล้ามเนื้อ`);
A('อาหาร',`🥓|Bacon|เบคอน
🍗|Fried chicken|ไก่ทอด
🍖|Meat|เนื้อสัตว์
🥩|Steak|สเต็ก
🍤|Shrimp|กุ้ง
🥟|Dumpling|เกี๊ยว
🍝|Spaghetti|สปาเกตตี
🥘|Curry|แกงกะหรี่
🍲|Soup|ซุป
🥗|Salad|สลัด
🥞|Pancake|แพนเค้ก
🧇|Waffle|วาฟเฟิล
🥐|Croissant|ครัวซองต์
🍯|Honey|น้ำผึ้ง
🧈|Butter|เนย
🥜|Peanut|ถั่วลิสง
🍿|Popcorn|ป๊อปคอร์น
🥧|Pie|พาย
🍮|Pudding|พุดดิ้ง
🧂|Salt|เกลือ
|Sugar|น้ำตาล
|Toast|ขนมปังปิ้ง
|Sausage|ไส้กรอก
|Smoothie|สมูทตี้
|Lemonade|น้ำมะนาว
|Bubble tea|ชานมไข่มุก
|Breakfast|อาหารเช้า
|Lunch|อาหารกลางวัน
|Dinner|อาหารเย็น
|Snack|ขนม`);
A('ยานพาหนะ',`🚐|Van|รถตู้
🛵|Scooter|สกูตเตอร์
🛺|Tuk-tuk|ตุ๊กตุ๊ก
🚁|Helicopter|เฮลิคอปเตอร์
🛩️|Airplane|เครื่องบิน
🚢|Ship|เรือใหญ่
⛵|Boat|เรือ
🚀|Rocket|จรวด
🚑|Ambulance|รถพยาบาล
🚓|Police car|รถตำรวจ
🚜|Tractor|รถแทรกเตอร์
🚇|Subway|รถไฟใต้ดิน
🛶|Canoe|เรือแคนู
🚤|Speedboat|เรือเร็ว
🏎️|Race car|รถแข่ง
🛹|Skateboard|สเกตบอร์ด
|Fire truck|รถดับเพลิง
|Jet ski|เจ็ตสกี`);
A('เสื้อผ้า',`👔|Shirt|เสื้อเชิ้ต
🧥|Jacket|แจ็กเก็ต
🩳|Shorts|กางเกงขาสั้น
🥾|Boots|รองเท้าบูต
🩴|Sandals|รองเท้าแตะ
👠|High heels|รองเท้าส้นสูง
🧤|Gloves|ถุงมือ
🕶️|Sunglasses|แว่นกันแดด
|Coat|เสื้อโค้ต
|Sweater|เสื้อกันหนาว
|Hoodie|เสื้อฮู้ด
|Skirt|กระโปรง
|Pants|กางเกงขายาว
|Pajamas|ชุดนอน
|Uniform|ชุดยูนิฟอร์ม
|Underwear|ชุดชั้นใน
|Belt|เข็มขัด
|Tie|เนกไท
|Suit|สูท
|Raincoat|เสื้อกันฝน`);
A('ของใช้',`🖍️|Crayon|ดินสอสี
🖌️|Paintbrush|พู่กัน
📓|Notebook|สมุดโน้ต
📎|Paper clip|คลิปหนีบกระดาษ
📌|Push pin|หมุดปักบอร์ด
🗂️|Folder|แฟ้ม
📄|Paper|กระดาษ
✉️|Envelope|ซองจดหมาย
|Eraser|ยางลบ
|Glue|กาว
|Tape|เทปกาว
|Stapler|แม็กเย็บกระดาษ
|Whiteboard|ไวต์บอร์ด
|Blackboard|กระดานดำ
|Chalk|ชอล์ก
|Desk|โต๊ะทำงาน
|Calculator|เครื่องคิดเลข
|Classroom|ห้องเรียน
|Homework|การบ้าน
|Lesson|บทเรียน
|Test|แบบทดสอบ
|Student|นักเรียน
|Pencil case|กล่องดินสอ
|Sharpener|กบเหลาดินสอ`);
A('สิ่งของ',`🔪|Knife|มีด
🔋|Battery|แบตเตอรี่
🔦|Flashlight|ไฟฉาย
🗑️|Trash can|ถังขยะ
🔨|Hammer|ค้อน
🕯️|Candle|เทียน
🔔|Bell|กระดิ่ง
🗺️|Map|แผนที่
🚩|Flag|ธง
🏅|Medal|เหรียญรางวัล
🏆|Trophy|ถ้วยรางวัล
🧲|Magnet|แม่เหล็ก
|Table|โต๊ะ
|Pillow|หมอน
|Blanket|ผ้าห่ม
|Curtain|ผ้าม่าน
|Fan|พัดลม
|Refrigerator|ตู้เย็น
|Towel|ผ้าเช็ดตัว
|Comb|หวี
|Plate|จาน
|Pot|หม้อ
|Kettle|กาต้มน้ำ
|Rope|เชือก
|Ladder|บันได
|Carpet|พรม
|Shelf|ชั้นวางของ
|Stairs|บันได`);
A('อาชีพ',`👩‍⚕️|Nurse|พยาบาล
👨‍🌾|Farmer|เกษตรกร
👩‍🔧|Mechanic|ช่างซ่อม
👨‍🔬|Scientist|นักวิทยาศาสตร์
👨‍🎤|Singer|นักร้อง
👩‍🎨|Artist|ศิลปิน
👷|Builder|คนงานก่อสร้าง
🕵️|Detective|นักสืบ
🧑‍🚀|Astronaut|นักบินอวกาศ
👨‍💻|Programmer|โปรแกรมเมอร์
|Dentist|ทันตแพทย์
|Driver|คนขับรถ
|Baker|คนทำขนมปัง
|Waiter|พนักงานเสิร์ฟ
|Judge|ผู้พิพากษา
|Lawyer|ทนายความ
|Soldier|ทหาร
|Cashier|แคชเชียร์
|Gardener|คนสวน
|Photographer|ช่างภาพ
|Fisherman|ชาวประมง
|Veterinarian|สัตวแพทย์
|Actor|นักแสดง
|Dancer|นักเต้น`);
A('อากาศ',`⛈️|Thunder|ฟ้าร้อง
⚡|Lightning|ฟ้าแลบ
🌫️|Foggy|มีหมอก
🌪️|Tornado|พายุทอร์นาโด
🌡️|Temperature|อุณหภูมิ
🍂|Autumn|ฤดูใบไม้ร่วง
⛄|Winter|ฤดูหนาว
☔|Rain|ฝน
🌄|Sunrise|พระอาทิตย์ขึ้น
|Weather|สภาพอากาศ
|Windy|มีลมแรง
|Hail|ลูกเห็บ
|Flood|น้ำท่วม
|Drought|ภัยแล้ง
|Season|ฤดูกาล
|Spring|ฤดูใบไม้ผลิ
|Summer|ฤดูร้อน
|Snow|หิมะ
|Cloud|เมฆ
|Sky|ท้องฟ้า
|Sunshine|แสงแดด
|Sunset|พระอาทิตย์ตก
|Storm|พายุ`);
A('ครอบครัว',`👨‍👩‍👧|Family|ครอบครัว
🧒|Child|เด็ก
👯|Twin|ฝาแฝด
🧑‍🤝‍🧑|Friend|เพื่อน
|Parents|พ่อแม่
|Brother|พี่ชาย / น้องชาย
|Sister|พี่สาว / น้องสาว
|Children|ลูก ๆ
|Grandparents|ปู่ย่าตายาย
|Uncle|ลุง / น้า / อา
|Aunt|ป้า / น้า / อา
|Cousin|ลูกพี่ลูกน้อง
|Husband|สามี
|Wife|ภรรยา
|Nephew|หลานชาย
|Niece|หลานสาว
|Teenager|วัยรุ่น
|Adult|ผู้ใหญ่
|Neighbor|เพื่อนบ้าน
|Mom|แม่
|Dad|พ่อ
|Man|ผู้ชาย
|Woman|ผู้หญิง
|Boy|เด็กชาย
|Girl|เด็กหญิง`);
A('กีฬา-ดนตรี',`🏸|Badminton|แบดมินตัน
🏓|Table tennis|เทเบิลเทนนิส
🏐|Volleyball|วอลเลย์บอล
⚾|Baseball|เบสบอล
🏉|Rugby|รักบี้
🏒|Hockey|ฮอกกี้
⛳|Golf|กอล์ฟ
🥋|Karate|คาราเต้
🥊|Boxing|มวย
🤼|Wrestling|มวยปล้ำ
🏋️|Weightlifting|ยกน้ำหนัก
⛷️|Skiing|เล่นสกี
🎣|Fishing|ตกปลา
🏹|Archery|ยิงธนู
♟️|Chess|หมากรุก
🎳|Bowling|โบว์ลิง
🎵|Music|ดนตรี
🎶|Song|เพลง
🎷|Saxophone|แซกโซโฟน
🎺|Trumpet|ทรัมเป็ต
🪈|Flute|ขลุ่ย
|Harp|พิณฝรั่ง
|Cello|เชลโล
|Ukulele|อูคูเลเล
|Xylophone|ระนาดฝรั่ง
|Harmonica|ฮาร์โมนิกา
|Running|วิ่ง
|Yoga|โยคะ
|Gymnastics|ยิมนาสติก
|Team|ทีม
|Coach|โค้ช`);
A('ทักทาย',`🍀|Good luck|โชคดี
⚠️|Be careful|ระวัง
|Excuse me|ขอโทษ (ขอทาง)
|See you later|แล้วเจอกัน
|See you tomorrow|เจอกันพรุ่งนี้
|Come in|เชิญเข้ามา
|Sit down|เชิญนั่ง
|Stand up|ยืนขึ้น
|Come here|มาที่นี่
|Hurry up|เร็วเข้า
|Take care|ดูแลตัวเองนะ
|I am fine|ฉันสบายดี
|What is your name|คุณชื่ออะไร
|My name is|ฉันชื่อ...
|How old are you|คุณอายุเท่าไร
|I love you|ฉันรักคุณ
|Thank you very much|ขอบคุณมาก
|You are welcome|ด้วยความยินดี
|Have a nice day|ขอให้เป็นวันที่ดี`);
A('เวลา',`🕒|Time|เวลา
🌄|Dawn|รุ่งเช้า
|Dusk|พลบค่ำ
|Date|วันที่
|Calendar|ปฏิทิน
|Holiday|วันหยุด
|Birthday|วันเกิด
|Bedtime|เวลานอน
|Sometimes|บางครั้ง
|Often|บ่อย ๆ
|Usually|ปกติ
|Soon|เร็ว ๆ นี้
|Later|ทีหลัง
|Before|ก่อน
|After|หลัง
|Next week|สัปดาห์หน้า
|Last week|สัปดาห์ที่แล้ว
|Every day|ทุกวัน
|Last year|ปีที่แล้ว
|Next year|ปีหน้า`);
A('ตัวเลข',`1st|First|ที่หนึ่ง
3rd|Third|ที่สาม
4th|Fourth|ที่สี่
5th|Fifth|ที่ห้า
200|Two hundred|สองร้อย
500|Five hundred|ห้าร้อย
➕|Plus|บวก
➖|Minus|ลบ
½|Half|ครึ่ง
|Number|ตัวเลข
|Pair|คู่
|Dozen|โหล
|Few|ไม่กี่
|Many|มาก (นับได้)
|Much|มาก (นับไม่ได้)
|Some|บาง
|All|ทั้งหมด
|None|ไม่มีเลย
|More|มากกว่า
|Less|น้อยกว่า
|Equal|เท่ากับ
|Double|สองเท่า`);
A('สรรพนาม',`|Me|ฉัน (กรรม)
|Him|เขา (กรรม)
|Them|พวกเขา (กรรม)
|Us|เรา (กรรม)
|Mine|ของฉัน
|Yours|ของคุณ
|Their|ของพวกเขา
|Its|ของมัน
|Whose|ของใครคนนั้น
|Myself|ตัวฉันเอง
|Himself|ตัวเขาเอง
|Herself|ตัวเธอเอง
|Everyone|ทุกคน
|Someone|บางคน
|Nobody|ไม่มีใคร
|Everything|ทุกสิ่ง
|Something|บางสิ่ง
|Nothing|ไม่มีอะไร
|Here|ที่นี่
|There|ที่นั่น
|Each|แต่ละ
|Both|ทั้งสอง
|Another|อีกอัน
|Other|อื่น ๆ
|Anyone|ใครก็ได้`);
A('คำบุพบท',`|Beside|ข้าง ๆ
|Beyond|เลยไป
|Through|ผ่าน
|Into|เข้าไปใน
|Onto|ขึ้นไปบน
|Off|ออก / หลุด
|Out|ข้างนอก
|Along|ตาม
|Toward|ไปทาง
|Against|พิง / ต่อต้าน
|Among|ท่ามกลาง
|Beneath|ใต้
|Opposite|ตรงข้าม
|By|ข้าง ๆ / โดย
|Of|ของ
|About|เกี่ยวกับ
|Without|ไม่มี
|Within|ภายใน
|Until|จนถึง
|Since|ตั้งแต่
|Except|ยกเว้น
|Past|ผ่านไป
|During|ในช่วง
|Over|เหนือ / ข้าม`);
A('กริยา',`👃|Smell|ได้กลิ่น
🔧|Fix|ซ่อม
🏗️|Build|สร้าง
🌱|Plant|ปลูก
💭|Dream|ฝัน
📢|Shout|ตะโกน
🔢|Count|นับ
▶️|Start|เริ่ม
🏁|Finish|เสร็จ
💼|Work|ทำงาน
|Bring|นำมา
|Carry|ถือ / แบก
|Send|ส่ง
|Call|โทร
|Meet|พบ
|Visit|เยี่ยม
|Travel|เดินทาง
|Fly|บิน
|Fall|ล้ม / ตก
|Find|ค้นหา
|Hide|ซ่อน
|Show|แสดง
|Keep|เก็บ
|Put|วาง
|Pull|ดึง
|Push|ผลัก
|Pick up|หยิบ
|Put on|สวม
|Take off|ถอด
|Turn on|เปิด (ไฟ)
|Turn off|ปิด (ไฟ)
|Paint|ทาสี
|Cut|ตัด
|Clean|ทำความสะอาด
|Brush|แปรง
|Tell|บอก
|Talk|พูดคุย
|Say|พูด / กล่าว
|Whisper|กระซิบ
|Choose|เลือก
|Win|ชนะ
|Lose|แพ้
|Try|ลอง
|Learn|เรียนรู้
|Remember|จำได้
|Forget|ลืม
|Understand|เข้าใจ
|Believe|เชื่อ
|Hope|หวัง
|Pay|จ่าย
|Sell|ขาย
|Share|แบ่งปัน
|Taste|ลิ้มรส
|Touch|สัมผัส
|Hear|ได้ยิน
|See|เห็น
|Feel|รู้สึก
|Hold|ถือ / จับ
|Rest|พักผ่อน
|Join|เข้าร่วม
|Follow|ตาม
|Return|กลับ
|Arrive|มาถึง
|Leave|ออกจาก
|Enter|เข้า
|Use|ใช้
|Spin|หมุน`);
A('อารมณ์',`🤓|Smart|ฉลาด
😎|Cool|เท่
😬|Nervous|ประหม่า
🥹|Grateful|ซาบซึ้ง
😡|Mad|โมโห
😱|Shocked|ตกใจ
|Proud|ภูมิใจ
|Lonely|เหงา
|Curious|อยากรู้อยากเห็น
|Jealous|อิจฉา
|Embarrassed|อาย
|Disappointed|ผิดหวัง
|Hopeful|มีความหวัง
|Peaceful|สงบสุข
|Cheerful|ร่าเริง
|Friendly|เป็นมิตร
|Kind|ใจดี
|Funny|ตลก
|Polite|สุภาพ
|Honest|ซื่อสัตย์
|Lazy|ขี้เกียจ
|Strong|แข็งแรง
|Weak|อ่อนแอ
|Upset|เสียใจ
|Afraid|กลัว
|Relaxed|ผ่อนคลาย
|Comfortable|สบาย
|Safe|ปลอดภัย
|Lucky|โชคดี
|Careful|ระมัดระวัง`);
A('สถานที่',`🏠|House|บ้าน
🏡|Home|บ้าน
🏫|School|โรงเรียน
🏥|Hospital|โรงพยาบาล
💊|Pharmacy|ร้านขายยา
🏤|Post office|ไปรษณีย์
🏧|ATM|ตู้เอทีเอ็ม
⛽|Gas station|ปั๊มน้ำมัน
🏭|Factory|โรงงาน
⛪|Church|โบสถ์
🕌|Mosque|มัสยิด
🏰|Castle|ปราสาท
🏜️|Desert|ทะเลทราย
🌋|Volcano|ภูเขาไฟ
🛝|Playground|สนามเด็กเล่น
⛲|Fountain|น้ำพุ
🌉|Bridge|สะพาน
🏘️|Village|หมู่บ้าน
🏙️|City|เมือง
🛣️|Road|ถนน
🚏|Bus stop|ป้ายรถเมล์
🛒|Supermarket|ซูเปอร์มาร์เก็ต
🏬|Shopping mall|ห้างสรรพสินค้า
🎡|Amusement park|สวนสนุก
|Police station|สถานีตำรวจ
|Cafe|ร้านกาแฟ
|Swimming pool|สระว่ายน้ำ
|Gym|ฟิตเนส
|Kitchen|ห้องครัว
|Bedroom|ห้องนอน
|Bathroom|ห้องน้ำ
|Living room|ห้องนั่งเล่น
|Garden|สวน
|Garage|โรงรถ`);
A('ธรรมชาติ',`🪨|Rock|หิน
🌱|Grass|หญ้า
🌹|Rose|กุหลาบ
🌻|Sunflower|ทานตะวัน
🪷|Lotus|ดอกบัว
🌵|Cactus|กระบองเพชร
🎋|Bamboo|ไผ่
🌍|Earth|โลก
🪐|Planet|ดาวเคราะห์
🧊|Ice|น้ำแข็ง
|Sand|ทราย
|Mud|โคลน
|Soil|ดิน
|Hill|เนินเขา
|Lake|ทะเลสาบ
|Waterfall|น้ำตก
|Cave|ถ้ำ
|Wave|คลื่น
|Ocean|มหาสมุทร
|Pond|สระน้ำ
|Stream|ลำธาร
|Branch|กิ่งไม้
|Root|ราก
|Seed|เมล็ด
|Bush|พุ่มไม้
|Space|อวกาศ
|Snowflake|เกล็ดหิมะ`);
A('คำคุณศัพท์',`🥵|Hot|ร้อน
🥶|Cold|หนาว / เย็น
🐇|Fast|เร็ว
✨|Clean|สะอาด
🤑|Rich|ร่ำรวย
🔊|Loud|เสียงดัง
🤫|Quiet|เงียบ
🌑|Dark|มืด
⚠️|Dangerous|อันตราย
|Big|ใหญ่
|Small|เล็ก
|Tall|สูง
|Short|เตี้ย / สั้น
|Long|ยาว
|Warm|อุ่น
|New|ใหม่
|Old|เก่า / แก่
|Young|อายุน้อย
|Slow|ช้า
|Good|ดี
|Bad|แย่
|Dirty|สกปรก
|Easy|ง่าย
|Hard|ยาก
|Heavy|หนัก
|Light|เบา
|Beautiful|สวย
|Pretty|น่ารัก
|Ugly|น่าเกลียด
|Poor|ยากจน
|Full|เต็ม / อิ่ม
|Empty|ว่างเปล่า
|Wet|เปียก
|Dry|แห้ง
|Soft|นุ่ม
|Sweet|หวาน
|Sour|เปรี้ยว
|Salty|เค็ม
|Spicy|เผ็ด
|Delicious|อร่อย
|Thick|หนา
|Thin|บาง / ผอม
|Wide|กว้าง
|Narrow|แคบ
|Low|ต่ำ
|Right|ถูก / ขวา
|Wrong|ผิด
|Left|ซ้าย
|Same|เหมือนกัน
|Different|แตกต่าง
|Busy|ยุ่ง
|Free|ว่าง / ฟรี
|Sharp|คม
|Round|กลม
|Flat|แบน
|Bright|สว่าง
|Far|ไกล
|Real|ของจริง
|Famous|มีชื่อเสียง
|Important|สำคัญ
|Special|พิเศษ`);
A('รูปทรง',`⭕|Circle|วงกลม
🟦|Square|สี่เหลี่ยมจัตุรัส
🔺|Triangle|สามเหลี่ยม
🔷|Diamond|ข้าวหลามตัด
|Rectangle|สี่เหลี่ยมผืนผ้า
|Oval|วงรี
|Cube|ลูกบาศก์
|Sphere|ทรงกลม
|Cone|กรวย
|Cylinder|ทรงกระบอก
|Line|เส้น
|Curve|เส้นโค้ง
|Corner|มุม
|Side|ด้าน
|Shape|รูปทรง`);
const TH='หนึ่ง สอง สาม สี่ ห้า หก เจ็ด แปด เก้า สิบ'.split(' ');
['One','Two','Three','Four','Five','Six','Seven','Eight','Nine','Ten'].forEach((e,i)=>W.push([i<9?(i+1)+'\uFE0F\u20E3':'🔟',e,TH[i],'ตัวเลข']));
const $=s=>document.querySelector(s),$$=s=>[...document.querySelectorAll(s)],G=$('#g'),sh=a=>[...a].sort(()=>Math.random()-.5);
const say=t=>{try{speechSynthesis.cancel();const u=new SpeechSynthesisUtterance(t),v=speechSynthesis.getVoices().filter(x=>/^en[-_]US/i.test(x.lang)),b=v.find(x=>/google|samantha|aria|jenny|natural/i.test(x.name))||v[0];if(b)u.voice=b;u.lang='en-US';u.rate=.55;u.pitch=1;speechSynthesis.speak(u)}catch(e){}};
const cats=[...new Set(W.map(w=>w[3]))];let cat='all',stars=0,lv=1,mx=1,tm=0;
const SK='vocabgame-progress-v1',PK='vocabgame-players-v1',AV=['🐶','🐱','🐰','🐼','🦁','🐸','🦄','🐯'];
let P={cur:'',list:{}};try{const x=JSON.parse(localStorage.getItem(PK));if(x&&x.list)P=x}catch(e){}
const esc=s=>String(s).replace(/[&<>"']/g,c=>'&#'+c.charCodeAt(0)+';'),av=()=>(P.list[P.cur]||{}).av||0,
hs=s=>{let h=7;for(const c of s.toLowerCase())h=(h*31+c.charCodeAt(0))%1296;return h.toString(36).padStart(2,'0')},
enc=o=>{const b=o.n+'~'+o.s.toString(36)+'-'+o.m+o.l+o.a;return b+hs(b)},
dec=c=>{try{c=c.trim();const b=c.slice(0,-2);if(hs(b)!=c.slice(-2).toLowerCase())return null;const i=b.lastIndexOf('~'),[s,r]=b.slice(i+1).toLowerCase().split('-');if(i<1||!r||r.length!=3)return null;return{n:b.slice(0,i),s:parseInt(s,36)||0,m:Math.min(5,Math.max(1,+r[0]||1)),l:Math.min(5,Math.max(1,+r[1]||1)),a:Math.min(7,Math.max(0,+r[2]||0))}}catch(e){return null}},
save=()=>{if(P.cur)P.list[P.cur]={stars,lv,mx,tm:tm?1:0,cat,av:av()};try{localStorage.setItem(PK,JSON.stringify(P))}catch(e){}};
function setP(n){P.cur=n;const d=P.list[n]||{};stars=d.stars||0;mx=Math.min(5,Math.max(1,d.mx||1));lv=Math.min(mx,Math.max(1,d.lv||1));tm=d.tm?1:0;cat=d.cat=='all'||cats.includes(d.cat)?d.cat:'all';save();home()}
function who(m=''){
 const ns=Object.keys(P.list);let a=0;
 G.innerHTML=`<h1>👋 ใครกำลังเล่น?</h1>${m?`<div class="msg bad">${m}</div>`:''}${ns.length?`<div class=menu>${ns.map(n=>`<button class=card data-p="${esc(n)}"><span>${AV[P.list[n].av||0]}</span><b>${esc(n)}</b><small>⭐ ${P.list[n].stars||0} · เลเวล ${P.list[n].mx||1}</small></button>`).join('')}</div>`:''}<h2>➕ ผู้เล่นใหม่</h2><input id=nm class=inp maxlength=12 placeholder="พิมพ์ชื่อเล่นของหนู"><div class=chips style="justify-content:center">${AV.map((x,i)=>`<button class="chip ${i?'':'on'}" data-a=${i}>${x}</button>`).join('')}</div><button class=big id=go>เริ่มเล่น 🚀</button><h2>🔑 มีรหัสผู้เล่นแล้ว?</h2><input id=cd class=inp style="font-size:16px" placeholder="วางรหัสที่นี่"><button class="big alt" id=ld>โหลดความคืบหน้า</button>`;
 $$('[data-p]').forEach(b=>b.onclick=()=>setP(b.dataset.p));
 $$('[data-a]').forEach(b=>b.onclick=()=>{a=+b.dataset.a;$$('[data-a]').forEach(x=>x.classList.toggle('on',x==b))});
 $('#go').onclick=()=>{const n=$('#nm').value.trim();if(!n)return who('กรุณาพิมพ์ชื่อเล่นก่อนนะ');if(!P.list[n])P.list[n]=ns.length?{av:a}:{stars,lv,mx,tm,cat,av:a};setP(n)};
 $('#ld').onclick=()=>{const d=dec($('#cd').value);if(!d)return who('รหัสไม่ถูกต้อง ลองคัดลอกใหม่อีกครั้ง');const o=P.list[d.n]||{};P.list[d.n]={stars:Math.max(o.stars||0,+d.s||0),mx:Math.max(o.mx||1,+d.m||1),lv:+d.l||1,av:+d.a||0};setP(d.n)}}
function mycode(){const c=enc({n:P.cur,s:stars,m:mx,l:lv,a:av()});
 G.innerHTML=`<div class=top><button class=back>⬅ กลับ</button></div><h2>🔑 รหัสผู้เล่นของ ${esc(P.cur)}</h2><p class=cen>คัดลอกรหัสนี้เก็บไว้ (เช่น ส่งเข้า LINE ตัวเอง) แล้วไปวางที่หน้า “ใครกำลังเล่น?” ในเครื่องอื่น เพื่อเล่นต่อจากเดิม</p><textarea id=cc class=inp rows=2 readonly style="font-size:22px;word-break:break-all;text-align:center">${c}</textarea><button class=big id=cp>📋 คัดลอกรหัส</button><p class=mut>รหัสจะเปลี่ยนเมื่อได้ดาวเพิ่ม ควรคัดลอกใหม่ทุกครั้งก่อนเปลี่ยนเครื่อง</p>`;
 $('.back').onclick=home;$('#cc').onclick=e=>e.target.select();
 $('#cp').onclick=async()=>{$('#cc').select();try{await navigator.clipboard.writeText(c);$('#cp').textContent='✅ คัดลอกแล้ว'}catch(e){try{document.execCommand('copy');$('#cp').textContent='✅ คัดลอกแล้ว'}catch(_){$('#cp').textContent='แตะที่กล่องแล้วกดคัดลอกเอง'}}}}
try{const s=P.cur&&P.list[P.cur]?P.list[P.cur]:JSON.parse(localStorage.getItem(SK));if(s){stars=+s.stars||0;mx=Math.min(5,Math.max(1,+s.mx||1));lv=Math.min(mx,Math.max(1,+s.lv||1));tm=s.tm?1:0;cat=cats.includes(s.cat)?s.cat:'all'}}catch(e){}
const pool=(f=()=>true)=>{const L=w=>f(w)&&w[1].length<=[4,5,7,9,99][lv-1],C=w=>cat=='all'||w[3]==cat;let p=W.filter(w=>C(w)&&L(w));if(p.length<4)p=W.filter(w=>C(w)&&f(w));return p.length>=4?p:W.filter(f)};
const rest=w=>sh(pool().filter(x=>x[1]!=w[1])).slice(0,lv>3?5:3);
const choose=(w,o,f)=>$$('.opt').forEach((b,k)=>b.onclick=()=>{$$('.opt').forEach(x=>x.disabled=true);const r=o[k]===w;$$('.opt')[o.indexOf(w)].classList.add('ok');if(!r)b.classList.add('bad');say(w[1]);f(r)});
const flash=b=>{b.classList.add('bad','shake');setTimeout(()=>b.classList.remove('bad','shake'),450)};
const E=w=>w[0]||w[2],pic=(w,spk=1)=>`<div class="pic ${w[0]?'':'t'}">${E(w)}</div><p class=cen>${w[2]} ${spk?'<button class=spk>🔊</button>':''}</p>`;
const GAMES=[{i:'📚',t:'เรียนรู้ (บัตรคำ)',d:'ดูรูป ฟังเสียง จำคำศัพท์',l:1},
{i:'🔤',t:'เติมตัวอักษร',d:'เลือกตัวอักษรที่หายไป',n:8,q(w,f){
 const s=[...w[1]],ix=s.map((c,k)=>/[a-z]/i.test(c)?k:-1).filter(k=>k>=0),bl=sh(ix).slice(0,Math.min(Math.ceil(lv/2),s.length>4?3:s.length>3?2:1)).sort((a,b)=>a-b);
 let p=0,m=0;const t=s.map((c,k)=>bl.includes(k)?'_':c),need=bl.map(k=>s[k].toLowerCase()),
 op=sh([...need,...sh([...'abcdefghijklmnopqrstuvwxyz'].filter(c=>!need.includes(c))).slice(0,6-need.length)]);
 $('#q').innerHTML=pic(w)+`<div class=word id=wd></div><div class=g3>${op.map(c=>`<button class=opt>${c}</button>`).join('')}</div>`;
 const dr=()=>$('#wd').innerHTML=t.map(c=>`<span class="${c=='_'?'bl':''}">${c}</span>`).join('');dr();
 $$('.opt').forEach(b=>b.onclick=()=>{if(b.textContent==need[p]){t[bl[p]]=s[bl[p]];p++;b.disabled=true;dr();if(p==bl.length){say(w[1]);f(m==0)}}else{m++;flash(b)}})}},
{i:'🖼️',t:'ทายคำจากรูป',d:'ดูรูปแล้วเลือกคำศัพท์',n:8,q(w,f){
 const o=sh([w,...rest(w)]);
 $('#q').innerHTML=`<div class="pic ${w[0]?'':'t'}">${E(w)}</div><p class=cen>ภาษาอังกฤษคืออะไร?</p><div class=g2>${o.map(x=>`<button class=opt>${x[1]}</button>`).join('')}</div>`;choose(w,o,f)}},
{i:'🧩',t:'เรียงตัวอักษร',d:'สะกดคำให้ถูกต้อง',n:6,f:w=>/^[A-Za-z]{3,9}$/.test(w[1]),q(w,f){
 const s=w[1].toLowerCase(),L=sh([...s]);let a='',m=0;const u=[];
 $('#q').innerHTML=pic(w)+`<div class=word id=wd></div><div class=g4>${L.map(c=>`<button class=opt>${c}</button>`).join('')}</div><button class=alt2 id=un>⌫ ลบตัวล่าสุด</button>`;
 const dr=()=>$('#wd').innerHTML=[...s].map((c,k)=>`<span class="${k<a.length?'':'bl'}">${k<a.length?a[k]:'_'}</span>`).join('');dr();
 const bs=$$('.opt');
 bs.forEach((b,k)=>b.onclick=()=>{a+=L[k];u.push(k);b.disabled=true;dr();
  if(a.length==s.length){if(a==s){$('#un').remove();say(w[1]);f(m==0)}else{m++;flash($('#wd'));setTimeout(()=>{a='';u.length=0;bs.forEach(x=>x.disabled=false);dr()},450)}}});
 $('#un').onclick=()=>{if(u.length&&a.length<s.length){bs[u.pop()].disabled=false;a=a.slice(0,-1);dr()}}}},
{i:'👂',t:'ฟังแล้วเลือกรูป',d:'ฟังเสียงแล้วแตะรูปที่ถูก',n:8,a:1,q(w,f){
 const o=sh([w,...rest(w)]);
 $('#q').innerHTML=`<p class=cen>ฟังแล้วเลือกรูปที่ใช่</p><button class=big id=pl>🔊 ฟังอีกครั้ง</button><div class=g2>${o.map(x=>`<button class="opt ${x[0]?'em':''}">${E(x)}</button>`).join('')}</div>`;
 $('#pl').onclick=()=>say(w[1]);choose(w,o,f)}},
{i:'🃏',t:'จับคู่รูปกับคำ',d:'เปิดการ์ดหาคู่ที่เหมือนกัน',n:3,s:45,q(w,f){
 const ps=sh([w,...rest(w)]),cs=sh(ps.flatMap(x=>[{x,t:0},{x,t:1}]));let sel=null,left=ps.length;
 $('#q').innerHTML=`<p class=cen>จับคู่รูปกับคำศัพท์</p><div class=g4>${cs.map(c=>`<button class="opt ${c.t||!c.x[0]?'':'em'}">${c.t?c.x[1]:E(c.x)}</button>`).join('')}</div>`;
 const bs=$$('.opt');
 bs.forEach((b,k)=>b.onclick=()=>{if(b.classList.contains('ok')||b==sel)return;
  if(!sel){sel=b;b.classList.add('on');say(cs[k].x[1]);return}
  const a=cs[bs.indexOf(sel)],c=cs[k];
  if(a.x===c.x&&a.t!=c.t){sel.classList.remove('on');sel.classList.add('ok');b.classList.add('ok');sel=null;say(c.x[1]);if(--left==0)f(true)}
  else{const s2=sel;sel=null;flash(b);flash(s2);s2.classList.remove('on')}})}},
{i:'✍️',t:'เขียนตามคำบอก',d:'ฟังแล้วพิมพ์คำศัพท์',n:6,a:1,f:w=>/^[A-Za-z ]+$/.test(w[1]),q(w,f){
 let m=0;const s=w[1].toLowerCase();
 $('#q').innerHTML=`<p class=cen>ฟังแล้วพิมพ์คำที่ได้ยิน</p><div class="pic ${w[0]?'':'t'}">${w[0]||'🎧'}</div><p class=cen>คำใบ้: ${w[2]}</p><button class=big id=pl>🔊 ฟังอีกครั้ง</button><input id=ip class=inp autocomplete=off autocapitalize=off autocorrect=off spellcheck=false placeholder="พิมพ์คำตอบที่นี่"><button class="big alt" id=ck>ตรวจคำตอบ ✔</button><p class=cen id=hn></p>`;
 $('#pl').onclick=()=>say(w[1]);
 const go=()=>{const v=$('#ip').value.trim().toLowerCase().replace(/\s+/g,' ');if(!v)return;
  if(v==s){$('#ip').disabled=$('#ck').disabled=true;say(w[1]);f(m==0)}
  else{m++;flash($('#ip'));if(m>=3){$('#ip').disabled=$('#ck').disabled=true;f(false)}else $('#hn').textContent='ลองอีกครั้ง! ขึ้นต้นด้วย '+s[0].toUpperCase()+' มี '+s.replace(/ /g,'').length+' ตัวอักษร'}};
 $('#ck').onclick=go;$('#ip').onkeydown=e=>{if(e.key=='Enter')go()};setTimeout(()=>$('#ip').focus(),100)}}
];
let dbp=null,sv=0,pd=0;
const cloud=async()=>{if(!dbp)return;if(sv){pd=1;return}sv=1;try{await dbp.set({stars,lv,mx,tm:tm?1:0,cat})}catch(e){}sv=0;if(pd){pd=0;cloud()}};
(async()=>{try{return;const[db,u]=await Promise.all([claude.use('db'),claude.use('user')]);if(!db||!u)return;const id=await u.id();if(!id)return;const r=db.doc('data/users/'+id+'/progress'),s=await r.get();if(s.exists){const d=s.data();stars=Math.max(stars,+d.stars||0);mx=Math.min(5,Math.max(mx,+d.mx||1));lv=Math.min(mx,Math.max(1,+d.lv||lv));if(d.cat=='all'||cats.includes(d.cat))cat=d.cat}dbp=r;if($('.menu'))home();else save()}catch(e){}})();
function home(){if(!P.cur||!P.list[P.cur])return who();save();
 G.innerHTML=`<h1>🌟 เกมคำศัพท์ภาษาอังกฤษ</h1><div class=chips style="justify-content:center"><button class=chip id=pw>${AV[av()]} ${esc(P.cur)} ▾ เปลี่ยนผู้เล่น</button><button class=chip id=kc>🔑 รหัสของฉัน</button></div><p class=mut>สำหรับเด็ก ป.1–ป.3 · ดาวของฉัน ⭐ <b>${stars}</b></p>
 <div class=chips>${['all',...cats].map(c=>`<button class="chip ${c==cat?'on':''}" data-c="${c}">${c=='all'?'ทุกหมวด':c}</button>`).join('')}</div>
 <div class=chips>${[1,2,3,4,5].map(n=>`<button class="chip ${n==lv?'on':''}" data-l=${n} ${n>mx?'disabled':''}>${n>mx?'🔒':'⭐'} เลเวล ${n}</button>`).join('')}<button class="chip ${tm?'on':''}" id=tmb>⏱️ จับเวลา: ${tm?'เปิด':'ปิด'}</button></div>
 <div class=menu>${GAMES.map((g,i)=>`<button class=card data-g=${i}><span>${g.i}</span><b>${g.t}</b><small>${g.d}</small></button>`).join('')}</div><button class=alt2 id=rs>🔄 เริ่มใหม่ (ล้างดาวและเลเวล)</button>`;
 $$('[data-c]').forEach(b=>b.onclick=()=>{cat=b.dataset.c;home()});
 $('#pw').onclick=()=>who();$('#kc').onclick=mycode;let rr=0;$('#rs').onclick=e=>{if(!rr){rr=1;e.target.textContent='แตะอีกครั้งเพื่อยืนยันการล้าง';return}stars=0;lv=1;mx=1;home()};
 $$('[data-l]').forEach(b=>b.onclick=()=>{lv=+b.dataset.l;home()});$('#tmb').onclick=()=>{tm=!tm;home()};
 $$('[data-g]').forEach(b=>b.onclick=()=>GAMES[b.dataset.g].l?learn():play(GAMES[b.dataset.g]));
}
function play(g){
 const ws=sh(pool(g.f)).slice(0,Math.round(g.n*1.5));let i=0,ok=0;
 const step=()=>{
  if(i>=ws.length)return end();
  const w=ws[i];let dn=0,tmr;
  G.innerHTML=`<div class=top><button class=back>⬅ กลับ</button><span>Lv.${lv} · ข้อ ${i+1}/${ws.length}</span><span>✅ ${ok}</span></div><div id=q></div><div id=fb></div>`;
  $('.back').onclick=()=>{clearInterval(tmr);home()};
  const fin=r=>{if(dn)return;dn=1;clearInterval(tmr);if(r){ok++;stars++}i++;save();
   $('#fb').innerHTML=`<div class="msg ${r?'ok':'bad'}">${r?'เก่งมาก! 🎉':'เกือบถูกแล้ว สู้ๆ 💪'}<br>${w[0]} ${w[1]} = ${w[2]}</div><button class=big id=nx>ต่อไป ➡</button>`;
   $('#nx').onclick=step;$('#nx').scrollIntoView({block:'nearest'})};
  g.q(w,fin);
  if(tm){let T=g.s||[20,18,16,14,12][lv-1],t=T;$('#q').insertAdjacentHTML('afterbegin','<div class=bar><i id=bar></i></div>');tmr=setInterval(()=>{t-=.1;$('#bar').style.width=(t/T*100)+'%';if(t<=0){$$('#q button,#q input').forEach(x=>x.disabled=true);fin(false)}},100)}
  $$('.spk').forEach(b=>b.onclick=()=>say(w[1]));
  if(g.a)setTimeout(()=>say(w[1]),350);
 };
 const end=()=>{const up=ok>=ws.length*.8&&lv==mx&&mx<5&&++mx;G.innerHTML=`<div class=end><div class=e>${ok>=ws.length*.8?'🏆':'⭐'}</div><h2>ได้ ${ok} จาก ${ws.length} ข้อ</h2>${up?`<div class="msg ok">🔓 ปลดล็อกเลเวล ${mx} แล้ว!</div>`:''}<p class=mut>ดาวทั้งหมด ⭐ ${stars}</p><button class=big id=ag>เล่นอีกครั้ง 🔁</button><button class="big alt" id=hm>เมนูหลัก 🏠</button></div>`;$('#ag').onclick=()=>play(g);$('#hm').onclick=home};
 step();
}
function learn(){const L=W.filter(w=>cat=='all'||w[3]==cat);let k=0;
 const dr=()=>{const w=L[k];G.innerHTML=`<div class=top><button class=back>⬅ กลับ</button><span>${k+1}/${L.length}</span></div>${pic(w)}<div class=word style="font-size:44px">${w[1]}</div><div class=g2><button class=opt id=pv>◀ ก่อนหน้า</button><button class=opt id=nt>ถัดไป ▶</button></div>`;
  $('.back').onclick=home;$('.spk').onclick=()=>say(w[1]);$('#pv').onclick=()=>{k=(k+L.length-1)%L.length;dr()};$('#nt').onclick=()=>{k=(k+1)%L.length;dr()};say(w[1])};dr()}
home();
</script></body></html>
