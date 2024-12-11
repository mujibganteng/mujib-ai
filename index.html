<meta name='viewport' content='width=device-width, initial-scale=1'/><!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mujib AI</title>
    <style>
        body {
            font-family: 'Courier New', Courier, monospace;
            background-color: #1e1e1e;
            color: #00ff00;
            margin: 0;
            padding: 20px;
        }
        header {
            background-color: #222;
            padding: 10px 0;
            text-align: center;
            border-bottom: 2px solid #00ff00;
        }
        .container {
            max-width: 600px;
            margin: auto;
            background: #333;
            padding: 20px;
            border-radius: 5px;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.5);
        }
        input, button, textarea {
            width: 100%;
            padding: 10px;
            margin: 10px 0;
            border: 1px solid #00ff00;
            border-radius: 5px;
            background: #222;
            color: #00ff00;
        }
        input[type="file"] {
            border: none;
            padding: 0;
        }
        button {
            background-color: #00ff00;
            color: #222;
            cursor: pointer;
        }
        button:hover {
            background-color: #00cc00;
        }
        #response {
            margin-top: 20px;
            background: #444;
            padding: 10px;
            border-radius: 5px;
        }
        #image {
            margin-top: 20px;
            max-width: 100%;
        }
    </style>
</head>
<body>

<header>
    <h1>Mujib AI</h1>
</header>

<div class="container">
    <h2>Masukkan Pertanyaan Anda</h2>
    <input type="text" id="question" placeholder="Tanyakan sesuatu...">
    <input type="file" id="media" accept="image/*,video/*">
    <input type="text" id="imagePrompt" placeholder="Deskripsi gambar yang ingin dibuat...">
    <button onclick="askQuestion()">Kirim</button>
    <div id="response"></div>
    <img id="image" style="display: none;" alt="Generated Image">
</div>

<script>
    async function askQuestion() {
        const question = document.getElementById('question').value;
        const mediaFile = document.getElementById('media').files[0];
        const imagePrompt = document.getElementById('imagePrompt').value;
        const responseDiv = document.getElementById('response');
        const imageElement = document.getElementById('image');
        responseDiv.innerHTML = 'Memproses...';
        imageElement.style.display = 'none';

        try {
            const formData = new FormData();
            formData.append('question', question);
            if (mediaFile) {
                formData.append('media', mediaFile);
            }

            // Mengirim pertanyaan dan file media ke server Anda
            const response = await fetch('https://platform.openai.com', {
                method: 'POST',
                body: formData
            });

            const data = await response.json();
            responseDiv.innerHTML = `<h3>Jawaban:</h3><p>${data.answer}</p>`;
            if (data.media) {
                responseDiv.innerHTML += `<img src="${data.media}" alt="Media" style="max-width: 100%;">`;
            }

            // Membuat gambar berdasarkan deskripsi
            if (imagePrompt) {
                const imageResponse = await fetch('https://api.openai.com/v1/images/generations', {
                    method: 'POST',
                    headers: {
                        'Authorization': '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',
                        'Content-Type': 'application/json'
                    },
                    body: JSON.stringify({ prompt: imagePrompt, n: 1, size: '1024x1024' })
                });

                const imageData = await imageResponse.json();
                if (imageData.data && imageData.data.length > 0) {
                    imageElement.src = imageData.data[0].url;
                    imageElement.style.display = 'block';
                }
            }
        } catch (error) {
            responseDiv.innerHTML = 'Terjadi kesalahan. Silakan coba lagi.';
            console.error('Error:', error);
        }
    }
</script>

</body>
</html>
