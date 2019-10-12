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
My primary working output files are here. After creating the GIMP file and exporting the PDF image the file is only a raw image and is larger than A4 paper. The text recognition software works far better at the size I have the GIMP output set at currently. I place these files in imgpdf. The file with text recognition is passed to a ruby script I found that creates the text recognition. The output of this goes into the ocrpdf directory. These files are still larger than A4. I pass them through pdfjam to resize the page to A4, then place this in the a4pdf directory. Then I upload the file to a website that does the individual page compression and place the output in the compressedpdf directory. (These directory names are all short and lowercase to make it easier to do these steps quickly from the commandline.) I am uploading all of this so that if someone has problems with some step of the process like the PDF doesn’t work on someone’s system anyone including me, can modify the toolchain and easily rework the entire document without needing to work from the bottom up.

GIMP XCF
This directory contains the compressed .xcf GIMP files with all the layers, added text, and makeshift alignment tools I used.

Errata
This has my full text based comparison of the Atmega versus LGT datasheets page for page and line by line. If you really want to see the differences, this is where I save the files for each page and write notes. I may edit a few details in the final text that are not in these files but this is like my first draft and initial markup document. These are usually several pages long for each single page final PDF.

Spreadsheets
This has the comprehensive spreadsheet comparisons I’ve done for the atmega vs LGT registers and instruction set.

Final Notes: I will be creating a notes page to replace the first page of the Chinese PDF in my final version. Each page of my edited PDF that contains text that was added and not is not present in the Atmel datasheet is in italics key differences are in bold. This is possible because the Chinese datasheet is a 1:1 copy translation and paste of the Atmel datasheet. Don’t take my word for it. Go look at and read my errata comparison pages and notes. 
  Look at page15errata.pdf on the second page in the yellow highlighted block of text for a great example. If you look at the corresponding Atmel datasheet page you will see the “following reference” line from the Atmel text is followed by an Assembly and C code example related to EEPROM. These examples are entirely omitted from the LGT DS but the copied Atmel text reference was not removed from their copy and paste translation. 
   This may seem off-putting to learn about at first, but know, this is a good thing. When someone does a line by line comparison, like I am doing, it is much easier to see exactly what was changed, omitted, and added. Finally, because the Chinese text is mostly machine translated English text a lot of errors exist. I have noted these in my errata docs. THERE ARE LOTS OF THESE ERRORS. After comparing the text like this from page 10 onwards I have learned to look for areas that do not match up at all with anything in the Atmel text. These are the lines LGT changed. There are a lot of places where the sentences match the Atmel text but odd and relevant word and syntax changes are present. I spend a lot of time trying to cross reference these and check/qualify what I can. I make errata notes about them and then use my best judgment. 
  After passing a bunch of the Chinese text through google translate (GT) manually it became quite clear that there are a lot of formatting errors in the way the pdf renders Chinese text. Just adding one space in the wrong place between characters can completely alter the content that GT outputs. Many times the difference is the complete opposite meaning of the sentence. 
  When a paragraph is placed in GT manually it will often create line breaks in the English translation where there is an issue. Every English translation of the Chinese datasheet I have seen has these errors that result from the PDF formatting. Anyone could try to edit these for flow if they don’t understand why the machine edited text looks odd. They are assuming these are simple issues with the translation program. THIS IS NOT THE CASE. If the formatting is corrected manually the text makes much more sense and it’s meaning is closer to the original. This is especially true of the text that was translated from Atmel’s English datasheet. However, these mistakes work two ways. These mistakes are already present in the Chinese text because of how it was created. The only way to create a worthwhile, accurate document in English is to manually compare the Atmel text line by line as this is first source of errors. I’m no expert here, but I have the time to work on this and am dumb enough to try.
-Jake
