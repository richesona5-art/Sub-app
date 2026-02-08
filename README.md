# Sub-app
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sub Application | Goddess Services</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;700&family=Lato:wght@300;400;700&display=swap');
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            background: linear-gradient(135deg, #0f0c29 0%, #302b63 50%, #24243e 100%);
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            font-family: 'Lato', sans-serif;
            color: #e0e0e0;
            padding: 20px;
        }
        
        .container {
            background: rgba(255, 255, 255, 0.05);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.1);
            border-radius: 20px;
            padding: 40px;
            max-width: 600px;
            width: 100%;
            box-shadow: 0 20px 60px rgba(0, 0, 0, 0.5);
        }
        
        h1 {
            font-family: 'Playfair Display', serif;
            font-size: 2.5rem;
            text-align: center;
            margin-bottom: 10px;
            background: linear-gradient(45deg, #ffd700, #ffed4e);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }
        
        .subtitle {
            text-align: center;
            color: #a0a0a0;
            margin-bottom: 30px;
            font-size: 0.9rem;
            letter-spacing: 2px;
            text-transform: uppercase;
        }
        
        .form-group {
            margin-bottom: 25px;
        }
        
        label {
            display: block;
            margin-bottom: 8px;
            font-weight: 700;
            color: #ffd700;
            font-size: 0.85rem;
            text-transform: uppercase;
            letter-spacing: 1px;
        }
        
        input, select, textarea {
            width: 100%;
            padding: 12px 15px;
            background: rgba(0, 0, 0, 0.3);
            border: 1px solid rgba(255, 215, 0, 0.3);
            border-radius: 8px;
            color: #fff;
            font-family: 'Lato', sans-serif;
            font-size: 1rem;
            transition: all 0.3s ease;
        }
        
        input:focus, select:focus, textarea:focus {
            outline: none;
            border-color: #ffd700;
            box-shadow: 0 0 10px rgba(255, 215, 0, 0.2);
        }
        
        textarea {
            resize: vertical;
            min-height: 100px;
        }
        
        .required {
            color: #ff6b6b;
        }
        
        .checkbox-group {
            display: flex;
            align-items: flex-start;
            margin-bottom: 15px;
        }
        
        .checkbox-group input {
            width: auto;
            margin-right: 10px;
            margin-top: 3px;
        }
        
        .checkbox-group label {
            font-weight: 400;
            text-transform: none;
            letter-spacing: 0;
            color: #e0e0e0;
            font-size: 0.9rem;
        }
        
        button {
            width: 100%;
            padding: 15px;
            background: linear-gradient(45deg, #ffd700, #ffed4e);
            border: none;
            border-radius: 8px;
            color: #0f0c29;
            font-family: 'Playfair Display', serif;
            font-size: 1.2rem;
            font-weight: 700;
            cursor: pointer;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            text-transform: uppercase;
            letter-spacing: 2px;
        }
        
        button:hover {
            transform: translateY(-2px);
            box-shadow: 0 10px 30px rgba(255, 215, 0, 0.4);
        }
        
        .disclaimer {
            margin-top: 20px;
            font-size: 0.75rem;
            color: #666;
            text-align: center;
            line-height: 1.5;
        }
        
        .success-message {
            display: none;
            background: rgba(0, 255, 0, 0.1);
            border: 1px solid rgba(0, 255, 0, 0.3);
            color: #00ff88;
            padding: 20px;
            border-radius: 8px;
            text-align: center;
            margin-top: 20px;
        }
        
        @media (max-width: 600px) {
            .container {
                padding: 25px;
            }
            h1 {
                font-size: 2rem;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Sub Application</h1>
        <p class="subtitle">Prove Your Worth</p>
        
        <form id="subApplication" action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
            <!-- Basic Info -->
            <div class="form-group">
                <label>Preferred Name / Sub Name <span class="required">*</span></label>
                <input type="text" name="sub_name" required placeholder="How you wish to be addressed">
            </div>
            
            <div class="form-group">
                <label>Age <span class="required">*</span></label>
                <input type="number" name="age" min="18" required placeholder="Must be 18+">
            </div>
            
            <div class="form-group">
                <label>Contact Method <span class="required">*</span></label>
                <select name="contact_method" required>
                    <option value="">Select preferred contact</option>
                    <option value="twitter">Twitter/X</option>
                    <option value="instagram">Instagram</option>
                    <option value="telegram">Telegram</option>
                    <option value="email">Email</option>
                    <option value="other">Other (specify in notes)</option>
                </select>
            </div>
            
            <div class="form-group">
                <label>Username / Handle <span class="required">*</span></label>
                <input type="text" name="username" required placeholder="@username or email">
            </div>
            
            <!-- Financial Info -->
            <div class="form-group">
                <label>Monthly Tribute Budget (USD) <span class="required">*</span></label>
                <select name="budget" required>
                    <option value="">Select range</option>
                    <option value="100-500">$100 - $500</option>
                    <option value="500-1000">$500 - $1,000</option>
                    <option value="1000-2500">$1,000 - $2,500</option>
                    <option value="2500-5000">$2,500 - $5,000</option>
                    <option value="5000+">$5,000+</option>
                    <option value="negotiable">Negotiable / Open</option>
                </select>
            </div>
            
            <div class="form-group">
                <label>Primary Payment Method <span class="required">*</span></label>
                <select name="payment_method" required>
                    <option value="">Select method</option>
                    <option value="cashapp">CashApp</option>
                    <option value="paypal">PayPal</option>
                    <option value="venmo">Venmo</option>
                    <option value="crypto">Cryptocurrency</option>
                    <option value="giftcards">Gift Cards</option>
                    <option value="other">Other</option>
                </select>
            </div>
            
            <!-- Experience & Interests -->
            <div class="form-group">
                <label>Experience Level <span class="required">*</span></label>
                <select name="experience" required>
                    <option value="">Select level</option>
                    <option value="new">New / Curious</option>
                    <option value="some">Some Experience</option>
                    <option value="experienced">Experienced</option>
                    <option value="veteran">Long-term Lifestyle</option>
                </select>
            </div>
            
            <div class="form-group">
                <label>Interests / Kinks <span class="required">*</span></label>
                <textarea name="interests" required placeholder="List your interests: CBT, chastity, humiliation, sissification, blackmail fantasy, ignore fetish, etc."></textarea>
            </div>
            
            <div class="form-group">
                <label>Hard Limits</label>
                <textarea name="limits" placeholder="What is absolutely off-limits for you?"></textarea>
            </div>
            
            <div class="form-group">
                <label>Why do you wish to serve? <span class="required">*</span></label>
                <textarea name="why_serve" required placeholder="Explain your motivations and what you seek from this dynamic..."></textarea>
            </div>
            
            <!-- Agreements -->
            <div class="form-group">
                <div class="checkbox-group">
                    <input type="checkbox" id="age_verify" name="age_verify" required>
                    <label for="age_verify">I confirm I am 18+ years old <span class="required">*</span></label>
                </div>
                
                <div class="checkbox-group">
                    <input type="checkbox" id="consent" name="consent" required>
                    <label for="consent">I understand this is a financial domination relationship and consent to consensual power exchange <span class="required">*</span></label>
                </div>
                
                <div class="checkbox-group">
                    <input type="checkbox" id="initial_tribute" name="initial_tribute" required>
                    <label for="initial_tribute">I understand an initial tribute is required for consideration <span class="required">*</span></label>
                </div>
                
                <div class="checkbox-group">
                    <input type="checkbox" id="privacy" name="privacy">
                    <label for="privacy">I consent to anonymized data collection for vetting purposes</label>
                </div>
            </div>
            
            <button type="submit">Submit Application</button>
            
            <p class="disclaimer">
                By submitting this form, you acknowledge that financial domination involves consensual exchange of power and money. 
                All interactions require mutual consent. No refunds on tributes. This is fantasy/entertainment.
            </p>
        </form>
        
        <div id="successMsg" class="success-message">
            Application received. If approved, you will be contacted within 24-48 hours. Initial tribute instructions will follow.
        </div>
    </div>
    
    <script>
        document.getElementById('subApplication').addEventListener('submit', function(e) {
            // For demonstration - remove this if using Formspree or similar
            // e.preventDefault();
            // document.getElementById('successMsg').style.display = 'block';
            // this.reset();
            
            // Uncomment below for Formspree integration
            /*
            fetch(this.action, {
                method: 'POST',
                body: new FormData(this),
                headers: {
                    'Accept': 'application/json'
                }
            }).then(response => {
                if (response.ok) {
                    document.getElementById('successMsg').style.display = 'block';
                    this.reset();
                }
            });
            */
        });
    </script>
</body>
</html>
