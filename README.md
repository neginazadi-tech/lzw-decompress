# lzw-decompress

LZW compression works by reading a sequence of symbols, grouping the symbols into strings, and converting the strings into codes. Because the codes take up less space than the strings they replace, we get compression. Characteristic features of LZW includes, 

LZW compression uses a code table, with 4096 as a common choice for the number of table entries. Codes 0-255 in the code table are always assigned to represent single bytes from the input file.
When encoding begins the code table contains only the first 256 entries, with the remainder of the table being blanks. Compression is achieved by using codes 256 through 4095 to represent sequences of bytes.
As the encoding continues, LZW identifies repeated sequences in the data and adds them to the code table.
Decoding is achieved by taking each code from the compressed file and translating it through the code table to find what character or characters it represents.

Reference to study more: https://www.geeksforgeeks.org/lzw-lempel-ziv-welch-compression-technique/
