# Group-6-project-
Nepal external sector 
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Nepal External Sector 2026</title>

<script src="https://cdn.tailwindcss.com"></script>
<script src="https://cdn.jsdelivr.net/npm/chart.js"></script>

</head>

<body class="bg-gray-100">

<!-- TITLE -->
<div class="text-center p-6 bg-blue-900 text-white">
  <h1 class="text-3xl font-bold">NEPAL EXTERNAL SECTOR (2026)</h1>
  <p class="text-lg mt-2">Balance of Trade & Balance of Payments</p>
</div>

<!-- GRID -->
<div class="grid md:grid-cols-2 gap-6 p-6">

  <!-- BALANCE OF TRADE -->
  <div class="bg-white p-4 rounded shadow">
    <h2 class="text-xl font-bold text-blue-800 mb-2">1. Balance of Trade (BoT)</h2>
    <p class="mb-2">BoT = Exports − Imports</p>
    <p class="mb-4 text-gray-600">Nepal imports much more than it exports</p>

    <canvas id="botChart"></canvas>

    <p class="mt-4 text-red-600 font-bold">Trade Deficit = Rs. 85 Billion</p>
  </div>

  <!-- BALANCE OF PAYMENTS -->
  <div class="bg-white p-4 rounded shadow">
    <h2 class="text-xl font-bold text-blue-800 mb-2">2. Balance of Payments (BoP)</h2>
    <p class="mb-2">BoP = Total Inflows − Total Outflows</p>

    <ul class="list-disc ml-6 text-gray-700">
      <li>Trade</li>
      <li>Services & Tourism</li>
      <li>Remittance</li>
      <li>FDI & Loans</li>
      <li>Others</li>
    </ul>
  </div>

  <!-- SURPLUS VS DEFICIT -->
  <div class="bg-white p-4 rounded shadow">
    <h2 class="text-xl font-bold text-blue-800 mb-2">3. Surplus vs Deficit</h2>

    <canvas id="sdChart"></canvas>

    <div class="mt-4 text-sm">
      <p class="text-green-600 font-bold">Surplus: Inflow > Outflow</p>
      <p class="text-red-600 font-bold">Deficit: Outflow > Inflow</p>
    </div>
  </div>

  <!-- FLOW -->
  <div class="bg-white p-4 rounded shadow">
    <h2 class="text-xl font-bold text-blue-800 mb-2">4. Flow of BoP</h2>

    <div class="grid grid-cols-2 gap-2 text-center">

      <div class="bg-blue-200 p-3 rounded">Exports</div>
      <div class="bg-red-200 p-3 rounded">Imports</div>

      <div class="bg-blue-100 p-3 rounded">Remittance</div>
      <div class="bg-green-100 p-3 rounded">FDI & Loans</div>

    </div>

    <div class="text-center mt-4 bg-yellow-200 p-3 rounded font-bold">
      Balance of Payments Result
    </div>
  </div>

</div>

<!-- CHART SCRIPT -->
<script>
  // Balance of Trade Chart
  new Chart(document.getElementById("botChart"), {
    type: "bar",
    data: {
      labels: ["Imports", "Exports"],
      datasets: [{
        label: "Value (Rs. Billion)",
        data: [100, 15],
        backgroundColor: ["red", "green"]
      }]
    }
  });

  // Surplus vs Deficit
  new Chart(document.getElementById("sdChart"), {
    type: "bar",
    data: {
      labels: ["Surplus", "Deficit"],
      datasets: [{
        label: "Example Values",
        data: [120, 110],
        backgroundColor: ["green", "red"]
      }]
    }
  });
</script>

</body>
</html>
