🌞 Créer un répertoire de travail dans votre répertoire personnel

blaireaux-furtif@vbox:~$ pwd  
/home/blaireaux-furtif  
blaireaux-furtif@vbox:~$ mkdir work  
blaireaux-furtif@vbox:~$ pwd  
/home/blaireaux-furtif  
blaireaux-furtif@vbox:~$ ls  
Desktop  Documents  Downloads  gameshell  Music  Pictures  Public  Templates  Videos  work  
blaireaux-furtif@vbox:~$ cd work  
blaireaux-furtif@vbox:~/work$  



# I. Programme minimal




## 2. Analyse du programme compilé



🌞 **Retrouvez à l'aide de `readelf` l'architecture pour laquelle le programme est compilé**
```
blaireaux-furtif@vbox:~/work$ readelf -h hello1  
ELF Header:  
  Magic:   7f 45 4c 46 01 01 01 00 00 00 00 00 00 00 00 00  
  Class:                             ELF32
  Data:                              2's complement, little   endian  
  Version:                           1 (current)  
  OS/ABI:                            UNIX - System V  
  ABI Version:                       0  
  Type:                              DYN (Shared object file)  
  Machine:                           Intel 80386  
  Version:                           0x1  
  Entry point address:               0x1000  
  Start of program headers:          52 (bytes into file)  
  Start of section headers:          13576 (bytes into file)  
  Flags:                             0x0  
  Size of this header:               52 (bytes)  
  Size of program headers:           32 (bytes)  
  Number of program headers:         11  
  Size of section headers:           40 (bytes)  
  Number of section headers:         20  
  Section header string table index: 19  
blaireaux-furtif@vbox:~/work$

```
🌞 **Afficher la liste des *sections* contenues dans le *programme***

```
blaireaux-furtif@vbox:~/work$ readelf -S hello1  
There are 20 section headers, starting at offset 0x3508:  

Section Headers:  
  [Nr] Name              Type            Addr     Off      Size   ES Flg Lk Inf Al  
  [ 0]                   NULL            00000000 000000   000000 00      0   0  0  
  [ 1] .interp           PROGBITS        00000194 000194 000013 00   A  0   0  1  
  [ 2] .note.gnu.bu[...] NOTE            000001a8 0001a8 000024 00   A  0   0  4  
  [ 3] .gnu.hash         GNU_HASH        000001cc 0001cc 000018 04   A  4   0  4  
  [ 4] .dynsym           DYNSYM          000001e4 0001e4 000010 10   A  5   1  4  
  [ 5] .dynstr           STRTAB          000001f4 0001f4 000001 00   A  0   0  1  
  [ 6] .text             PROGBITS        00001000 001000 000060 00  AX  0   0  1  
  [ 7] .eh_frame_hdr     PROGBITS        00002000 002000 00001c 00   A  0   0  4  
  [ 8] .eh_frame         PROGBITS        0000201c 00201c 000058 00   A  0   0  4  
  [ 9] .dynamic          DYNAMIC         00003f98 002f98 000068 08  WA  5   0  4  
  [10] .got.plt          PROGBITS        00004000 003000 00000c 04  WA  0   0  4  
  [11] .comment          PROGBITS        00000000 00300c 000027 01  MS  0   0  1  
  [12] .debug_aranges    PROGBITS        00000000 003033 000020 00      0   0  1  
  [13] .debug_info       PROGBITS        00000000 003053 000074 00      0   0  1  
  [14] .debug_abbrev     PROGBITS        00000000 0030c7 000063 00      0   0  1  
  [15] .debug_line       PROGBITS        00000000 00312a 000047 00      0   0  1  
  [16] .debug_str        PROGBITS        00000000 003171 0000b3 01  MS  0   0  1  
  [17] .symtab           SYMTAB          00000000 003224 0001b0 10     18  22  4  
  [18] .strtab           STRTAB          00000000 0033d4 00006a 00      0   0  1  
  [19] .shstrtab         STRTAB          00000000 00343e 0000c9 00      0   0  1  
Key to Flags:
  W (write), A (alloc), X (execute), M (merge), S (strings), I (info),  
  L (link order), O (extra OS processing required), G (group), T (TLS),  
  C (compressed), x (unknown), o (OS specific), E (exclude),
  p (processor specific)  

```
🌞 **Affichez le code *assembleur* de la section `.text` à l'aide d'`objdump`**

```
blaireaux-furtif@vbox:~/work$ objdump -M intel -j .text -s hello1  

hello1:     file format elf32-i386  

Contents of section .text:  
 1000 5589e557 565383ec 10e84e00 000005f2  U..WVS....N.....  
 1010 2f0000c7 45e54865 6c6cc745 e96f2c20  /...E.Hell.E.o,  
 1020 57c745ed 6f726c64 66c745f1 210ac645  W.E.orldf.E.!..E  
 1030 f3008d75 e5bf0e00 0000b804 000000bb  ...u............  
 1040 01000000 89f189fa cd80b801 00000031  ...............1  
 1050 dbcd8090 83c4105b 5e5f5dc3 8b0424c3  .......[^_]...$. 
 
``` 
## 2. Librairie et compilation dynamique


### C. Tracer les appels à des librairies



🌞 **Tracez à l'aide de la commande `ldd` les *librairies* appelées par...**
```
blaireaux-furtif@vbox:~/work$ ldd hello2  
        linux-gate.so.1 (0xf7f65000)  
        libc.so.6 => /lib32/libc.so.6 (0xf7d5f000)  
        /lib/ld-linux.so.2 (0xf7f67000)  
blaireaux-furtif@vbox:~/work$ ldd hello1  
        statically linked  
blaireaux-furtif@vbox:~/work$ which ls  
/usr/bin/ls  
blaireaux-furtif@vbox:~/work$ file /bin/ls  
/bin/ls: ELF 64-bit LSB pie executable, x86-64, version 1 (SYSV), dynamically linked, interpreter /lib64/ld-linux-x86-64.so.2, BuildID[sha1]=6461a544c35b9dc1d172d1a1c09043e487326966, for GNU/Linux 3.2.0, stripped  
blaireaux-furtif@vbox:~/work$ ldd /bin/ls  
        linux-vdso.so.1 (0x00007ffe6dfad000)  
        libselinux.so.1 => /lib/x86_64-linux-gnu/libselinux.so.1 (0x00007f6ef9014000)  
        libc.so.6 => /lib/x86_64-linux-gnu/libc.so.6 (0x00007f6ef8e40000)  
        libpcre2-8.so.0 => /lib/x86_64-linux-gnu/libpcre2-8.so.0 (0x00007f6ef8da8000)   
        libdl.so.2 => /lib/x86_64-linux-gnu/libdl.so.2 (0x00007f6ef8da2000)  
        /lib64/ld-linux-x86-64.so.2 (0x00007f6ef907b000)
        libpthread.so.0 => /lib/x86_64-linux-gnu/libpthread.so.0 (0x00007f6ef8d80000)  
blaireaux-furtif@vbox:~/work$ which firefox  
/usr/bin/firefox  
blaireaux-furtif@vbox:~/work$ file /bin/firefox  
/bin/firefox: POSIX shell script, ASCII text executable  
blaireaux-furtif@vbox:~/work$ ldd /bin/firefox  
        not a dynamic executable  

```
🌞 **Parmi les *librairies* appelées par *hello2*, déterminer le type du fichier nommé `libc.so.X`**

## 3. Compilation statique





🌞 **Affichez le type des fichiers `hello2` et `hello3`**
```bash
blaireaux-furtif@vbox:~/work$ file hello2  
hello2: ELF 32-bit LSB pie executable, Intel 80386, version 1 (SYSV), dynamically linked, interpreter /lib/ld-linux.so.2, BuildID[sha1]=7d87e146585a76a77955ee3a7170aa8a96672954, for GNU/Linux 3.2.0, with debug_info, not stripped  
blaireaux-furtif@vbox:~/work$ file hello3  
hello3: ELF 32-bit LSB executable, Intel 80386, version 1 (GNU/Linux), statically linked, BuildID[sha1]=582d5dc5be5fb3b3b67bb65365e90dd05cd017f6, for GNU/Linux 3.2.0, with debug_info, not stripped 
``` 

🌞 **Affichez leurs tailles**
```bash
blaireaux-furtif@vbox:~/work$ du -h hello2  
20K     hello2  
blaireaux-furtif@vbox:~/work$ du -h hello3  
684K    hello3  
```
## 4. Compilation cross-platform

🌞 **Affichez l'*architecture* de votre *CPU***

```bash
blaireaux-furtif@vbox:~/work$ cat /proc/cpuinfo
processor       : 0
vendor_id       : GenuineIntel
cpu family      : 6
model           : 186
model name      : 13th Gen Intel(R) Core(TM) i7-1355U
stepping        : 3
cpu MHz         : 2611.204
cache size      : 12288 KB
physical id     : 0
siblings        : 1
core id         : 0
cpu cores       : 1
apicid          : 0
initial apicid  : 0
fpu             : yes
fpu_exception   : yes
cpuid level     : 22
wp              : yes
flags           : fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ht syscall nx rdtscp lm constant_tsc rep_good nopl xtopology nonstop_tsc cpuid tsc_known_freq pni pclmulqdq monitor ssse3 fma cx16 sse4_1 sse4_2 x2apic movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm 3dnowprefetch fsgsbase bmi1 avx2 bmi2 invpcid rdseed adx clflushopt sha_ni arat md_clear flush_l1d arch_capabilities
bugs            : spectre_v1 spectre_v2 spec_store_bypass swapgs rfds
bogomips        : 5222.40
clflush size    : 64
cache_alignment : 64
address sizes   : 39 bits physical, 48 bits virtual
power management:
```

🌞 **Vérifiez que vous avez la commande `x86-64-linux-gnu-gcc`**
```bash
blaireaux-furtif@vbox:~/work$  sudo find / -name "x86_64-linux-gnu-gcc"  
/usr/bin/x86_64-linux-gnu-gcc  
```

🌞 **Compilez votre fichier `hello3.c` dans un fichier cible nommé `hello4` vers une autre *architecture* que la vôtre**
```bash
blaireaux-furtif@vbox:~/work$ sudo apt install   gcc-arm-linux-gnueabihf  
blaireaux-furtif@vbox:~/work$ arm-linux-gnueabihf-gcc -o hello4 hello3.c  
blaireaux-furtif@vbox:~/work$ file hello4  
hello4: ELF 32-bit LSB pie executable, ARM, EABI5 version 1 (SYSV), dynamically linked, interpreter /lib/ld-linux-armhf.so.3, BuildID[sha1]=85312dbbd4b86adff3d040f2405951ea76fadc91, for GNU/Linux 3.2.0, not stripped  

```

🌞 **[Désassemblez](../../cours/memo/glossary.md#désassembler) `hello3` et `hello4` à l'aide d'`objdump`**

- vous devriez constater que malgré le même *programme* C d'entrée, le contenu des deux *programmes* une fois compilés est bien différent

🌞 **Essayez d'exécuter le *programme* `hello4`**

- sproutch !
- should NOT work
