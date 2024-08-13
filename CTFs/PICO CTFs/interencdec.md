1) Use base64 decoder to decode the file
   
```
base64 -d enc_flag
```

Output: b'd3BqdkpBTXtqaGx6aHlfazNqeTl3YTNrX2g0N2o2azY5fQ=='

2) Hmm, this seems to be double encoded. we will grab the inner string and put it in temp.txt file : d3BqdkpBTXtqaGx6aHlfazNqeTl3YTNrX2g0N2o2azY5fQ==
   
```
touch temp.txt
echo 'd3BqdkpBTXtqaGx6aHlfazNqeTl3YTNrX2g0N2o2azY5fQ==' >> temp.txt
```

3)  Now we will try to decode again:
   
```
base64 -d temp.txt
```

Output: wpjvJAM{jhlzhy_k3jy9wa3k_h47j6k69}

4) I noticed that there is a tag for caesar cipher in challenge, lets try to d-cipher, found that it was 7 a-h shift:
```
picoCTF{caesar_d3cr9pt3d_a47c6d69}
```

## Final results :
```
picoCTF{the_m3tadata_1s_modified}
```
