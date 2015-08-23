# GNU Compiler Collection Internals の日本語版みたいなもの

## はじめに
GNU Compiler Collection Internals の日本語版みたいなものです。

gccのソースコードを読んでいて gccintの日本語版のpdfとepub版が欲しかったので作成してます。

## 原本
gcc-2.95.3 に付属の Texinfo 形式マニュアルの日本語訳

* https://lists.gnu.org/archive/html/gnu-devels-jp/2001-07/msg00003.html
* https://web.archive.org/web/20091224143355/http://www.sra.co.jp/wingnut/gcc/index.html

## 編集方針
gcc 6.0 になってtexinfoをPDFに変換できるように修正されたので、
原本をgcc 6.0のtexinfoの形式に変換し、ちょっとだけ校正しました。

## PDF EPUB 変換手順

ubuntuの場合
* sudo apt-get install texinfo
* sudo apt-get install texlive
* sudo apt-get install texlive-lang-cjk
* sudo apt-get install dbtoepub

* weget https://github.com/fukusaka/texinfo-ja/raw/master/texinfo.tex

* TEX=ptex  texi2dvi gccint.texi
* dvipdfmx gccint.dvi
* texi2pdf gccint.texi

* makeinfo --docbook --enable-encoding gccint.texi
* dbtoepub gccint.xml

## License

GFDL 1.3

## contact

* http://twitter.com/eggman
* http://github.com/eggman/gccint-japanese


