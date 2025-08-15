<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="description" content="Try our simple Free Fire account tracker! Enter a name and ID, see it in the list, and remove it with a click. Fast, easy, and safe way to manage your accounts online. Lightweight web app for quick tracking.">
<title>Free Fire Accounts</title>
<style>
body { font-family: Arial; direction: rtl; padding: 20px; }
input, button { padding: 8px; margin: 5px 0; width: 100%; }
ul { list-style: none; padding: 0; }
li { padding: 8px; background: #f0f0f0; margin: 5px 0; cursor: pointer; }
</style>
</head>
<body>

<h2>تسجيل حسابات فري فاير</h2>

<input type="text" id="nameInput" placeholder="اسم الحساب">
<input type="text" id="idInput" placeholder="ID الحساب">
<button onclick="addAccount()">إضافة الحساب</button>

<ul id="accountsList"></ul>

<script>
let accounts = [];
function addAccount() {
    const name = document.getElementById("nameInput").value;
    const id = document.getElementById("idInput").value;
    if(name && id) {
        accounts.push(name + " - " + id);
        updateList();
        document.getElementById("nameInput").value = "";
        document.getElementById("idInput").value = "";
    } else { alert("أدخل الاسم وID"); }
}
function updateList() {
    const list = document.getElementById("accountsList");
    list.innerHTML = "";
    accounts.forEach((acc, i) => {
        const li = document.createElement("li");
        li.text
