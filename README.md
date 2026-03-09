# Prank Malware Simulator (Educational Demo)

A small collection of **harmless malware-style simulations** written in Python.
This project was created as a **learning experiment** to explore GUI programming, Windows system interaction, scheduling tasks, and how certain malware behaviors are commonly demonstrated in security training.

The programs in this repository **simulate the appearance of malware**, such as flashing screens, fake alerts, or ransomware-style messages, but they are intended **only for educational demonstrations and entertainment**.

---

# ⚠️ Important Disclaimer

This repository is **not real malware** and is published strictly for educational and demonstration purposes.

However, some demos may imitate behaviors seen in malware such as:

* fullscreen prank messages
* fake ransomware screens
* startup persistence demonstrations

These programs **must only be run on your own system or in a controlled testing environment**.

Do **not run these programs on computers that contain important data**.

---

# Included Demos

## Flash Screen Demo

A GUI program that rapidly changes colors and displays prank-style messages to simulate a disruptive screen takeover.

Purpose:

* Demonstrate basic GUI manipulation
* Show how prank-style visual effects work

---

## Persistence Demo

A demonstration of how programs can register themselves to run at system startup using the Windows startup registry.

The demo periodically shows a small notification window indicating that persistence has been detected.

Purpose:

* Demonstrate how startup persistence mechanisms work
* Help beginners understand how such behavior is detected and removed

---

## Fake Ransomware Simulation

This demo **simulates ransomware behavior** for educational purposes.

Important notes:

* It may temporarily encrypt or modify files **inside a test directory**
* It **does not spread** and **does not access the internet**
* The encryption used in the demo is reversible
* Removing the program restores access to the files

⚠️ **Do not run this demo on folders containing important data.**

This demo is intended only to illustrate how ransomware-style programs appear during security demonstrations.

---

# Requirements

* Python 3.9+
* Windows operating system

Install dependencies:

```bash
pip install schedule
```

---

# Running a Demo

Clone the repository:

```bash
git clone https://github.com/yourusername/prank-malware-simulator.git
cd prank-malware-simulator
```

Run one of the demos:

```bash
python flash_demo.py
```

or

```bash
python persistence_demo.py
```

or

```bash
python fake_ransomware_demo.py
```

---

# Removing Startup Persistence

If the persistence demo was executed, it may create a startup registry entry:

```
HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Run
```

with the name:

```
PentestDemo
```

To remove it:

1. Press **Win + R**
2. Type `regedit`
3. Navigate to the path above
4. Delete the entry named **PentestDemo**

---

# Safety

These programs are designed to be **non-destructive**, but they should still be treated as experimental code.

Best practices:

* Run in a **virtual machine** or test environment
* Avoid running on systems with important data
* Always review the code before execution

---

# License

This project is released under the **MIT License**.

You are free to study, modify, and experiment with the code for educational purposes.
