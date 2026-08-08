<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width,initial-scale=1.0">
<title>USDT Wallet</title>

<style>
*{box-sizing:border-box}

body{
    margin:0;
    background:#e9e5dc;
    font-family:Arial,Helvetica,sans-serif;
    color:#191815;
}

.app{
    width:100%;
    max-width:520px;
    min-height:100vh;
    margin:auto;
    background:#f7f4ea;
    padding-bottom:90px;
}

/* HEADER */
header{
    height:75px;
    padding:14px 20px;
    display:flex;
    align-items:center;
    justify-content:space-between;
    background:#f7f4ea;
    position:sticky;
    top:0;
    z-index:10;
}

.menu-btn,.profile-circle{
    width:45px;
    height:45px;
    border-radius:14px;
    display:flex;
    align-items:center;
    justify-content:center;
}

.menu-btn{
    border:1px solid #ddd8ca;
    background:#fffdf8;
    font-size:24px;
    cursor:pointer;
}

.profile-circle{
    border-radius:50%;
    background:#29251d;
    color:#d7b54b;
    font-weight:bold;
}

.logo{
    display:flex;
    align-items:center;
    gap:9px;
    font-weight:bold;
    font-size:20px;
}

.logo-box{
    width:42px;
    height:42px;
    border:1px solid #caa948;
    border-radius:12px;
    display:flex;
    align-items:center;
    justify-content:center;
    color:#b18a20;
    font-size:23px;
}

/* CONTENT */
.content{
    padding:28px 20px;
}

.small-title{
    color:#aa821c;
    letter-spacing:2px;
    font-weight:bold;
    font-size:13px;
    margin-bottom:10px;
}

h1{
    font-size:43px;
    margin:0 0 28px;
    letter-spacing:-2px;
}

h2{
    margin:0;
}

/* BALANCE */
.balance{
    background:#302b20;
    color:white;
    border-radius:30px;
    padding:28px;
}

.balance-label{
    color:#bdb7a9;
}

.live{
    float:right;
    color:#a9d873;
    font-size:13px;
}

.balance-number{
    font-size:62px;
    font-weight:300;
    margin:50px 0 35px;
}

.balance-number span{
    font-size:20px;
}

.value{
    color:#c5beb0;
}

.rate{
    float:right;
    background:#4a4029;
    color:#e0c052;
    padding:10px;
    border-radius:10px;
}

/* ACTIONS */
.section-title{
    display:flex;
    justify-content:space-between;
    margin:38px 0 15px;
}

.actions{
    display:grid;
    grid-template-columns:1fr 1fr;
    gap:14px;
}

.action{
    height:205px;
    border-radius:28px;
    border:1px solid #ddd8ca;
    padding:22px;
    text-align:left;
    cursor:pointer;
}

.action.dark{
    background:#302b20;
    color:white;
}

.action.light{
    background:#eee5cf;
}

.action-icon{
    font-size:28px;
    margin-bottom:55px;
}

.action-title{
    font-size:20px;
    font-weight:bold;
    margin-bottom:6px;
}

/* CARDS */
.card{
    background:#fffdf9;
    border:1px solid #e3ded2;
    border-radius:24px;
    padding:24px;
    margin-bottom:18px;
}

.activity{
    display:flex;
    align-items:center;
    gap:15px;
}

.activity-icon{
    width:55px;
    height:55px;
    border-radius:16px;
    background:#f3dddd;
    display:flex;
    align-items:center;
    justify-content:center;
}

.grow{
    flex:1;
}

/* FORMS */
.form-card{
    background:#fffdf9;
    border:1px solid #e3ded2;
    border-radius:25px;
    padding:25px;
}

.networks{
    display:grid;
    grid-template-columns:1fr 1fr;
    gap:12px;
    margin:20px 0;
}

.network{
    padding:18px;
    border:1px solid #ded9ce;
    background:white;
    border-radius:17px;
    text-align:left;
    cursor:pointer;
}

.network.active{
    border:2px solid #d2b45c;
    background:#fcf8e9;
}

label{
    display:block;
    font-weight:bold;
    margin:18px 0 8px;
}

input{
    width:100%;
    padding:17px;
    border:1px solid #ddd8ce;
    border-radius:15px;
    background:#f8f6f1;
    font-size:16px;
    outline:none;
}

input:focus{
    border-color:#c49a27;
}

.summary{
    margin-top:20px;
    background:#fffdf9;
    border:1px solid #e3ded2;
    border-radius:24px;
    padding:24px;
}

.row{
    display:flex;
    justify-content:space-between;
    padding:14px 0;
    border-bottom:1px solid #e5e0d6;
}

.primary{
    width:100%;
    border:0;
    background:#c69b21;
    padding:18px;
    border-radius:16px;
    font-weight:bold;
    font-size:16px;
    cursor:pointer;
    margin-top:20px;
}

/* QUICK BUTTONS */
.quick{
    display:flex;
    gap:8px;
    margin-top:10px;
}

.quick button{
    flex:1;
    padding:12px 5px;
    background:white;
    border:1px solid #ddd8ce;
    border-radius:12px;
    cursor:pointer;
}

/* BOTTOM NAV */
.bottom-nav{
    position:fixed;
    bottom:0;
    left:50%;
    transform:translateX(-50%);
    width:100%;
    max-width:520px;
    height:82px;
    background:#fffdf9;
    border-top:1px solid #ddd8ce;
    display:grid;
    grid-template-columns:repeat(4,1fr);
    z-index:20;
}

.bottom-nav button{
    border:0;
    background:none;
    color:#77736c;
    cursor:pointer;
    display:flex;
    flex-direction:column;
    align-items:center;
    justify-content:center;
    gap:5px;
}

.bottom-nav button.active{
    color:#b08a21;
    font-weight:bold;
}

.nav-icon{
    font-size:24px;
}

/* SIDE MENU */
.overlay{
    position:fixed;
    inset:0;
    background:#0005;
    display:none;
    z-index:50;
}

.overlay.show{
    display:block;
}

.drawer{
    width:min(90%,420px);
    height:100%;
    background:#f7f4ea;
    padding:25px 20px;
}

.drawer-head{
    display:flex;
    justify-content:space-between;
    align-items:center;
    margin-bottom:20px;
}

.close{
    width:45px;
    height:45px;
    border:1px solid #ddd8ce;
    background:white;
    border-radius:14px;
    font-size:25px;
}

.menu-item{
    padding:20px 10px;
    border-bottom:1px solid #e0dbd0;
    font-size:18px;
    cursor:pointer;
}

/* PROFILE */
.profile-box{
    display:flex;
    align-items:center;
    gap:18px;
}

.big-avatar{
    width:65px;
    height:65px;
    border-radius:50%;
    background:#29251d;
    color:#d7b54b;
    display:flex;
    justify-content:center;
    align-items:center;
    font-size:24px;
    font-weight:bold;
}

.muted{
    color:#8b877f;
}

@media(max-width:390px){
    h1{font-size:37px}
    .balance-number{font-size:52px}
    .actions{gap:9px}
    .action{padding:18px}
}
</style>
</head>

<body>

<div class="app">

<header>
    <button class="menu-btn" onclick="openMenu()">☰</button>

    <div class="logo">
        <div class="logo-box">W</div>
        USDT Wallet
    </div>

    <div class="profile-circle">P</div>
</header>

<div class="content" id="content"></div>

<!-- BOTTOM NAV -->
<div class="bottom-nav">

<button id="nav-home" onclick="page('home')">
<span class="nav-icon">⌂</span>
Home
</button>

<button id="nav-orders" onclick="page('orders')">
<span class="nav-icon">▤</span>
Orders
</button>

<button id="nav-history" onclick="page('history')">
<span class="nav-icon">◴</span>
History
</button>

<button id="nav-profile" onclick="page('profile')">
<span class="nav-icon">♙</span>
Profile
</button>

</div>

<!-- SIDE MENU -->
<div class="overlay" id="overlay">

<div class="drawer">

<div class="drawer-head">
<h2>Menu</h2>
<button class="close" onclick="closeMenu()">×</button>
</div>

<div class="menu-item" onclick="menuPage('home')">
⌂ &nbsp; Home
</div>

<div class="menu-item" onclick="menuPage('orders')">
▤ &nbsp; Orders
</div>

<div class="menu-item" onclick="menuPage('history')">
◴ &nbsp; History
</div>

<div class="menu-item" onclick="menuPage('profile')">
♙ &nbsp; Profile
</div>

<div class="menu-item">
♧ &nbsp; Support
</div>

<div class="menu-item">
▧ &nbsp; Legal & Policies
</div>

<div class="menu-item">
? &nbsp; About USDT Wallet
</div>

</div>
</div>

</div>


<script>

let balance = 3;
let network = "TRC20";
let buyAmount = 15;


/* HOME */

function home(){

return `

<div class="small-title">
GOOD MORNING, PRINCE
</div>

<h1>Overview</h1>

<div class="balance">

<div class="balance-label">
Available balance

<span class="live">● LIVE</span>
</div>

<div class="balance-number">
${balance.toFixed(2)}
<span>USDT</span>
</div>

<div class="value">
₹${(balance*96).toFixed(2)} estimated value

<span class="rate">
1 USDT = ₹96
</span>
</div>

</div>


<div class="section-title">
<h2>Move money</h2>
<span class="muted">Fast & direct</span>
</div>


<div class="actions">

<button class="action dark" onclick="page('buy')">

<div class="action-icon">↓</div>

<div class="action-title">
Buy USDT
</div>

From ₹1,440

</button>


<button class="action light" onclick="page('send')">

<div class="action-icon">↗</div>

<div class="action-title">
Send USDT
</div>

TRC20 or BEP20

</button>

</div>


<div class="section-title">
<h2>Recent activity</h2>
<span class="muted">View all ›</span>
</div>


<div class="card activity">

<div class="activity-icon">↗</div>

<div class="grow">
<b>One-time signup bonus</b>
<div class="muted">
03 Aug 2026 · Completed
</div>
</div>

<b>+3.00 USDT</b>

</div>

`;

}


/* BUY */

function buy(){

return `

<div class="small-title">
SIMPLE, TRANSPARENT PRICING
</div>

<h1>Buy USDT</h1>


<div class="form-card">

<div style="display:flex;justify-content:space-between">
<b>How much USDT?</b>
<span class="muted">Min 15 · Max 5,000</span>
</div>


<label>USDT amount</label>

<input
id="buyInput"
type="number"
min="15"
max="5000"
value="${buyAmount}"
oninput="calculateBuy()"
>


<div class="quick">

<button onclick="setBuy(15)">15</button>
<button onclick="setBuy(50)">50</button>
<button onclick="setBuy(100)">100</button>
<button onclick="setBuy(250)">250</button>
<button onclick="setBuy(500)">500</button>

</div>

</div>


<div class="summary">

<div class="muted">
You'll pay
</div>

<div id="total"
style="font-size:42px;font-weight:bold;margin:12px 0 25px">
₹${(buyAmount*96).toLocaleString('en-IN')}.00
</div>


<div class="row">
<span>Rate</span>
<b>₹96.00 / USDT</b>
</div>

<div class="row">
<span>Processing fee</span>
<b style="color:#4d7e69">Included</b>
</div>

<div class="row">
<span>You'll receive</span>
<b id="receive">${buyAmount.toFixed(2)} USDT</b>
</div>


<button class="primary" onclick="payment()">
Continue to payment ↗
</button>

</div>

`;

}


function calculateBuy(){

let value=Number(document.getElementById("buyInput").value);

if(value<0)value=0;

buyAmount=value;

document.getElementById("total").innerText=
"₹"+(value*96).toLocaleString("en-IN")+".00";

document.getElementById("receive").innerText=
value.toFixed(2)+" USDT";

}


function setBuy(value){

buyAmount=value;

page("buy");

}


function payment(){

alert(
"Demo payment page.\n\nNo real UPI or cryptocurrency transaction is processed."
);

}


/* SEND */

function send(){

return `

<div class="small-title">
MOVE USDT SECURELY
</div>

<h1>Send USDT</h1>


<div class="form-card">

<div style="display:flex;justify-content:space-between">
<b>Choose network</b>
<span class="muted">Network fees may apply</span>
</div>


<div class="networks">

<button
class="network ${network==="TRC20"?"active":""}"
onclick="chooseNetwork('TRC20')"
>

<b>⌘ TRC20</b>
<span class="muted">Tron network</span>

</button>


<button
class="network ${network==="BEP20"?"active":""}"
onclick="chooseNetwork('BEP20')"
>

<b>⌘ BEP20</b>
<span class="muted">BNB Smart Chain</span>

</button>

</div>


<label>
Recipient wallet address
</label>

<input
id="wallet"
placeholder="Paste wallet address"
>


<label>
Amount to send
</label>

<input
id="sendAmount"
type="number"
placeholder="0.00"
min="0"
max="${balance}"
oninput="updateSummary()"
>


<div class="row">
<span>Available balance</span>
<b>${balance.toFixed(2)} USDT</b>
</div>

</div>


<div class="summary">

<h2>Transfer summary</h2>


<div class="row">
<span>Network</span>
<b>${network}</b>
</div>


<div class="row">
<span>Amount</span>
<b id="sendSummary">—</b>
</div>


<div class="row">
<span>Remaining balance</span>
<b id="remaining">${balance.toFixed(2)} USDT</b>
</div>


<button class="primary" onclick="reviewSend()">
Review transfer ↗
</button>

</div>

`;

}


function chooseNetwork(value){

network=value;

page("send");

}


function updateSummary(){

let amount=Number(
document.getElementById("sendAmount").value
)||0;

document.getElementById("sendSummary").innerText=
amount.toFixed(2)+" USDT";

document.getElementById("remaining").innerText=
Math.max(0,balance-amount).toFixed(2)+" USDT";

}


function reviewSend(){

let address=document.getElementById("wallet").value.trim();

let amount=Number(
document.getElementById("sendAmount").value
);

if(!address){

alert("Please enter a wallet address.");

return;

}

if(!amount || amount<=0){

alert("Please enter an amount.");

return;

}

if(amount>balance){

alert("Insufficient demo balance.");

return;

}

alert(
"Transfer review\n\n"+
"Network: "+network+
"\nAmount: "+amount.toFixed(2)+" USDT"+
"\n\nDemo only — no real USDT is sent."
);

}


/* ORDERS */

function orders(){

return `

<div class="small-title">
YOUR ORDERS
</div>

<h1>Orders</h1>

<div class="card">

<h3>No orders yet</h3>

<p class="muted">
Your USDT purchase orders will appear here.
</p>

</div>

`;

}


/* HISTORY */

function history(){

return `

<div class="small-title">
ACTIVITY
</div>

<h1>History</h1>


<div class="card activity">

<div class="activity-icon">
↗
</div>

<div class="grow">

<b>One-time signup bonus</b>

<div class="muted">
03 Aug 2026 · Completed
</div>

</div>

<b>+3.00 USDT</b>

</div>

`;

}


/* PROFILE */

function profile(){

return `

<div class="small-title">
YOUR ACCOUNT
</div>

<h1>Profile</h1>


<div class="card">

<div class="profile-box">

<div class="big-avatar">
P
</div>

<div>

<div style="font-size:24px">
Prince
</div>

<div class="muted">
Demo account
</div>

<div class="muted">
demo@example.com
</div>

</div>

</div>

</div>


<div class="card">
<h3>🔒 Change password</h3>
</div>

<div class="card">
<h3>♧ Support centre</h3>
</div>

<div class="card">
<h3>▧ Legal & Policies</h3>
</div>

<div class="card">

<h3>? About USDT Wallet</h3>

<p class="muted">
Version 1.0 · Demo website
</p>

</div>


<button
class="primary"
style="background:#f5dddd;color:#a74343"
onclick="alert('Demo logout')"
>
↪ Log out
</button>

`;

}


/* PAGE ROUTING */

function page(name){

if(name==="home")
document.getElementById("content").innerHTML=home();

if(name==="buy")
document.getElementById("content").innerHTML=buy();

if(name==="send")
document.getElementById("content").innerHTML=send();

if(name==="orders")
document.getElementById("content").innerHTML=orders();

if(name==="history")
document.getElementById("content").innerHTML=history();

if(name==="profile")
document.getElementById("content").innerHTML=profile();


document.querySelectorAll(".bottom-nav button")
.forEach(button=>{
button.classList.remove("active");
});


let nav=document.getElementById("nav-"+name);

if(nav)
nav.classList.add("active");


window.scrollTo(0,0);

}


/* SIDE MENU */

function openMenu(){

document.getElementById("overlay")
.classList.add("show");

}


function closeMenu(){

document.getElementById("overlay")
.classList.remove("show");

}


function menuPage(name){

closeMenu();

page(name);

}


/* START */

page("home");

</script>

</body>
</html>
