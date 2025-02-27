# 6 Days of Solidity

### Day 1 Making the Zombie Factory

In NutShell it's all about the basics of whole solidity programming language and I will bet you will get more excited to learn more in this Course.
    
  CHAPTER 1: LESSON OVERVIEW:
    
    In Starting you will get to know that what is our main mission and at the end what you want to achieve. 
    Basically we are going to make Zombiefactory in which zombie get created so we will be going to implement 
    such feature so that user can easily make their own choice of Zombie.
    
  CHAPTER 2: Contracts
   
    Contracts is nothing just the piece of code which get migrated into blockchain and once it get migrated into 
    blockchain it become immutable.
    Do take care of this line as well before writing solidity. It is just kind of compiler version. 
    pragma solidity >=0.5.0 <0.6.0; 
   
  CHAPTER 3: State Variables & Integers  
    
    State variables are permanently stored in contract storage. This means they're written to the Ethereum blockchain.    
    Unsigned Integers: (uint) It is non-negative integers.
    Signed Integers: (int) for any integers in solidity.
    
  CHAPTER 4: Math Operations
   
    Addition Operation => (3 + 2) >= 5
    Subtraction Operation => (3 - 2) => 1
    Multiplication Operation => (3 * 2) => 6
    Division Operation => (3 / 2)  => 1 (Gives the Quotient value)
    Modulo Operation => (3 % 2) => 1 (Gives the Remainder value)
    Exponentiation Opeerartion => (2 ** 3) => 8 (Gives the Power value)
    
  CHAPTER 5: Structs
  
    Struct is similar to that we had learnt in C,C++ nothing special here too. 
    It allows us to create our data Type in simple terms.
    In this Course we are using beacuse it will hold the basic charcteristic of our Zombie. (Initially the name and DNA).
    
  CHAPTER 6: Arrays  
    
    Array is a common Data Structure in every Programming language.Everyone know how it works and its feature,its useCase.
    
    In Solidity also two types of Array are present:
    Fixed Size Array -> As name suggest we have to give the size before hand.
    Dynamic Array -> Again name Suggest we don't have to give the actual size before hand, it can keep growing.
    
    Public Arrays - It is nothing but we just give the array scope by public means we can access it from any contract,
    Also by default it will create its getter method by solidity.
    
    Declaration of array
    Fixed Size Array = uint[5] fxd;
    Dynamic Array = uint[] dyn;
    
  CHAPTER 7: Function Declarations
  
    Function is used in programming to write better cdes. It also helps to remove redundancy in our code.
    
    Decalaration:
       
       function  nameOfFunction( string _str, uint _y) public {
       
                //write code here
        }  
    
    Little About Argument & Parameter that are used in function.
    
    In function declaration we pass Parameters.It can be used in two ways:
    
        1) Pass by Value => It means it will create a new copy of what you are passing as Argument while calling 
           the function. In this it will not affect your original argument.
        2) Pass by reference => It means it will not create any copy,it just use the address of argument that 
           you are passing.while calling the function.But It will manipulate your original argument.
                 
           We use memory for pass by Value in Solidity.
           
           Example:
           function exmaple(string memory _name, uint memory _age) public {
           }
            
    In function call we pass argument. example: nameofFunction("Aman" , 20); 
    
    
  CHAPTER 8: Working With Structs and Arrays
    
    In this Lesson you will be goin to use struct and array together. It is not complicate that it looks initially.
    
    -> You know how to create Array.
    -> you know how to make struct.
    -> Now just change the data Type of Array with struct name. In this way that array will become the struct Array to hold
       Zombie feature such as name,dna.
       
    To Insert into Array take help of push() function it come handy with array.

  CHAPTER 9: Private / Public Functions
    
    Private Function -> It will be used only in that contract where it defined.
    Public Function ->  From any where we can access it.
    
    Be Cautiuos with public function beacuse it causes vulnerabilities issue in our code. So, better use Private instead Public. 
    
  CHAPTER 10: More on Functions:
     
    Return Values: It is completely depend upon the return type of function,if function type is string then it will return string only.
    
       Example: 
       
       uint numbePlate = 5955;      
       function _taxiNumber() private returns (uint memory)
       {
            return numberPlate;
       }
    
    Function Modifiers: So, It is actually new to me and very suprising to see that function also have modifiers.
        
        There is two types of Function Modeifiers we have in Solidity.
        
        View - In View it doesn't change the function at all it just allow us to look inside function.
            
            Example:
            
            string name = "Aman";
            function test( --- here we are not passing any parameter ---) private view returns (string memory)
            {
                return name;
            }
            
        Pure - But using Pure we can modify our function for sure but with our parameter only. it will not access any 
        other elemnet in our code.
        
            Example:
           
            function test(uint _a,uint _b) private view returns (uint)
            {
                return a + b;
            }
            
        Note: It may be hard to remember when to mark functions as pure/view. Luckily the Solidity compiler is 
        good about issuing warnings to let you know when you should use one of these modifiers.
           
    
  CHAPTER 11 & 12: Keccak256 and Typecasting
        
        Keccak256 is just the random hashing genrator.For Random generation of DNA for our Zombies.
        
            Declaration Example:
                keccak256(abi.encodePacked("aaaab"));
        
        TypeCasting we know changing the data type in between our code of any variable as per our useCase.
            
            Example:
                bytes eg;           
                uint test = uint(eg);
                
        At last In this will pretty much completed our lesson just put it all together to make whole code work.Hurray!!!             
    
  CHAPTER 13: Events
  
        Events are a way for your contract to communicate that something happened on the blockchain to your app front-end, 
        which can be 'listening' for certain events and take action when they happen.
        
            Declaration example:
            
                event IntegersAdded(uint x, uint y, uint result);
                emit IntegersAdded(_x, _y, result);
        
    
  CHAPTER 14: Web3.js
          
          In this Chapter you will get a little glimpse of web3.0, how it is going to work.
          Ethereum has a Javascript library called Web3.js.
          
          Now In Chapter 15 you make your own Zombie and share with friends.


### Day 2 Zombies Attack Their Victims
        
In this Module we are going to add Multiplayer feature as well as adding some extra feature in creating Zombie army.
  
  CHAPTER 1: Lesson 2 Overview:
    
     Zombie Feeding :  When a zombie feeds, it infects the host with a virus. The virus then turns the host into a new 
                       zombie that joins your army.The new zombie's DNA will be calculated from the previous zombie's 
                       DNA and the host's DNA.
                          
  CHAPTER 2: Mappings and Addresses
  
    Addresses: The Ethereum blockchain is made up of accounts, which you can think of like bank accounts. An account has a balance 
               of Ether (the currency used on the Ethereum blockchain), and you can send and receive Ether payments to other accounts, 
               just like your bank account can wire transfer money to other bank accounts.
   
  
    Mapping:   A mapping is essentially a key-value store for storing and looking up data. In the first example, the key is an 
               address and the value is a uint, and in the second example the key is a uint and the value a string.
 
   
  CHAPTER 3: Msg.sender  
  
    Now that we have our mappings to keep track of who owns a zombie, we'll want to update the _createZombie method to use them.

    In order to do this, we need to use something called msg.sender.

    msg.sender : In Solidity, there are certain global variables that are available to all functions. One of these is msg.sender, 
                 which refers to the address of the person (or smart contract) who called the current function.
    
  CHAPTER 4: Require
    
    In lesson 1, we made it so users can create new zombies by calling createRandomZombie and entering a name. However, if users 
    could keep calling this function to create unlimited zombies in their army, the game wouldn't be very fun.
    
    Thus require is quite useful for verifying certain conditions that must be true before running a function.
   
    
  CHAPTER 5: Inheritance
    
    Our game code is getting quite long. Rather than making one extremely long contract, sometimes it makes sense 
    to split your code logic across multiple contracts to organize the code.
    
    Inheritance provide the code reusibilty feature.
    
  CHAPTER 6: Import  
  
    Our code was getting pretty long, so we split it up into multiple files to make it more manageable. 
    This is normally how you will handle long codebases in your Solidity projects.

    When you have multiple files and you want to import one file into another, Solidity uses the import keyword.
    
  CHAPTER 7: Storage vs Memory (Data location)
  
    Storage refers to variables stored permanently on the blockchain. 
    
    Memory variables are temporary, and are erased between external function calls to your contract. 
    Think of it like your computer's hard disk vs RAM.
    
  CHAPTER 8: Zombie DNA
    
    The formula for calculating a new zombie's DNA is simple: the average between the feeding zombie's DNA and the target's DNA.
    
    Using thsi we will Calculate:
    uint newZombieDna = (zombieDna + targetDna) / 2;
    
  CHAPTER 9: More on Function Visibility
  
    Internal is the same as private, except that it's also accessible to contracts that inherit from this contract.
    External is similar to public, except that these functions can ONLY be called outside the contract — they can't 
    be called by other functions inside that contract.


  CHAPTER 10: What Do Zombies Eat?
    
    CryptoZombies love to eat... CryptoKitties!
    In order to do this we'll need to read the kittyDna from the CryptoKitties smart contract. We can do that because 
    the CryptoKitties data is stored openly on the blockchain.
    
    By including this interface in our dapp's code our contract knows what the other contract's functions look like, 
    how to call them, and what sort of response to expect.Now let's declare our interface for the CryptoKitties contract.
    
  CHAPTER 11: Using an Interface

    Continuing our previous example with NumberInterface, once we've defined the interface as:

    contract NumberInterface {
      function getNum(address _myAddress) public view returns (uint);
    }
    
  CHAPTER 12: Handling Multiple Return Values
  
    This getKitty function is the first example we've seen that returns multiple values. Let's look at how to handle them:          
    
  Bonus: Kitty Genes

    Let's make it so zombies made from kitties have some unique feature that shows they're cat-zombies.
    To do this, we can add some special kitty code in the zombie's DNA.

    If you recall from lesson 1, we're currently only using the first 12 digits of our 16 digit DNA to determine 
    the zombie's appearance. So let's use the last 2 unused digits to handle "special" characteristics.

    We'll say that cat-zombies have 99 as their last two digits of DNA (since cats have 9 lives). 
    So in our code,we'll say if a zombie comes from a cat, then set the last two digits of DNA to 99.

### Day 3 Learnings

Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.

### Day 4 Learnings

Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.

### Day 5 Learnings

Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.

### Day 6 Learnings

Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
