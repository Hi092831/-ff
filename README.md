# -ff<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Test Money System</title>
</head>
<body>
    <h1>เงินปลอม: <span id="balance">1000</span> บาท</h1>
    <button onclick="addMoney(500)">เพิ่มเงิน 500 บาท</button>
    <button onclick="subtractMoney(200)">ลดเงิน 200 บาท</button>

    <script>
        let balance = 1000; // เงินเริ่มต้น

        function updateBalance() {
            document.getElementById('balance').innerText = balance;
        }

        function addMoney(amount) {
            balance += amount;
            updateBalance();
        }

        function subtractMoney(amount) {
            if (balance >= amount) {
                balance -= amount;
                updateBalance();
            } else {
                alert('เงินไม่พอ');
            }
        }
    </script>
</body>
</html>
