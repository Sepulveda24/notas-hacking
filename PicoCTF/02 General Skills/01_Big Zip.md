Descripción
Unzip this archive and find the flag.

- [Download zip file](https://artifacts.picoctf.net/c/504/big-zip-files.zip)

Hints:
1.⁠ ⁠Can grep be instructed to look at every file in a directory and its subdirectories?

Solución 1

Con web shell


files/folder_oetovspdce/ggaudayrwjdgsfqhblcipvp.txt  
  inflating: big-zip-files/folder_oetovspdce/vafilzrbxkgmc.txt  
  inflating: big-zip-files/folder_oetovspdce/file_nknvubiszsqbem.txt  
  inflating: big-zip-files/folder_oetovspdce/jbtcszddkznvilr.txt  
  inflating: big-zip-files/folder_oetovspdce/file_xqilkclm.txt  
  inflating: big-zip-files/folder_oetovspdce/file_vxltdsxzzjwllxb.txt  
  inflating: big-zip-files/folder_oetovspdce/file_rineobitmhqsmuxiyadn.txt  
  inflating: big-zip-files/folder_oetovspdce/kdbijtyzmsp.txt  
  inflating: big-zip-files/folder_oetovspdce/file_ebzjtlwmamwyuqjt.txt  
  inflating: big-zip-files/folder_oetovspdce/file_xubuxtijyhtmbjxcgyj.txt  
  inflating: big-zip-files/folder_oetovspdce/file_bxjqjjnkknubrdtex.txt  
  inflating: big-zip-files/folder_oetovspdce/file_gvrbclkrjwxcgqnfyyygupi.txt  
  inflating: big-zip-files/folder_oetovspdce/file_bhngwuoxvxmswhrbhe.txt  
   creating: big-zip-files/folder_wdhgdgrbfc/
  inflating: big-zip-files/folder_wdhgdgrbfc/gqcyepbiqxaaou.txt  
  inflating: big-zip-files/folder_wdhgdgrbfc/fldojuhvoksgzmvjui.txt  
  inflating: big-zip-files/folder_wdhgdgrbfc/file_yzszguvjqowihejtbczb.txt  
  inflating: big-zip-files/folder_wdhgdgrbfc/file_mdynxfbelqmkccuptpfvsx.txt  
  inflating: big-zip-files/folder_wdhgdgrbfc/zoyegjwhsekui.txt  
 extracting: big-zip-files/folder_wdhgdgrbfc/izpsdjrflyxcpuhjtaflbtp.txt  
  inflating: big-zip-files/folder_wdhgdgrbfc/fxaxiryjldhjugrsxhndjglp.txt  
  inflating: big-zip-files/folder_wdhgdgrbfc/file_qmzrrkkuaqnol.txt  
  inflating: big-zip-files/folder_wdhgdgrbfc/xktktzhdxnfu.txt  
  inflating: big-zip-files/folder_wdhgdgrbfc/puqtvrnhomqbrkguy.txt  
  inflating: big-zip-files/folder_wdhgdgrbfc/file_czpkyijqgdzhwkfkyd.txt  
  inflating: big-zip-files/folder_wdhgdgrbfc/ncpphsegf.txt  
  inflating: big-zip-files/folder_wdhgdgrbfc/rpagkqbzcuxepx.txt  
  inflating: big-zip-files/folder_wdhgdgrbfc/pdppdhedydlawgvhwym.txt  
  inflating: big-zip-files/folder_wdhgdgrbfc/qbwalzyyprvrcjpepe.txt  
  inflating: big-zip-files/folder_wdhgdgrbfc/file_ljeldszgyuc.txt  
 extracting: big-zip-files/folder_wdhgdgrbfc/lmjsuinfffmpmyjmmk.txt  
 extracting: big-zip-files/folder_wdhgdgrbfc/tdwocpenvymtoj.txt  
 extracting: big-zip-files/folder_wdhgdgrbfc/fdsjfllubxcxwhpv.txt  
  inflating: big-zip-files/folder_wdhgdgrbfc/file_jyvxtmmtpl.txt  
  inflating: big-zip-files/folder_wdhgdgrbfc/file_epcuiockebhmxxtago.txt  
  inflating: big-zip-files/folder_wdhgdgrbfc/tvnwbgmapeulf.txt  
 extracting: big-zip-files/folder_wdhgdgrbfc/finitvya.txt  
  inflating: big-zip-files/folder_wdhgdgrbfc/bondkyoxvdcgxyq.txt  
  inflating: big-zip-files/folder_wdhgdgrbfc/file_hacfyxtdwkdiycfwatiyvusg.txt  
  inflating: big-zip-files/folder_wdhgdgrbfc/file_jdlhinpycace.txt  
  inflating: big-zip-files/folder_wdhgdgrbfc/gnsnwwhmlslslscapr.txt  
  inflating: big-zip-files/folder_wdhgdgrbfc/file_ximyquuowm.txt  
  inflating: big-zip-files/folder_wdhgdgrbfc/siizcxeduftjnvian.txt  
  inflating: big-zip-files/mktyhgmedcj.txt  
Sepulveda24-picoctf@webshell:~$ ls
README.txt  big-zip-files  big-zip-files.zip  files  files.zip
Sepulveda24-picoctf@webshell:~$ grep grep -h
^C
Sepulveda24-picoctf@webshell:~$ grep -h
Usage: grep [OPTION]... PATTERNS [FILE]...
Try 'grep --help' for more information.
Sepulveda24-picoctf@webshell:~$ cd big-zip-files/
Sepulveda24-picoctf@webshell:~/big-zip-files$ grep | pico
Usage: grep [OPTION]... PATTERNS [FILE]...
Try 'grep --help' for more information.
Too many errors from stdin
Sepulveda24-picoctf@webshell:~/big-zip-files$ grep -r pico
folder_pmbymkjcya/folder_cawigcwvgv/folder_ltdayfmktr/folder_fnpfclfyee/whzxrpivpqld.txt:information on the record will last a billion years. Genes and brains and books encode picoCTF{gr3p_15_m4g1c_ef8790dc}
Sepulveda24-picoctf@webshell:~/big-zip-files$ 


Notas adicionales

-------------

Referencias

https://webshell.picoctf.org