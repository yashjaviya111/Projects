# Password Strength Creation and Evaluation

## 📝 Objective
To understand the characteristics of strong passwords, evaluate their strength using online tools, and explore techniques and best practices for secure password creation and protection.

## 🛠️ Tools Used

- **Online Password Strength Checkers**
  - [Password Meter](https://www.passwordmeter.com/)
  - [Password Monster](http://passwordmonster.com/)

## 🔍 Passwords Tested

| S.No | Password                  | Complexity Level | Score | Strength Category | Notes                                          |
|------|---------------------------|------------------|-------|-------------------|------------------------------------------------|
| 1    | password123               | Weak             | 25%   | Weak              | Common, easily guessable                      |
| 2    | P@ssw0rd!                 | Medium           | 65%   | Moderate          | Better with special characters                |
| 3    | MyDog$Is@Brave2024        | Strong           | 90%   | Strong            | Passphrase-style with symbols & numbers       |
| 4    | 123456                    | Very Weak        | 10%   | Very Weak         | Extremely common                              |
| 5    | L#9d$gT@3hV!u@7% (Random) | Very Strong      | 100%  | Very Strong       | High entropy and unpredictability             |

## 📘 Key Learnings

- **Length matters** – Longer passwords are harder to crack.
- **Character diversity** – Mix upper/lowercase, digits, and symbols.
- **Avoid predictable patterns** – e.g., “123456”, “password”.
- **Use passphrases** – More secure and easier to remember.
- **Avoid repetition** – Makes passwords more vulnerable.

## 🛡️ Common Password Attacks

| Type              | Description                                                                 |
|-------------------|-----------------------------------------------------------------------------|
| **Brute Force**   | Tries every combination until the right one is found.                        |
| **Dictionary**    | Uses a list of common passwords.                                             |
| **Credential Stuffing** | Reuses leaked credentials across platforms.                         |
| **Phishing**      | Tricks users into giving credentials via fake sites/messages.                |

## 🧠 Password Attack Insights

### Brute Force
- **Tools**: Hydra, John the Ripper
- **Targets**: SSH, FTP, login forms
- **Prevention**: MFA, rate-limiting, CAPTCHA

### Dictionary Attack
- **Tools**: John the Ripper, Hashcat, CeWL
- **Prevention**: Strong password policies, block common passwords

### Credential Stuffing
- **Tools**: Sentry MBA, Snipr
- **Prevention**: MFA, bot detection, dark web monitoring

### Phishing
- **Tools**: Evilginx2, Gophish, King Phisher
- **Prevention**: User awareness, email filtering, phishing-resistant MFA

## 🔐 Tips for Strong Passwords

1. Use 12–16+ characters.
2. Combine upper/lowercase, digits, and symbols.
3. Avoid personal info (names, DOB).
4. Prefer passphrases (e.g., `Sky@Is$Blue!23`).
5. Don’t reuse passwords.
6. Use a password manager.

## 🔒 Multi-Factor Authentication (MFA)

### What is MFA?
Authentication using two or more of the following:
- **Something You Know** – Password, PIN
- **Something You Have** – OTP device, Authenticator app
- **Something You Are** – Biometrics (fingerprint, face)

### Common Methods
- **TOTP Apps**: Google Authenticator, Authy
- **Push Notifications**: Duo, Okta
- **Hardware Tokens**: YubiKey
- **Biometrics**: Face ID, fingerprint

### Benefits
- Prevents credential stuffing
- Stronger than passwords alone
- Required for compliance (e.g., GDPR, HIPAA)

### Caution
- Avoid SMS OTPs (susceptible to SIM swapping)
- Prefer phishing-resistant methods (FIDO2/WebAuthn)

## ✅ Best Practices

- Don’t rely solely on passwords—use MFA.
- Avoid SMS for MFA on critical accounts.
- Use app-based or hardware token MFA.
- Backup recovery codes.
- Watch out for fake MFA prompts.

## 🎯 Outcome

- Understood how password complexity affects strength.
- Learned tools to measure password quality.
- Explored real-world attacker methods.
- Established strong password and MFA practices.

## Author
**Yash Javiya**  
