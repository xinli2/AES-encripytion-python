# AES-encripytion-python

The DES encryption algorithm can be developed into a 3DES encryption algorithm, and later upgraded to an AES encryption algorithm, which increases the length of the key and increases the difficulty of brute force cracking.
This time, Python is used to encrypt and decrypt AES, and it is performed under ubuntu:

<!-- wp:paragraph -->
<p>First， we need to install python and pip:</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>#sudo apt-get install python
#sudo apt-get install python-pip</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Then install</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>#pip install Ctypto
#pip install binascii</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>AES has many modes, and this time the CBC mode is adopted: the key and the salt (for scramble) are used to generate the key and iv according to a fixed algorithm (md5). then use key and<br>iv (initial vector, encrypted first block of plaintext) Encrypt (plaintext) and decrypt (ciphertext).<br>The idea of the following code implementation: encrypt the encrypted text in units of 8*16 bits, and encrypt each 16-byte data into 16-byte ciphertext.<br>In the following code, in order to simplify the code, the key and iv generated by the key are replaced with 16-bit keys. In fact, they can be different, but whether the number of digits can be different, I will<br>Did not try.</p>
<!-- /wp:paragraph -->
