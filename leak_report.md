# Leak report
It is saying that 46 Bytes were lost that were allocated by calloc and then called in strip
is_clean and main. We need to fix it by freeing the variable which was allocated at the appropriate spot. 
After searching through the allocated variable which is result. We can see that in the is_clean function
that result is reassigned as cleaned. The clean function can then be freed. 

This however causes an invalid error that value can't be freed or invalid delete me on certain strings. 
