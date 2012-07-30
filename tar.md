
只用 tar xf 就可以解压bz2或gzip压缩的包。


忽略执行的文件（参数--exclude非要放在前面，不然就不管用，可能是tar版本的问题吧，坑爹。）

tar --exclude=.git -zcvf


