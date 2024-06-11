# PICOCTF

SOLVING PICOCTF

## MOD 26

<p>Description
Crptyptography can be easy, do you know what ROT13 is? cvpbPGS{arkg_gvzr_V'yy_gel_2_ebhaqf_bs_ebg13_jdJBFOXJ}<p>
<p> Rot13 is changing a character with the 13th letter from it. THis can be solve by online rot13 converter but in terminal we can use echo and tr <br>
 echo 'cvpbPGS{arkg_gvzr_V'yy_gel_2_ebhaqf_bs_ebg13_jdJBFOXJ}' | tr 'A-Za-z' 'N-ZA-Mn-za-m'<br>
 FLAG:picoCTF{next_time_I'll_try_2_rounds_of_rot13_wqWOSBKW}<br>

## Mind your Ps and Qs

<p>In RSA, a small e value can be problematic, but what about N? Can you decrypt this? "https://mercury.picoctf.net/static/b9ddda080c56fb421bf30409bec3460d/values"<br>

first lets get the values out of this give link bu using wget to download it<br>
wget https://mercury.picoctf.net/static/b9ddda080c56fb421bf30409bec3460d/values<br>
After downloading use cat to extract value out of "values" file<br>

cat values<br>

<p>Decrypt my super sick RSA:
c: 964354128913912393938480857590969826308054462950561875638492039363373779803642185
n: 1584586296183412107468474423529992275940096154074798537916936609523894209759157543
e: 65537 <br>

now we can use online rsa decoder and public key n,e<br>

FLAG: picoCTF{sma11_N_n0_g0od_73918962}<br>

## Morse code

<p>Description
Morse code is well known. Can you decrypt this?
Download the file here.
Wrap your answer with picoCTF{}, put underscores in place of pauses, and use all lowercase.<br>
lets download the file<br>
wget https://artifacts.picoctf.net/c/79/morse_chal.wav<br>
now by online morse code audio decoder we can get the secret flag<br>
W H 4 7 H 4 7 H 9 0 D W 2 Š U 9 H 7<br>
changing it into required format<br>
picoCTF{WH47_H47H_90D_W20U9H7}<br>

## flag

 <p>What do the flags mean?<p>
 <p>hint:-The flag is in the format PICOCTF{}<p>

<p>In the given link https://jupiter.challenges.picoctf.org/static/fbeb5f9040d62b18878d199cdda2d253/flag.png we have pictures of some flag i we observe it we can see it is in format of the flag so we can find what different flag here means till the bracket
But I don't have any idea of other flags so I searched "flag symbols and their meaning" on browser and I found some flags and number they represent in see.
In browser I found "flagid.org" i.e a flag identifier if we make the flag we can see what letter they represent so at last I got key as
"PICOCTF{F1AG5AND5TUFF}"<p>

## Transposition-trial

<p>Our data got corrupted on the way here. Luckily, nothing got replaced, but every block of 3 got scrambled around! The first word seems to be three letters long, maybe you can use that to recover the rest of the message.
Download the corrupted message "https://artifacts.picoctf.net/c/192/message.txt"<p>
<p>HINT:-Split the message up into blocks of 3 and see how the first block is scrambled<p>
<p>Hidden message:- heTfl g as iicpCTo      {7F4NRP051N5_16_35P3X51N3_V091B0AE}2<p>
<p>If we observe every set of 3 letters we can see that it's making sense only if 3rd letter of set is change to 1st and 1st to second and 2nd to third like
het - the
fl_ - _fl
g_a - ag_
and so on..<p>
<p>So the code to decrypt the message will be <p>
''' 
s = "heTfl g as iicpCTo{7F4NRP051N5_16_35P3X51N3_V091B0AE}2"
txt = [s[i:i+3] for i in range(0, len(s), 3)]
dec = []

for chunk in txt:
rearranged = chunk[2] + chunk[0] + chunk[1]

        dec.append(rearranged)

for element in dec:
print(element, end='')
'''

# OUTPUT

key= "picoCTF{7R4N5P051N6_15_3XP3N51V3_109AB02E}"

## Substitution1

<p>Description:- It seems that another encrypted message has been intercepted. The encryptor seems to have learned their lesson though and now there isn't any punctuation! Can you still crack the cipher?
Download the message https://artifacts.picoctf.net/c/114/message.txt<p>
<p>HINT:-Try refining your frequency attack, maybe analyzing groups of letters would improve your results?<p>
<p>Message:-"LKOb (bwvek ove lgqkhej kwj osgx) gej g kyqj vo lvrqhkje bjlhetky lvrqjktktvu. Lvukjbkgukb gej qejbjukjz dtkw g bjk vo lwgssjuxjb dwtlw kjbk kwjte lejgktftky, kjlwutlgs (guz xvvxstux) bitssb, guz qevmsjr-bvsftux gmtstky. Lwgssjuxjb hbhgssy lvfje g uhrmje vo lgkjxvetjb, guz dwju bvsfjz, jglw ytjszb g bketux (lgssjz g osgx) dwtlw tb bhmrtkkjz kv gu vustuj blvetux bjeftlj. LKOb gej g xejgk dgy kv sjgeu g dtzj geegy vo lvrqhkje bjlhetky bitssb tu g bgoj, sjxgs juftevurjuk, guz gej wvbkjz guz qsgyjz my rguy bjlhetky xevhqb gevhuz kwj dvesz ove ohu guz qeglktlj. Ove kwtb qevmsjr, kwj osgx tb: qtlvLKO{OE3AH3ULY_4774LI5_4E3_L001_6J0659OM}"<p>

<p>SOLUTION:- From the hint it is clear that it can be solved using frequency attack so, on quipqiup.com we just need to past the message and chose the output that has required format in our case it is picoCTF{}<p>
<p>KEY = "picoCTF{FR3QU3NCY_4774CK5_4R3_C001_6E0659FB}"

## Dachshund Attacks

<p>DESCRIPTION:- What if d is too small? Connect with nc mercury.picoctf.net 58978<p>
<p>HINT:- A picture of Dachshund dog<p>

<p>given in nc mercury.picoctf.net 58978 :- 
e: 12102709540732812992944327037658423375506624694330975987328416449304590892041073972039552005855397807977832223051541783744475039723666151516476945890471106716821786003090954935646985632471538751698950841007365504191824716802754339582713365262382596277657786103988726211471842504516658959590186395216973620337
n: 81497084937029711949971847593603148172032326337340554229397711519822770558769458996742708200746897568370398185862718382762558629295193724375202777846841902540883269912009762851325937421172459079372655894143364484231218644189439143083413982169986874639086957884282882641828652965201544538533814132761212084157
c: 61542505732063943596748994002968623421430413364438423311658878708169099740321043855421664050515641694806812851531031708445436117069684649956174175857434355513078420868692482076347984197952446445353250503945294728325362714240102315791617147985495195792700265195468173803180178635280683127709691575910182361698<p>
 <p>It is clear from here its rsa now from hint we know it is something related to name of dog, now when I searched rsa when d is small it gives "Wiener's attack" that is use in these cases but we don't need to go deep into this as dcode.fr/rsa-cipher can work even if d is small that is it can perform wiener attack
 So, putting values of n,e,d in this we get key as 
 "picoCTF{proving_wiener_6907362}"<p>
