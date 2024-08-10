1) Use exiftool cat.jpg to get the meta data from the jpg file 
```
exiftool cat.jpg
```

2) Found that License seems to be encoded. We can create a new temp.txt file .
```
touch temp.txt
```

4)  We can append the License string in temp file:
```
echo 'cGljb0NURnt0aGVfbTN0YWRhdGFfMXNfbW9kaWZpZWR9' >> temp.txt
```

5) Decode the temp.txt file using :
```
base64 -d temp.txt
```

## Final results :
```
picoCTF{the_m3tadata_1s_modified}
```
