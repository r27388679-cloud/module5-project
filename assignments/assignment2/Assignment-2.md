
module2-solution/
├── index.html
└── css/
    └── styles.css

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Responsive Layout Assignment</title>
  <link rel="stylesheet" href="css/styles.css" />
</head>
<body>
  <h1>My Responsive Page</h1>
  
  <div class="container">
    <section class="section chicken">
      <div class="section-title">Chicken</div>
      <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla vitae.</p>
    </section>

    <section class="section beef">
      <div class="section-title">Beef</div>
      <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla vitae.</p>
    </section>

    <section class="section sushi">
      <div class="section-title">Sushi</div>
      <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla vitae.</p>
    </section>
  </div>
</body>
</html>

/* Box sizing */
*,
*::before,
*::after {
  box-sizing: border-box;
}

/* Base styles */
body {
  font-family: Arial, sans-serif;
  margin: 20px;
}

h1 {
  font-size: 1.75em; /* 75% larger than normal */
  margin-bottom: 20px;
}

.container {
  overflow: hidden; /* clear floats */
}

/* Section base */
.section {
  position: relative;
  border: 1px solid black;
  padding: 40px 20px 20px 20px; /* padding top leaves space for title */
  margin-bottom: 20px;
  color: white;
}

/* Section titles */
.section-title {
  position: absolute;
  top: 5px;
  right: 5px;
  background-color: black;
  border: 1px solid black;
  padding: 5px 10px;
  font-size: 1.25em; /* 25% larger than paragraph text */
  color: white;
}

/* Colors for sections */
.chicken {
  background-color: #e67e22; /* orange */
}

.beef {
  background-color: #c0392b; /* red */
}

.sushi {
  background-color: #2980b9; /* blue */
}

/* Paragraph text */
.section p {
  font-size: 1em;
  margin: 0;
}

/* --- DESKTOP (≥992px) --- */
/* Three equal sections in one row */
@media (min-width: 992px) {
  .section {
    width: 32%; /* ~100% / 3 minus margins */
    float: left;
    margin-right: 2%;
  }
  .section:last-child {
    margin-right: 0;
  }
}

/* --- TABLET (768px to 991px) --- */
/* First two sections in one row, third full row */
@media (min-width: 768px) and (max-width: 991px) {
  .section {
    margin-right: 2%;
  }
  .section:nth-child(1),
  .section:nth-child(2) {
    float: left;
    width: 49%;
  }
  .section:nth-child(3) {
    float: none;
    width: 100%;
    margin-right: 0;
  }
}

/* --- MOBILE (≤767px) --- */
/* All sections stacked full width */
@media (max-width: 767px) {
  .section {
    float: none;
    width: 100%;
    margin-right: 0;
  }
}

