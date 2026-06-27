<!DOCTYPE html>

<html lang="vi">
<head>
<meta charset="UTF-8">
<title>Tra cứu điểm ĐGNL BCA</title>

<style>
body {
    margin: 0;
    font-family: Arial;
    background: #8B0000;
    color: white;
    text-align: center;
}

/* HEADER */
.header {
    background: #a40000;
    padding: 20px;
}

.logo {
    width: 90px;
}

/* BOX */
.container {
    margin-top: 50px;
}

.box {
    background: #b30000;
    padding: 30px;
    width: 350px;
    margin: auto;
    border-radius: 12px;
    box-shadow: 0 0 15px rgba(0,0,0,0.4);
}

input {
    padding: 12px;
    width: 85%;
    border-radius: 6px;
    border: none;
    margin-bottom: 15px;
    font-size: 16px;
}

button {
    padding: 10px 25px;
    background: gold;
    border: none;
    border-radius: 6px;
    cursor: pointer;
    font-weight: bold;
    font-size: 15px;
}

button:hover {
    background: orange;
}

.result {
    margin-top: 20px;
    text-align: left;
    background: #7a0000;
    padding: 15px;
    border-radius: 8px;
}
</style>

</head>

<body>

<div class="header">
    <img class="logo" src="https://upload.wikimedia.org/wikipedia/commons/3/3a/Emblem_of_the_Vietnam_People%27s_Public_Security.svg">
    <h2>TRA CỨU ĐIỂM THI ĐÁNH GIÁ NĂNG LỰC<br>BỘ CÔNG AN</h2>
</div>

<div class="container">
    <div class="box">
        <input type="text" id="sbd" placeholder="Nhập số báo danh">
        <br>
        <button onclick="traCuu()">TRA CỨU</button>

```
    <div class="result" id="kq"></div>
</div>
```

</div>

<script>
// DỮ LIỆU GỘP TRONG FILE
const data = {
    "CA001": {
        ten: "Trần Đức Quý",
        phong: "P.101",
        diem: 24.5
    },
    "CA002": {
        ten: "Nguyễn Văn A",
        phong: "P.203",
        diem: 21.0
    },
    "CA003": {
        ten: "Lê Văn B",
        phong: "P.305",
        diem: 26.0
    }
};

function traCuu() {
    let sbd = document.getElementById("sbd").value.trim();
    let kq = document.getElementById("kq");

    if(data[sbd]) {
        let hs = data[sbd];

        kq.innerHTML = `
            <p><b>Họ và tên:</b> ${hs.ten}</p>
            <p><b>Số báo danh:</b> ${sbd}</p>
            <p><b>Phòng thi:</b> ${hs.phong}</p>
            <p><b>Điểm thi:</b> ${hs.diem}</p>
        `;
    } else {
        kq.innerHTML = "<p>Không tìm thấy số báo danh!</p>";
    }
}
</script>

</body>
</html>
