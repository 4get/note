
find . * -exec md5sum {} >checksum.md5 \;

md5sum -c ckechsum.md5

