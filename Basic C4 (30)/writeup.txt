`
$ cat da_bomb.txt 
SGFoLCB5b3UgdGhvdWdodA==
UmVhbGx5PyBEaWQgeW91IGFjdHVhbGx5IGtlZXAgZ29pbmc=
bG93a2V5IGRpc3NhcG9pbnRlZC4uLg==
ZnVuIGZhY3Q6IEplc3MgaXMgYWN0dWFsbHkgYSBjYXQ=
bWVycA==
Kmluc2VydCBmaWxsZXIgbWF0ZXJpYWwgaGVyZSo=
d2VscCB0aGF0IHNob3VsZCBiZSBlbm91Z2ggZGF0YQ==
aWYgeW91IGNhbid0IHRlbGwgYWxyZWFkeSwgZGVjb2RpbmcgdGhpcyBpc24ndCB0aGUgYW5zd2Vy
`
so we are provided with a file containing lines which looks like base64 encoded and actualy they are so let's decode
them

$ for i in $(cat da_bomb.txt);do echo $i| base64 -d; done
Hah, you thoughtReally? Did you actually keep goinglowkey dissapointed...fun fact: Jess is actually a catmerp*insert filler material here*welp that should be enough dataif you can't tell already, decoding this isn't the answer

Nop! but at last you see "decoding this isn't the answer" so may be there is something else look at i tried stegno stuff
and failed then i moved back to the ctf challenge page there i see that flag starts with "c4" and 90 chars which
indicates that it may be some kind of hash so i did a google search with 

"hash starting with c4"

and Boom! the first result has description "C4 IDs are an encoding of a SHA-512 hash" I clicked on it and
there is file upload option so i uploaded the file and got this so let's check if it is 90 chars long

c43tb1oG5pLtwxs9n28KdEqb8Puy3TfY9Qjz5U28yYEYdKHFfYNUAdGnCRJhMJ1XVmvMAbQaBR59kAHznn5V86MoRb

rtcp{c43tb1oG5pLtwxs9n28KdEqb8Puy3TfY9Qjz5U28yYEYdKHFfYNUAdGnCRJhMJ1XVmvMAbQaBR59kAHznn5V86MoRb}


