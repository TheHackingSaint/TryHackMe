# **Task 2 — Phishing Attack Walkthrough (Clear, Concise & GitHub-Ready)**

Room Link: *TryHackMe — Phishing (AOC 2025)*

---

# 🚀 **Overview**

This task demonstrates how a phishing attack is executed using a custom phishing server and the Social-Engineer Toolkit (SET). The goal is to:

* Host a phishing page
* Capture credentials
* Craft & send a phishing email
* Lure the target into interacting with the malicious link

Everything below is intentionally **short, visual, and extremely easy to remember.**

---

# 🎯 **1. Start the Phishing Server**

Run the Python phishing server:

```
./server.py
```

This:

* Starts listening on **port 8000**
* Binds to **0.0.0.0 (all interfaces)**
* Displays **captured credentials directly in the same terminal**

### ✔ Preview the phishing page

Open Firefox on the AttackBox:

* `http://CONNECTION_IP:8000`
* or `http://127.0.0.1:8000`

This shows **exactly what the victim will see**.

---

# ✉️ **2. Social-Engineer Toolkit (SET)**

SET is a powerful framework for creating and sending phishing attacks.
Start it with:

```
setoolkit
```

You will see a menu ending with `set>`.

---

# 🛠 **3. SET Menu Navigation (Quick Path)**

```
1 → Social-Engineering Attacks
5 → Mass Mailer Attack
```

If you select a wrong option:

* `99` = return to main menu
* `Ctrl + C` = abort email creation

---

# 📬 **4. Configure the Phishing Email**

Answer the prompts in SET:

| Field              | Input                            |
| ------------------ | -------------------------------- |
| **Send email to**  | `factory@wareville.thm`          |
| **How to deliver** | Use your own server / open relay |
| **From address**   | `updates@flyingdeer.thm`         |
| **From name**      | `Flying Deer`                    |
| **SMTP server**    | `MACHINE_IP`                     |
| **Port**           | `25`                             |

Leave username/password blank.

### Optional choices

* High priority → **no**
* Attach a file → **n**
* Inline file → **n**

### Email details

* **Subject:** `Shipping Schedule Changes`
* **Format:** Plaintext (press Enter)
* **Body:** Write a believable message and include:

  * `http://CONNECTION_IP:8000`

Type `END` when finished.

---

# 🕵️ **5. Monitor Credential Capture**

Return to the terminal where `server.py` is running.

* If the victim logs in → **Credentials appear instantly**
* Wait **1–2 minutes** if needed

---

# ✅ **Task Questions & Answers**

### **Q2. Password used to access the TBFC portal**

**→ unranked-wisdom-anthem**

### **Q3. Total number of toys expected for delivery**

Browse to: `http://MACHINE_IP` → Login → Check mailbox

**→ 1,984,000**

---

# 🎉 **End of Task**

You can explore further by completing the "Phishing Prevention" room on TryHackMe.

---

Need this format for future tasks too? I can generate a reusable prompt template for you.
