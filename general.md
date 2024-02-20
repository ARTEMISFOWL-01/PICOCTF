# GENERAL PROBLEMS

## Obedient Cat

  <p>Description
This file has a flag in plain sight (aka "in-the-clear"). Download flag.<br>
link contain by download flag: "https://mercury.picoctf.net/static/704f877da185904ec3992e7255a15c6c/flag"<br>
downloading using wget <br>
after downloading we got file name flag.1<br>
cat flag.1<br>
FLAG:picoCTF{s4n1ty_v3r1f13d_1a94e0f9}<br>

## Python Wrangling<br>

<p>Description
Python scripts are invoked kind of like programs in the Terminal... Can you run "this Python script" using this "password" to get the "flag"?<br>
downloading all files given in "" marks<br>
wget https://mercury.picoctf.net/static/5c4c0cbfbc149f3b0fc55c26f36ee707/ende.py<br>
file got  :ende.py.3<br>
wget https://mercury.picoctf.net/static/5c4c0cbfbc149f3b0fc55c26f36ee707/pw.txt<br>
file got:pw.txt.2<br>
text : 192ee2db192ee2db192ee2db192ee2db<br>
wget https://mercury.picoctf.net/static/5c4c0cbfbc149f3b0fc55c26f36ee707/flag.txt.en<br>
file got:flag.txt.en.1<br>
lets try to run python file <br>
python ende.py.3<br>
it gives (-e/-d)<br>
lets use -h to see information abt function<br>
python ende.py.3 -h<br>
<p>Usage: ende.py.3 (-e/-d) [file]
Examples:
  To decrypt a file named 'pole.txt', do: '$ python ende.py.3 -d pole.txt<p>
  lets use this<p>
python ende.py.3 -d flag.txt.en.1<br>
ENTER PASSWORD: 192ee2db192ee2db192ee2db192ee2db<br>
FLAG:picoCTF{4p0110_1n_7h3_h0us3_192ee2db}<br>


