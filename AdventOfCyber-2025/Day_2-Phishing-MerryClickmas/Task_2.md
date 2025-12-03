# **Task 2 — Phishing Simulation (Clear & Concise Guide)**


---

## 🔗 **Room Link**

**TryHackMe:** [https://tryhackme.com/room/phishing-aoc2025-h2tkye9fzU](https://tryhackme.com/room/phishing-aoc2025-h2tkye9fzU)

---

# **1. Starting the Phishing Server**

Run the phishing script:

```
./server.py
```

* The server starts on **port 8000**.
* It listens on **0.0.0.0** → all network interfaces.

### ✅ Preview What the Victim Sees

Open Firefox inside AttackBox:

* `http://CONNECTION_IP:8000`
* or `http://127.0.0.1:8000`

This shows exactly what the target will see.

---

# **2. Using the Social-Engineer Toolkit (SET)**

SET allows composing and sending phishing emails.
Launch it:

```
setoolkit
```

Select:

First, **Social-Engineering Attacks**
then, in that  **Mass Mailer Attack**

Use **99** anytime to return to the main menu.
Use **Ctrl + C** if you make a mistake while typing email content.

---

# **3. Configuring the Phishing Email**

Answer the prompts as follows:

### **📧 Email Delivery Settings**

* **Send email to:** `factory@wareville.thm`
* **Delivery method:** *Use your own server or open relay*
* **From address:** `updates@flyingdeer.thm`
* **From name:** *Flying Deer*
* **Username:** *(leave blank)*
* **Password:** *(leave blank)*
* **SMTP server:** `MACHINE_IP`
* **Port:** `25`

### **📎 Email Options**

* **High priority:** no
* **Attach a file:** n
* **Attach inline file:** n

### **✉️ Email Content**

* **Subject:** `Shipping Schedule Changes`
* **Format:** plaintext
* **Body:** Write a convincing message and include:

  * `http://CONNECTION_IP:8000`
* End input with: `END`

The phishing email is now sent.

---

# **4. Monitoring for Captured Credentials**

Watch the terminal where `server.py` is running.

* Credentials appear here if the user falls for the phishing page.
* May take **1–2 minutes**.

---

# **5. Answers**

### **Q.1] :** I have successfully started the AttackBox and the target machine!

➡️ **No answer needed**


### **Q.2] :** Password used to access TBFC portal

➡️ **unranked-wisdom-anthem**

### **Q.3] :** Total number of toys expected

➡️ **1984000**

### **Q.4] :** If you enjoyed today's room, feel free to check out the Phishing Prevention room.

➡️ **No answer needed**

---


