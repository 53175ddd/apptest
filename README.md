# apptest

Web アプリ作成用事前テスト

<!DOCTYPE html>
<html lang="ja">
<head>
  <meta charset="UTF-8">
  <title>公式計算シート</title>
  <style>
    body { font-family: sans-serif; padding: 20px; line-height: 1.8; }
    input { width: 80px; margin: 5px; }
    .result { font-weight: bold; }
  </style>
</head>
<body>
  <h1>計算シート</h1>
  <p>公式: <code>y = a × b + c</code></p>
  
  <p>
    a: <input type="number" id="a" value="1"><br>
    b: <input type="number" id="b" value="2"><br>
    c: <input type="number" id="c" value="3"><br>
  </p>
  
  <button onclick="calc()">計算する</button>
  <p>結果: <span id="result" class="result">0</span></p>

  <script>
    function calc() {
      const a = parseFloat(document.getElementById("a").value) || 0;
      const b = parseFloat(document.getElementById("b").value) || 0;
      const c = parseFloat(document.getElementById("c").value) || 0;

      const y = a * b + c;
      document.getElementById("result").textContent = y;
    }
  </script>
</body>
</html>

