<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Bible Study Website</title>
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;700&family=Poppins:wght@300;400&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Poppins', sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f8f9fa;
            color: #333;
        }

        h1, h2 {
            font-family: 'Playfair Display', serif;
            color: #343a40;
            text-align: center;
            margin-bottom: 20px;
        }

        .container {
            display: flex;
            flex-direction: row;
            padding: 20px;
            justify-content: space-between;
            max-width: 1200px;
            margin: 0 auto;
        }

        .bible-text {
            width: 70%;
            background-color: #ffffff;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.05);
            overflow-y: scroll;
            max-height: 90vh;
            transition: all 0.3s ease;
        }

        .bible-text:hover {
            box-shadow: 0 6px 15px rgba(0, 0, 0, 0.1);
        }

        .study-references {
            width: 25%;
            background-color: #ffffff;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.05);
            position: sticky;
            top: 20px;
            max-height: 90vh;
            overflow-y: auto;
            transition: all 0.3s ease;
        }

        .study-references h3 {
            font-family: 'Playfair Display', serif;
            color: #343a40;
            font-size: 22px;
        }

        .study-references ul {
            list-style-type: none;
            padding-left: 10px;
        }

        .study-references li {
            margin-bottom: 12px;
            color: #6c757d;
            cursor: pointer;
            transition: all 0.3s;
        }

        .study-references li:hover {
            color: #007bff;
            font-weight: bold;
        }

        .notepad-container {
            position: fixed;
            right: 20px;
            top: 100px;
            z-index: 10;
            display: flex;
            flex-direction: column;
        }

        .notepad {
            width: 250px;
            background-color: #ffffff;
            border: 1px solid #ddd;
            border-radius: 8px;
            margin-bottom: 15px;
            display: none;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
            transition: all 0.3s ease;
        }

        .notepad-header {
            background-color: #28a745;
            color: white;
            padding: 8px 12px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            border-top-left-radius: 8px;
            border-top-right-radius: 8px;
            font-weight: bold;
            font-size: 14px;
        }

        .notepad-body {
            background-color: #f8f9fa;
            padding: 10px;
            color: #333;
            min-height: 120px;
        }

        .notepad-header span {
            cursor: pointer;
            font-size: 18px;
        }

        .notepad-toggle {
            display: inline-block;
            margin-top: 20px;
            background-color: #28a745;
            color: white;
            cursor: pointer;
            font-size: 16px;
            text-transform: uppercase;
            font-weight: 600;
            border-radius: 20px;
            padding: 8px 18px;
            border: none;
            transition: background-color 0.3s ease;
        }

        .notepad-toggle:hover {
            background-color: #218838;
        }

        .bible-content {
            background-color: #f8f9fa;
            padding: 15px;
            margin-bottom: 15px;
            border-radius: 6px;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
        }

        .bible-content h2 {
            font-family: 'Playfair Display', serif;
            color: #28a745;
            margin-bottom: 10px;
        }

        .bible-content p {
            font-size: 16px;
            color: #333;
        }

        .study-note {
            background-color: #f1f3f5;
            padding: 10px;
            margin-top: 10px;
            color: #6c757d;
            font-style: italic;
            border-radius: 6px;
            font-size: 14px;
        }

        .study-prompt {
            background-color: #e9ecef;
            padding: 10px;
            margin-top: 15px;
            color: #495057;
            font-weight: bold;
            border-radius: 6px;
            font-size: 14px;
        }

    </style>
</head>
<body>

    <h1>Bible Study Website</h1>

    <div class="container">
        <!-- Bible Text Section -->
        <div class="bible-text">
            <div class="bible-content" id="genesis1">
                <h2>Genesis 1:1</h2>
                <p>In the beginning, God created the heavens and the earth.</p>
                <div class="study-note">
                    <p><strong>Study Note:</strong> This verse speaks to God's omnipotence and sovereignty as Creator. It sets the stage for the entire Biblical narrative, introducing the act of creation.</p>
                </div>
                <div class="study-prompt">
                    <p><strong>Study Prompt:</strong> Reflect on the significance of God as the Creator. How does this impact your understanding of the world around you?</p>
                </div>
            </div>

            <div class="bible-content" id="genesis2">
                <h2>Genesis 1:2</h2>
                <p>The earth was without form, and void; and darkness was on the face of the deep. And the Spirit of God was hovering over the face of the waters.</p>
                <div class="study-note">
                    <p><strong>Study Note:</strong> This verse highlights the initial state of the earth. It’s important to note that God’s Spirit was present, bringing order and preparation for creation.</p>
                </div>
                <div class="study-prompt">
                    <p><strong>Study Prompt:</strong> How does this verse demonstrate the presence and involvement of God's Spirit in creation? How do you perceive the Spirit's role in your life?</p>
                </div>
            </div>

            <!-- More Bible Content Here -->
        </div>

        <!-- Study References Section -->
        <div class="study-references">
            <h3>Study References</h3>
            <ul>
                <li onclick="scrollToVerse('genesis1')">Genesis 1:1 - In the Beginning</li>
                <li onclick="scrollToVerse('genesis2')">Genesis 1:2 - Earth Without Form</li>
                <!-- Add more references as you wish -->
            </ul>
        </div>
    </div>

    <!-- Notepad Section -->
    <div class="notepad-container">
        <div class="notepad" id="notepad1">
            <div class="notepad-header">
                <span>Notepad 1</span><span onclick="closeNotepad('notepad1')">X</span>
            </div>
            <div class="notepad-body">
                <p>Note down your thoughts here. Reflect on the Bible verses you read today.</p>
                <textarea style="width: 100%; height: 100px; border: none; font-size: 14px; color: #333; background-color: #f8f9fa;"></textarea>
            </div>
        </div>

        <div class="notepad" id="notepad2">
            <div class="notepad-header">
                <span>Notepad 2</span><span onclick="closeNotepad('notepad2')">X</span>
            </div>
            <div class="notepad-body">
                <p>Write down your questions and insights here.</p>
                <textarea style="width: 100%; height: 100px; border: none; font-size: 14px; color: #333; background-color: #f8f9fa;"></textarea>
            </div>
        </div>

        <div class="notepad-toggle" onclick="toggleNotepad('notepad1')">Open Notepad 1</div>
        <div class="notepad-toggle" onclick="toggleNotepad('notepad2')">Open Notepad 2</div>
    </div>

    <script>
        // Scroll to the relevant verse when a reference is clicked
        function scrollToVerse(verseId) {
            const verseElement = document.getElementById(verseId);
            verseElement.scrollIntoView({ behavior: 'smooth' });
        }

        // Function to open a notepad
        function toggleNotepad(notepadId) {
            const notepad = document.getElementById(notepadId);
            notepad.style.display = notepad.style.display === "none" || notepad.style.display === "" ? "block" : "none";
        }

        // Function to close a notepad
        function closeNotepad(notepadId) {
            const notepad = document.getElementById(notepadId);
            notepad.style.display = "none";
        }
    </script>

</body>
</html>
