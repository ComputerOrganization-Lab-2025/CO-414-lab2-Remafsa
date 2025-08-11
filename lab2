.data
str1:   .asciiz "Enter an integer value: "
str2:   .asciiz "Double of the number is: "

.text
.globl main

main:
    # Ask for input
    li $v0, 4              # service code to print string
    la $a0, str1           # load address of str1 into $a0
    syscall                # print str1

    li $v0, 5              # service code to read integer
    syscall                # read integer
    move $t0, $v0          # store input in $t0

    # Double the number
    add $t1, $t0, $t0      # $t1 = $t0 + $t0

    # Print message
    li $v0, 4              # print string
    la $a0, str2
    syscall

    # Print doubled value
    li $v0, 1              # service code to print integer
    move $a0, $t1
    syscall

    # Exit program
    li $v0, 10
    syscall
