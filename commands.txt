//Install the pdfminer utility to convert to machine-readable format
pip install pdfminer

//Use pdf2txt.py tool on each .pdf document
pdf2txt.py -o DEM2012.html 2012-National-Platform.pdf
pdf2txt.py -o GOP2012.html 2012GOPPlatform.pdf

//Search each .html document for keywords
grep -inr 'internet' GOP2012.html > internet-gop.txt
grep -inr 'internet' DEM2012.html > internet-dem.txt
grep -inr 'intellectual' GOP2012.html > ip-gop.txt
grep -inr 'intellectual' DEM2012.html > ip-dem.txt
grep -inr 'digital' DEM2012.html > digital-dem.txt
grep -inr 'digital' GOP2012.html > digital-gop.txt
grep -inr 'multi' DEM2012.html > multi-dem.txt
grep -inr 'multi' GOP2012.html > multi-gop.txt

//Count number of results in Democratic Platform (excluding 'multi')
wc -l *-dem.txt
    >>>  11 cyber-dem.txt
    >>>   2 digital-dem.txt
    >>>  10 internet-dem.txt
    >>>   6 ip-dem.txt
    >>>  29 total

//Count number of results in Republican Platform (excluding 'multi')
wc -l *-gop.txt
    >>>  20 cyber-gop.txt
    >>>   0 digital-gop.txt
    >>>  17 internet-gop.txt
    >>>   5 ip-gop.txt
    >>>  42 total

