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
