1) lets figure out the file type
   
```
file flag2of2-final.pdf 
```


2) This one is little tricky, lets try to change the file type to PNG
   
```
touch temp.JPEG
cat flag2of2-final.pdf >> temp.PNG
```

3)  Now open the PNG file and pdf file, hmm seems like CTF is the combinations of PNG file and pdf content. 
   

## Final results :
```
picoCTF{f1u3n7_1n_pn9_&_pdf_90974127}
```
