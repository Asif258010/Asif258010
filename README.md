<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Remove Background</title>
</head>
<body>
    <h1>Remove Background from Your Image</h1>
    <form action="/" method="POST" enctype="multipart/form-data">
        <input type="file" name="image" accept="image/*" required>
        <button type="submit">Upload and Process</button>
    </form>

    {% if error %}
        <p style="color: red;">{{ error }}</p>
    {% endif %}

    {% if image_url %}
        <h2>Processed Image</h2>
        <img src="{{ image_url }}" alt="Processed Image">
        <br>
        <a href="{{ image_url }}" download>Download Image</a>
    {% endif %}

    <h2>Leave a Review</h2>
    <form action="/review" method="POST">
        <textarea name="feedback" placeholder="Write your review here..." required></textarea>
        <button type="submit">Submit Review</button>
    </form>

    <h2><a href="/reviews">View Reviews</a></h2>
</body>
</html>

<!---
Asif258010/Asif258010 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
