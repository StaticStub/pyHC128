![Alt text](https://autumn.revolt.chat/attachments/wS_r8tQoSBbBgZxEVd7z-pIgquQahbZ59QjSNLRF6j/01.jpg)

### Description

The `HC128` class is a Python implementation of the HC-128 stream cipher. It provides methods for encrypting and decrypting data using the HC-128 algorithm.

### Installation

To use the `HC128` class in your own Python code, simply install it using pip:

```
$ pip install hc128
```

### Usage
Constructor

The constructor takes two arguments: key and iv. The key argument should be a bytes object containing the encryption key, and the iv argument should be a bytes object containing the initialization vector.

```
cipher = HC128(key, iv)
```

### set_iv Method

The set_iv method allows you to change the initialization vector after the HC128 object has been created. This can be useful if you want to reuse the same key but encrypt different messages with different IVs.

```
cipher.set_iv(iv)
```

### encrypt and decrypt Methods

The encrypt and decrypt methods use the keystream generated by the HC128 object to encrypt or decrypt a given message.

```
encrypted_data = cipher.encrypt(data)
decrypted_data = cipher.decrypt(encrypted_data)
```

### generate_keystream_bytes Method

The generate_keystream_bytes method generates a sequence of keystream bytes by repeatedly calling the generate_keystream_byte method.

```
keystream_bytes = cipher.generate_keystream_bytes(nbytes)
```

### Example

Here's an example of how to use the HC128 class to encrypt and decrypt a message:

```
from hc128 import HC128

key = b'\x00' * 16
iv = b'\x00' * 16
data = b'This is a secret message.'

cipher = HC128(key, iv)
encrypted_data = cipher.encrypt(data)
decrypted_data = cipher.decrypt(encrypted_data)

assert decrypted_data == data
```

License

This project is licensed under the MIT License - see the LICENSE file for details.

> If you found this implementation helpful, please consider giving it a ⭐️ on GitHub.
Feel free to open an issue or pull request if you have any questions or suggestions.

![Alt text](https://autumn.revolt.chat/attachments/nlpdp4r6IBfvhz9-wHkj1_JrIVkl40E81kumNQ_Euh/02.jpg)

