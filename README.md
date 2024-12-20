<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>PCS INFRAGOLD Locator</title>
    <style>
        body {
            margin: 0;
            font-family: Arial, sans-serif;
            background: linear-gradient(135deg, #6a11cb, #2575fc);
            color: white;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: flex-start;
            height: 100vh;
            padding-top: 20px;
        }

        h1 {
            font-size: 2em;
            font-weight: bold;
            text-transform: uppercase;
            color: #ffeb3b;
            margin-bottom: 10px;
        }

        .search-bar {
            margin-bottom: 20px;
            text-align: center;
        }

        input[type="text"] {
            width: 300px;
            padding: 10px;
            border: none;
            border-radius: 5px 0 0 5px;
            outline: none;
            font-size: 1em;
        }

        button {
            padding: 10px 20px;
            background-color: #ffeb3b;
            color: black;
            border: none;
            border-radius: 0 5px 5px 0;
            cursor: pointer;
            font-size: 1em;
            font-weight: bold;
            transition: background-color 0.3s;
        }

        button:hover {
            background-color: #ffc107;
        }

        .image-container {
            position: relative;
            width: 80%;
            max-width: 800px;
        }

        .image-container img {
            width: 100%;
            height: auto;
            border-radius: 10px;
        }

        .dot {
            position: absolute;
            width: 20px;
            height: 20px;
            border-radius: 50%;
            background: transparent;
            border: 3px solid red;
            display: none; /* Initially hidden */
            pointer-events: none;
        }
    </style>
</head>
<body>
    <h1>PCS INFRAGOLD Locator</h1>
    <div class="search-bar">
        <input type="text" id="categoryCode" placeholder="Enter Category Code">
        <button onclick="searchCategory()">Search</button>
    </div>

    <div class="image-container">
        <!-- Insert the inventory map -->
       <!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Test Image</title>
</head>
<body>
    <h1>Image Test</h1>
    <img src="![Screenshot 2024-12-19 214813](https://github.com/user-attachments/assets/865c45b6-8c2d-4dd9-b1cb-1cdd3e69714d)" alt="Test Image">
</body>
</html>

        
        <!-- Dots (placeholders for red circles) -->
        <div id="dot-D" class="dot" style="top: 10%; left: 20%;"></div>
        <div id="dot-E" class="dot" style="top: 10%; left: 30%;"></div>
        <div id="dot-H" class="dot" style="top: 10%; left: 40%;"></div>
        <div id="dot-N" class="dot" style="top: 10%; left: 50%;"></div>
        <div id="dot-A" class="dot" style="top: 70%; left: 10%;"></div>
        <!-- Add similar <div> elements for all other points -->
    </div>

    <script>
        // Inventory data with category codes and area mappings
        const inventory = [
            { categoryCode: 'A123', area: 'D' },
            { categoryCode: 'B456', area: 'E' },
            { categoryCode: 'C789', area: 'H' }
            // Add more category codes and areas as needed
        ];

        // Function to reset highlights
        function resetHighlights() {
            // Hide all red circles (dots)
            document.querySelectorAll('.dot').forEach(dot => {
                dot.style.display = 'none';
            });
        }

        // Search function
        function searchCategory() {
            const categoryCode = document.getElementById('categoryCode').value.trim();
            resetHighlights(); // Reset any previous highlights

            if (categoryCode) {
                const item = inventory.find(i => i.categoryCode.toLowerCase() === categoryCode.toLowerCase());
                if (item) {
                    // Highlight the corresponding dot
                    const dotId = `dot-${item.area}`;
                    const dot = document.getElementById(dotId);
                    if (dot) {
                        dot.style.display = 'block'; // Show the red circle
                    }
                    alert(`Item found in area ${item.area}`);
                } else {
                    alert('Item not found!');
                }
            } else {
                alert('Please enter a category code!');
            }
        }
    </script>
</body>
</html>
# Output

![Screenshot 2024-12-19 214813](https://github.com/user-attachments/assets/76162770-c45d-4cab-8e12-ba0ccb5e1e04)
