Readme

Goals:
	1) Text that makes sense, is useful, and as accurate as I am capable of
	2) To determine what differences exist between the Atmega and LGT
	3) Communicate #2 seamlessly in the final document
	4) A 1:1 page match of the Chinese datasheet in English
	5) A complete bookmark index and document with text recognition
	5) Only use a Free software toolchain with Linux
	6) Upload all files so anyone can access and modify if there is a problem

Directories:

Burst-328
This is the last Atmel branded datasheet broken up into individual pages, it's metadata, and a copy of the original

Burst-Ch
This contains the original Chinese PDF broken up into individual pages, and a copy of the original. This also contains the .txt metadata files I used to create the PDF bookmark indices. I use this directory a lot for making my version of the edited PDF. This is where I was experimenting with the index too. There are two versions of the metadata here (doc_data and testdoc_data) where I was messing with the default page sizing. There are 2 modified Chinese PDF's here with English indices. Version .0 has the default page size set differently. I think your PDF viewer should take control of this after your first time viewing the doc. Version .1 is the result after passing the .0 file through an app called qpdf’s "linearization” command, aka - "optimizing the doc for web viewing."

Burst-En
Just like the Chinese one but English. I don’t really use this much now. The translation is not useful for me. I’m manually running everything through google translate.

Final PDF
For now,this is the folder for files that are intended for the final viewer. 

Housekeeping
My basic toolchain version info, commands, and notes are saved here.

todo
My primary working output files are here. After creating the GIMP file and exporting the PDF image the file is only a raw image and is larger than A4 paper. The text recognition software works far better at the size I have the GIMP output set at currently. I place these files in imgpdf. The file with text recognition is passed to a ruby script I found that creates the text recognition. The output of this goes into the ocrpdf directory. These files are still larger than A4. I pass them through pdfjam to resize the page to A4, then place this in the a4pdf directory. Then I upload the file to a website that does the individual page compression and place the output in the compressedpdf directory. (These directory names are all short and lowercase to make it easier to do these steps quickly from the commandline.) I am uploading all of this so that if someone has problems with some step of the process like the PDF doesn’t work on someone’s system anyone including me, and modify the toolchain and easily rework the entire document without needing to work from the bottom up.
GIMP XCF
This directory contains the compressed .xcf GIMP files with all the layers, added text, and makeshift alignment tools I used.
Errata
This has my full text based comparison of the Atmega versus LGT datasheets page for page and line by line. If you really want to see the differences, this is where I save the files for each page and write notes. I may edit a few details in the final text that are not in these files but this is like my first draft and initial markup document. These are usually several pages long for each single page final PDF.

Spreadsheets
This has the comprehensive spreadsheet comparisons I’ve done for the atmega vs LGT registers and instruction set.
