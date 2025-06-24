# Alfido-tech-task-3


# 🔐 Task 3: Password Cracking with John the Ripper / Hashcat

This project demonstrates password cracking using brute-force attacks on password hashes with tools like **John the Ripper** and **Hashcat** as part of a cybersecurity learning module.

## Project Structure

├── hashes.txt # Sample password hashes
├── wordlist.txt # Wordlist for dictionary attacks
├── crack_john.sh # Shell script to crack with John the Ripper
├── crack_hashcat.sh # Shell script to crack with Hashcat
└── README.md # Project documentation


---

##  Tools Used

- [John the Ripper](https://www.openwall.com/john/)
- [Hashcat](https://hashcat.net/hashcat/)
- Kali Linux or any Linux-based environment

---

##  Requirements

- A system with Linux (Kali preferred)
- John the Ripper installed (`sudo apt install john`)
- Hashcat installed (`sudo apt install hashcat`)
- A password hash file (`hashes.txt`)
- A wordlist (`/usr/share/wordlists/rockyou.txt` or custom)

---

## How to Use

### With John the Ripper

1. Prepare your hash file (`hashes.txt`)
2. Run the command:
   ```bash
   john --wordlist=wordlist.txt hashes.txt

    To show cracked passwords:

    john --show hashes.txt

⚡ With Hashcat

    Identify the hash mode (e.g., 0 for MD5, 1000 for NTLM)

    Run the command:

hashcat -m 0 -a 0 hashes.txt wordlist.txt

Check cracked passwords:

    hashcat -m 0 -a 0 hashes.txt wordlist.txt --show

🔍 Supported Hash Types

Common hash types supported in this task:

    MD5

    SHA1

    NTLM

    bcrypt (with limitations)

You can use hashid or hash-identifier to determine the type:

hashid <hash>

⚠️ Disclaimer

    This project is for educational and ethical hacking purposes only. Do not use these tools on unauthorized systems or data.

📚 References

    John the Ripper Documentation

    Hashcat Wiki

    Kali Linux Tools List

