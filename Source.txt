 .model small
.stack 100h
.data
Var db ‘hello$’
Var1 db ‘world$’
.code
Main proc
	Mov ax,@data
	Mov ds,ax
	Lea dx,var
	Mov ah, 9
	Int  21h
	Lea dx,var1
	Mov ah, 9
	Int  21h
mov ah, 4ch
int 21h
	
main endp
end main

