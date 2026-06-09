# banari-family-.html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>BANARI FAMILY</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Playfair+Display:wght@700&family=Roboto:wght@400;500;700&display=swap');
        
        :root {
            --primary: #8B4513;
            --accent: #D4A017;
            --light: #F5F5F5;
        }
        
        * { margin: 0; padding: 0; box-sizing: border-box; }
        
        body {
            font-family: 'Roboto', sans-serif;
            background: linear-gradient(135deg, #f8f1e3 0%, #e8d9c0 100%);
            color: #333;
            line-height: 1.6;
            min-height: 100vh;
        }
        
        header {
            background: var(--primary);
            color: white;
            padding: 1rem 1rem;
            position: sticky;
            top: 0;
            z-index: 100;
            box-shadow: 0 4px 10px rgba(0,0,0,0.2);
            display: flex;
            align-items: center;
            justify-content: space-between;
        }
        
        .logo-btn {
            font-family: 'Playfair Display', serif;
            font-size: 1.8rem;
            font-weight: bold;
            letter-spacing: 3px;
            background: none;
            border: none;
            color: white;
            cursor: pointer;
            text-align: center;
            flex: 1;
        }
        
        .add-btn {
            background: var(--accent);
            color: #333;
            padding: 10px 20px;
            border: none;
            border-radius: 50px;
            font-weight: bold;
            cursor: pointer;
            white-space: nowrap;
        }
        
        /* HOME PAGE */
        .home-page {
            text-align: center;
            padding: 20px;
        }
        
        .hero-gallery {
            display: flex;
            flex-direction: column;
            gap: 20px;
            margin: 30px 0;
        }
        
        .hero-gallery img {
            width: 100%;
            max-height: 320px;
            object-fit: cover;
            border-radius: 12px;
            box-shadow: 0 10px 25px rgba(139, 69, 19, 0.25);
        }
        
        .welcome {
            font-size: 2.2rem;
            color: var(--primary);
            margin: 20px 0;
            font-family: 'Playfair Display', serif;
        }
        
        /* MAIN NAV PAGE */
        .main-page, .fakrudheen-page, .kadheeja-page, .their-family-page, .child-detail-page {
            display: none;
            padding: 20px;
        }
        
        .nav-column {
            display: flex;
            flex-direction: column;
            gap: 18px;
            max-width: 500px;
            margin: 40px auto;
        }
        
        .nav-btn {
            background: var(--primary);
            color: white;
            padding: 20px;
            font-size: 1.3rem;
            border: none;
            border-radius: 12px;
            cursor: pointer;
            text-align: center;
            box-shadow: 0 6px 15px rgba(139, 69, 19, 0.3);
        }
        
        .nav-btn:hover {
            background: #6B3A10;
            transform: scale(1.03);
        }
        
        /* FORM */
        .form-container {
            background: white;
            border-radius: 12px;
            padding: 25px;
            box-shadow: 0 6px 20px rgba(0,0,0,0.1);
            max-width: 600px;
            margin: 20px auto;
        }
        
        .form-grid {
            display: grid;
            grid-template-columns: 1fr;
            gap: 16px;
        }
        
        .form-group {
            display: flex;
            flex-direction: column;
        }
        
        label {
            font-weight: 500;
            margin-bottom: 6px;
            color: #444;
        }
        
        input, select, textarea {
            padding: 12px;
            border: 2px solid #ddd;
            border-radius: 8px;
            font-size: 1rem;
        }
        
        .photo-upload {
            border: 2px dashed var(--accent);
            padding: 20px;
            text-align: center;
            cursor: pointer;
        }
        
        .preview-img {
            max-width: 200px;
            max-height: 200px;
            margin: 10px auto;
            border-radius: 8px;
        }
        
        .btn-save {
            background: #228B22;
            color: white;
            padding: 15px;
            font-size: 1.2rem;
            width: 100%;
            border: none;
            border-radius: 50px;
            margin-top: 10px;
        }
        
        /* TABLES */
        table {
            width: 100%;
            border-collapse: collapse;
            margin: 20px 0;
            background: white;
            border-radius: 8px;
            overflow: hidden;
        }
        
        th, td {
            padding: 14px 10px;
            text-align: left;
            border-bottom: 1px solid #eee;
        }
        
        th {
            background: var(--primary);
            color: white;
        }
        
        .back-btn {
            background: #555;
            color: white;
            padding: 10px 20px;
            border: none;
            border-radius: 50px;
            margin-bottom: 20px;
        }
        
        .footer {
            text-align: center;
            padding: 30px 10px;
            color: #666;
            font-size: 0.95rem;
        }
    </style>
</head>
<body>

    <!-- HOME PAGE -->
    <div id="homePage" class="home-page">
        <header>
            <button class="logo-btn" onclick="showMainPage()">BANARI FAMILY</button>
            <button class="add-btn" onclick="showAddMember()">+ Add Member</button>
        </header>
        
        <h2 class="welcome">Welcome to Our Family</h2>
        
        <div class="hero-gallery">
            <img src="/home/workdir/attachments/SnVld" alt="Family Gathering 1">
            <img src="/home/workdir/attachments/8z3lU" alt="Family Gathering 2">
            <img src="/home/workdir/attachments/AO71L" alt="Family Gathering 3">
        </div>
        
        <p style="margin-top: 30px; font-size: 1.1rem;">Tap the BANARI FAMILY button above to explore the family directory</p>
    </div>

    <!-- ADD MEMBER MODAL / PAGE -->
    <div id="addMemberPage" class="main-page form-container">
        <button class="back-btn" onclick="hideAddMember()">â Back</button>
        <h2 style="text-align:center; color:var(--primary);">Add New Family Member</h2>
        <form id="familyForm">
            <div class="form-grid">
                <div class="form-group">
                    <label>Full Name *</label>
                    <input type="text" id="name" required>
                </div>
                <div class="form-group">
                    <label>Photo</label>
                    <div class="photo-upload" onclick="document.getElementById('photoInput').click()">
                        <input type="file" id="photoInput" accept="image/*" style="display:none" onchange="previewPhoto(event)">
                        <p>ð¸ Click to upload photo</p>
                    </div>
                    <img id="photoPreview" class="preview-img" style="display:none">
                </div>
                <div class="form-group"><label>Date of Birth</label><input type="date" id="dob"></div>
                <div class="form-group"><label>Father's Name</label><input type="text" id="father"></div>
                <div class="form-group"><label>Mother's Name</label><input type="text" id="mother"></div>
                <div class="form-group"><label>Blood Group</label>
                    <select id="blood">
                        <option value="">Select</option>
                        <option>A+</option><option>A-</option><option>B+</option><option>B-</option>
                        <option>AB+</option><option>AB-</option><option>O+</option><option>O-</option>
                    </select>
                </div>
                <div class="form-group"><label>Phone Number</label><input type="tel" id="phone"></div>
                <div class="form-group"><label>Spouse Name</label><input type="text" id="spouse"></div>
                <div class="form-group"><label>Children (comma separated)</label><textarea id="children" rows="3"></textarea></div>
            </div>
            <button type="submit" class="btn-save">Save Member</button>
        </form>
    </div>

    <!-- MAIN NAV PAGE -->
    <div id="mainPage" class="main-page">
        <header>
            <button class="logo-btn" onclick="goToHome()">BANARI FAMILY</button>
            <button class="add-btn" onclick="showAddMember()">+ Add Member</button>
        </header>
        <div class="nav-column">
            <button class="nav-btn" onclick="showFakrudheenPage()">1. FAKRUDHEEN HAJI</button>
            <button class="nav-btn" onclick="showKadheejaPage()">2. KADHEEJA HAJJUMMA</button>
            <button class="nav-btn" onclick="showTheirFamilyPage()">3. THEIR FAMILY</button>
        </div>
    </div>

    <!-- FAKRUDHEEN HAJI PAGE -->
    <div id="fakrudheenPage" class="fakrudheen-page">
        <header>
            <button class="logo-btn" onclick="showMainPage()">BANARI FAMILY</button>
            <button class="add-btn" onclick="showAddMember()">+ Add</button>
        </header>
        <button class="back-btn" onclick="showMainPage()">â Back</button>
        <div class="form-container">
            <h2>Fakrudheen Haji</h2>
            <p><strong>Head of the Family</strong></p>
            <p>Details about Fakrudheen Haji will be displayed here. You can expand this section with more information later.</p>
        </div>
    </div>

    <!-- KADHEEJA HAJJUMMA PAGE -->
    <div id="kadheejaPage" class="kadheeja-page">
        <header>
            <button class="logo-btn" onclick="showMainPage()">BANARI FAMILY</button>
            <button class="add-btn" onclick="showAddMember()">+ Add</button>
        </header>
        <button class="back-btn" onclick="showMainPage()">â Back</button>
        <div class="form-container">
            <h2>Kadheeja Hajjumma</h2>
            <p><strong>Wife of Fakrudheen Haji</strong></p>
            <p>Details about Kadheeja Hajjumma will be displayed here.</p>
        </div>
    </div>

    <!-- THEIR FAMILY PAGE -->
    <div id="theirFamilyPage" class="their-family-page">
        <header>
            <button class="logo-btn" onclick="showMainPage()">BANARI FAMILY</button>
            <button class="add-btn" onclick="showAddMember()">+ Add</button>
        </header>
        <button class="back-btn" onclick="showMainPage()">â Back</button>
        <h2 style="text-align:center; margin:20px;">Their Children & Families</h2>
        <div id="childrenList" style="max-width:700px; margin:0 auto;"></div>
    </div>

    <footer class="footer">
        <p>Â© BANARI FAMILY â¢ All data saved locally in your browser â¢ Optimized for Mobile</p>
    </footer>

    <script>
        // Data storage
        let familyMembers = JSON.parse(localStorage.getItem('banariFamily')) || [];
        
        // Page navigation
        function goToHome() {
            hideAllPages();
            document.getElementById('homePage').style.display = 'block';
        }
        
        function showMainPage() {
            hideAllPages();
            document.getElementById('mainPage').style.display = 'block';
        }
        
        function showFakrudheenPage() {
            hideAllPages();
            document.getElementById('fakrudheenPage').style.display = 'block';
        }
        
        function showKadheejaPage() {
            hideAllPages();
            document.getElementById('kadheejaPage').style.display = 'block';
        }
        
        function showTheirFamilyPage() {
            hideAllPages();
            document.getElementById('theirFamilyPage').style.display = 'block';
            renderTheirFamily();
        }
        
        function hideAllPages() {
            document.querySelectorAll('.main-page, .home-page, .fakrudheen-page, .kadheeja-page, .their-family-page').forEach(p => p.style.display = 'none');
        }
        
        function showAddMember() {
            hideAllPages();
            document.getElementById('addMemberPage').style.display = 'block';
            document.getElementById('photoPreview').style.display = 'none';
        }
        
        function hideAddMember() {
            hideAllPages();
            showMainPage();
        }
        
        // Photo preview
        function previewPhoto(event) {
            const file = event.target.files[0];
            if (file) {
                const reader = new FileReader();
                reader.onload = function(e) {
                    const preview = document.getElementById('photoPreview');
                    preview.src = e.target.result;
                    preview.style.display = 'block';
                };
                reader.readAsDataURL(file);
            }
        }
        
        // Form submission
        document.getElementById('familyForm').addEventListener('submit', function(e) {
            e.preventDefault();
            
            const photoPreview = document.getElementById('photoPreview');
            const photoData = photoPreview.src && photoPreview.style.display !== 'none' ? photoPreview.src : '';
            
            const newMember = {
                id: Date.now(),
                name: document.getElementById('name').value.trim(),
                photo: photoData,
                dob: document.getElementById('dob').value,
                father: document.getElementById('father').value.trim(),
                mother: document.getElementById('mother').value.trim(),
                blood: document.getElementById('blood').value,
                phone: document.getElementById('phone').value,
                spouse: document.getElementById('spouse').value.trim(),
                children: document.getElementById('children').value.trim()
            };
            
            if (newMember.name) {
                familyMembers.push(newMember);
                localStorage.setItem('banariFamily', JSON.stringify(familyMembers));
                alert('â Member added successfully!');
                this.reset();
                document.getElementById('photoPreview').style.display = 'none';
                hideAddMember();
            } else {
                alert('Please enter a name');
            }
        });
        
        // Render children under "Their Family"
        function renderTheirFamily() {
            const container = document.getElementById('childrenList');
            container.innerHTML = '';
            
            // Filter children of Fakrudheen & Kadheeja
            const children = familyMembers.filter(m => 
                (m.father && m.father.toLowerCase().includes('fakrudheen')) || 
                (m.mother && m.mother.toLowerCase().includes('kadheeja'))
            );
            
            if (children.length === 0) {
                container.innerHTML = '<p style="text-align:center; padding:40px;">No children added yet. Use "Add Member" to add family members with parents as Fakrudheen Haji & Kadheeja Hajjumma.</p>';
                return;
            }
            
            children.forEach(child => {
                const card = document.createElement('div');
                card.style = 'background:white; border-radius:12px; padding:20px; margin-bottom:20px; box-shadow:0 4px 12px rgba(0,0,0,0.1);';
                card.innerHTML = `
                    <h3>${child.name}</h3>
                    <p><strong>Spouse:</strong> ${child.spouse || 'Not added'}</p>
                    <p><strong>Children:</strong> ${child.children || 'None listed'}</p>
                    ${child.photo ? `<img src="${child.photo}" style="max-width:180px; border-radius:8px; margin-top:10px;">` : ''}
                `;
                container.appendChild(card);
            });
        }
        
        // Initialize
        window.onload = function() {
            // Show home page by default
            document.getElementById('homePage').style.display = 'block';
            
            // For demo, you can pre-populate some data here if needed
        };
    </script>
</body>
</html>