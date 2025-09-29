# MY-Job-and-Services# <!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Job Consultancy & Service</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 20px;
      background-color: #e0f7fa; /* sky blue background */
      color: #000; /* black text */
    }
    header {
      background-color: white;
      border: 2px solid #29b6f6;
      padding: 15px;
      margin-bottom: 30px;
      text-align: center;
      font-weight: bold;
      font-size: 24px;
      color: #0277bd;
      border-radius: 8px;
      box-shadow: 0 2px 5px rgba(0,0,0,0.1);
    }
    .container {
      display: flex;
      justify-content: center;
      gap: 40px;
      margin-bottom: 50px;
    }
    .button {
      padding: 20px 50px;
      background-color: white;
      color: #0288d1;
      border: 3px solid #03a9f4;
      cursor: pointer;
      font-size: 20px;
      border-radius: 12px;
      font-weight: bold;
      transition: background-color 0.3s ease, color 0.3s ease;
      box-shadow: 2px 2px 8px rgba(3,169,244,0.3);
      width: 160px;
      text-align: center;
    }
    .button:hover {
      background-color: #03a9f4;
      color: white;
      box-shadow: 2px 2px 12px rgba(3,169,244,0.7);
    }
    .section {
      max-width: 600px;
      margin: 0 auto 40px auto;
      padding: 20px;
      background-color: white;
      border-radius: 8px;
      border: 2px solid #29b6f6;
      box-shadow: 1px 1px 5px rgba(2,119,189,0.3);
    }
    .section h2 {
      color: #01579b;
      margin-bottom: 15px;
      text-align: center;
    }
    .job-categories, .service-categories {
      display: flex;
      justify-content: center;
      gap: 20px;
      flex-wrap: wrap;
    }
    .job-categories .button, .service-categories .button {
      width: 120px;
      font-size: 16px;
      padding: 15px 10px;
    }
    label {
      font-weight: bold;
      display: block;
      margin-bottom: 8px;
      color: #01579b;
      text-align: center;
    }
    input[type="text"] {
      display: block;
      margin: 0 auto 20px auto;
      padding: 8px;
      font-size: 16px;
      border: 2px solid #03a9f4;
      border-radius: 6px;
      width: 250px;
      transition: border-color 0.3s ease;
    }
    input[type="text"]:focus {
      border-color: #0288d1;
      outline: none;
    }
    .display-section {
      margin-top: 20px;
      padding: 15px;
      background-color: #f1f8ff;
      border: 1px solid #03a9f4;
      border-radius: 6px;
      display: none;
      color: #01579b;
    }
    .back-button {
      display: block;
      margin: 0 auto;
      margin-top: 20px;
      background-color: white;
      color: #0288d1;
      border: 3px solid #03a9f4;
      cursor: pointer;
      font-size: 18px;
      border-radius: 12px;
      font-weight: bold;
      padding: 12px 50px;
      box-shadow: 2px 2px 8px rgba(3,169,244,0.3);
      transition: background-color 0.3s ease, color 0.3s ease;
      text-align: center;
      width: 200px;
      text-decoration: none;
    }
    .back-button:hover {
      background-color: #03a9f4;
      color: white;
      box-shadow: 2px 2px 12px rgba(3,169,244,0.7);
    }
  </style>
  <script>
    function showSection(sectionId) {
      document.getElementById('mainContainer').style.display = 'none';
      document.getElementById(sectionId).style.display = 'block';
    }
    function backToMain() {
      document.getElementById('mainContainer').style.display = 'flex';
      document.getElementById('jobSection').style.display = 'none';
      document.getElementById('serviceSection').style.display = 'none';
    }
    function toggleServiceDisplay(id){
      const el = document.getElementById(id);
      if(el.style.display === 'block'){
        el.style.display = 'none';
      } else {
        el.style.display = 'block';
      }
    }
  </script>
</head>
<body>

<header>Add Display</header>

<div class="container" id="mainContainer">
  <button class="button" onclick="showSection('jobSection')">Job</button>
  <button class="button" onclick="showSection('serviceSection')">Service</button>
</div>

<!-- Job Section -->
<div class="section" id="jobSection" style="display:none;">
  <h2>Job Categories</h2>
  <div class="job-categories">
    <button class="button">mt app Job</button>
    <button class="button">Local</button>
    <button class="button">non-Local</button>
    <button class="button">All</button>
  </div>
  <button class="back-button" onclick="backToMain()">Back</button>
</div>

<!-- Service Section -->
<div class="section" id="serviceSection" style="display:none;">
  <h2>Service Locations & Types</h2>
  <label for="locationInput">Enter Location:</label>
  <input type="text" id="locationInput" placeholder="Type location" />
  <div class="service-categories">
    <button class="button" onclick="toggleServiceDisplay('pgHostel')">PG / Hostel</button>
    <button class="button" onclick="toggleServiceDisplay('rentedRoom')">Rented Room</button>
    <button class="button" onclick="toggleServiceDisplay('teachingCenter')">Teaching Center</button>
  </div>
  <div class="display-section" id="pgHostel">
    <h3>PG / Hostel Display</h3>
    <p>Display listings for PG / Hostel in the selected location.</p>
  </div>
  <div class="display-section" id="rentedRoom">
    <h3>Rented Room Display</h3>
    <p>Display listings for Rented Rooms in the selected location.</p>
  </div>
  <div class="display-section" id="teachingCenter">
    <h3>Teaching Center Display</h3>
    <p>Display listings for Teaching Centers in the selected location.</p>
  </div>
  <button class="back-button" onclick="backToMain()">Back</button>
</div>

</body>
</html>
