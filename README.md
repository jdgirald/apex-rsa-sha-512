# RSA-SHA512 in Apex

<img src="https://bigassforce.com/wp-content/uploads/rsa-sha-512-small-num.png" />

<ol>
  <li>Our <strong>private key file</strong> holds secret prime numbers</li>
  <li>An <strong>ASN key reader</strong> handles the binary file format</li>
  <li>The <strong>message to sign</strong> consists of a JSON Web Token</li>
  <li>A <strong>SHA512 hash</strong> reduces the message to a big integer</li>
  <li>Finally the <strong>RSA signer</strong> executes the modPow signature math</li>
</ol>

## Usage:

```
Blob signature = CryptoRsaSha512.sign(message, privateKey);
```
