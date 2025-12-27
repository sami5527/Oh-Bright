<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>BrightPath Academy | Registration</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary: #4834d4;
            --secondary: #6c5ce7;
            --tg-blue: #0088cc;
            --success: #00b894;
            --text: #2d3436;
            --light-bg: #f8f9fa;
            --gradient: linear-gradient(135deg, #4834d4 0%, #6c5ce7 100%);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Poppins', sans-serif;
            background: var(--light-bg);
            color: var(--text);
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 20px;
        }

        .container {
            display: flex;
            max-width: 1200px;
            width: 100%;
            gap: 40px;
            align-items: stretch;
        }

        /* Hero Section */
        .hero {
            flex: 1;
            background: var(--gradient);
            border-radius: 20px;
            padding: 40px;
            color: white;
            display: flex;
            flex-direction: column;
            justify-content: center;
            box-shadow: 0 15px 35px rgba(72, 52, 212, 0.2);
        }

        .hero h1 {
            font-size: 42px;
            margin-bottom: 20px;
            font-weight: 700;
        }

        .hero p {
            font-size: 18px;
            opacity: 0.9;
            line-height: 1.6;
            margin-bottom: 30px;
        }

        .features {
            list-style: none;
            margin: 30px 0;
        }

        .features li {
            margin-bottom: 15px;
            display: flex;
            align-items: center;
            font-size: 16px;
        }

        .features i {
            margin-right: 12px;
            background: rgba(255, 255, 255, 0.2);
            width: 30px;
            height: 30px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .stats {
            display: flex;
            gap: 30px;
            margin-top: 40px;
        }

        .stat-item {
            text-align: center;
        }

        .stat-number {
            font-size: 32px;
            font-weight: 700;
            display: block;
        }

        .stat-label {
            font-size: 14px;
            opacity: 0.8;
        }

        /* Card Styling */
        .card {
            background: white;
            width: 100%;
            max-width: 500px;
            border-radius: 20px;
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.1);
            overflow: hidden;
        }

        .card-header {
            background: var(--gradient);
            color: white;
            padding: 25px 30px;
            text-align: center;
        }

        .card-header h2 {
            font-size: 28px;
            font-weight: 600;
            margin-bottom: 5px;
        }

        .card-header p {
            opacity: 0.9;
        }

        .card-body {
            padding: 30px;
        }

        .hidden {
            display: none !important;
        }

        .step-indicator {
            display: flex;
            justify-content: center;
            margin-bottom: 30px;
        }

        .step {
            display: flex;
            flex-direction: column;
            align-items: center;
            position: relative;
            width: 120px;
        }

        .step-circle {
            width: 40px;
            height: 40px;
            border-radius: 50%;
            background: #e0e0e0;
            color: #999;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: 600;
            margin-bottom: 8px;
            transition: all 0.3s ease;
        }

        .step.active .step-circle {
            background: var(--primary);
            color: white;
        }

        .step-line {
            position: absolute;
            top: 20px;
            left: 70px;
            width: 50px;
            height: 2px;
            background: #e0e0e0;
        }

        .step:last-child .step-line {
            display: none;
        }

        /* Form Styling */
        .form-group {
            margin-bottom: 20px;
        }

        label {
            display: block;
            font-weight: 500;
            margin-bottom: 8px;
            color: var(--text);
            font-size: 14px;
        }

        input, select {
            width: 100%;
            padding: 14px 18px;
            border: 2px solid #e9ecef;
            border-radius: 12px;
            font-size: 15px;
            font-family: 'Poppins', sans-serif;
            transition: all 0.3s ease;
        }

        input:focus, select:focus {
            border-color: var(--primary);
            outline: none;
            box-shadow: 0 0 0 3px rgba(72, 52, 212, 0.1);
        }

        .payment-info {
            background: #f8f9fa;
            border-left: 4px solid var(--primary);
            padding: 20px;
            border-radius: 12px;
            margin: 20px 0;
        }

        .bank-row {
            display: flex;
            justify-content: space-between;
            margin-bottom: 12px;
            padding-bottom: 12px;
            border-bottom: 1px dashed #dee2e6;
        }

        .bank-row:last-child {
            border-bottom: none;
            margin-bottom: 0;
            padding-bottom: 0;
        }

        .account-name {
            text-align: center;
            font-weight: 600;
            color: var(--primary);
            font-size: 16px;
            margin-bottom: 15px;
            padding-bottom: 15px;
            border-bottom: 2px solid #dee2e6;
        }

        .price-badge {
            background: linear-gradient(135deg, #00b894, #00cec9);
            color: white;
            padding: 10px 25px;
            border-radius: 30px;
            font-weight: 600;
            display: inline-block;
            margin-bottom: 20px;
            box-shadow: 0 5px 15px rgba(0, 184, 148, 0.3);
        }

        .screenshot-area {
            border: 2px dashed #cbd5e0;
            padding: 25px;
            text-align: center;
            border-radius: 12px;
            background: #fffcf0;
            margin: 20px 0;
            cursor: pointer;
            transition: all 0.3s ease;
        }

        .screenshot-area:hover {
            border-color: var(--primary);
            background: #fff9e6;
        }

        .screenshot-area i {
            font-size: 40px;
            color: #fdcb6e;
            margin-bottom: 15px;
        }

        /* Buttons */
        .btn {
            width: 100%;
            padding: 16px;
            border: none;
            border-radius: 12px;
            font-size: 16px;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 10px;
        }

        .btn-primary {
            background: var(--gradient);
            color: white;
        }

        .btn-primary:hover {
            transform: translateY(-2px);
            box-shadow: 0 7px 20px rgba(72, 52, 212, 0.3);
        }

        .btn-tg {
            background: var(--tg-blue);
            color: white;
        }

        .btn-tg:hover {
            background: #0077b3;
            transform: translateY(-2px);
        }

        .btn-secondary {
            background: #f1f2f6;
            color: var(--text);
            margin-top: 15px;
        }

        .btn-secondary:hover {
            background: #e4e6eb;
        }

        /* Success Message */
        .success-message {
            text-align: center;
            padding: 40px 30px;
        }

        .success-icon {
            width: 80px;
            height: 80px;
            background: linear-gradient(135deg, #00b894, #00cec9);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto 25px;
        }

        .success-icon i {
            font-size: 40px;
            color: white;
        }

        /* Responsive */
        @media (max-width: 992px) {
            .container {
                flex-direction: column;
            }
            
            .hero {
                order: -1;
            }
            
            .card {
                max-width: 100%;
            }
        }

        @media (max-width: 576px) {
            .hero h1 {
                font-size: 32px;
            }
            
            .stats {
                flex-direction: column;
                gap: 20px;
            }
            
            .card-body {
                padding: 20px;
            }
        }

        /* Loading Animation */
        .loader {
            display: none;
            width: 20px;
            height: 20px;
            border: 3px solid rgba(255, 255, 255, 0.3);
            border-radius: 50%;
            border-top-color: white;
            animation: spin 1s ease-in-out infinite;
        }

        @keyframes spin {
            to { transform: rotate(360deg); }
        }

        .processing .loader {
            display: inline-block;
        }
    </style>
</head>
<body>

<div class="container">
    <!-- Hero Section -->
    <div class="hero">
        <h1>BrightPath Academy</h1>
        <p>Empowering the next generation of leaders, innovators, and thinkers through quality education and personalized learning experiences.</p>
        
        <ul class="features">
            <li><i class="fas fa-check"></i> Expert Ethiopian Teachers</li>
            <li><i class="fas fa-check"></i> Comprehensive Curriculum</li>
            <li><i class="fas fa-check"></i> Interactive Online Classes</li>
            <li><i class="fas fa-check"></i> Regular Progress Reports</li>
            <li><i class="fas fa-check"></i> Affordable Quality Education</li>
        </ul>
        
        <div class="stats">
            <div class="stat-item">
                <span class="stat-number">1,200+</span>
                <span class="stat-label">Students</span>
            </div>
            <div class="stat-item">
                <span class="stat-number">98%</span>
                <span class="stat-label">Success Rate</span>
            </div>
            <div class="stat-item">
                <span class="stat-number">50+</span>
                <span class="stat-label">Expert Teachers</span>
            </div>
        </div>
    </div>

    <!-- Registration Card -->
    <div class="card">
        <div class="card-header">
            <h2>Student Registration</h2>
            <p>Join BrightPath Academy Today</p>
        </div>
        
        <div class="card-body">
            <!-- Step Indicator -->
            <div class="step-indicator">
                <div class="step active" id="step1-indicator">
                    <div class="step-circle">1</div>
                    <span>Student Info</span>
                    <div class="step-line"></div>
                </div>
                <div class="step" id="step2-indicator">
                    <div class="step-circle">2</div>
                    <span>Payment</span>
                </div>
            </div>

            <!-- Step 1: Student Information -->
            <div id="step1">
                <form id="studentForm">
                    <div class="form-group">
                        <label for="name"><i class="fas fa-user"></i> Full Name</label>
                        <input type="text" id="name" placeholder="Enter your full name" required>
                    </div>
                    
                    <div class="form-group">
                        <label for="phone"><i class="fas fa-phone"></i> Phone Number</label>
                        <input type="tel" id="phone" placeholder="09XX XXX XXX" required>
                    </div>
                    
                    <div class="form-group">
                        <label for="email"><i class="fas fa-envelope"></i> Email Address</label>
                        <input type="email" id="email" placeholder="email@example.com" required>
                    </div>
                    
                    <div class="form-group">
                        <label for="level"><i class="fas fa-graduation-cap"></i> Educational Level</label>
                        <select id="level" required>
                            <option value="">Select your level</option>
                            <option value="Freshman Course">Freshman Course</option>
                            <option value="Remedial Course">Remedial Course</option>
                            <option value="Secondary (Grade 9-12)">Secondary (Grade 9-12)</option>
                            <option value="Grade 8">Grade 8</option>
                            <option value="Grade 7">Grade 7</option>
                            <option value="Primary School">Primary School</option>
                        </select>
                    </div>
                    
                    <button type="button" class="btn btn-primary" onclick="showStep2()">
                        Continue to Payment <i class="fas fa-arrow-right"></i>
                    </button>
                </form>
            </div>

            <!-- Step 2: Payment Information -->
            <div id="step2" class="hidden">
                <center>
                    <div class="price-badge">Registration Fee: 300 ETB</div>
                </center>
                
                <div class="payment-info">
                    <div class="account-name">
                        <i class="fas fa-user-circle"></i> Account Name: Samuel Ashenafi
                    </div>
                    
                    <div class="bank-row">
                        <strong><i class="fas fa-university"></i> Commercial Bank of Ethiopia (CBE):</strong>
                        <span>1000354138216</span>
                    </div>
                    
                    <div class="bank-row">
                        <strong><i class="fas fa-mobile-alt"></i> Telebirr:</strong>
                        <span>0955273939</span>
                    </div>
                    
                    <div class="bank-row">
                        <strong><i class="fas fa-university"></i> COOP Bank (COB):</strong>
                        <span>1004000057532</span>
                    </div>
                </div>

                <div class="form-group">
                    <label for="transactionId"><i class="fas fa-receipt"></i> Transaction ID (Optional)</label>
                    <input type="text" id="transactionId" placeholder="Enter your transaction reference">
                </div>

                <div class="screenshot-area" onclick="document.getElementById('screenshot').click()">
                    <i class="fas fa-cloud-upload-alt"></i>
                    <h4>Upload Payment Screenshot</h4>
                    <p>Click here or drag and drop your payment proof</p>
                    <input type="file" id="screenshot" accept="image/*" hidden>
                    <p id="fileName" style="margin-top: 10px; color: #666;"></p>
                </div>

                <button class="btn btn-tg" onclick="finishRegistration()">
                    <i class="fab fa-telegram"></i> Confirm & Complete Registration
                </button>
                
                <button class="btn btn-secondary" onclick="showStep1()">
                    <i class="fas fa-arrow-left"></i> Go Back
                </button>
            </div>

            <!-- Step 3: Success Message -->
            <div id="step3" class="hidden success-message">
                <div class="success-icon">
                    <i class="fas fa-check"></i>
                </div>
                
                <h2>Registration Submitted!</h2>
                <p>Your registration details have been sent successfully.</p>
                <p>You will be redirected to Telegram to send your payment screenshot.</p>
                
                <div style="margin: 30px 0;">
                    <div class="loader" style="margin: 0 auto;"></div>
                    <p style="margin-top: 15px;">Redirecting in <span id="countdown">5</span> seconds...</p>
                </div>
                
                <button class="btn btn-primary" onclick="openTelegramNow()">
                    <i class="fab fa-telegram"></i> Open Telegram Now
                </button>
            </div>
        </div>
    </div>
</div>

<script>
    // Telegram Configuration
    const BOT_TOKEN = "YOUR_BOT_TOKEN"; // Replace with your bot token
    const CHAT_ID = "YOUR_CHAT_ID"; // Replace with your chat ID
    const ADMIN_TELEGRAM_LINK = "https://t.me/YourUsername"; // Replace with your Telegram username

    // DOM Elements
    const step1 = document.getElementById('step1');
    const step2 = document.getElementById('step2');
    const step3 = document.getElementById('step3');
    const step1Indicator = document.getElementById('step1-indicator');
    const step2Indicator = document.getElementById('step2-indicator');
    const screenshotInput = document.getElementById('screenshot');
    const fileName = document.getElementById('fileName');

    // File upload handler
    screenshotInput.addEventListener('change', function(e) {
        if (e.target.files.length > 0) {
            fileName.textContent = `Selected: ${e.target.files[0].name}`;
            fileName.style.color = 'var(--primary)';
        }
    });

    // Form validation and step navigation
    function showStep2() {
        const name = document.getElementById('name').value.trim();
        const phone = document.getElementById('phone').value.trim();
        const email = document.getElementById('email').value.trim();
        const level = document.getElementById('level').value;

        if (!name || !phone || !email || !level) {
            alert("Please fill in all required fields.");
            return;
        }

        if (!validatePhone(phone)) {
            alert("Please enter a valid Ethiopian phone number (09XXXXXXXX).");
            return;
        }

        if (!validateEmail(email)) {
            alert("Please enter a valid email address.");
            return;
        }

        // Update step indicators
        step1Indicator.classList.remove('active');
        step2Indicator.classList.add('active');

        // Show step 2
        step1.classList.add('hidden');
        step2.classList.remove('hidden');
    }

    function showStep1() {
        // Update step indicators
        step1Indicator.classList.add('active');
        step2Indicator.classList.remove('active');

        // Show step 1
        step2.classList.add('hidden');
        step1.classList.remove('hidden');
    }

    // Validation functions
    function validatePhone(phone) {
        const ethiopianPhoneRegex = /^09[0-9]{8}$/;
        return ethiopianPhoneRegex.test(phone);
    }

    function validateEmail(email) {
        const emailRegex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
        return emailRegex.test(email);
    }

    // Main registration function
    async function finishRegistration() {
        const name = document.getElementById('name').value;
        const phone = document.getElementById('phone').value;
        const email = document.getElementById('email').value;
        const level = document.getElementById('level').value;
        const transactionId = document.getElementById('transactionId').value;
        const screenshotFile = screenshotInput.files[0];

        if (!screenshotFile) {
            alert("Please upload your payment screenshot!");
            return;
        }

        // Show loading state
        const btn = event.target;
        btn.classList.add('processing');
        btn.innerHTML = '<div class="loader"></div> Processing...';

        // Prepare the message
        const timestamp = new Date().toLocaleString('en-US', {
            timeZone: 'Africa/Addis_Ababa',
            hour12: true
        });

        const message = `
🎓 *NEW BRIGHTPATH REGISTRATION*
━━━━━━━━━━━━━━━━━━━━━━━━
👤 *Student Name:* ${name}
📱 *Phone:* ${phone}
📧 *Email:* ${email}
📚 *Educational Level:* ${level}
💰 *Registration Fee:* 300 ETB
🆔 *Transaction ID:* ${transactionId || 'Not provided'}
⏰ *Time:* ${timestamp}
━━━━━━━━━━━━━━━━━━━━━━━━
📸 *Payment Proof:* Screenshot attached
        `;

        try {
            // Send message to Telegram bot
            const response = await fetch(`https://api.telegram.org/bot${BOT_TOKEN}/sendMessage`, {
                method: 'POST',
                headers: { 'Content-Type': 'application/json' },
                body: JSON.stringify({
                    chat_id: CHAT_ID,
                    text: message,
                    parse_mode: "Markdown"
                })
            });

            if (response.ok) {
                // Show success message
                step2.classList.add('hidden');
                step3.classList.remove('hidden');
                
                // Start countdown
                let countdown = 5;
                const countdownElement = document.getElementById('countdown');
                const countdownInterval = setInterval(() => {
                    countdown--;
                    countdownElement.textContent = countdown;
                    
                    if (countdown <= 0) {
                        clearInterval(countdownInterval);
                        openTelegramNow();
                    }
                }, 1000);
            } else {
                throw new Error('Failed to send message');
            }
        } catch (error) {
            console.error('Error:', error);
            alert("There was an error sending your registration. Please try again.");
            btn.classList.remove('processing');
            btn.innerHTML = '<i class="fab fa-telegram"></i> Confirm & Complete Registration';
        }
    }

    function openTelegramNow() {
        // Save registration data to localStorage
        const registrationData = {
            name: document.getElementById('name').value,
            phone: document.getElementById('phone').value,
            email: document.getElementById('email').value,
            level: document.getElementById('level').value,
            timestamp: new Date().toISOString()
        };
        
        localStorage.setItem('brightpath_registration', JSON.stringify(registrationData));
        
        // Open Telegram
        window.location.href = ADMIN_TELEGRAM_LINK;
    }

    // Auto-fill form from localStorage if available
    window.addEventListener('load', function() {
        const savedData = localStorage.getItem('brightpath_registration');
        if (savedData) {
            try {
                const data = JSON.parse(savedData);
                if (Date.now() - new Date(data.timestamp).getTime() < 24 * 60 * 60 * 1000) {
                    // Data is less than 24 hours old
                    document.getElementById('name').value = data.name || '';
                    document.getElementById('phone').value = data.phone || '';
                    document.getElementById('email').value = data.email || '';
                    document.getElementById('level').value = data.level || '';
                }
            } catch (e) {
                console.log('No valid saved data found');
            }
        }
    });
</script>

</body>
</html>
