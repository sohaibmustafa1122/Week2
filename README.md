# Week2
SecurityEngineering-2023-security-engineering-submissions-sohaibmustafa1122-Week2

## Task 1A: Browsers and Banking Security

### 1. What does the "Not Secure" warning mean in the first picture, and what risks does visiting sites with the warning pose?
The "Not Secure" warning indicates that the website does not use HTTPS, meaning the connection is unencrypted. Visiting such a site poses significant risks, as any data entered, such as passwords or personal details, could be intercepted by attackers. This opens the user to phishing attempts, data theft, and unauthorized access to sensitive information.

### 2. Why does the second site show up as "trusted" to the browser?
The second site is marked as "trusted" because it uses HTTPS, which ensures that the communication between the browser and the server is encrypted. Additionally, the browser verifies the security certificate of the website, indicating that it is authentic and safe to visit. This helps in reducing risks related to data interception and identity theft.

### 3. What other ways are there to detect a phishing/scam site? Are there any tools available online?
Phishing sites often have spelling errors, unusual domain names, or request personal information. To detect scam sites, users can utilize online tools such as Google Safe Browsing, PhishTank, and VirusTotal. These tools scan websites for potential threats and provide warnings if a site is suspected to be a phishing attempt.

### 4. What is typosquatting, and how does it relate to the pictures?
Typosquatting is a technique where attackers register domain names that closely resemble legitimate ones, hoping to exploit users who make typing errors. In the images, the second domain (danskebank.io) is an example of typosquatting. Although it looks similar to the real website, it uses a different top-level domain (".io" instead of ".fi"), potentially misleading users into thinking it's the official site.

### 5. What is UDRP, and how does it help with combating typosquatting?
The Uniform Domain-Name Dispute-Resolution Policy (UDRP) helps resolve disputes over domain names, especially in cases of typosquatting. It allows legitimate brand or domain owners to claim rights over similar domain names that are used in bad faith, helping to protect their brand and prevent attackers from using misleading domains to scam users.

### 6. If you were to own the domain ouspg.org and would be running your crypto banking application at bank.ouspg.org, what domains could you monitor for warning signs of possible phishing attempts against your customers?
To safeguard your crypto banking application at bank.ouspg.org, it’s important to monitor similar domains that could be exploited for phishing, such as bank0uspg.org (using "0" instead of "o"), bank-ouspg.org (with a dash), ouspgbank.org (swapping word order), or bankouspg.com (different domain extension). Monitoring these potential phishing domains will help in protecting your customers from scams.


## Task 1B: Certificates

### 1. What are digital certificates used for?
Digital certificates are used to verify the identity of websites and ensure secure communication between a browser and a website. They are critical for online payments and banking security as they encrypt sensitive data such as credit card details, protecting it from attackers. Certificates also have other uses, such as securing emails, authenticating servers, and ensuring the integrity of software updates.

### 2. What kind of attacks does TLS mitigate and why is this important for online banking?
TLS (Transport Layer Security) mitigates attacks like **man-in-the-middle (MITM)**, where attackers intercept and alter communication between a user and a website. It also protects against eavesdropping, where attackers try to steal sensitive data. For online banking, TLS is essential because it ensures that personal and financial information is encrypted and protected from being accessed by unauthorized parties.

### 3. How do browsers use certificates for ensuring browsing security? What does the warning in the picture above mean?
Browsers use digital certificates to confirm the legitimacy of a website. When a website’s certificate is valid, the browser establishes an encrypted connection (HTTPS). If the certificate is invalid, expired, or mismatched (as shown in the warning), the browser alerts the user that the connection is not private, meaning attackers could potentially steal sensitive information.

### 4. Why would it be bad if a trusted certificate authority was compromised?
If a trusted certificate authority (CA) was compromised, attackers could issue fake certificates for websites, making it look like users were visiting legitimate sites when, in fact, they were on phishing sites. This could lead to widespread data breaches and loss of trust in the entire web security infrastructure.

### 5. Why is certificate transparency important?
Certificate transparency is important because it helps detect and prevent the issuance of fraudulent or unauthorized certificates. By maintaining an open log of all certificates issued, it allows companies and users to verify that no illegitimate certificates have been issued for their domains, adding an additional layer of security against certificate authority compromise.


## Task 2: Cards and Payments

### 1. Why do modern payment cards use a chip and not a magnetic stripe?
Modern payment cards use a chip because it provides enhanced security compared to the older magnetic stripe. The chip generates a unique code for each transaction, making it harder for attackers to clone the card or steal information. In contrast, magnetic stripes store static data that can easily be copied or skimmed by criminals.

### 2. What are EMV Certificates and why are they relevant for payment protection?
EMV Certificates are a type of security standard used in chip-enabled cards. They authenticate the cardholder and encrypt transaction data, ensuring that the information exchanged during payment cannot be easily intercepted or altered. EMV technology is crucial for protecting payments, especially against fraud and counterfeiting, by making it significantly more difficult for attackers to duplicate cards.

### 3. What attacks exist against payment cards?
- **Card-not-present**: This attack happens when a transaction is made online or over the phone, where the card is not physically present. Fraudsters can steal card details and use them without needing the actual card.
- **Contactless payment**: In this attack, criminals may exploit vulnerabilities in contactless cards by using unauthorized scanners to read payment information from nearby users, although such attacks are relatively rare due to security layers built into contactless systems.

---

## Questions: MFA

### 4. How is multi-factor authentication (MFA) used in banking?
MFA in banking is used to add extra layers of security beyond just a password. Typically, it requires the user to provide two or more verification factors, such as a password (something they know) and a one-time passcode sent to their phone (something they have). This ensures that even if one factor is compromised, unauthorized access is still prevented.

### 5. How does multi-factor authentication increase payment security?
MFA enhances payment security by making it much harder for attackers to gain access to accounts. Even if they steal the user's password, they still need to bypass the second or third authentication factor, such as a time-sensitive code or biometric verification, which makes unauthorized transactions far less likely.

### 6. What MFA methods are you using in your daily life?
Common MFA methods include time-based one-time passwords (TOTP) through apps like Google Authenticator, SMS-based codes, or biometric options like fingerprint or facial recognition on mobile devices.

### 7. What attacks exist against different forms of 2FA?
- **Time-based-one-time-password (TOTP)**: Attackers may exploit weaknesses by tricking users into sharing their one-time codes via phishing.
- **Text Message (SMS)**: Attackers could use **SIM swapping** or intercept SMS messages to gain access to accounts. This is less secure than app-based or biometric factors.

## Task 3: Card Fraud

### Summary on the Evolution of Card Fraud (2008-2019)

The evolution of card fraud between 2008 and 2019 has shown significant changes, mainly driven by advancements in technology and the rise of online transactions. Card fraud comes in various forms, with the most common being card-present fraud and card-not-present (CNP) fraud. Card-present fraud occurs when the physical card is used during a transaction, and fraudsters use techniques like skimming to steal information. On the other hand, CNP fraud involves transactions made online or over the phone, where the cardholder's physical card is not required. This type of fraud has become more prevalent as online shopping and digital payments have grown.
 Geographically, the prevalence of different types of fraud varies. In regions where EMV chip technology was quickly adopted, such as in Europe, card-present fraud has decreased significantly. EMV chips make it difficult for criminals to clone cards, as the chip generates a unique code for each transaction, unlike magnetic stripes that store static data. However, the decrease in card-present fraud has led to a rise in CNP fraud, especially in areas where e-commerce is booming. Countries with less robust online security measures or slower adoption of EMV technology tend to face more significant challenges with fraud.
 The period between 2008 and 2019 saw substantial changes in the fraud landscape. One of the most notable trends was the sharp increase in CNP fraud. As more consumers shifted to online shopping and businesses expanded their digital platforms, fraudsters also adapted, finding new ways to exploit the weaknesses in online payment systems. The increase in CNP fraud is due to the fact that these transactions are more vulnerable. Without the need for a physical card, fraudsters can use stolen card details more easily. During this period, card-present fraud decreased significantly, thanks to the widespread adoption of EMV technology, which made it more challenging for criminals to clone physical cards.
 Several technologies and regulations have played a crucial role in shaping the fraud landscape. The introduction of EMV chips has had a significant impact, particularly in reducing card-present fraud. EMV cards use advanced encryption and generate a unique transaction code, making it much harder for fraudsters to create fake cards. In addition to EMV technology, regulations like the Revised Payment Services Directive (PSD2) in the European Union have been instrumental in combating fraud. PSD2 introduced Strong Customer Authentication (SCA), which requires multiple layers of verification for online payments, such as passwords, biometric authentication, or one-time passcodes. This regulation was designed to improve security for online payments and has been effective in reducing CNP fraud in regions where it was implemented.
 The way people conduct transactions also changed dramatically during this period. One significant shift was the increasing popularity of contactless payments. Contactless cards, which allow users to make payments by simply tapping their card on a reader, became widely adopted due to their convenience. However, this also opened the door for new types of fraud, such as unauthorized contactless transactions. Fortunately, limits on transaction amounts and security monitoring have kept this type of fraud relatively low compared to CNP fraud.

Transactions involving CNP, especially e-commerce purchases, have consistently had a higher risk of fraud throughout 2008-2019. Fraudsters can steal card details through phishing, data breaches, or other means and use them for online purchases, often without needing any additional authentication. While the introduction of EMV chips helped reduce card-present fraud, CNP fraud continued to grow, particularly in countries with high rates of online shopping. Fraud prevention methods like tokenization, where sensitive card information is replaced with a unique identifier or "token," have helped mitigate some of the risks in CNP transactions. Tokenization adds an extra layer of security by ensuring that even if transaction data is intercepted, the stolen information is useless to attackers without the token.
 The growth of the internet and the explosion of e-commerce has been a major factor in the evolution of card fraud. As more people shop online, fraudsters have shifted their focus to exploiting weaknesses in digital payment systems. Internet-based transactions are inherently more vulnerable because they rely on less secure verification methods compared to in-person payments. However, technologies like biometric authentication and the aforementioned tokenization are being implemented to improve security in online transactions.
 Preventing data breaches has become crucial in the fight against card fraud. When a company suffers a data breach, millions of card details can be exposed, leading to a sharp rise in fraud. One way to prevent this is through card tokenization, which helps ensure that even if hackers access transaction data, they cannot use it to commit fraud. Tokenization replaces sensitive card details with a unique token that is only usable by the authorized parties involved in the transaction, making it useless to anyone else.
 Hence, between 2008 and 2019, the card fraud landscape has shifted significantly, with card-present fraud declining due to the introduction of EMV technology, while CNP fraud has risen sharply alongside the growth of e-commerce. Regulatory measures like PSD2 and technologies like tokenization and biometric authentication have played key roles in mitigating these risks, but the continued evolution of digital payments means that the battle against fraud is ongoing. The challenge remains to stay ahead of fraudsters in an increasingly interconnected world.
