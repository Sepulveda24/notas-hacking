Descripción
Connect to this PostgreSQL server and find the flag!

Additional details will be available after launching your challenge instance.

Hints:
1.⁠What does a SQL database contain?

Solución 1

Con inspeccion de elemento



Entramos al servidor y observamos los comandos con \h y tambien
observamos que hay dentro  y hacemos un select a las banderas para poder rescatar la bandera.



Sepulveda24-picoctf@webshell:~$ psql -h saturn.picoctf.net -p 58091 -U postgres pico
Password for user postgres: 
psql (14.17 (Ubuntu 14.17-0ubuntu0.22.04.1), server 15.2 (Debian 15.2-1.pgdg110+1))
WARNING: psql major version 14, server major version 15.
         Some psql features might not work.
Type "help" for help.

pico=# []{}_:;,.-|||?M"#$%&/()=????
ABORT                      DROP                       RELEASE
ALTER                      END                        RESET
ANALYZE                    EXECUTE                    REVOKE
BEGIN                      EXPLAIN                    ROLLBACK
CALL                       FETCH                      SAVEPOINT
CHECKPOINT                 GRANT                      SECURITY LABEL
CLOSE                      IMPORT FOREIGN SCHEMA      SELECT
CLUSTER                    INSERT INTO                SET
COMMENT                    LISTEN                     SHOW
COMMIT                     LOAD                       START
COPY                       LOCK                       TABLE
CREATE                     MOVE                       TRUNCATE
DEALLOCATE                 NOTIFY                     UNLISTEN
DECLARE                    PREPARE                    UPDATE
DELETE FROM                REASSIGN                   VACUUM
DISCARD                    REFRESH MATERIALIZED VIEW  VALUES
DO                         REINDEX                    WITH
pico=# \h                          
pico=# \dt
         List of relations
 Schema | Name  | Type  |  Owner   
--------+-------+-------+----------
 public | flags | table | postgres
(1 row)

pico=# select * from flags;
 id | firstname | lastname  |                address                 
----+-----------+-----------+----------------------------------------
  1 | Luke      | Skywalker | picoCTF{L3arN_S0m3_5qL_t0d4Y_31fd14c0}
  2 | Leia      | Organa    | Alderaan
  3 | Han       | Solo      | Corellia
(3 rows)

picoCTF{L3arN_S0m3_5qL_t0d4Y_31fd14c0}


Notas adicionales

--------------------


Referencias

https://webshell.picoctf.org