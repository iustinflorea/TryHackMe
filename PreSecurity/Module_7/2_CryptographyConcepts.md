
Learning Objectives
By the end of this room, you'll be able to:

Explain what cryptography is and why it matters for protecting confidentiality and integrity.
Describe the difference between plaintext and ciphertext with actual examples.
Explain what keys and algorithms are, and why keeping keys secret is critical.
Explain the difference between symmetric and asymmetric encryption using everyday objects, such as lockboxes and mailboxes.
Describe how symmetric and asymmetric encryption work together to protect your web browsing.

What We've Covered
In this room, we explored the basics of cryptography and its role in protecting confidentiality—one of the three pillars of the CIA Triad. We covered the core ideas:

Plaintext is what you can read. Ciphertext is scrambled gibberish.
A key is the secret that controls scrambling and unscrambling.
An algorithm is the public method for using the key.
We looked at two flavours of encryption:

Symmetric encryption uses a single key for both encryption and decryption. It's fast and efficient, but you need a secure way to share that key. We used the Caesar cipher to see how this works.
Asymmetric encryption uses two linked keys: a public key that anyone can use and a private key that only one person keeps. This solves the key distribution problem and powers the initial handshake for HTTPS connections.
We also saw how real systems combine both types:

Asymmetric encryption sets up a shared key at the start.
Symmetric encryption handles the actual data because it's faster.
That combo is what protects your passwords, banking details, and messages when you see that padlock in your browser.

Cryptography is one of the most critical tools in a defender's arsenal. It protects confidentiality and integrity, and it's the backbone of almost every secure system you use online. But it's not magic. It's one layer in a much bigger security picture that includes:

Strong password practices.
Secure key storage.
User awareness and training.
Regular software updates.
Monitoring and incident response.
Understanding how crypto works and where it can fail helps you think more carefully about those other layers.
