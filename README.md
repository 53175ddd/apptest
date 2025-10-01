# apptest

Web アプリ作成用事前テスト

  <h1>LED の保護抵抗の最低値</h1>
  <p>公式: <code>R = (Vcc - Vf) / If</code></p>
  
  <p>
    Vcc: <input type="number" id="Vcc" value="5"><br>
    Vf: <input type="number" id="Vf" value="1.4"><br>
    If: <input type="number" id="If" value="10"><br>
  </p>
  
  <button onclick="calc()">計算する</button>
  <p>結果: <span id="result" class="result">0</span></p>

  <script>
    function calc() {
      const Vcc = parseFloat(document.getElementById("Vcc").value) || 0;
      const Vf = parseFloat(document.getElementById("Vf").value) || 0;
      const If = parseFloat(document.getElementById("If").value) || 0;

      const R = (Vcc - Vf) / If;
      document.getElementById("result").textContent = R;
    }
  </script>
</body>
</html>

