
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Semester 4 Marksheet</title>
  <style>
    body {
      /* font-family: Arial, sans-serif; */
      margin: 0;
      background-color: #fff;
      position: relative;
    }

    .container {
      max-width: 1000px;
      margin: auto;
      padding: 20px;
      position: relative;
    }

    .top-bar {
      text-align: center;
      font-size: 14px;
      margin-bottom: 20px;
      font-weight: bold;
    }

    .student-section {
      display: flex;
      justify-content: flex-end;
      gap: 40px;
      padding: 0 10px;
      margin-bottom: 10px;
    }

    .student-info, .program-info {
      text-align: left;
    }

    .student-info p, .program-info p {
      margin: 0;
      font-weight: bold;
    }

    .student-info h2, .program-info h2 {
      margin: 5px 0 10px 0;
      font-size: 20px;
    }

    .semester-title {
      text-align: center;
      font-size: 18px;
      margin: 20px 0;
    }

    table {
      width: 100%;
      border-collapse: collapse;
      margin-bottom: 20px;
      font-size: 15px;
    }

    th, td {
      border: 1px solid #999;
      padding: 8px 10px;
      text-align: center;
    }

    .footer {
      display: flex;
      justify-content: space-between;
      font-size: 16px;
      margin-bottom: 20px;
      padding: 0 10px;
    }

    .footer p {
      margin: 5px 0;
    }

    .side-text {
      writing-mode: vertical-rl;
      transform: rotate(180deg);
      position: fixed;
      top: 40%;
      right: 10px;
      font-size: 14px;
      color: black;
      font-weight: bold;
    }
  </style>
</head>
<body>
  <div class="container">
    <div class="top-bar">
      CampX | Digital Campus Ecosystem
    </div>

    <div class="student-section">
      <div class="student-info">
        <p>Student Name</p>
        <h2>CHINTHALA JISHNU SAYEE</h2>
      </div>
      <div class="program-info">
        <p>Program</p>
        <h2>B TECH in Artificial Intelligence</h2>
      </div>
    </div>

    <div class="semester-title">
      <h3>Semester – 4</h3>
    </div>

    <table>
      <thead>
        <tr>
          <th>S.No.</th>
          <th>Course Code</th>
          <th>Course Name</th>
          <th>Credits</th>
          <th>Grade</th>
          <th>Status</th>
        </tr>
      </thead>
      <tbody id="marksTableBody">
        <!-- JS inserts rows here -->
      </tbody>
    </table>

    <div class="footer">
      <p><strong>SGPA :</strong> 8.26</p>
      <p><strong>Total secured credits:</strong> 20 / 20</p>
    </div>
  </div>

  <div class="side-text">Need Help?</div>

  <script>
    const courses = [
      { sno: 1, code: "A54028", name: "Data Wrangling and Visualization", credits: 3.00, grade: "A+", status: "P" },
      { sno: 2, code: "A54026", name: "Design and Analysis of Algorithms", credits: 4.00, grade: "A", status: "P" },
      { sno: 3, code: "A54029", name: "Fundamentals of Artificial Intelligence", credits: 3.00, grade: "B+", status: "P" },
      { sno: 4, code: "A54027", name: "Data Base Management Systems", credits: 3.00, grade: "B+", status: "P" },
      { sno: 5, code: "A54220", name: "Soft Skills for Success Lab", credits: 1.00, grade: "A", status: "P" },
      { sno: 6, code: "A54221", name: "Data Wrangling and Visualization Lab", credits: 1.50, grade: "O", status: "P" },
      { sno: 7, code: "A54222", name: "Data Base Management Systems Lab", credits: 1.50, grade: "A+", status: "P" },
      { sno: 8, code: "A54022", name: "Gender Sensitization", credits: 0.00, grade: "-", status: "P" },
      { sno: 9, code: "A53027", name: "Discrete Mathematics", credits: 3.00, grade: "A", status: "P" }
    ];

    const tbody = document.getElementById("marksTableBody");

    courses.forEach(course => {
      const row = document.createElement("tr");
      row.innerHTML = `
        <td>${course.sno}</td>
        <td>${course.code}</td>
        <td>${course.name}</td>
        <td>${course.credits.toFixed(2)}</td>
        <td>${course.grade}</td>
        <td>${course.status}</td>
      `;
      tbody.appendChild(row);
    });
  </script>
</body>
</html>
