#problem 2
function binary_subtraction of bin1 and bin2
 max between length of bin1 and bin2 declared as max_length 
 Set bin1 to the zero-filled representation with a total length of max_len
Set bin2 to the zero-filled representation with a total length of max_len
Initialize result  
Initialize borrow =0
Declare bit1,bit2,diff
For i starting from (max_len - 1) down to 0 (inclusive) in steps of  -1: 1.1
     bin1[i]= integer bit1 
     bin1[i]= integer bit2 
     bit2 = bit2 +borrow
     diff = bit1 – bit2
     if diff is less than 0
             diff = diff+2
             borrow =1
     else
             borrow =0
     end if
     assign result= string diff +result 
end for
Set result to the string obtained by removing leading '0's from the original result
If result is empty
    result =’0’
return result value
#menu1
declare choice1, num, is_not_binary, choice2
while true
 output binary calculator 
 output A) insert a number 
 output B) exit program
 input choice1  
 if choice1 = A
  input num 
  set is_not_binary = True
  while is not binary:
   set is_not_binary = False
   for digit = first item in num to last item in num 
    if digit not equal 1 and digit not equal 0 
     set is_not_binary = True
     output please insert a valid binary number 
     set num = input
     end if
    end for
   end while
 else if choice1 = B
  output exiting program 
  break 
 else
  output please select a valid choice

 
menu2  
 while is_not_binary = False
  output **please select the operation**
  output "A) Compute one's complement"
  output "B) Compute two's complement"
  output "C) addition"
  output "D) subtraction"
  input choice2 
if choice2 is "A":
    declare first_comp 
    for bit in usernum:
        if bit is "1":
            first_comp = first_comp + "0"
        elif bit is "0":
            first_comp = first_comp + "1"
    
    print("The first complement of", usernum, "is", first_comp)

else if choice2 is "B":
    declare first_comp
    for bit in usernum:
        if bit is "1":
            first_comp = first_comp + "0"
        elif bit is "0":
            first_comp = first_comp + "1"
    
    set second_comp = int(first_comp) + 1
    print("The second complement of", usernum, "is", second_comp)
  Else if choice2 = C
   Declare num2, carry, sum, last_digit, last_digit2,sum_digit
   Input num2
   set is_not_binary = True
   while is not binary:
    set is_not_binary = False
    for digit = first item in num to last item in num 
     if digit not equal 1 and digit not equal 0 
      set is_not_binary = True
      output please insert a valid binary number 
      set num = input
     end if
    end for
   end while
  set carry = 0 
  set sum = []
  while num > 0 or num2 > 0
   set last_digit = num%10 
   set last_digit2 = num2 %10
   if last_digit + last_digit2 + carry = 2 
    set sum_digit = 0
    set carry = 1
   else if last_digit + last_digit2 + carry = 3 
    set sum_digit = 1 
    set carry = 1
   else 
    set sum_digit = last_digit +last_digit2 +carry
   add sum_digit to sum
   set num = num // 10
   set num2 = num2 // 10
  reverse items in sum
  output carry
  for i. = first item in sum to last item in sum 
   output i. 
  break
 else if choice2 = D
  declare num2,
  input num 2 
  set is_not_binary = True
  while is not binary:
   set is_not_binary = False
   for digit = first item in num to last item in num 
    if digit not equal 1 and digit not equal 0 
     set is_not_binary = True
     output please insert a valid binary number 
     set num = input
    end if
   end for
  end while
 assign result= binary_subtraction(num,num2) 
 print “the result = “
output result
Else 
 Output please insert a valid choice
end if
