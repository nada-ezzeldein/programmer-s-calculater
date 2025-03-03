#include <iostream>
using namespace std;
int main (){
cout << "                                 _________________________________________" << endl;
cout << "                                    (welcome to programmer's clculator)                                   " << endl;
cout << "                                 _________________________________________" << endl;
// the title
cout << endl << endl << endl;
cout << "What do you want to do? " << endl << endl;
cout << " 1) conversion. \n 2) Addition. \n 3) Subtraction. \n 4) Exit.\n" ;
cout << "======================================================================================================\n";
cout << "Warning: If you enter a wrong number, you will exit the program automatically!\n";
cout << "======================================================================================================\n";
// choose the number of the operation that we want to do
int num; 
cin >> num;
cout << "==============================================================\n";
if (!num)
{cout << "Invalid number! Please enter acorrect number from 1 to 4." << endl;
num=4;}
while ((num > 4) || (num <1))
{cout << "Invalid number! Please enter acorrect number from 1 to 4." << endl;
num=4;}
// if the number is incorrect

{
switch (num){

//**********************************************************************************************************************************
case 1:
{cout << " Choose the number of the operation please. \n" << endl;
cout << " 1) Convert from Binary to Octal.                        2) Convert from Binary to Decimal. "<< endl;
cout << " 3) Convert from Binary to Hexa.                         4) Convert from Octal to Binary. "<< endl;
cout << " 5) Convert from Octal to Decimal.                       6) Convert from Octal to Hexa "<< endl;
cout << " 7) Convert from Decimal to Binary.                      8) Convert from Decimal to octal.  "<< endl;
cout << " 9) Convert from Decimal to Hexa.                        10) Convert from Hexa to Binary.  "<< endl;
cout << " 11) Convert from Hexa to Octal.                         12) Convert from Hexa to Decimal.  "<< endl;
cout << "==================================================================================================\n";

int number;
cin >> number;
if (!number)
{cout << "Invalid number! Please enter acorrect number from 1 to 12." << endl;
return 1;}
while (number > 12 || number <1)
{cout << " Invalid number please enter acorrect number from 1 to 12 : ";
num=4;}
//to make sure thet the number which the user entered is correct
 
// ===================================from binary to octal=======================================================
 if (number == 1){cout << "                                    Convertion from binary to octal\n";
                  cout << "                                 **************************************\n\n\n";
            cout << "Enter the Binary number that you want to convert it : ";
            long long binary;
            int base=1, decimal,sum=0,octal=0;
            cin >> binary;
            // make sure that there is no errors
            if (!binary)
                {
                   cout << "Please enter a correct number to convert it! \n";
                    cout << "==============================================================\n";
                    cout << "Thank you for using our program!\n";
                   return 1;
                }
                else if ( binary < 0)
                {cout << " Please enter a positive number to convert it !\n";
                 cout << "==============================================================\n";
                 cout << "Thank you for using our program!\n";
                 return 1;}
                while (binary > 0) {
                decimal = binary % 10;
                if (decimal !=0 && decimal != 1)
                {
                   cout << "Please enter a correct number to convert it\n";
                   cout << "==============================================================\n";
            cout << "Thank you for using our program!\n";
                   return 1;
                }

                                                         //convertion to decimal 
    while(binary>0){       //Loops until the binary number becomes zero
    decimal=binary%10;       //Extracts the last digit from the binary number
    sum+=decimal*base;      //Converts the digit to decimal and adds it to the total sum
    base*=2;                 // double the base
    binary/=10;}              //Removes the last digit 

                                                    //convertion from decimal to octal 

    base = 1;                     //Resets the base for octal conversion
     while (sum > 0) {            //Loops until the decimal number becomes zero
      int remainder = sum % 8;    //Finds the remainder when divided by 8
        octal += remainder * base;   //Adds the number of the octal digit to the result
        base *= 10;                        
        sum /= 8;                  //Reduces the decimal number by dividing it by 8
           }
          
           cout << octal << endl;
            cout << "==============================================================\n";
            cout << "Thank you for using our program!\n";
           return 0;
            }
 }
//                         *********************************************************************************
// ================================from binary to decimal===================================================
else if  (number == 2){int binary, decimal = 0, base = 1;

            cout << "                                   Convertion from binary to decimal\n";
            cout << "                                 ****************************************\n\n\n";
            cout << "Enter a Binary number to convert: ";
            cin >> binary;
            // make sure that the number wich user entered is correct
            if (!binary)
                {
                    cout << "==============================================================\n";
                   cout << "Invalid number! \n Exiting program.\n";
        cout << "================================================================\n";
        cout << "Thank you for using our program!\n";
        return 1;
                }
                 // convertion to decimal
            while (binary != 0) {
                int digit = binary % 10;   // make sure that the digits is only 0s & 1s
                if (digit !=0 && digit != 1)
                {
                    cout << "==============================================================\n";
                   cout << "Invalid number ! Please enter only 0 or 1 to convert it \n Exiting program.\n";
        cout << "================================================================\n";
        cout << "Thank you for using our program!\n";
        return 1;
                }
               
                decimal += digit * base;  //Adds the converted binary digit to the decimal result
                binary /= 10; //Removes the last digit from the binary number
                base *= 2;    //Multiplies the base by 2 
            }
            cout << "==============================================================\n";
            cout << "\nThe Decimal number is : ";
            cout << decimal << endl;
        cout << "================================================================\n";
        cout << "Thank you for using our program!\n";
    return 0;
}
//                         *************************************************************************************
// ================================from binary to hexa===================================================
else if  (number == 3){
      cout << "                                    Convertion from binary to hexa\n";
      cout << "                                 **************************************\n\n\n";
      cout << "Enter the Binary number that you want to convert it: ";
    
       long long binary;
            int base=1, decimal,sum=0,octal=0;
            cin >> binary;
          
            if (!binary)    // make sure that the number wich user entered is correct
                {
                   cout << "Please enter a correct number to convert it! \n";
                    cout << "==============================================================\n";
                    cout << "Thank you for using our program!\n";
                   return 1;
                }
                else if ( binary < 0)
                {cout << " Please enter a positive number to convert it !\n";
                 cout << "==============================================================\n";
                 cout << "Thank you for using our program!\n";
                 return 1;}
                while (binary > 0) {
                decimal = binary % 10;
                if (decimal !=0 && decimal != 1)
                {
                   cout << "Please enter a correct number to convert it\n";
                   cout << "==============================================================\n";
            cout << "Thank you for using our program!\n";
                   return 1;
                }

                                                         //convertion to decimal 
    while(binary>0){             //Loops until the binary number becomes zero
    decimal=binary%10;             //Extracts the last digit from the binary number
    sum+=decimal*base;             //Adds the converted binary digit to the decimal result
    base*=2;                            //Multiplies the base by 2 
    binary/=10;}                      //Removes the last digit from the binary number
    // from decimal to hexa
    cout << "The hexa decimal number is : ";
    if (decimal == 0) {
        cout << "0"; // special case for zero
    } else {
        long long hexResult = 0; 
        int factor = 1;         
        while (decimal > 0) {   //Loops until the decimal number becomes zero
            int remainder = decimal % 16;   //Find the remainder when dividing by 16
            hexResult += remainder * factor;   //Add the remainder to the result, multiplying by the factor
            factor *= 10;           //Multiply the factor by 10 to shift the position left in the hexadecimal result
            decimal /= 16;           // remove the last hexadecimal digit
        }

           //Loop to display the hexadecimal digits

        while (hexResult > 0) {
            int digit = hexResult % 10;     //Extract the hexadecimal digit from the result
            // test the digit if it was less than or equal 9 print it
            if (digit < 10) {       
                cout << digit; 
            } else {
                //special case to digits that is greater than 9 
                cout << char(digit - 10 + 'A'); 
            }
            hexResult /= 10;  // remove the last  hexa digit 
        }}
    cout << endl;
         cout << "==============================================================\n";
    cout << "Thank you for using our program!\n";}
         cout << "==============================================================\n";
    return 0;
   
}
//                         *************************************************************************************
// ================================from octal to binary===================================================
else if  (number == 4){
    cout << "                       Convertion from octal to binary\n";
    cout << "                     ***********************************\n";
    int octalNumber, remainder;
    bool invalidFound;

    do {
        // Enter the octal number
        cout << "Enter the octal number: ";
        cin >> octalNumber;
          if (!octalNumber) {
            cout << "==============================================================\n";
            cout << "Invalid octal number!" << endl;
            cout << "============================================================\n";
            cout << "Thank you for using our program!\n";
            return 1;
        }
                if (octalNumber < 0 || octalNumber > 999999999) {
                    cout << "==============================================================\n";
            cout << "Invalid octal number!" << endl;
            cout << "==============================================================\n";
            cout << "Thank you for using our program!\n";
            return 1;
        }
        // Validate the digits in the octal number
        int temp = octalNumber;
        invalidFound = false;

        while (temp > 0) {
            remainder = temp % 10;  // Extract the last digit
            if (remainder > 7) {    // If the digit is greater than 7
                cout << "The digit " << remainder << " is invalid in the octal system!" << endl;
                invalidFound = true; // Mark as invalid
            }
            temp /= 10;  // Remove the last digit
        }

    } while (invalidFound);  // Repeat if an invalid digit is found

    // If the number is valid, convert it to binary
    int tempOctal = octalNumber;  // Store the input value
    int binaryDigits[100];  // Array to store binary result (output could be large)
    int index = 0;          // Index for the array

    // Convert each octal digit to binary
    while (tempOctal > 0) {
        int octalDigit = tempOctal % 10;  // Extract the last octal digit
        tempOctal /= 10;

        // Convert the octal digit to binary (3 bits per digit)
        for (int i = 0; i < 3; i++) {
            binaryDigits[index++] = octalDigit % 2;  // Extract the last bit
            octalDigit /= 2;                         // Update the digit
        }
    }

    // Print the binary result (in reverse since it was stored backwards)
    cout << "==============================================================\n";
    cout << "The number in binary is: ";
    for (int i = index - 1; i >= 0; i--) {
        cout << binaryDigits[i];
    }
    cout << endl;
       cout << "==============================================================\n";
            cout << "Thank you for using our program!\n";
    return 0;
}
//                         *************************************************************************************
// ================================from octal to decimal===================================================
else if  (number == 5){
    cout << "                                   Convertion from octal to decimal\n";
    cout << "                                 *************************************\n\n\n";
    int octalNumber, remainder;
    bool invalidFound;

    do {
        // Enter the octal number
        cout << "Enter the octal number: ";
        cin >> octalNumber;
        if (octalNumber < 0 || octalNumber > 999999999) {
            cout << "==============================================================\n";
            cout << "Invalid octal number!" << endl;
            cout << "==============================================================\n";
            cout << "Thank you for using our program!\n";
            return 1;
        }
        if (!octalNumber) {
            cout << "==============================================================\n";
            cout << "Invalid octal number!" << endl;
            cout << "============================================================\n";
            cout << "Thank you for using our program!\n";
            return 1;
        }


        // Check the digits in the octal number
        int temp = octalNumber;
        invalidFound = false;  // Reset the variable each time

        // Verify each digit in the octal number
        while (temp > 0) {
            remainder = temp % 10;  // Extract the last digit
            if (remainder > 7) {  // If the digit is greater than 7
                cout << "The digit " << remainder << " is invalid in the octal system!" << endl;  // Print the error message
                invalidFound = true; // Mark that there is an invalid digit
            }
            temp /= 10;  // Remove the last digit
        }

    } while (invalidFound);  // Repeat the input if an invalid digit is found

    // If there are no invalid digits, convert to decimal system
    int decimalNumber = 0, base = 1;
    int temp = octalNumber;  // Reset the input value to use it for conversion

    // Convert the octal number to decimal
    while (temp > 0) {
        remainder = temp % 10;  // Extract the last digit
        decimalNumber += remainder * base;  // Add the value to the decimal number
        temp /= 10;  // Remove the last digit
        base *= 8;  // Update the base (8, 8^2, 8^3, ...)
    }

    // Print the result in decimal
    cout << "==============================================================\n";
    cout << "The number in decimal is: " << decimalNumber << endl;
    cout << "==============================================================\n";
            cout << "Thank you for using our program!\n";

    return 0;
}
//                         *************************************************************************************
// ================================from octal to hexa===================================================
else if  (number == 6){
     cout << "                                   Convertion from octal to hexa\n";
    cout << "                                 *************************************\n\n\n";
    long long octalNumber, remainder;
    bool invalidFound;

    do {
        // Enter the octal number
        cout << "Enter the octal number: ";
        cin >> octalNumber;
if (!octalNumber) {
    cout << "==============================================================\n";
            cout << "Invalid octal number!" << endl;
            cout << "============================================================\n";
            cout << "Thank you for using our program!\n";
            return 1;
        }
            if (octalNumber < 0 || octalNumber > 9999999999) {
                cout << "==============================================================\n";
            cout << "Invalid octal number!" << endl;
            cout << "==============================================================\n";
            cout << "Thank you for using our program!\n";
            return 1;
        }
     
        // Check if all digits in the number are valid
        long long temp = octalNumber;
        invalidFound = false; // Reset the flag each time

        // Validate each digit in the octal number
        while (temp > 0) {
            remainder = temp % 10; // Extract the last digit
            if (remainder > 7) { // If the digit is greater than 7, it is invalid
                cout << "The digit " << remainder << " is invalid in the octal system!" << endl; // Print error message
                invalidFound = true; // Mark the number as invalid
            }
            temp /= 10; // Remove the last digit
        }

    } while (invalidFound); // Repeat if an invalid digit is found

    // If the number is valid, convert it to decimal
    long long decimalNumber = 0, base = 1;
    long long temp = octalNumber; // Store the number for conversion

    // Convert the octal number to decimal
    while (temp > 0) {
        remainder = temp % 10; // Extract the last digit
        decimalNumber += remainder * base; // Add to the decimal result
        temp /= 10; // Remove the last digit
        base *= 8; // Increase the base (8, 8^2, 8^3, ...)
    }

    // Convert the decimal number to hexadecimal
    string hexNumber = "";
    while (decimalNumber > 0) {
        remainder = decimalNumber % 16; // Get the remainder when divided by 16
        if (remainder < 10)
            hexNumber = char(remainder + '0') + hexNumber; // Digits from 0 to 9
        else
            hexNumber = char(remainder - 10 + 'A') + hexNumber; // Letters from A to F
        decimalNumber /= 16; // Remove the converted part
    }

    // Print the result in hexadecimal
    cout << "==============================================================\n";
    cout << "The number in hexadecimal is: " << hexNumber << endl;
     cout << "==============================================================\n";
      cout << "Thank you for using our program!\n";

    return 0;
}
//                         *************************************************************************************
// ================================from decimal to binary===================================================
else if  (number == 7){
   cout << "                                 Convertion from decimal to binary\n";
    cout <<"                               ***************************************\n\n\n";
    long long Dec_num, remainder;
    bool invalid = false;
    cout << "Enter the decimal number:" << " ";
    cin >> Dec_num;
    if (!Dec_num) {
        cout << "==============================================================\n";
        cout << "invalid input " << "\n";
        cout << "==============================================================\n";
        cout << "Thank you for using our program." << "\n";
        return 1;
    }
    if (Dec_num > 999999999999 || Dec_num < 0) {
        invalid = true;
    }
    while (invalid) {
        cout << "==============================================================\n";
        cout << "you entered an invalid number." << "\n";
        cout << "==============================================================\n";
        cout << "Thank you for using our program." << "\n";
        return 1;

    }
    int BIN_nums[] = { 0,1 };
    int  index = 0;
    int Binary[65];
    while (Dec_num > 0) {
        remainder = Dec_num % 2;
        Binary[index++] = BIN_nums[remainder];
        Dec_num /= 2;
    }
    cout << "==============================================================\n";
    cout << "the binary number is : " << " ";
    for (int i = index - 1; i >= 0;i--) {
        cout << Binary[i];
    }
    cout << "\n==============================================================\n";
    cout << "Thank you for using our program." << "\n";
    cout << "\n";

    return 0;
}
//                         *************************************************************************************
// ================================from decimal to octal===================================================
else if  (number == 8){ 
    cout << "                                Convertion from decimal to octal\n";
    cout <<"                               *************************************\n\n\n";
    long long Dec_num, remainder;
    bool invalid = false;
    cout << "enter the decimal number :" << " ";
    cin >> Dec_num;
    if (!Dec_num) {
        cout << "==============================================================\n";
        cout << "invalid input " << "\n";
        cout << "==============================================================\n";
        cout << "thank you for using our program." << "\n";
        return 1;
    }
    if (Dec_num > 999999999999 || Dec_num < 0) {
        invalid = true;
    }
    while (invalid) {
        cout << "==============================================================\n";
        cout << "you entered an invalid number." << "\n";
        cout << "==============================================================\n";
        cout << "Thank you for using our program!\n";
        return 1;

    }
    int oct_nums[] = { 0,1,2,3,4,5,6,7 };
    int  index = 0;
    int octal[20];
    while (Dec_num > 0) {
        remainder = Dec_num % 8;
        octal[index++] = oct_nums[remainder];
        Dec_num /= 8;
    }
    cout << "==============================================================\n";
    cout << "the octal number is :" << " ";
    for (int i = index - 1; i >= 0;i--) {
        cout << octal[i];
    }
    cout << "\n";
    cout << "==============================================================\n";
            cout << "Thank you for using our program!\n";

    return 0;
}
//                         *************************************************************************************
// ================================from decimal to hexa===================================================
else if  (number == 9){
        cout << "                                 Convertion from decimal to hexa\n";
        cout << "                               **************************************\n\n\n";
    long long  Dec_num, remainder;
    bool invalid = false;
    cout << "enter the decimal number:" << " ";
    cin >> Dec_num;
    if (!Dec_num) {
        cout << "==============================================================\n";
        cout << "invalid input " << "\n";
              cout << "==============================================================\n";
        cout << "Thank you for using our program!\n";
            return 1;
    }
    if (Dec_num > 999999999999|| Dec_num<0) {
        invalid = true;
    }
        while (invalid) {
            cout << "==============================================================\n";
            cout << "you entered an invalid number." << "\n";
              cout << "==============================================================\n";
        cout << "Thank you for using our program!\n";
            return 1;

        }
    char hex_nums[] = { '0', '1', '2', '3', '4', '5', '6', '7', '8', '9', 'A', 'B', 'C', 'D', 'E', 'F' };
    int  index = 0;
    char hexa[20];
    while (Dec_num > 0) {
        remainder = Dec_num % 16;
        hexa[index++] = hex_nums[remainder];
        Dec_num /= 16;
    }
    cout << "==============================================================\n";
    cout << "the hexadecimal number is :" << " ";
    for (int i = index - 1; i >= 0;i--) {

        cout << hexa[i];
    }
    cout << "\n";
  cout << "==============================================================\n";
        cout << "Thank you for using our program!\n";
    return 0;
}
//                         *************************************************************************************
// ================================from hexa to binary===================================================
else if  (number == 10){
cout << "                           Convertion from hexa decimal to binary " << endl;
cout << "                          *****************************************\n\n\n";
 int number_of_digits;
    cout << "Enter the number of digits of your hexadecimal number: ";
    cin >> number_of_digits;
    if (!number_of_digits)
     {
        cout << "==============================================================\n";
        cout << "Invalid number of digits!\n Exiting program.\n";
        cout << "===================================================================================\n";
        cout << "Thank you for using our program !\n";
        return 1;
    }
    if (number_of_digits <= 0 || number_of_digits > 16 ) {
        cout << "==============================================================\n";
        cout << "Invalid number of digits!\n Exiting program.\n";
        cout << "===================================================================================\n";
        cout << "Thank you for using our program !\n";
        return 1;
    }
    /*we use return 1 instead of using break to exit from the whole program if there is an invalide number
    ,as break make us only to exit from only the current loop not from all program
    */
    char hexanumber[16];
    cout << "Please enter the hexadecimal number : ";
    for (int i = 0; i < number_of_digits; i++) {
        cin >> hexanumber[i];

        // and here we put our conditions
        if (!((hexanumber[i] >= '0' && hexanumber[i] <= '9') ||
              (hexanumber[i] >= 'A' && hexanumber[i] <= 'F') ||
              (hexanumber[i] >= 'a' && hexanumber[i] <= 'f'))) {
                cout << "==============================================================\n";
            cout << "Invalid hexadecimal digit detected!\n Exiting program.\n";
            cout << "===================================================================================\n";
             cout << "Thank you for using our program !\n";
            return 1;
        }
    }
    // this is an array of int to store the result in binary
    int binary[64] = {0}; /*here we put the size of array 64 as the maxi. number of digits in hexa is 16 digit and after that an overflow ganna happen
    and we also know that each one bit in hexa number equal 4 bits in binary ,so 4 bits * 16 digits = 64 digit in binary*/
    int counter = 0;      // this counter help us to follow the next position in the array
    // here we will start the conversion from hexa to binary
    for (int i = 0; i < number_of_digits; i++) {
        int decimalValue;
         //we need first to declar this integer to use it
        // here we need to convert each letter into a decimal number which help us to convert more easily the letters in hexa into binary
        if (hexanumber[i] >= '0' && hexanumber[i] <= '9') {
            decimalValue = hexanumber[i] - '0';
            //here there is no need to convert first into decimal number, so we just subtract zero from it
        }
         else if (hexanumber[i] >= 'A' && hexanumber[i] <= 'F') {
            decimalValue = hexanumber[i] - 'A' + 10;
        }
         else if (hexanumber[i] >= 'a' && hexanumber[i] <= 'f') {
            decimalValue = hexanumber[i] - 'a' + 10;
        }
/*in this two conditions we use the ASCII code table to help us to subtract the char of 'a' or 'A'  from any
 letter and we take this differance and add 10 to it
because in ASCII code table the differance between each two consecutive numbers is 1
*/
//after this operation now all number are ready for the next operation
        // conversion from decimal into binary start from here
        for (int j = 3; j >= 0; j--) {
            binary[counter++] = (decimalValue >> j) & 1;
        }
    }
/*here we extract each bit (from most significant bit to Least significant bit ) by shifting to right
and isolating the bit, then store in binary array
*/
    // now we will output the binary number by using this loop to help us to pass through the array
     cout << "===================================================================================\n";
    cout << "The number in binary is: ";
    for (int i = 0; i < counter; i++) {
        cout << binary[i];
    }
    cout << endl;
    cout << "===================================================================================\n";
    cout << "Thank you for using our program !\n";
 return 0;
}


//                         *************************************************************************************
// ================================from hexa to octal===================================================
else if  (number == 11){
    cout << "                                Convertion from hexa decimal to octal   " << endl;
    cout << "                              *******************************************\n\n\n";
    int number_of_digits;
    cout << "Enter the number of digits of your hexadecimal number: ";
    cin >> number_of_digits;
 if (!number_of_digits)
     {
        cout << "==============================================================\n";
        cout << "Invalid number of digits!\n Exiting program.\n";
        cout << "===================================================================================\n";
        cout << "Thank you for using our program !\n";
        return 1;
    }
    if (number_of_digits <= 0 || number_of_digits > 16) {
        cout << "==============================================================\n";
        cout << "Invalid number of digits!\n Exiting program.\n";
        cout << "==============================================================\n";
            cout << "Thank you for using our program!\n";
        return 1;
    }
    /*we use return 1 instead of using break to exit from the whole program if there is an invalide number
    ,as break make us only to exit from only the current loop not from all program
    */
    char hexanumber[16];
    cout << "Please enter the hexadecimal number: ";
    for (int i = 0; i < number_of_digits; i++) {
        cin >> hexanumber[i];
        // and here we put our conditions
        if (!((hexanumber[i] >= '0' && hexanumber[i] <= '9') ||(hexanumber[i] >= 'A' && hexanumber[i] <= 'F') ||(hexanumber[i] >= 'a' && hexanumber[i] <= 'f'))) {
           cout << "==============================================================\n";
            cout << "Invalid hexadecimal digit detected!\n Exiting program.\n";
            cout << "==============================================================\n";
            cout << "Thank you for using our program!\n";
            return 1;
        }
    }
    long long totaldecimal=0;
    // here we will start the conversion from hexa to decimal
    for (int i = 0; i < number_of_digits; i++) {
        int decimalValue;
//we need first to declar this integer to use it
        if (hexanumber[i] >= '0' && hexanumber[i] <= '9') {
            decimalValue = hexanumber[i] - '0';
        }
         else if (hexanumber[i] >= 'A' && hexanumber[i] <= 'F') {
            decimalValue = hexanumber[i] - 'A' + 10;
        }
         else if (hexanumber[i] >= 'a' && hexanumber[i] <= 'f') {
            decimalValue = hexanumber[i] - 'a' + 10;
        }
/*in this two conditions we use the ASCII code table to help us to subtract the char of 'a' or 'A'  from any
 letter and we take this differance and add 10 to it
because in ASCII code table the differance between each two consecutive numbers is 1
*/
totaldecimal = totaldecimal*16+decimalValue ;
    }
long long remainder;
    if (!totaldecimal) {
        cout << "==============================================================\n";
        cout << "invalid input " << "\n";
       cout << "==============================================================\n";
            cout << "Thank you for using our program!\n";
        return 1;
    }
    int  index = 0;
    int octal[50];
    while (totaldecimal> 0) {
octal[index++]=totaldecimal% 8;
totaldecimal/=8;
    }
    cout << "==============================================================\n";
    cout << "the octal number is :" << " ";
    for (int i = index - 1; i >= 0;i--) {
        cout << octal[i];
    }
    cout << "\n";
cout << "==============================================================\n";
            cout << "Thank you for using our program!\n";
    return 0;
}
//                         *************************************************************************************
// ================================from hexa to decimal===================================================
else if  (number == 12){
cout << "                                Convertion from hexa decimal to decimal   " << endl;
cout << "                              ********************************************\n\n\n";
 int number_of_digits;
    cout << "Enter the number of digits of your hexadecimal number: ";
    cin >> number_of_digits;
 if (!number_of_digits)
     {
        cout << "==============================================================\n";
        cout << "Invalid number of digits!\n Exiting program.\n";
        cout << "===================================================================================\n";
        cout << "Thank you for using our program !\n";
        return 1;
    }
    if (number_of_digits <= 0 || number_of_digits > 16) {
        cout << "==============================================================\n";
        cout << "Invalid number of digits! \n Exiting program.\n";
        cout << "================================================================\n";
        cout << "Thank you for using our program!\n";
        return 1;
    }
    /*we use return 1 instead of using break to exit from the whole program if there is an invalide number
    ,as break make us only to exit from only the current loop not from all program
    */
    char hexanumber[16];
    cout << "Please enter the hexadecimal number: ";
    for (int i = 0; i < number_of_digits; i++) {
        cin >> hexanumber[i];
        // and here we put our conditions
        if (!((hexanumber[i] >= '0' && hexanumber[i] <= '9') ||(hexanumber[i] >= 'A' && hexanumber[i] <= 'F') ||(hexanumber[i] >= 'a' && hexanumber[i] <= 'f'))) {
           cout << "==============================================================\n";
            cout << "Invalid hexadecimal digit detected! \nExiting program.\n";
            cout << "================================================================\n";
        cout << "Thank you for using our program!\n";
            return 1;
        }
    }
    long long totaldecimal=0;
    // here we will start the conversion from hexa to decimal
    for (int i = 0; i < number_of_digits; i++) {
        int decimalValue;
//we need first to declar this integer to use it
        if (hexanumber[i] >= '0' && hexanumber[i] <= '9') {
            decimalValue = hexanumber[i] - '0';
        }
         else if (hexanumber[i] >= 'A' && hexanumber[i] <= 'F') {
            decimalValue = hexanumber[i] - 'A' + 10;
        }
         else if (hexanumber[i] >= 'a' && hexanumber[i] <= 'f') {
            decimalValue = hexanumber[i] - 'a' + 10;

        }
/*in this two conditions we use the ASCII code table to help us to subtract the char of 'a' or 'A'  from any
 letter and we take this differance and add 10 to it
because in ASCII code table the differance between each two consecutive numbers is 1
*/
totaldecimal = totaldecimal*16+decimalValue ;
    }
    cout << "==============================================================\n";
    cout << "the number in decimal is equal : "<< totaldecimal << endl;
    cout << "================================================================\n";
        cout << "Thank you for using our program!\n";
    return 0;
}}
//                         *************************************************************************************
break;
// addition
//=========================================================================================
case 2:
{cout << "What is the type of addition do you want to do ? \n" <<endl;
cout << " 1) Binary.                2) Octal. \n 3) Decimal.                4) Hexa. \n";
cout << "==============================================================\n";

int num1;
cin >> num1;

if (num1>4 || num1<1)
{
     cout << "==============================================================\n";
    cout << "Invalid number! Please enter acorrect number from 1 to 4." << endl;
     cin >> num1;
cout << "==============================================================\n";}

else if (!num1)
{cout << "==============================================================\n";
    cout << "Please enter acorrect number from 1 to 4" << endl;
cout << "==============================================================\n";
cout << "Thank you for using our program!\n";

    return 0;}

//==============================================================================
else if (num1 ==1) {
    // convert the two binary numbers to the decimal and convert the result to decimal
    cout << "                            (Binary addition)                                   \n";
    cout << "                           *******************                                     \n\n\n";
    int num1, num2, sumf;
            int decimal2 = 0, decimal1 = 0;
            int base = 1;
           
            cout << "Enter 2 Binary numbers: ";
                cin >> num1 >> num2;
                 if (!(num1 > 0 && num2 > 0)) {
                     cout << "==============================================================\n";
                  cout << "Please enter only positive numbers\n";
                  cout << "==============================================================\n";
            cout << "Thank you for using our program!\n";
    return 0;
            }
            while (num1 != 0) {
                int digit = num1 % 10;
                if (digit !=0 && digit != 1)
                {
                     cout << "==============================================================\n";
                   cout << "invalid number! it exceed the limit.\n";
                    cout << "==============================================================\n";
            cout << "Thank you for using our program!\n";
    return 0;
                }
                decimal1 += digit * base;
                num1 /= 10;
                base *= 2;
            }
            base = 1;
            while (num2 != 0) {
                int digit = num2 % 10;
                if (digit !=0 && digit != 1)
                { 
                    cout << "==============================================================\n";
                   cout << "invalid number! it exceed the limit.\n";
                   cout << "==============================================================\n";
            cout << "Thank you for using our program!\n";
    return 0;
                }
                decimal2 += digit * base;
                num2 /= 10;
                base *= 2;
            }
            sumf = decimal1 + decimal2;
            int y = 1, sum = 0, counter = 0;
            cout << "\nThe result is : ";
            while (y * 2 <= sumf) // counts number of digits and returns n to the power of counter 
            {
                y *= 2;
                counter++;
            }
            for (int i = counter; i >= 0; i--) {
                if (y == 0) {
                    y = 1;
                }
                if (sum + y <= sumf) {
                    cout << 1;
                    sum += y;
                }
                else {
                    cout << 0;
                }
                y /= 2;
            }
            cout << endl;
              cout << "==============================================================\n";
            cout << "Thank you for using our program!\n";
    return 0;
             
   
    }
    //============================================================
    //============================================================
     
else if (num1 ==2) {
    cout << "                             (Octal addition)                                   \n";
    cout << "                           ********************                                    \n\n\n";

    int octalNumber1, remainder1, octalNumber2, remainder2;
    bool invalidFound;

    do {
        // Enter the first octal number
        cout << "Enter the two octal numbers: ";
        cin >> octalNumber1 >> octalNumber2;
        if (octalNumber1 < 0 || octalNumber1 > 999999) {
             cout << "\n==============================================================\n";
            cout << "Invalid octal number!\n" << endl;
            cout << "==============================================================\n";
            cout << "Thank you for using our program!\n";
        }

       
        if (octalNumber2 < 0 || octalNumber2 > 999999) {
             cout << "\n==============================================================\n";
            cout << "Invalid octal number!\n" << endl;
            cout << "==============================================================\n";
            cout << "Thank you for using our program!\n";

            return 1;
        }

        // Verify the digits in the octal numbers
        int temp1 = octalNumber1;
        int temp2 = octalNumber2;
        invalidFound = false;  // Reset the flag each time

        // Check each digit in the octal numbers
        while (temp1 > 0 && temp2 > 0) {
            remainder1 = temp1 % 10; // Extract the last digit of the first number
            remainder2 = temp2 % 10; // Extract the last digit of the second number

            // Check if the digit in the first number is invalid
            if (remainder1 > 7) {
                cout << "The digit " << remainder1 << " is invalid in the octal system!" << endl;
                invalidFound = true;
            }

            // Check if the digit in the second number is invalid
            if (remainder2 > 7) {
                cout << "The digit " << remainder2 << " is invalid in the octal system!" << endl;
                invalidFound = true;
            }

            temp1 /= 10; // Remove the last digit from the first number
            temp2 /= 10; // Remove the last digit from the second number
        }

    } while (invalidFound); // Repeat input if an invalid digit is found

    // Convert to decimal if no invalid digits are found
    int decimalNumber1 = 0, base = 1, decimalNumber2 = 0;
    int temp1 = octalNumber1;
    int temp2 = octalNumber2;

    // Convert the first and second octal numbers to decimal
    while (temp1 > 0 && temp2 > 0) {
        remainder1 = temp1 % 10;
        remainder2 = temp2 % 10;
        decimalNumber1 += remainder1 * base;
        decimalNumber2 += remainder2 * base;
        temp1 /= 10;
        temp2 /= 10;
        base *= 8; // Update the base (8, 8^2, 8^3, ...)
    }

    // Perform addition in decimal
    long long result_Dec = decimalNumber1 + decimalNumber2;

    // Convert the result back to octal
    long long remainder;
    int oct_nums[] = {0, 1, 2, 3, 4, 5, 6, 7};
    int index = 0;
    int octal[20];

    while (result_Dec > 0) {
        remainder = result_Dec % 8;
        octal[index++] = oct_nums[remainder];
        result_Dec /= 8;
    }

    // Print the result in octal
     cout << "\n==============================================================\n";
    cout << " The Octal number is: ";
    for (int i = index - 1; i >= 0; i--) {
        cout << octal[i];
    }
    cout << "\n";
    cout << "==============================================================\n";
            cout << "Thank you for using our program!\n";

    return 0;}

       //============================================================
        //============================================================

else if (num1 ==3) {
     cout << "                            (Decimal addition)                                   \n";
      cout << "                           ********************                                    \n\n\n";
      long long  num1, num2;
    bool invalid = false;
    cout << "Enter the two decimal numbers:";
   cin >> num1 >> num2;
   if (!num1 ) {
     cout << "\n==============================================================\n";
       cout << "invalid input" << "\n";
     cout << "==============================================================\n";
            cout << "Thank you for using our program!\n";
       return 1;
   }
   if (num1> 99999999999999 || num1 < 0) {
       invalid = true;
   }
   
   while (invalid) {
     cout << "==============================================================\n";
       cout << "invalid input" << "\n";
     cout << "==============================================================\n";
            cout << "Thank you for using our program!\n";
       return 1;

   }
 
   if (!num2) {
     cout << "==============================================================\n";
       cout << "invalid input. " << "\n";
       cout << "==============================================================\n";
            cout << "Thank you for using our program!\n";
       return 1;
   }
   if (num2 > 9999999999999999 || num2< 0) {
       invalid = true;
   }
   while (invalid) {
     cout << "==============================================================\n";
       cout << "invalid input." << "\n";
       cout << "==============================================================\n";
            cout << "Thank you for using our program!\n";
       return 1;

   }
   long long  addition = num1 + num2;
    cout << "==============================================================\n";
   cout << "the addition of two numbers is :" << " " << addition << "\n";
   cout << "==============================================================\n";
            cout << "Thank you for using our program!\n";
    return 0;
}

//===================================================================================================================

else if (num1 ==4) {
    cout << "                            (Hexa addition)                                    \n";
    cout << "                           *****************                                     \n\n\n";
   
long long n1 ,n2;
    long long digit_of_n1,digit_of_n2;
    cout << "Enter the digits of first number in your hexadecimal number: ";
    cin >>digit_of_n1 ;
    if (digit_of_n1 <= 0 ||digit_of_n1 > 16) {
        cout << "Invalid number of digits! \nExiting program.\n";
          cout << "==============================================================\n";
            cout << "Thank you for using our program!\n";
        return 1;
    }
    cout << "Enter the digits of second number in your hexadecimal number: ";
    cin >>digit_of_n2 ;
    if (digit_of_n2 <= 0 ||digit_of_n2 > 16) {
        cout << "Invalid number of digits! \nExiting program.\n";
          cout << "==============================================================\n";
            cout << "Thank you for using our program!\n";
        return 1;
    }
    char hexanumber1[16],hexanumber2[16];
    cout << "Please enter the first hexadecimal number: ";
    for (int i = 0; i < digit_of_n1; i++) {
        cin >> hexanumber1[i];
if (!((hexanumber1[i] >= '0' && hexanumber1[i] <= '9') ||(hexanumber1[i] >= 'A' && hexanumber1[i] <= 'F') ||(hexanumber1[i] >= 'a' && hexanumber1[i] <= 'f'))) {
            cout << "Invalid hexadecimal digit detected! \nExiting program.\n";
              cout << "==============================================================\n";
            cout << "Thank you for using our program!\n";
            return 1;
        }
    }
    cout << "Please enter the second hexadecimal number: ";
    for (int i = 0; i < digit_of_n2; i++) {
        cin >> hexanumber2[i];
if (!((hexanumber2[i] >= '0' && hexanumber2[i] <= '9') ||(hexanumber2[i] >= 'A' && hexanumber2[i] <= 'F') ||(hexanumber2[i] >= 'a' && hexanumber2[i] <= 'f'))) {
            cout << "Invalid hexadecimal digit detected!\n Exiting program.\n";
              cout << "==============================================================\n";
            cout << "Thank you for using our program!\n";
            return 1;
        }
    }
    long long totaldecimal1=0 , totaldecimal2=0;
    for (int i = 0; i <digit_of_n1 ; i++) {
        int n1;
        if (hexanumber1[i] >= '0' && hexanumber1[i] <= '9') {
            n1 = hexanumber1[i] - '0';
        }
         else if (hexanumber1[i] >= 'A' && hexanumber1[i] <= 'F') {
            n1 = hexanumber1[i] - 'A' + 10;
        }
         else if (hexanumber1[i] >= 'a' && hexanumber1[i] <= 'f') {
            n1 = hexanumber1[i] - 'a' + 10;
        }
totaldecimal1 = totaldecimal1*16+n1 ;
if(totaldecimal1>9223372036854775807){
   cout << "the number exceeded the allowed limit!\n";
     cout << "==============================================================\n";
            cout << "Thank you for using our program!\n";
    return 1;
}
    }
    for (int i = 0; i <digit_of_n2 ; i++) {
        int n2;
        if (hexanumber2[i] >= '0' && hexanumber2[i] <= '9') {
            n2 = hexanumber2[i] - '0';
        }
         else if (hexanumber2[i] >= 'A' && hexanumber2[i] <= 'F') {
            n2 = hexanumber2[i] - 'A' + 10;
        }
         else if (hexanumber2[i] >= 'a' && hexanumber2[i] <= 'f') {
            n2 = hexanumber2[i] - 'a' + 10;
        }
totaldecimal2 = totaldecimal2* 16 + n2 ;
if(totaldecimal2>9223372036854775807){
   cout << "the number exceeded the allowed limit!\n";
     cout << "==============================================================\n";
            cout << "Thank you for using our program!\n";
    return 1;
}
    }
   long long  addition = totaldecimal1 + totaldecimal2 ,remainder;
   char hex_nums[] = { '0', '1', '2', '3', '4', '5', '6', '7', '8', '9', 'A', 'B', 'C', 'D', 'E', 'F' };
    int  index = 0;
    char hexa[64];
    if (addition==0) {
        cout << "the sum of two hexadecimal numbers is: "<< addition ;
            return 0;
    }
    while (addition > 0) {
        remainder = addition % 16;
        hexa[index++] = hex_nums[remainder];
        addition /= 16;
    }
    cout << "the sum of two hexadecimal numbers is :" << " ";
    for (int i = index - 1; i >= 0;i--) {

        cout << hexa[i];
    }
    cout << "\n";
    return 0;
      cout << "==============================================================\n";
            cout << "Thank you for using our program!\n";
}}
break;
// subtraction
//********************************************************************************************************************************

 case 3:{
{cout << "What is the type of subtraction do you want to do ? \n" <<endl;
cout << " 1) Binary.                 2) Octal. \n 3) Decimal.                4) Hexa. \n";
cout << "==============================================================\n";
// Ask the user about the process that he wants to do
int num1;
cin >> num1 ;
if (!num1)
{cout << "Invalid number! Please enter acorrect number from 1 to 4." << endl;
cout << "==============================================================\n";
       cout << "Thank you for using our program!\n";
return 1;}
if (num1>4 || num1<1)
{cout << "==============================================================\n";
    cout << "Invalid number! Please enter acorrect number from 1 to 4." << endl;
    cout << "==============================================================\n";
       cout << "Thank you for using our program!\n";
    return 0;
}
// To make sure that the number is correct
else if (!num)
{cout << "==============================================================\n";
cout << "Please enter acorrect number from 1 to 4" << endl;
cout << "==============================================================\n";
       cout << "Thank you for using our program!\n";
    return 0;}

//==============================================================================
else if (num1 ==1) {
    // we convert the two binary numbers to decimal and convert the result to binary
    cout << "                            (Binary subtraction)                                   \n";
    cout << "                           ***********************                                     \n\n\n";
   int num1, num2, subtraction;
            int decimal2 = 0, decimal1 = 0;
            int base = 1;
           
            cout << "Enter 2 Binary numbers: ";
                cin >> num1 >> num2;
                cout << "==============================================================\n";
                 if (!(num1 > 0 && num2 > 0)) {
            cout << "\nPlease enter only positive numbers\n";
                  cout << "==============================================================\n";
            cout << "Thank you for using our program!\n";
    return 0;
            }
            while (num1 != 0) {
                int digit = num1 % 10;
                if (digit !=0 && digit != 1)
                {
                   
                   cout << "Invalid input ! ";
                    cout << "\n==============================================================\n";
            cout << "Thank you for using our program!\n";
    return 0;
                }
                decimal1 += digit * base;
                num1 /= 10;
                base *= 2;
            }
            base = 1;
            while (num2 != 0) {
                int digit = num2 % 10;
                if (digit !=0 && digit != 1)
                {
                   
                   cout << "Please enter only 0 or 1 ";
                   cout << "\n==============================================================\n";
            cout << "Thank you for using our program!\n";
    return 0;
                }
                decimal2 += digit * base;
                num2 /= 10;
                base *= 2;
            }
            subtraction = decimal1 - decimal2;
            if (subtraction <0 )
            { 
                cout<<"The first number must be greater than the second number.\n"<<endl;
         cout << "==============================================================\n";
            cout << "Thank you for using our program!\n"; 
            return 0;}
            int y = 1, sum = 0, counter = 0;
            cout << "\nThe result is : ";
            while (y * 2 <= subtraction) // counts number of digits and returns n to the power of counter 
            {
                y *= 2;
                counter++;
            }
            for (int i = counter; i >= 0; i--) {
                if (y == 0) {
                    y = 1;
                }
                if (sum + y <= subtraction) {
                    cout << 1;
                    sum += y;
                }
                else {
                    cout << 0;
                }
                y /= 2;
            }
            cout << endl;
              cout << "\n==============================================================\n";
            cout << "Thank you for using our program!\n";
    return 0;      
   }
   
    //============================================================
    //============================================================
   if (num1 == 2) {
        cout << "                             (Octal subtraction)                                   \n";
        cout << "                           ***********************                                    \n\n\n";
        
    int octalNumber1, octalNumber2, remainder1, remainder2;
    bool invalidFound;

    do {
        // Input the first octal number
        cout << "Enter the two octal numbers : ";
        cin >> octalNumber1, octalNumber2;

        // Check if the number is within valid range
        if (octalNumber1 < 0 || octalNumber1 > 999999) {
            cout << "Invalid octal number!" << endl;
              cout << "==============================================================\n";
             cout << "Thank you for using our program!\n";
            return 1;
        }

        // Check if the number is within valid range
        if (octalNumber2 < 0 || octalNumber2 > 999999) {
            cout << "Invalid octal number!" << endl;
              cout << "==============================================================\n";
            cout << "Thank you for using our program!\n";
              return 1;
        }

        // Verify that the entered numbers are valid octal numbers
        invalidFound = false;

        // Check the validity of the first number
        int temp1 = octalNumber1;
        while (temp1 > 0) {
            remainder1 = temp1 % 10;
            if (remainder1 > 7) {
                cout << "The digit " << remainder1 << " is invalid in the octal system!" << endl;
                invalidFound = true;
            }
            temp1 /= 10;
        }

        // Check the validity of the second number
        int temp2 = octalNumber2;
        while (temp2 > 0) {
            remainder2 = temp2 % 10;
            if (remainder2 > 7) {
                cout << "The digit " << remainder2 << " is invalid in the octal system!" << endl;
                invalidFound = true;
                  cout << "==============================================================\n";
            cout << "Thank you for using our program!\n";
            }
            temp2 /= 10;
        }

    } while (invalidFound);

    // Convert the first octal number to decimal
    int decimalNumber1 = 0, decimalNumber2 = 0, base = 1;

    int temp1 = octalNumber1;
    while (temp1 > 0) {
        remainder1 = temp1 % 10;
        decimalNumber1 += remainder1 * base;
        base *= 8;
        temp1 /= 10;
    }

    // Convert the second octal number to decimal
    base = 1;
    int temp2 = octalNumber2;
    while (temp2 > 0) {
        remainder2 = temp2 % 10;
        decimalNumber2 += remainder2 * base;
        base *= 8;
        temp2 /= 10;
    }

    // Check if the first number is greater than the second
    if (decimalNumber1 < decimalNumber2) {
        cout << "Invalid input! The first number must be greater than the second number." << endl;
          cout << "==============================================================\n";
            cout << "Thank you for using our program!\n";
        return 1;
    }

    // Subtract the two numbers in decimal
    int result_Dec = decimalNumber1 - decimalNumber2;

    // Convert the result from decimal to octal
    int octalResult[20];
    int index = 0;

    if (result_Dec == 0) {
        octalResult[index++] = 0; // If the result is zero
    } else {
        while (result_Dec > 0) {
            octalResult[index++] = result_Dec % 8;
            result_Dec /= 8;
        }
    }

    // Print the result in octal
    cout << "Subtraction result in octal: ";
    for (int i = index - 1; i >= 0; i--) {
        cout << octalResult[i];
    }
    cout << endl;
      cout << "==============================================================\n";
            cout << "Thank you for using our program!\n";
        return 0;
    }

    // ============================================================
    // ============================================================

    else if (num1 == 3) {
        cout << "                            (Decimal subtraction)                                   \n";
        cout << "                           ************************                                    \n\n\n";

        long long num1, num2;
        bool invalid = false;
        cout << "Enter the two decimal numbers: ";
        cin >> num1 >> num2;
        if (!num1) {
            cout << "Invalid input" << "\n";
            cout << "==============================================================\n";
            cout << "Thank you for using our program!\n";
            return 1;
        }
        if (num1 > 99999999999999 || num1 < 0) {
            invalid = true;
        }
        while (invalid) {
            cout << "Invalid input" << "\n";
            cout << "==============================================================\n";
            cout << "Thank you for using our program!\n";
            return 1;
        }

        if (!num2) {
            cout << "Invalid input." << "\n";
            cout << "==============================================================\n";
            cout << "Thank you for using our program!\n";
            return 1;
        }
        if (num2 > 9999999999999999 || num2 < 0) {
            invalid = true;
        }
        while (invalid) {
            cout << "Invalid input." << "\n";
            cout << "==============================================================\n";
            cout << "Thank you for using our program!\n";
            return 1;
        }
        long long subtraction = num1 - num2;
        cout << "The subtraction of two numbers is: " << subtraction << "\n";
        cout << "==============================================================\n";
        cout << "Thank you for using our program!\n";
        return 0;
    }

    return 0; 
}}
break;
//*********************************************************************************************************************************

case 4: {cout << " \n Thank you for using our program ! \n ============================================================" << endl;
break;
}

}
    return 0;
}}
