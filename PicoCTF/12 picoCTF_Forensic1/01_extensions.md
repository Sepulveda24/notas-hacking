Descripción
This is a really weird text file [TXT](https://jupiter.challenges.picoctf.org/static/e7e5d188621ee705ceeb0452525412ef/flag.txt)? Can you find the flag?

Hints:
1.⁠ ⁠How do operating systems know what kind of file it is? (It's not just the ending!
2.Make sure to submit the flag as picoCTF{XXXXX}

Solución 1

Con terminal linux
''
┌──(parallels㉿kali-linux-2022-2)-[~]
└─$ wget https://jupiter.challenges.picoctf.org/static/e7e5d188621ee705ceeb0452525412ef/flag.txt
--2025-04-02 23:37:11--  https://jupiter.challenges.picoctf.org/static/e7e5d188621ee705ceeb0452525412ef/flag.txt
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 9984 (9.8K) [application/octet-stream]
Saving to: ‘flag.txt’

flag.txt            100%[================>]   9.75K  --.-KB/s    in 0s      

2025-04-02 23:37:11 (49.2 MB/s) - ‘flag.txt’ saved [9984/9984]

                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~]
└─$ ls
 cookies.txt   Downloads   Pictures    Templates   webshell.php
 Desktop       flag.txt    Public     '~.venv'     webshell.png.php
 Documents     Music       server.py   Videos
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~]
└─$ cat flag.txt                    
�PNG
▒
IHDR���^�sRGB���gAMA��
                      �a        pHYs%%IR$�&�IDATx^��kB��;.��0�L&���_�N=%�L��Z���Jut$y'���H&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�˿����������'~��n疓��?��^xQ2>��osD�����9�����
                             ���m�`Ł����_R��d|���       Y�G��Ϳ=�e_������W$���.��y��|�Ŀ���gt;B^�'w�֐��-�<�09��w�]�O���?��.n���L��j�8L�����ǖ��
�xI2>�k�D��&'�U���Q����=�n�n����(�Wcš�=g�ǵ���zd|<�$�
=nu�{���fd|���[f�H|^���w����,xi2>�����z�w����O�,���.[t�����E��:=�w�:����%�y5/��E~�ȍ������qhxi2>���'p�)��497�]�w~|�|/o{q���?r*/��}m�{��z��煽����sz�)��u�v[x��rd|�n������ޏ�>�J���R�����W��+n���
                                        �maW�rd|�f����_���uuy�"��;x��j^s���9=aA�-�
^�����'�9(������翚�\q�|NOX�n
                            ���#��E����cby�"��;x��j^s���9=aA�-�
^�������O��s�.?h�9N�����/��▒��w�GM�u~����!�c�G��y▒�=/�*�P2����bΖ���w/�ߦ���{;�������>�j�_h{?a{/�hD�Ĺ�Fܮ���?�:z��Ǽd�/{����i���k��W�|��m��B;g��i_1OA;c���.�>��V>���[_�������������n[�}J_}3��r��]���;mo�ة�fg����-ڽJ{F�S*|��
                                                             �U���y{�NG��9=�p��;����}h
         ߥn��G�n�C^�-���0]啋N
c{����Y{����Y/���;���v������k���h��z�g���c��j+�܆�~��+{��e��|�>��;�e�,x2>��ht9�7NQ���r���7�C\���-���<�Gd|����u���16[R�w��2���^4�u��#�z5փ�⎴_޴�U�W�������ɇ���Uw�����RWc}-W��U����▒Xĵ��i��zYs�=9`gm%���snK�*��5�j�����?���IY�Zd|T������&���?W���8�:ί���uo��[|����s�ٷ�\-VTG�<�>�<j�I�f|m[U����(���
                                                      }�,������$�����^S{������Ջ�&tTw���N�;o��Z-���>ڼ�&����z?�������fLn�l�t���^|��_2�n:��\u�hc}n���ԝS�n.��y8�J�Z�n�VK�O���}��w�K)k�5����j��w>iM�ʧ������T׹s�ԥ�7n��x�Q�7���|�zz�\����}�|P���Y���p��h[��n���X�ځ
                    ����O�/�{����,����ճR�Nq�׳O��MZ�UO]�O��!��u~����I�ZQ�Jju��d��<�tq�q�6+uN�=��|~c��=9r��>���-mm\BK���b��C������f����V2>�����lr��Q���9=t���n��.�����œ���%S��]vUz��w�����ls���n��U=t�&MY��u�v���3�Nns�
                                                           ��<��'�����5�f���NL�>���s.m�O�]�Y��U8v�N�5�d��<Z_�]�n���6��hO��E��ꁯ▒�w,oO+&4`��ՁF[��,����QMOl;��z������S��▒ſ���_Wώ�g��,'7
                           �����G�)�Xm��}�4�|��}fA�x��cn2�r;�S�Y~v���;aR����$?���n�o%���=�M�����'��'.(ם�7[g��9�<k�Qu=Z{��ի��]7�;r�*▒[����p'�#�5���8�v��չO_S�[-+����o�{-�W>�YF�go���<~!vGlk�iۻ��jN������\�_��Y|)W�06��F�J�������c�'GϢ����hu��▒k�E�ea�Ձ��~��2������{G���A���3w\7o�Sz���i���_;���������>ba���l�����ݛ�N���iH�f�uPW����M}�yye>�5�M�<d��X��u�yۻWG]�+5�az�3Vj��r�jó>N��p�7n(��>�C=9|�+���N<���u��o�z�,��O�u�^wO�����'��`ףK��O�>��7��:�▒�|�����l��
                                                          ���GnO��)]����}%<`R^}c7P��4w��}](w-԰���gϟ۞�v����[3?u6�R'�quԧ��X�}%���(��>����+6k-+��Z���?����ٳ^��z���b&��/���;���}��=&��▒<����,G��N�9B���]��w�k�{���Y��=��9�r�B�[�6��޹5����co����c�~���Wy�D
              F���▒OY��a��]�ܚ�v�Ov����w����a����:���VK7l�x2Va�zu5�g}���q۵.޹'Gzr�,W��5�Ҍ������^1?`�?�s��׹� ���j��vR����t�lr-�z��p�{���E��
�
 n������/�����g>n��xhe��!:jZ�Цr�l��u�{S�kR^��H���-|�ܖ��W�dcS�7iS�mV�X�5�g}�2���I������▒�p������R�:�m��𧖆���HO�����������V�S�߿}�m��'w�j��?]�d|T��"�O��:w6�a����;��Sڳs�-�[��bs�C�OX��R��%+�\.rp�Z��d��7O��X7��#��^
                                                      ��.vvbl�;����8�S����ps�r��3=D����7]���v_/��/w�Q��RcnT��/V���u��;�6������q�,W�-����_}����b�7����~T��QG�X��d|T��"v�C�λ�b��P��V��l�]J#��i�������G[�|r�X���kV��T��D�������𔮎��\�]���+��*dpշ�)
       q�xM��r�R��=B-�����l��b|e9�OY��
�ի%���(}�ݥv���Ǝ9����Y
                     �H��^1�����������h5O:v���'��▒<����9Av�o�R�����'K�#O٩T��xp{�E·}��]-���qrۼ��ymq��7JzJW������Z+���d���e����S�j�����e�#������
                                                                 �Z�a��/;+5V�Vy_�g}��}y�ٸu1V[�i�'��bpE:v��R��q{����N�g?�����o!��*'��3���k�j[s�ѵ<ui�uЧG���L����ᶪ�]-raا,�ռ�[3��98���Y^
                          h?�Y�3�:o疱���^�{�Xg�t�L�g�7�77�n��98�C���<s��g�l�^�g��X�}W���i�n�iѾ�&���n�'��bpE:v���v��g�C����@�����@2U=���p�X�x�c�����}�����&�\�aډ����'�t�X����'�9��t���W�h�\▒�)
                                   w5m��'�j/>���(�9�0P�3�Z���4�����ܖ�l�3׎�4�3��\y��y���ɴ���]z1��W�P;�������
                              vRe��!�_2�U�}�[��mV;4�c=9ze���ډݵ~��f�3�؋گ�T▒�z$��Q�3���        ��▒�xG��0['�ӻ��p���Uo5���V/���'��(q���򌑳h�Dϓ�u��;V���8�s��v�����Y*�^��L��[{������?���!�F�>�ddS6kV�d����g���WKX�__>�V.�v�d}Ў�>a�&C��x�L6��
                                                                           ���Q�d��%w��Ձ/�u�U�/#㣚�o�g�م+筞#��X�#u��j��&���!΃�w�{��'��y�|c���z��e�#g�R����f��*zV��q���v����C����J:���rfq�i�/<��ﵻ-�կLsw���P;�خ�-��ו        ͻ;���~�x�L��<���_2y�zK�{r�,�`˗�6�b\�Z9]�M�˼%]���T��e�W������ئ���\��}w�z��;.>��q�.=mv&�X��t��ݽj�!on�_m�@?�����)G����p�'�G���pkK�r����b���=r|WgoOV� �>r����ѳ-'�/�e{?Ѵ�S
                                                                           No���N�~��J_��f_�?���ڭݘ𒙯��x��y��.m�s����޼���0�:�rՓg�7e�'G���
                                                          ���▒e��z�O�LK^xXg1���Ձ/mY�U�/#㣚�����d��N��\�i�q]�~Z�0��Tc��e���������f��*�W�j�@�x�ݬ�����#�*▒�"w��%z�����(}�r����Oյ�;�����n�C���7�SW/��U�Խw�׹�_�5�!�e���
                                                        �{r�,.�8���▒5-W�_��Gu�K;�~U�����Nl��^�5r��6�����{k��3����]ڳwnm��5�b�ᶪ▒Y�}���+M�بb~���`V��9;������▒s�>�Q�Җ�_�22>����D�|���r��=j�u���M~����N�j�z�o��z���g�MƸռwd�q▒�܈���_{��8�~j����z�a��f=hwL���+��4��i�����7�k���'O6�]F*}�ܤ��b��,Q�����w�������Z��+�,�tk�F����O����|�▒.�8�ѩ��Z�6���V~��k����7�O�Ÿt��v��e2{�+���}��:��>��Ax2>�rw6z��|V���/M�G%�{M��?Py1Z��i2>*ߋj�Řu�D|0���S�����Q��^TY��?�]�>�@���ǖ�_�����J�����~�`
                                                                          �W�rXXQ�V�F��+��Q��^�B�g
                     ,XLC����<㗼O����0�����v��
                                              �k��Q��^���\|�˶�.p��WY}�/Y�o��L�,/��{����y�������1��(��w�{�y����ۼQ�5o��
                                        �)��xi2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��'l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>�&��l2>H����?
q'�\e�IEND�B`�                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~]
└─$ mv flag.txt flag.png        
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~]
 cookies.txt   Downloads   Pictures    Templates   webshell.php
 Desktop       flag.png    Public     '~.venv'     webshell.png.php
 Documents     Music       server.py   Videos
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~]
└─$ open flag.png 
                                                                             
┌──(parallels㉿kali-linux-2022-2)-[~]
└─$ 
''

picoCTF{now_you_know_about_extensions}


Notas adicionales

--------------------


Referencias

file:///home/parallels/flag.png