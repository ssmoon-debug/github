<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Sanjina's Assignment Tracker</title>
  <style>
    body {
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background-color: #FAF3E0;
      color: #3B3B3B;
      margin: 0;
      padding: 0;
    }
    header {
      background-color: #B5D3C3;
      padding: 20px;
      text-align: center;
      font-size: 2em;
      font-weight: bold;
    }
    header img {
      max-height: 100px;
      margin-top: 10px;
    }
    #assignment-section {
      max-width: 600px;
      margin: 30px auto;
      padding: 20px;
      background-color: #ffffff;
      border-radius: 15px;
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.05);
      text-align: center;
    }
    .assignment-grid {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 15px;
      margin-top: 20px;
    }
    .assignment {
      background-color: #FAF3E0;
      padding: 15px;
      border-radius: 10px;
      text-align: center;
      box-shadow: 0 2px 6px rgba(0, 0, 0, 0.1);
      transition: transform 0.2s, box-shadow 0.2s;
      cursor: pointer;
    }
    .assignment:hover {
      transform: translateY(-3px);
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.15);
    }
    .assignment-title {
      font-weight: bold;
      font-size: 1.1em;
      color: #1E6F5C;
    }
    .admin-controls {
      margin-top: 8px;
      display: flex;
      justify-content: center;
      gap: 5px;
    }
    .admin-controls button {
      background-color: #B5D3C3;
      border: none;
      padding: 5px 10px;
      border-radius: 5px;
      cursor: pointer;
      font-size: 0.85em;
    }
    .admin-controls button:hover {
      background-color: #98C1AC;
    }
    footer {
      text-align: center;
      padding: 15px;
      background-color: #FAF3E0;
      font-size: 0.9em;
      color: #3B3B3B;
      margin-top: 30px;
    }
    input, button {
      padding: 8px;
      margin: 5px;
      border-radius: 5px;
      border: 1px solid #ccc;
    }
    #add-btn, #admin-btn, #exit-admin-btn {
      background-color: #B5D3C3;
      border: none;
      cursor: pointer;
      font-weight: bold;
      padding: 10px 15px;
    }
    #add-btn:hover, #admin-btn:hover, #exit-admin-btn:hover {
      background-color: #98C1AC;
    }
    #admin-form {
      background-color: #f9f9f9;
      padding: 15px;
      border-radius: 10px;
      margin: 15px 0;
    }
    h2 {
      color: #1E6F5C;
      margin-bottom: 20px;
    }
  </style>
</head>
<body>
  <header>
    Sanjina's Assignments 🐾<br>
    <img src="https://upload.wikimedia.org/wikipedia/en/5/53/Snoopy_Peanuts.png" alt="Snoopy" />
  </header>

  <div id="assignment-section">
    <h2>My Assignments</h2>
    
    <button id="admin-btn">Enter Admin Mode</button>
    <button id="exit-admin-btn" style="display: none;">Exit Admin Mode</button>
    
    <div id="admin-form" style="display: none;">
      <input type="text" id="assignment-input" placeholder="Assignment name" />
      <input type="url" id="link-input" placeholder="Assignment URL" />
      <button id="add-btn">Add Assignment</button>
    </div>

    <div id="assignments" class="assignment-grid"></div>
  </div>

  <footer>© 2025 Sanjina. All rights reserved. Life is good.</footer>

  <script>
    const password = "starsandsaturn";
    let isAdmin = false;

    const assignmentInput = document.getElementById("assignment-input");
    const linkInput = document.getElementById("link-input");
    const assignmentsDiv = document.getElementById("assignments");
    const adminBtn = document.getElementById("admin-btn");
    const exitAdminBtn = document.getElementById("exit-admin-btn");
    const adminForm = document.getElementById("admin-form");

    // Pre-defined assignments
    const initialAssignments = [
      { name: "Assignment 1", url: "https://ssmoon-debug.github.io/assignment-1/" },
      { name: "Assignment 2", url: "https://example.com/assignment2" },
      { name: "Assignment 3", url: "https://example.com/assignment3" },
      { name: "Assignment 4", url: "https://example.com/assignment4" },
      { name: "Assignment 5", url: "https://example.com/assignment5" },
      { name: "Assignment 6", url: "https://example.com/assignment6" },
      { name: "Assignment 7", url: "https://example.com/assignment7" },
      { name: "Assignment 8", url: "https://example.com/assignment8" },
      { name: "Assignment 9", url: "https://example.com/assignment9" },
      { name: "Assignment 10", url: "https://example.com/assignment10" }
    ];

    async function loadAssignments() {
      try {
        const response = await fetch('https://api.npoint.io/7c19cf4022061ea268b0');
        return await response.json();
      } catch (error) {
        console.error("Could not load assignments from API, using initial data:", error);
        return initialAssignments;
      }
    }

    async function saveAssignments(assignments) {
      try {
        await fetch('https://api.npoint.io/7c19cf4022061ea268b0', {
          method: 'POST',
          headers: { 'Content-Type': 'application/json' },
          body: JSON.stringify(assignments)
        });
      } catch (error) {
        console.error("Could not save assignments to API:", error);
        alert("Could not save changes. Please try again later.");
      }
    }

    let savedAssignments = [];

    async function initialize() {
      savedAssignments = await loadAssignments();
      if (savedAssignments.length === 0) {
        savedAssignments = initialAssignments;
        await saveAssignments(savedAssignments);
      }
      renderAssignments(savedAssignments);
    }

    document.getElementById("add-btn").onclick = async () => {
      const name = assignmentInput.value.trim();
      const url = linkInput.value.trim();
      if (!name || !url) {
        alert("Please enter both assignment name and URL");
        return;
      }
      const newAssignment = { name, url };
      savedAssignments.push(newAssignment);
      await saveAssignments(savedAssignments);
      renderAssignments(savedAssignments);
      assignmentInput.value = "";
      linkInput.value = "";
    };

    function renderAssignments(list) {
      assignmentsDiv.innerHTML = "";
      list.forEach((a, index) => {
        const div = document.createElement("div");
        div.className = "assignment";
        div.onclick = () => {
          if (!isAdmin) {
            window.open(a.url, '_blank');
          }
        };

        const title = document.createElement("div");
        title.className = "assignment-title";
        title.textContent = a.name;

        div.appendChild(title);

        if (isAdmin) {
          const adminDiv = document.createElement("div");
          adminDiv.className = "admin-controls";

          const editUrlBtn = document.createElement("button");
          editUrlBtn.textContent = "Edit URL";
          editUrlBtn.onclick = async (e) => {
            e.stopPropagation();
            const newUrl = prompt("Edit assignment URL:", a.url);
            if (newUrl) {
              a.url = newUrl;
              await saveAssignments(savedAssignments);
              renderAssignments(savedAssignments);
            }
          };

          const renameBtn = document.createElement("button");
          renameBtn.textContent = "Rename";
          renameBtn.onclick = async (e) => {
            e.stopPropagation();
            const newName = prompt("Rename assignment:", a.name);
            if (newName) {
              a.name = newName;
              await saveAssignments(savedAssignments);
              renderAssignments(savedAssignments);
            }
          };

          const deleteBtn = document.createElement("button");
          deleteBtn.textContent = "Delete";
          deleteBtn.onclick = async (e) => {
            e.stopPropagation();
            if (confirm("Delete this assignment?")) {
              savedAssignments.splice(index, 1);
              await saveAssignments(savedAssignments);
              renderAssignments(savedAssignments);
            }
          };

          adminDiv.appendChild(renameBtn);
          adminDiv.appendChild(editUrlBtn);
          adminDiv.appendChild(deleteBtn);
          div.appendChild(adminDiv);
        }

        assignmentsDiv.appendChild(div);
      });
    }

    adminBtn.onclick = () => {
      const input = prompt("Enter admin password:");
      if (input === password) {
        isAdmin = true;
        adminForm.style.display = "block";
        adminBtn.style.display = "none";
        exitAdminBtn.style.display = "inline-block";
        renderAssignments(savedAssignments);
      }
    };

    exitAdminBtn.onclick = () => {
      isAdmin = false;
      adminForm.style.display = "none";
      adminBtn.style.display = "inline-block";
      exitAdminBtn.style.display = "none";
      renderAssignments(savedAssignments);
    };

    initialize();
  </script>
</body>
</html>
