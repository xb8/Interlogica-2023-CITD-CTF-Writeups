# CRYPTO CHALLENGES:

### CRYPTO: Intercepted Message
Caesar cipher where the n of rot(n) increments by 1 each character position


### CRYPTO: Espionage
Scytale every 3 characters (example: https://dencode.com/en/cipher/scytale)


### CRYPTO: Space
You can bruteforce the dates until you find the correct one to retrieve the secret key. 
Example code:
```
import hashlib

def md5(msg:str)->str:
    return hashlib.md5(msg.encode()).hexdigest()

def xor(data:str,key:str) -> str:    
    return ''.join(chr(ord(a) ^ ord(b)) for a,b in zip(data, key))

def decrypt():
    for y in range(0,3000):
        for m in range(0,12):
            for d in range(0, 31):
                key = f"{y:04}-{m+1:02}-{d+1:02}"
                hk = md5(key)
                xs = xor(ct, hk)
                if xs.startswith("NTRLGC{"):
                    print(xs)
                    exit()
```

### CRYPTO: My heart
Gr rers so Qzjxkjwue Vmbp. W's 33 fsapw zqb. Gv pmonq kx wr kpw tawixoteh qbszhqr pr Osxfnx, wmsje fjh wxa iopvov bno, tjx A fi fbl sdfjykk. T iecm aq fh odptpywc jzk llp Mawb Wy mapdfhukai mzffwq, fhp H yak pmuk jgabv tak ew 8 DD el kpw vouxmz. L tmv'm cgbua, cch Y alzealiniuju mnwqm. S'u ga aap sy 11 LW, fhp deuz egpk F vaz poubm nevnm pr ivkjm, re hwhpbd wiel. Drhcx gbjkgq a cuuax qz hwju cfqu sgt xuxhm pdqjd hkkaig gljgpbc ek mlmshehjj dooije zgkcy lp vwd, G tjksilc bfzo cq pmizvkbj mhpslaso yclws kmpbfoy. Jzeh xxko p decy, S kodx kd xohbraz prg ywhyitx qb bdjenc kc lxz kmpbfoy. K xwi prjp wxams ecxj oq kbegen uz dg tdeh ehjzu-ye. O'o powkcy lp sdrdntr zmwh A't u dlnmpj eza rtmlpe hu umxl e jzfc qufxl hlrw. A muil cems nsv un lbfczxb iuxaty asnh nog ogsoabc, hhua hontgav efq lmqxhm, wxek ammdk zeybs oe mg hbma llwcz ni rknph. Pyuz hm xpa S dknq ikap iudmowg, eqt S wbzf lltd sq jnsw dnvjuo cj uedeonenc. Selxpcuz, gi T iocs hu ammil W higvla'i tebs hu fhubra. QDJVIL{XjocyhbxhmHmEUiRsXjwabpjye}

Solution 1: Cipher text is an easily crackable beaufort (example: https://www.boxentriq.com/code-breaking/beaufort-cipher)

Solution 2: Known Plaintext attacks for jojo fans that recognize "My name is Yoshikage Kira. I'm 33 years old. My house is in the northeast section of Morioh..." copypasta


### CRYPTO: Hills
Running strings charlie.jpg gives you this string: WKNAWPVIOBRPHKQKHVWGHLKGVZCA

It is a hill cipher that dcode.fr can brute it and you get ICANDOITBETTERWITHMIDJOURNEY

strings flag.jpg has an encripted zip file embedded at the end containing the flag, you can unzip it using the key in the charlie.jpg picture


### CRYPTO: Collision Course!
The hashing function is very vulnerable. An idea is to create a 8 characters long string and changing characters to match each byte from the hash, one at a time.
Each byte changes when a character at index n and length-n is changed.




# STEGO CHALLENGES:

### STEGO: GIFted
One of the frames contains the flag

### STEGO: Unpleasant challenge
Ishihara test for color blindness contains the flag

### STEGO: Blue!
Open the image with paint and use bucket to reveal the flag (: (: (: (: (: (: (: (: (: (: (: (: (: (: (: (: (: (: (: (: (: (: (: (: (: (: (: (: (: (: (: (: (: (: (: 

### STEGO: Gadgets
HEX code of the pixels in the left corner can be decoded to ascii to reveal the flag

### STEGO: PWNVOYAGE-Cover
exiftool will reveal a key in the meta data, that can be used with steghide to retrieve the flag

### STEGO: PWNVOYAGE-Cover 2
strings will reveal a serie of numbers. They are indexes that point to the letters in the cover and can be followed to get the flag. & needs to be replaced with { and } to keep the same format as other ones.

### STEGO: Touchless
NxM where N is the button to press in old phones before smartphones and M how many times you have to press the button

### STEGO: The Cake
strings to find hidden zip inside that contains a mp3. The voice reads in welsch the binary code of the flag
