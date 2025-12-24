<!DOCTYPE html>
<html lang="th">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>EMS Inventory</title>
    <script src="https://unpkg.com/html5-qrcode"></script>
    <style>
        body { font-family: 'Kanit', sans-serif; background: #f0f2f5; margin: 0; padding: 15px; }
        .card { background: white; padding: 20px; border-radius: 15px; box-shadow: 0 4px 6px rgba(0,0,0,0.1); margin-bottom: 20px; }
        h2 { color: #d32f2f; margin-top: 0; }
        input { width: 100%; padding: 12px; margin: 8px 0; border: 1px solid #ddd; border-radius: 8px; box-sizing: border-box; }
        .btn { width: 100%; padding: 15px; border: none; border-radius: 8px; font-weight: bold; cursor: pointer; margin-top: 10px; font-size: 16px; }
        .btn-update { background: #007bff; color: white; }
        .btn-add { background: #28a745; color: white; }
        .btn-delete { background: #dc3545; color: white; }
        #reader { border-radius: 10px; overflow: hidden; }
    </style>
</head>
<body>

<div class="card">
    <h2>🚑 สแกนอุปกรณ์</h2>
    <div id="reader"></div>
</div>

<div class="card">
    <h3>จัดการข้อมูล</h3>
    <input type="text" id="qrId" placeholder="รหัส QR Code (จากการสแกน)">
    <input type="text" id="itemName" placeholder="ชื่ออุปกรณ์ (เฉพาะกรณีเพิ่มของใหม่)">
    <input type="number" id="qty" placeholder="จำนวนปัจจุบัน">
    <input type="number" id="minQty" placeholder="จำนวนที่ต้องมีขั้นต่ำ">
    
    <button class="btn btn-update" onclick="submitData('update')">🔄 อัปเดตจำนวน</button>
    <button class="btn btn-add" onclick="submitData('add')">➕ เพิ่มของเข้าเครื่อง</button>
    <button class="btn btn-delete" onclick="submitData('delete')">🗑️ ลบออกจากระบบ</button>
</div>

<script>
    const APP_URL = "วางURL_ที่ได้จากขั้นตอนที่2_ที่นี่";

    // ระบบสแกน
    function onScanSuccess(decodedText) {
        document.getElementById('qrId').value = decodedText;
        vibratePhone(); // สั่นเตือนเบาๆ ว่าสแกนติดแล้ว
    }
    let scanner = new Html5QrcodeScanner("reader", { fps: 10, qrbox: 250 });
    scanner.render(onScanSuccess);

    async function submitData(action) {
        const data = {
            action: action,
            qrCode: document.getElementById('qrId').value,
            itemName: document.getElementById('itemName').value,
            newQty: document.getElementById('qty').value,
            minQty: document.getElementById('minQty').value
        };

        if(!data.qrCode) return alert("กรุณาสแกนหรือใส่รหัสก่อน!");

        try {
            const res = await fetch(APP_URL, { method: 'POST', body: JSON.stringify(data) });
            const msg = await res.text();
            alert(msg);
            location.reload(); // รีเฟรชหน้าจอเพื่อเริ่มใหม่
        } catch (e) {
            alert("ผิดพลาด: " + e);
        }
    }

    function vibratePhone() { if(navigator.vibrate) navigator.vibrate(100); }
</script>
</body>
</html>
