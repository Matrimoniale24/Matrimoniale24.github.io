# Matrimoniale24.github.io
<!DOCTYPE html>
<html lang="ro">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Site gratuit de matrimoniale pentru a găsi sufletul pereche!">
    <title>Matrimoniale Online</title>
    <style>
        body { font-family: Arial, sans-serif; background: #f8f9fa; }
        .container { width: 90%; max-width: 800px; margin: auto; background: white; padding: 20px; border-radius: 10px; box-shadow: 0px 0px 10px rgba(0,0,0,0.1); }
        h1, p { text-align: center; }
        input, button { width: 100%; padding: 10px; margin-top: 10px; border: 1px solid #ccc; border-radius: 5px; }
        button { background: #28a745; color: white; border: none; cursor: pointer; }
        button:hover { background: #218838; }
        .profile-list { margin-top: 20px; display: flex; flex-wrap: wrap; gap: 10px; }
        .profile-card { background: #fff; padding: 10px; border-radius: 5px; box-shadow: 0 0 5px rgba(0,0,0,0.1); width: calc(50% - 10px); text-align: center; }
        img { width: 100px; height: 100px; border-radius: 50%; object-fit: cover; }
    </style>
</head>
<body>
    <div class="container">
        <h1>Matrimoniale Online</h1>
        <p>Înscrie-te pentru a găsi sufletul pereche!</p>
        <input type="text" id="name" placeholder="Numele tău">
        <input type="number" id="age" placeholder="Vârsta">
        <input type="url" id="photo" placeholder="URL poză">
        <button onclick="addProfile()">Înscrie-te</button>
        <h2>Profiluri recente</h2>
        <div class="profile-list" id="profiles"></div>
    </div>

    <script>
        function addProfile() {
            let name = document.getElementById('name').value;
            let age = document.getElementById('age').value;
            let photo = document.getElementById('photo').value;
            
            if (name && age && photo) {
                let profileList = document.getElementById('profiles');
                let profile = document.createElement('div');
                profile.classList.add('profile-card');
                profile.innerHTML = `<img src="${photo}" alt="Profil"><p><strong>${name}</strong>, ${age} ani</p>`;
                profileList.appendChild(profile);
                
                document.getElementById('name').value = '';
                document.getElementById('age').value = '';
                document.getElementById('photo').value = '';
            }
        }
    </script>
</body>
</html>
