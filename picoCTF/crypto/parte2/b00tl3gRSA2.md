## Objetivo
In RSA d is a lot bigger than e, why don't we use d to encrypt instead of e? Connect with `nc jupiter.challenges.picoctf.org 18243`.
## Solución

si d es pequeña podemos hacer un ataque de Wiener
se puede usar la herramienta RsaCtfTool

```
(kali㉿kali)-[~/Desktop/pico/RsaCtfTool]
└─$ ./RsaCtfTool.py --createpub -e 5108002799648714669178447603410963837284100111817816822266242929304175238309941115628431697977491061615482685728645634433296220836798499899251471759582291556875421016456842604253163339017970525524065447341953013378164558390511391481170550541433866524086395521569701293777632248125807850029498437164107086705 -n 47598916462473739979233317301968482440507332436826995745892615222210682865508120417309900211908265563073210404464417594746898112467121184117338789237557903996971486319249984379210057578996126923872376977198473732992361924191302346825586847807350587666622424457978084494309770283503119688336998401799020166993 > ~/Desktop/pico/key.pub

(kali㉿kali)-[~/Desktop/pico/RsaCtfTool]
└─$ c=23742443802836507345791144542157091509297212031594659443954955727180617776398853317201982638589614344153528982497011885293269675495944342414480456646213013352483523828397923860911018400697773438904362052292301105014344549199034304662396551096931640130251323084280297536000198480967729690206994949714723461700


─(kali㉿kali)-[~/Desktop/pico/RsaCtfTool]
└─$ echo "obase=16; $c" | BC_LINE_LENGTH=0 bc | awk '{ print (length($0) % 2 == 0) ? $0 : 0$0; }' | xxd -p -r > c.bin
                                                                                                                                                                       
┌──(kali㉿kali)-[~/Desktop/pico/RsaCtfTool]
└─$ xxd -g 1 c.bin
00000000: 21 cf 73 e6 cc 45 c8 63 fa 09 a8 47 18 68 ce e5  !.s..E.c...G.h..
00000010: f0 f2 39 2a db 55 36 21 ef cb 09 45 b1 f5 7b 94  ..9*.U6!...E..{.
00000020: 54 dc 91 44 3a 4d 5a 57 c0 ff 2a 0e e9 b2 07 00  T..D:MZW..*.....
00000030: bb fe d9 ac 35 58 5a ae 29 d5 65 f8 64 17 5b be  ....5XZ.).e.d.[.
00000040: dc 92 31 f1 98 f0 d8 9a f1 da a7 aa 0f 3a 0d c1  ..1..........:..
00000050: 39 94 df eb cc 88 f9 09 87 09 ff 25 bd 11 28 68  9..........%..(h
00000060: 33 b6 d4 54 7e 30 49 59 0e 7c 1f 6d cb 0d 46 96  3..T~0IY.|.m..F.
00000070: 5d b5 c3 6d d4 0e 51 62 ef 1e 41 15 0a 2f da 44  ]..m..Qb..A../.D



┌──(kali㉿kali)-[~/Desktop/pico/RsaCtfTool]
└─$ ./RsaCtfTool.py --publickey ../key.pub  --decryptfile c.bin 

private argument is not set, the private key will not be displayed, even if recovered.
['../key.pub']

[*] Testing key ../key.pub.
attack initialized...
attack initialized...
[*] Performing lucas_gcd attack on ../key.pub.
100%|███████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████| 9999/9999 [00:00<00:00, 87552.81it/s]
[+] Time elapsed: 0.1286 sec.
[*] Performing mersenne_primes attack on ../key.pub.
 27%|██████████████████████████████████▌                                                                                           | 14/51 [00:00<00:00, 319131.83it/s]
[+] Time elapsed: 0.0006 sec.
[*] Performing smallq attack on ../key.pub.
[+] Time elapsed: 0.2869 sec.
[*] Performing rapid7primes attack on ../key.pub.
[+] loading prime list file data/ea229f977fb51000.pkl.bz2...
loading pickle data/ea229f977fb51000.pkl.bz2...
100%|███████████████████████████████████████████████████████████████████████████████████████████████████████████████████████| 61174/61174 [00:00<00:00, 1421075.87it/s]
[+] loading prime list file data/fbcc4333b5f183fc.pkl.bz2...
loading pickle data/fbcc4333b5f183fc.pkl.bz2...
100%|███████████████████████████████████████████████████████████████████████████████████████████████████████████████████████| 21048/21048 [00:00<00:00, 1438164.22it/s]
[+] Time elapsed: 0.5005 sec.
[*] Performing nonRSA attack on ../key.pub.
[+] Time elapsed: 0.0016 sec.
[*] Performing factordb attack on ../key.pub.
[!] Composite not in factordb, couldn't factorize...
[+] Time elapsed: 0.6316 sec.
[*] Performing system_primes_gcd attack on ../key.pub.
100%|██████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████| 7007/7007 [00:00<00:00, 515713.63it/s]
[+] Time elapsed: 0.0382 sec.
[*] Performing fibonacci_gcd attack on ../key.pub.
100%|███████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████| 9999/9999 [00:00<00:00, 84473.23it/s]
[+] Time elapsed: 0.1194 sec.
[*] Performing pastctfprimes attack on ../key.pub.
[+] loading prime list file data/pastctfprimes.txt...
100%|████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████| 121/121 [00:00<00:00, 970383.91it/s]
[+] loading prime list file data/visa_emv.txt...
100%|█████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████| 2/2 [00:00<00:00, 69327.34it/s]
[+] loading prime list file data/ti_rsa_signing_keys.txt...
100%|██████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████| 34/34 [00:00<00:00, 792257.42it/s]
[+] Time elapsed: 0.0121 sec.
[*] Performing cube_root attack on ../key.pub.
[+] Time elapsed: 0.0001 sec.
[*] Performing factor_2PN attack on ../key.pub.
[+] Time elapsed: 0.0002 sec.
[*] Performing pollard_p_1 attack on ../key.pub.
  6%|████████▏                                                                                                                        | 63/997 [00:59<14:20,  1.08it/s][!] Timeout.                                                                                                                                                           
  6%|████████▏                                                                                                                        | 63/997 [01:00<14:49,  1.05it/s]
[+] Time elapsed: 60.0093 sec.
[*] Performing small_crt_exp attack on ../key.pub.
Can't load small_crt_exp because sage binary is not installed
[*] Performing primorial_pm1_gcd attack on ../key.pub.
100%|█████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████| 10000/10000 [00:00<00:00, 10932.12it/s]
[+] Time elapsed: 0.9157 sec.
[*] Performing noveltyprimes attack on ../key.pub.
100%|██████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████| 21/21 [00:00<00:00, 444850.42it/s]
[+] Time elapsed: 0.0005 sec.
[*] Performing partial_q attack on ../key.pub.
[!] partial_q attack is only for partial private keys not pubkeys...
[+] Time elapsed: 0.0003 sec.
[*] Performing wiener attack on ../key.pub.
  4%|████▌                                                                                                                        | 12/326 [00:00<00:00, 102092.59it/s]
[*] Attack success with wiener method !
[+] Total time elapsed min,max,avg: 0.0001/60.0093/4.1764 sec.

Results for ../key.pub:

Decrypted data :
HEX : 0x0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000007069636f4354467b6261645f31643361355f343738333235327d
INT (big endian) : 180638594769037903267909311328535969949661653466129492033745533
INT (little endian) : 87915708203145282610294972968911366155903715376253613591493747328997039762324724152737381588249902516221925909575347268323406342359083908236607141716518709062203918941441530400517793579352373597960230114723867721326316384129937388432851450794910176330916868853347433852177960598981938565164199179134034771968
utf-8 : picoCTF{bad_1d3a5_4783252}




```
## Notas adicionales

## Referencias

