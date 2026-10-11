# SEMI-AEMI-<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<meta name="theme-color" content="#FFF5F5">
<title>SEMI AEMI | Cute Things, Happy You</title>
<style>
:root{--cream:#FFF5F5;--pink:#F7D6D0;--rose:#E2B4BD;--dark:#4A4A4A}
*{box-sizing:border-box}
body{margin:0;background:var(--cream);color:var(--dark);font-family:Arial,sans-serif}
header{padding:20px 6%;display:flex;justify-content:space-between;align-items:center;gap:12px;flex-wrap:wrap;background:#fff8f8;border-bottom:1px solid var(--pink)}
.brand{font-size:25px;font-weight:bold;letter-spacing:2px}
.brand span{color:#C88798}
nav{display:flex;gap:16px;flex-wrap:wrap}
a{color:inherit;text-decoration:none}
.hero{text-align:center;padding:65px 6%;background:linear-gradient(135deg,#FFF5F5,#F7D6D0)}
.hero h1{font-size:clamp(38px,7vw,65px);margin:10px}
.hero h1 span{color:#C88798}
.hero p{line-height:1.8}
.btn{border:0;border-radius:25px;padding:13px 20px;background:var(--dark);color:white;cursor:pointer;display:inline-block;margin:6px}
.btn.pink{background:var(--rose);color:var(--dark)}
section{padding:45px 6%}
.heading{text-align:center;margin-bottom:28px}
.products{display:grid;grid-template-columns:repeat(3,minmax(0,1fr));gap:20px}
.card{background:white;border:1px solid #F0DCDC;border-radius:16px;overflow:hidden}
.card img{width:100%;aspect-ratio:1;object-fit:contain;background:#fff8f7;padding:10px}
.info{padding:15px}
.info h3{margin:5px 0}
.price{font-size:20px;font-weight:bold;margin:12px 0}
.order{width:100%;padding:12px;border:0;border-radius:22px;background:var(--pink);cursor:pointer}
.custom{background:var(--pink)}
form,.panel{max-width:650px;margin:20px auto;background:white;padding:22px;border-radius:16px}
label{display:block;font-size:14px;font-weight:bold;margin:13px 0 6px}
input,textarea,select{width:100%;padding:12px;border:1px solid #e5cece;border-radius:9px;background:#fffafa}
footer{text-align:center;padding:30px;background:var(--dark);color:white}
#admin-area{display:none;background:#f9e6e8;padding:30px 6%}
.admin-row{display:flex;gap:8px;align-items:center;flex-wrap:wrap;margin:10px 0;padding:12px;background:#fff;border-radius:10px}
.admin-row span{flex:1;min-width:130px}
.small{font-size:12px;line-height:1.6}
@media(max-width:700px){.products{grid-template-columns:repeat(2,minmax(0,1fr))}header{align-items:flex-start}nav{font-size:13px;gap:12px}}
@media(max-width:380px){.products{grid-template-columns:1fr}}
</style>
</head>
<body>

<header>
  <a class="brand" href="#home">SEMI <span>AEMI</span>
    <div style="font-size:10px;letter-spacing:2px">CUTE THINGS ♡ HAPPY YOU</div>
  </a>
  <nav>
    <a href="#home">Home</a>
    <a href="#shop">Shop</a>
    <a href="#custom">Custom Orders</a>
    <a href="#about">About</a>
  </nav>
</header>

<main>
<section class="hero" id="home">
  <div style="font-size:55px">🎀</div>
  <h1>Small Things.<br><span>Big Smiles.</span></h1>
  <p>Welcome to SEMI AEMI — your little world of cute crafts, stickers and handmade happiness!</p>
  <a class="btn" href="#shop">Explore Our Collection ♡</a>
</section>

<section id="shop">
  <div class="heading">
    <h2>Shop the Cuteness ♡</h2>
    <p>Find something special just for you.</p>
  </div>
  <div class="products" id="product-list"></div>
</section>

<section class="custom" id="custom">
  <div class="heading">
    <h2>Have a Custom Idea? 🎀</h2>
    <p>Tell us what you would like to create.</p>
  </div>
  <form id="custom-form">
    <label for="cname">Your Name</label>
    <input id="cname" required maxlength="80">
    <label for="ccontact">Your Contact Number</label>
    <input id="ccontact" required maxlength="30">
    <label for="ctype">Request Type</label>
    <select id="ctype" required>
      <option value="">Choose one</option>
      <option>Custom Stickers</option>
      <option>Handmade Craft</option>
      <option>Personalised Gift</option>
      <option>Other</option>
    </select>
    <label for="cdetails">Describe Your Idea</label>
    <textarea id="cdetails" rows="4" required maxlength="1500"></textarea>
    <button class="btn" type="submit">Send Request on WhatsApp</button>
    <p class="small">WhatsApp will open so you can review and send your request.</p>
  </form>
</section>

<section id="about" class="heading">
  <h2>A Little About Us ♡</h2>
  <p>Little things, made to bring big happiness.</p>
</section>
</main>

<footer>
  <h2>SEMI AEMI ♡</h2>
  <p>CUTE THINGS · HAPPY YOU</p>
  <p>© <span id="year"></span> SEMI AEMI</p>
</footer>

<a class="btn" style="position:fixed;right:12px;bottom:12px;background:#267B50"
   id="wa-float" target="_blank" rel="noopener">WhatsApp Us ♡</a>

<!-- ADMIN LOGIN -->
<section>
  <div class="heading">
    <h2>Owner Area</h2>
    <p>Shop owner ke liye.</p>
    <button class="btn pink" id="admin-login">Admin Login</button>
  </div>
</section>

<section id="admin-area">
  <div class="panel">
    <h2>🎀 SEMI AEMI Admin Panel</h2>
    <p class="small">Product details yahan manage karo. Image ke liye apni uploaded image ka public URL ya repository path use karo.</p>

    <form id="product-form">
      <input type="hidden" id="edit-id">
      <label for="pname">Product Name</label>
      <input id="pname" required maxlength="100">
      <label for="pprice">Price (Rs.)</label>
      <input id="pprice" type="number" min="0" step="1" required>
      <label for="pimage">Image Path or Public URL</label>
      <input id="pimage" placeholder="images/product-1.jpg" required>
      <label for="pdesc">Description</label>
      <textarea id="pdesc" rows="2" maxlength="300"></textarea>
      <button class="btn" type="submit">Save Product</button>
      <button class="btn pink" type="button" id="cancel-edit">Clear</button>
    </form>

    <h3>Manage Products</h3>
    <div id="admin-products"></div>
    <button class="btn pink" id="logout">Log Out</button>
  </div>
</section>

<script>
/*
 IMPORTANT:
 This is a basic demo admin panel, NOT secure authentication.
 Change the demo password before testing, but remember that a password
 written in public website code can be discovered by visitors.
 Do not use a real or reused personal password here.
*/
const ADMIN_PASSWORD = "ChangeThisDemoPassword";

const WHATSAPP_NUMBER = "923060412406";

const starterProducts = [
  {id:1,name:"Product Name 1",price:100,image:"images/product-1.jpg",description:"Add your product description."},
  {id:2,name:"Product Name 2",price:50,image:"images/product-2.jpg",description:"Add your product description."},
  {id:3,name:"Product Name 3",price:50,image:"images/product-3.jpg",description:"Add your product description."},
  {id:4,name:"Product Name 4",price:50,image:"images/product-4.jpg",description:"Add your product description."},
  {id:5,name:"Product Name 5",price:200,image:"images/product-5.jpg",description:"Add your product description."}
];

let products = loadProducts();
let loggedIn = false;

function loadProducts(){
  try {
    const saved = localStorage.getItem("semiAemiProducts");
    return saved ? JSON.parse(saved) : starterProducts.slice();
  } catch {
    return starterProducts.slice();
  }
}

function saveProducts(){
  localStorage.setItem("semiAemiProducts", JSON.stringify(products));
}

function safeText(value){
  const el = document.createElement("span");
  el.textContent = String(value ?? "");
  return el.innerHTML;
}

function waURL(message){
  return "https://wa.me/" + WHATSAPP_NUMBER +
    "?text=" + encodeURIComponent(message);
}

function renderProducts(){
  const list = document.getElementById("product-list");
  list.replaceChildren();

  products.forEach(p => {
    const card = document.createElement("article");
    card.className = "card";

    const img = document.createElement("img");
    img.src = p.image;
    img.alt = p.name;
    img.loading = "lazy";
    img.onerror = () => {
      img.alt = "Product image not available. Check the image path.";
    };

    const info = document.createElement("div");
    info.className = "info";
    info.innerHTML =
      "<h3>" + safeText(p.name) + "</h3>" +
      "<p>" + safeText(p.description) + "</p>" +
      '<div class="price">Rs. ' + Number(p.price) + "</div>";

    const order = document.createElement("button");
    order.className = "order";
    order.textContent = "Order on WhatsApp ♡";
    order.addEventListener("click", () => {
      window.open(waURL(
        "Hello SEMI AEMI! I want to order:\n" +
        "Product: " + p.name + "\n" +
        "Price: Rs. " + p.price + "\n" +
        "Please tell me how to proceed."
      ), "_blank", "noopener");
    });

    info.appendChild(order);
    card.append(img, info);
    list.appendChild(card);
  });

  renderAdminProducts();
}

function renderAdminProducts(){
  const list = document.getElementById("admin-products");
  list.replaceChildren();
  if(!loggedIn) return;

  products.forEach(p => {
    const row = document.createElement("div");
    row.className = "admin-row";

    const label = document.createElement("span");
    label.textContent = p.name + " — Rs. " + p.price;

    const edit = document.createElement("button");
    edit.className = "btn pink";
    edit.textContent = "Edit";
    edit.addEventListener("click", () => {
      document.getElementById("edit-id").value = p.id;
      document.getElementById("pname").value = p.name;
      document.getElementById("pprice").value = p.price;
      document.getElementById("pimage").value = p.image;
      document.getElementById("pdesc").value = p.description || "";
      document.getElementById("product-form").scrollIntoView({behavior:"smooth"});
    });

    const del = document.createElement("button");
    del.className = "btn";
    del.textContent = "Delete";
    del.addEventListener("click", () => {
      if(confirm("Delete this product?")){
        products = products.filter(item => item.id !== p.id);
        saveProducts();
        renderProducts();
      }
    });

    row.append(label, edit, del);
    list.appendChild(row);
  });
}

document.getElementById("admin-login").addEventListener("click", () => {
  const entered = prompt("Enter demo admin password:");
  if(entered === null) return;

  if(entered === ADMIN_PASSWORD){
    loggedIn = true;
    document.getElementById("admin-area").style.display = "block";
    document.getElementById("admin-area").scrollIntoView({behavior:"smooth"});
    renderAdminProducts();
  } else {
    alert("Incorrect password.");
  }
});

document.getElementById("logout").addEventListener("click", () => {
  loggedIn = false;
  document.getElementById("admin-area").style.display = "none";
});

document.getElementById("product-form").addEventListener("submit", event => {
  event.preventDefault();
  if(!loggedIn){
    alert("Please log in first.");
    return;
  }

  const idValue = document.getElementById("edit-id").value;
  const product = {
    id: idValue ? Number(idValue) : Date.now(),
    name: document.getElementById("pname").value.trim(),
    price: Number(document.getElementById("pprice").value),
    image: document.getElementById("pimage").value.trim(),
    description: document.getElementById("pdesc").value.trim()
  };

  if(!product.name || !product.image || !Number.isFinite(product.price) || product.price < 0){
    alert("Please check the product name, price and image path.");
    return;
  }

  if(idValue){
    products = products.map(p => p.id === product.id ? product : p);
  } else {
    products.push(product);
  }

  saveProducts();
  event.target.reset();
  document.getElementById("edit-id").value = "";
  renderProducts();
  alert("Product saved in this browser.");
});

document.getElementById("cancel-edit").addEventListener("click", () => {
  document.getElementById("product-form").reset();
  document.getElementById("edit-id").value = "";
});

document.getElementById("custom-form").addEventListener("submit", event => {
  event.preventDefault();

  const message =
    "Hello SEMI AEMI! Custom order request:\n" +
    "Name: " + document.getElementById("cname").value.trim() + "\n" +
    "Contact: " + document.getElementById("ccontact").value.trim() + "\n" +
    "Type: " + document.getElementById("ctype").value + "\n" +
    "Details: " + document.getElementById("cdetails").value.trim();

  window.open(waURL(message), "_blank", "noopener");
});

document.getElementById("wa-float").href =
  "https://wa.me/" + WHATSAPP_NUMBER;
document.getElementById("year").textContent = new Date().getFullYear();

renderProducts();
</script>
</body>
</html>
