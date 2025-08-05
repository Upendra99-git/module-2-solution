# module-2-solution
coding assignment for moduel 2 
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Responsive Layout Module 2</title>
  <link rel="stylesheet" href="css/styles.css" />
</head>
<body>
  <h1>Delicious Meats</h1>

  <div class="container">
    <section class="section chicken">
      <div class="section-title">Chicken</div>
      <p>
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Quisque
        dignissim lacus nec diam pulvinar, ac dignissim purus malesuada.
      </p>
    </section>

    <section class="section beef">
      <div class="section-title">Beef</div>
      <p>
        Sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut
        enim ad minim veniam, quis nostrud exercitation ullamco laboris.
      </p>
    </section>

    <section class="section sushi">
      <div class="section-title">Sushi</div>
      <p>
        Duis aute irure dolor in reprehenderit in voluptate velit esse cillum
        dolore eu fugiat nulla pariatur.
      </p>
    </section>
  </div>
</body>
</html>
/* General Reset and box-sizing */
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

/* Body styling */
body {
  font-family: Arial, sans-serif;
  padding: 20px;
  background-color: #f5f5f5;
}

/* Page Heading */
h1 {
  font-size: 1.75em; /* 75% larger than paragraph */
  margin-bottom: 20px;
  text-align: center;
}

/* Container to hold the sections */
.container {
  width: 100%;
  overflow: hidden; /* clear floats */
}

/* Sections */
.section {
  position: relative; /* for absolutely positioned titles */
  border: 1px solid black;
  padding: 40px 20px 20px 20px; /* top padding to avoid overlap with title */
  color: #333;
  margin-bottom: 20px; /* vertical spacing for mobile/tablet */
}

/* Section Titles */
.section-title {
  position: absolute;
  top: 5px;
  right: 5px;
  border: 1px solid black;
  padding: 5px 10px;
  font-size: 1.25em; /* 25% larger than paragraph */
  font-weight: bold;
  color: white;
}

/* Individual section background colors and title background colors */
.chicken {
  background-color: #ffecb3; /* light yellow */
}
.chicken .section-title {
  background-color: #f57c00; /* orange */
}

.beef {
  background-color: #ffcdd2; /* light red */
}
.beef .section-title {
  background-color: #c62828; /* dark red */
}

.sushi {
  background-color: #c8e6c9; /* light green */
}
.sushi .section-title {
  background-color: #2e7d32; /* dark green */
}

/* Paragraph text size */
.section p {
  font-size: 1em;
  line-height: 1.5;
}

/* -------- MOBILE -------- */
/* ≤ 767px - each section full width stacked vertically */
@media (max-width: 767px) {
  .section {
    width: 100%;
  }
}

/* -------- TABLET -------- */
/* 768px to 991px */
/* first two sections side-by-side, equal width; third full width below */
@media (min-width: 768px) and (max-width: 991px) {
  .container {
    overflow: hidden;
  }
  .section {
    float: left;
    margin-right: 20px;
    width: 48%;
    margin-bottom: 20px;
  }
  /* Remove right margin on the 2nd section */
  .section:nth-child(2) {
    margin-right: 0;
  }
  /* 3rd section full width */
  .section:nth-child(3) {
    float: none;
    width: 100%;
    margin-right: 0;
  }
}

/* -------- DESKTOP -------- */
/* 992px and above */
/* all three sections in one row, equal width */
@media (min-width: 992px) {
  .container {
    overflow: hidden;
  }
  .section {
    float: left;
    width: 32%;
    margin-right: 2%;
    margin-bottom: 0;
  }
  /* Remove right margin on last section */
  .section:last-child {
    margin-right: 0;
  }
}

