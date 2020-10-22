# md5sum 安全性已遭質疑(參見MD5演算法缺陷)
```
md5sum是一種電腦程式，用於計算與校驗RFC 1321所描述的128位元MD5雜湊值，
此處MD5雜湊值（或校驗和）作一個檔案的數字指紋使用。
```
```
md5sum --h
Usage: md5sum [OPTION]... [FILE]...
Print or check MD5 (128-bit) checksums.

With no FILE, or when FILE is -, read standard input.

  -b, --binary         read in binary mode
  -c, --check          read MD5 sums from the FILEs and check them
      --tag            create a BSD-style checksum
  -t, --text           read in text mode (default)

The following five options are useful only when verifying checksums:
      --ignore-missing  don't fail or report status for missing files
      --quiet          don't print OK for each successfully verified file
      --status         don't output anything, status code shows success
      --strict         exit non-zero for improperly formatted checksum lines
  -w, --warn           warn about improperly formatted checksum lines

      --help     display this help and exit
      --version  output version information and exit

The sums are computed as described in RFC 1321.  When checking, the input
should be a former output of this program.  The default mode is to print a
line with checksum, a space, a character indicating input mode ('*' for binary,
' ' for text or where binary is insignificant), and name for each FILE.

GNU coreutils online help: <http://www.gnu.org/software/coreutils/>
Full documentation at: <http://www.gnu.org/software/coreutils/md5sum>
or available locally via: info '(coreutils) md5sum invocation'
```
```
# md5sum --v
md5sum (GNU coreutils) 8.28
Copyright (C) 2017 Free Software Foundation, Inc.
License GPLv3+: GNU GPL version 3 or later <http://gnu.org/licenses/gpl.html>.
This is free software: you are free to change and redistribute it.
There is NO WARRANTY, to the extent permitted by law.

Written by Ulrich Drepper, Scott Miller, and David Madore.
```
# md5sum簡單測試
```
gedit test.txt

cat test.txt


md5sum test.txt 
2202ac317aa26f1b5c727de59005576a  test.txt

更改字元大小寫

md5sum test.txt 
5f9954d6a59ed890f99c01632022f40a  test.txt

32*4 bits = 128 bits
```
