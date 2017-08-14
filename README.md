# binaries

This is the finesse binary from the end of the "fortress" VM challenge produced by NCC

Dump of assembler code for function main:
   0x00000000004005e6 <+0>:	push   rbp
   0x00000000004005e7 <+1>:	mov    rbp,rsp
   0x00000000004005ea <+4>:	sub    rsp,0x20
   0x00000000004005ee <+8>:	mov    DWORD PTR [rbp-0x14],edi
   0x00000000004005f1 <+11>:	mov    QWORD PTR [rbp-0x20],rsi
   0x00000000004005f5 <+15>:	mov    QWORD PTR [rbp-0x8],0x600b34
   0x00000000004005fd <+23>:	cmp    DWORD PTR [rbp-0x14],0x1
   0x0000000000400601 <+27>:	jle    0x400667 <main+129>
   0x0000000000400603 <+29>:	mov    edi,0x400708 ###This is the "apparently you have this much finesse" message###
   0x0000000000400608 <+34>:	call   0x4004a0 <puts@plt> ###This is where it is printed
   0x000000000040060d <+39>:	mov    rax,QWORD PTR [rbp-0x20]
   0x0000000000400611 <+43>:	add    rax,0x8
   0x0000000000400615 <+47>:	mov    rax,QWORD PTR [rax]
   0x0000000000400618 <+50>:	mov    rdi,rax ### RAX currently points to my ARGV, this is being loaded to rdi to print
   0x000000000040061b <+53>:	mov    eax,0x0
   0x0000000000400620 <+58>:	call   0x4004c0 <printf@plt> 
   0x0000000000400625 <+63>:	mov    edi,0xa
   0x000000000040062a <+68>:	call   0x400490 <putchar@plt> ### Prints amount of finesse I entered in ARGV
   0x000000000040062f <+73>:	mov    eax,DWORD PTR [rip+0x2004ff]        # 0x600b34 <finesse_level>
   0x0000000000400635 <+79>:	cmp    eax,0x2329 ###Need eax to equal 9001
   0x000000000040063a <+84>:	jne    0x40065b <main+117>
   0x000000000040063c <+86>:	mov    edi,0x400738 ### This is the "perfect amount" message
   0x0000000000400641 <+91>:	call   0x4004a0 <puts@plt>      ### This is where it is printed
   0x0000000000400646 <+96>:	mov    rax,QWORD PTR [rbp-0x20] ### THIS  is where the answer is printed
   0x000000000040064a <+100>:	add    rax,0x10                 ###
   0x000000000040064e <+104>:	mov    rax,QWORD PTR [rax]      ###
   0x0000000000400651 <+107>:	mov    rdi,rax                  ###
   0x0000000000400654 <+110>:	call   0x4004b0 <system@plt>    ###
   0x0000000000400659 <+115>:	jmp    0x400671 <main+139>      ###
   0x000000000040065b <+117>:	mov    edi,0x400760 ### This is the "Still not enough" message
   0x0000000000400660 <+122>:	call   0x4004a0 <puts@plt> ### This is where it is printed
   0x0000000000400665 <+127>:	jmp    0x400671 <main+139>
   0x0000000000400667 <+129>:	mov    edi,0x400788 ### This is the "you didnt specify finesse" message###
   0x000000000040066c <+134>:	call   0x4004a0 <puts@plt> ###This is where it is printed
   0x0000000000400671 <+139>:	leave  
   0x0000000000400672 <+140>:	ret  
