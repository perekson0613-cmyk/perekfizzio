<!DOCTYPE html>
<html lang="pl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Gabinet Fizjoterapii i Masażu</title>
<style>
body {
  margin: 0;
  font-family: Arial, sans-serif;
  background: #f4f7f6;
  color: #24332f;
}
header {
  background: #315c50;
  color: white;
  text-align: center;
  padding: 60px 20px;
}
header h1 { font-size: 42px; margin: 0 0 15px; }
header p { font-size: 20px; }
section {
  max-width: 900px;
  margin: 30px auto;
  padding: 30px;
  background: white;
  border-radius: 18px;
}
h2 { color: #315c50; }
.services {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
  gap: 20px;
}
.card {
  padding: 25px;
  background: #eef4f1;
  border-radius: 15px;
}
form {
  display: grid;
  gap: 15px;
}
input, select, button {
  padding: 14px;
  font-size: 16px;
  border-radius: 10px;
  border: 1px solid #ccc;
}
button {
  background: #315c50;
  color: white;
  border: none;
  cursor: pointer;
}
button:hover { background: #24473e; }
footer {
  text-align: center;
  padding: 30px;
  color: #666;
}
</style>
</head>

<body>

<header>
  <h1>Gabinet Fizjoterapii i Masażu</h1>
  <p>Zadbaj o swoje ciało i dobre samopoczucie</p>
</header>

<section>
  <h2>Nasze usługi</h2>

  <div class="services">
    <div class="card">
      <h3>💆 Masaż klasyczny</h3>
      <p>60 minut</p>
      <strong>150 zł</strong>
    </div>

    <div class="card">
      <h3>🌿 Masaż relaksacyjny</h3>
      <p>60 minut</p>
      <strong>160 zł</strong>
    </div>

    <div class="card">
      <h3>🧑‍⚕️ Fizjoterapia</h3>
      <p>60 minut</p>
      <strong>180 zł</strong>
    </div>
  </div>
</section>

<section>
  <h2>Umów wizytę</h2>

  <form onsubmit="rezerwacja(event)">
    <select id="usluga" required>
      <option value="">Wybierz usługę</option>
      <option>Masaż klasyczny</option>
      <option>Masaż relaksacyjny</option>
      <option>Fizjoterapia</option>
    </select>

    <input type="date" id="data" required>

    <select id="godzina" required>
      <option value="">Wybierz godzinę</option>
      <option>09:00</option>
      <option>10:00</option>
      <option>11:00</option>
      <option>12:00</option>
      <option>13:00</option>
      <option>14:00</option>
      <option>15:00</option>
      <option>16:00</option>
      <option>17:00</option>
    </select>

    <input type="text" id="imie" placeholder="Imię i nazwisko" required>

    <input type="tel" id="telefon" placeholder="Numer telefonu" required>

    <button type="submit">Zarezerwuj wizytę</button>
  </form>

  <p id="wynik"></p>
</section>

<section>
  <h2>Kontakt</h2>
  <p>📍 Twój adres</p>
  <p>📞 Twój numer telefonu</p>
  <p>✉️ Twój adres e-mail</p>
</section>

<footer>
  © 2026 Gabinet Fizjoterapii i Masażu
</footer>

<script>
function rezerwacja(event) {
  event.preventDefault();

  const usluga = document.getElementById("usluga").value;
  const data = document.getElementById("data").value;
  const godzina = document.getElementById("godzina").value;
  const imie = document.getElementById("imie").value;

  document.getElementById("wynik").innerHTML =
    "Dziękujemy, " + imie +
    "! Wybrano: " + usluga +
    ", " + data +
    " o " + godzina + ".";
}
</script>

</body>
</html>
