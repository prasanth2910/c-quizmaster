# c-quizmaster
#include<stdio.h>
#include<conio.h>
#include<ctype.h>
#include<stdlib.h>
#include<string.h>
void show_record();
void reset_score();
void help();
void edit_score(float , char []);
int main()
     {
     int countr,r,r1,count,i,n;
     float score;
     char choice;
     char playername[20];
     mainhome:
     system("cls");
     printf("\t\t\tC PROGRAM QUIZ GAME\n");
     printf("\n\t\t________________________________________");

     printf("\n\t\t\t   WELCOME ");
     printf("\n\t\t\t      to ");
     printf("\n\t\t\t   THE GAME ");
     printf("\n\t\t________________________________________");
     printf("\n\t\t________________________________________");
     printf("\n\t\t     !!!C-QUIZMASTER!!!    ") ;
     printf("\n\t\t________________________________________");
     printf("\n\t\t________________________________________");
     printf("\n\t\t > Press S to start the game");
     printf("\n\t\t > press H for help            ");
     printf("\n\t\t > press Q to quit             ");
     printf("\n\t\t________________________________________\n\n");
     choice=toupper(getch());
    if (choice=='H')
	{
	help();getch();
	goto mainhome;
	}
	else if (choice=='Q')
	exit(1);
    else if(choice=='S')
    {
     system("cls");

    printf("\n\n\n\n\n\n\n\n\n\n\t\t\tResister your name:");
     gets(playername);

    system("cls");
    printf("\n ------------------  Welcome %s to C Program Quiz Game --------------------------",playername);
    printf("\n\n Here are some tips you might wanna know before playing:");
    printf("\n -------------------------------------------------------------------------");
    printf("\n >> Your game starts with 3 Level. In this  you will be asked a");
    printf("\n    total of 10 questions. ");
    printf("\n >> You will be given 4 options and you have to press A, B ,C or D for the");
    printf("\n    right option.");
    printf("\n >> You will be asked questions continuously, till right answers are given");
    printf("\n >> No negative marking for wrong answers!");
    printf("\n\n\t!!!!!!!!!!!!! ALL THE BEST !!!!!!!!!!!!!");
    printf("\n\n\n Press Y  to start the game!\n");
    printf("\n Press any other key to return to the main menu!");
    if (toupper(getch())=='Y')
		{
		    goto home;
        }
	else
		{
        goto mainhome;
       system("cls");
       }

     home:
     system("cls");
     count=0;
     int opt;
     int up;
 Rep:    printf("\n\nChoose Option to Select the Level of Questions\n 1.Easy 2.Medium 3.Hard\n");
     scanf("%d",&opt);
     if(opt==1)
     {
     	i=1;
     	up=10;
	 }
	 else if(opt==2)
	 {
	 	i=11;
	 	up=20;
	 }
	 else if (opt ==3)
	 {
	 	i=21;
	 	up=30;
	 }
	 else 
	 { 
	    printf("Invalid Choice\n");
	 	goto Rep;
	 }
game:
     countr=0;
     for(;i<=up;i++)
     {system("cls");
     r=i;

     switch(r)
		{
		case 1:
		printf("\n\n Identify the C compiler of UNIX. ?");
        printf("\n\nA.GCC\t\tB.CC\n\nC.-VC\t\tD.NONE");
		if (toupper(getch())=='B')
			{printf("\n\nCorrect!!!");countr++;getch();
			 break;getch();}
		else
		       {printf("\n\nWrong!!! The correct answer is B.CC");getch();
		       goto score;
		       break;}

		case 2:
		printf("\n\n\n Which of the following operator can be used to access value at address stored in a pointer variable?");
		printf("\n\nA.*\t\tB.#\n\nC.&\t\tD.@");
		if (toupper(getch())=='A')
			{printf("\n\nCorrect!!!");countr++;getch();
			 break;}
		else
		       {printf("\n\nWrong!!! The correct answer is A.*");getch();
		      goto score;
		       break;
		       }

        case 3:
		printf("\n\n\nIn DOS, how many bytes exist for near, far and huge pointers? ");
		printf("\n\nA.  Near: 2, far: 4, huge: 7\t\tB.near: 4, far: 2, huge: 8\n\nC. near: 2, far: 4, huge: 4\t\tD. near: 4, far: 0, huge: 0");
		if (toupper(getch())=='C')
			{printf("\n\nCorrect!!!");countr++;getch();
			 break;}
		else
		       {printf("\n\nWrong!!! The correct answer is C. near: 2, far: 4, huge: 4");getch();
		       goto score;
		       break;}

        case 4:
		printf("\n\n\n Which of the following is not a storage class specifier in C?");
		printf("\n\nA.Auto\t\tB.Static\n\nC.Volatile\t\tD.all the above");
		if (toupper(getch())=='C')
			{printf("\n\nCorrect!!!");countr++;getch();
			 break;}
		else
		       {
                printf("\n\nWrong!!! The correct answer is C.Volatile");getch();
		       goto score;
		       break;
		       }

        case 5:
		printf("\n\n\nIn What does the 'sizeof' operator return in C?");
		printf("\n\nA.Coulomb\t\tB.Watt\n\nC.Power\t\tD.Units");
		if (toupper(getch())=='B')
			{printf("\n\nCorrect!!!");countr++;getch(); break;}
		else
		       {
		           printf("\n\nWrong!!! The correct answer is B.Power");
		       getch();
		       goto score;
		       break;
			
		       }

		case 6:
		printf("\n\n\nWhich of the following is not a logical operator?");
		printf("\n\nA.&&\t\tB.!\n\nC.||\t\tD.|");
		if (toupper(getch())=='D' )
			{printf("\n\nCorrect!!!");countr++;getch();
			 break;}
		else
		       {printf("\n\nWrong!!! The correct answer is D.|");goto score;
		       getch();
		       break;}

        case 7:
		printf("\n\n\nIn C, parameters are always?");
		printf("\n\nA.PASS BY VALUE\t\tB.PASS BY REFERENCE\n\nC.PASS BY VALUE RESULT\t\tD.NONE");
		if (toupper(getch())=='A')
			{printf("\n\nCorrect!!!");countr++;getch();
			 break;}
		else
		       {printf("\n\nWrong!!! The correct answer is A.PASS BY VALUE");getch();
		       goto score;
		       break;}

        case 8:
		printf("\n\n\nWhich one of the following is a loop construct that will always be executed once?");
		printf("\n\nA.for\t\tB.switch\n\nC.do while\t\tD.while");
		if (toupper(getch())=='C')
			{printf("\n\nCorrect!!!");countr++;getch(); break;}
		else
		       {printf("\n\nWrong!!! The correct answer is C.do while");getch();
		       goto score;
		       break;}

        case 9:
		printf("\n\n\n Directives are translated by the?");
		printf("\n\nA.compiler\t\tB.linker\n\nC.pre-processor\t\tD.editor");
		if (toupper(getch())=='C')
			{printf("\n\nCorrect!!!");countr++; getch();
			break;}
		else
		       {printf("\n\nWrong!!! The correct answer is C.pre-processor");getch();
		       goto score;
		       break;}

        case 10:
		printf("\n\n\n Each instance of a class has a different set of?");
		printf("\n\nA.class interfaces\t\tB.attribute values\n\nC.methods\t\tD.none");
		if (toupper(getch())=='B')
			{printf("\n\nCorrect!!!");countr++;getch(); break;}
		else
		       {printf("\n\nWrong!!! The correct answer is B.attribute values");getch();
			   goto score;
			   break;}

        case 11:
		printf("\n\n\nHow many instances of a class can be declared??");
		printf("\n\nA.6\t\tB.10\n\nC.as per required\t\tD.2");
		if (toupper(getch())=='C')
			{printf("\n\nCorrect!!!");countr++;getch();
			 break;}
		else
              {printf("\n\nWrong!!! The correct answer is C.as per required");getch();
              goto score;
			  break;}

        case 12:
		printf("\n\n\nWhat is the maximum number of characters that can be held in the string variable char address line [40]?");
		printf("\n\nA.39\t\tB.40\n\nC.41\t\tD.42");
		if (toupper(getch())=='A')
			  {printf("\n\nCorrect!!!");countr++;getch();
			   break;}
		else
              {printf("\n\nWrong!!! The correct answer is A.39");getch();
              goto score;
			  break;}

		case 13:
		printf("\n\n\nWhich of the following SLT template class is a container adaptor class??");
		printf("\n\nA.list\t\tB.vector\n\nC.deque\t\tD.stack");
		if (toupper(getch())=='D')
			{printf("\n\nCorrect!!!");countr++;getch();
			break;}
		else
		       {printf("\n\nWrong!!! The correct answer is D.stack");getch();
		       goto score;
			   break;}

        case 14:
		printf("\n\n\nWhat kinds of iterators can be used with vectors?");
		printf("\n\nA.Forward iterator\t\tB.Bi-directional iterator\n\nC.Random access iterator\t\tD.All of the above");
		if (toupper(getch())=='D')
			{printf("\n\nCorrect!!!");countr++;getch();
			 break;}
		else
		       {printf("\n\nWrong!!! The correct answer is D.All of the above");getch();
		       goto score;
			   break;}

		case 15:
		printf("\n\n\n Let p1 and p2 be integer pointers. Which one is a syntactically wrong statement?");
		printf("\n\nA.p1 = p1 + p2;\t\tB.p1 = p1 - 9;\n\nC.p2 = p2 + 9;\t\tD.cout << p1 - p2;");
		if (toupper(getch())=='A')
			{printf("\n\nCorrect!!!");countr++;getch();
			 break;}
		else
		       {printf("\n\nWrong!!! The correct answer is A.p1 = p1 + p2;");getch();
		       goto score;
		       break;}

		case 16:
		printf("\n\n\n The following statements are about EOF. Which of them is true?");
		printf("\n\nA. Its value is defined within stdio.h\t\tB. Its value is implementation dependent\n\nC.Its value can be negative\t\tD.All of the above");
		if (toupper(getch())=='D')
			{printf("\n\nCorrect!!!");countr++; getch();
			break;
			}
		else
		       {printf("\n\nWrong!!! The correct answer is D.All of the above");getch();
		       goto score;
		       break;}


		case 17:
		printf("\n\n\n _ is used to break out of a program?");
		printf("\n\nA.break\t\tB.continue\n\nC.terminate\t\tD.exit");
		if (toupper(getch())=='D')
			{printf("\n\nCorrect!!!");countr++; getch();
			break;}
		else
		       {printf("\n\nWrong!!! The correct answer is D.exit");getch();
			   goto score;
		       break;}

		case 18:
		printf("\n\n\nWhich is an indirection operator among the following");
		printf("\n\nA.&\t\tB.$\n\nC.!\t\tD.*\n\n");
		if (toupper(getch())=='D')
			{printf("\n\nCorrect!!!");countr++; getch();
			break;}
		else
		       {printf("\n\nWrong!!! The correct answer is D.*");getch();
			   goto score;
		       break;}

		case 19:
		printf("\n\n\n When a function is called by itself again and again, then it is?");
		printf("\n\nA.call by value\tB.call by reference\n\nC.recursion\tD.system function call\n\n");
		if (toupper(getch())=='C')
			{printf("\n\nCorrect!!!");countr++; getch();
			break;}
		else
		       {printf("\n\nWrong!!! The correct answer is C.recursion");getch();
			   goto score;
		       break;}

		case 20:
		printf("\n\n\nWhich can never be called by value using call by value method?");
		printf("\n\nA.structure\t\tB. union\n\nC. array\t\tD.all of these");
		if (toupper(getch())=='C')
			{printf("\n\nCorrect!!!");countr++; getch();
			break;}
		else
		       {printf("\n\nWrong!!! The correct answer is C. array");getch();
			   goto score;
		       break;}

		case 21:
		printf("\n\n\n What is the maximum number of arguments that can be passed in a single function ?");
		printf("\n\nA.324\t\tB.213\n\nC.342\t\tD.253 ");
		if (toupper(getch())=='D')
			{printf("\n\nCorrect!!!");countr++; getch();
			break;}
		else
		       {printf("\n\nWrong!!! The correct answer is D.253");getch();
			   goto score;
		       break;}

		case 22:
		printf("\n\n\nWhat can not be declared?");
		printf("\n\nA. Array of integers\t\tB.Array of pointers\n\nC.Array of structures\t\tD.None of the above");
		if (toupper(getch())=='D')
			{printf("\n\nCorrect!!!");countr++; getch();
			break;}
		else
		       {printf("\n\nWrong!!! The correct answer is D.None of the above");getch();
			   goto score;
		       break;}

		case 23:
		printf("\n\n\nWhich of the following is not a arithmetic operation?");
		printf("\n\nA.n/=10\t\tB.n*=10\n\nC.n!=10\t\tD.n+=10");
		if (toupper(getch())=='C')
			{printf("\n\nCorrect!!!");countr++; getch();
			break;}
		else
		       {printf("\n\nWrong!!! The correct answer is C.n!=10");getch();
			   goto score;
		       break;}
			   
		case 24:
		printf("\n\n\nWhich datatype is not applicable for mod(%) operation?");
		printf("\n\nA.data\t\tB.char\n\nC.int\t\tD.float");
		if (toupper(getch())=='D')
			{printf("\n\nCorrect!!!");countr++; getch();
			break;}
		else
		       {printf("\n\nWrong!!! The correct answer is D.float");getch();
			   goto score;
		       break;}	
			   
		case 25:
		printf("\n\n\n In C, order of passing arguments to a function is done?");
		printf("\n\nA.manually\t\tB.randomly\n\nC.left to right\t\tD.right to left");
		if (toupper(getch())=='D')
			{printf("\n\nCorrect!!!");countr++; getch();
			break;}
		else
		       {printf("\n\nWrong!!! The correct answer is D.right to left");getch();
			   goto score;
		       break;}
		case 26:
		printf("\n\n\nTo avoid repetition of code and bulky programs, statements are isolated inside a ?");
		printf("\n\nA.arrays\t\tB.Modules\n\nC.Header Files\t\tD. Functions");
		if (toupper(getch())=='D')
			{printf("\n\nCorrect!!!");countr++; getch();
			break;}
		else
		       {printf("\n\nWrong!!! The correct answer is D. Functions");getch();
			   goto score;
		       break;}
			 
		case 27:
		printf("\n\n\nIn pointers, meaning of ‘*’ is?");
		printf("\n\nA.pointer varaiable\t\tB.value at address\n\nC.value of address\t\tD.none of the above");
		if (toupper(getch())=='B')
			{printf("\n\nCorrect!!!");countr++; getch();
			break;}
		else
		       {printf("\n\nWrong!!! The correct answer is B. value at address");getch();
			   goto score;
		       break;}	   	
			   
		case 28:
		printf("\n\n\nWhen double is converted to float then the value is?");
		printf("\n\nA.Truncated\t\tB.Rounded\n\nC.Depends upon compiler\t\tD.None of the mentioned");
		if (toupper(getch())=='C')
			{printf("\n\nCorrect!!!");countr++; getch();
			break;}
		else
		       {printf("\n\nWrong!!! The correct answer is C.Depends upon compiler");getch();
			   goto score;
		       break;}	     
		case 29:
		printf("\n\n\nCan we declare function inside structure of C");
		printf("\n\nA.YES\t\tB.NO\n\nC.BOTH OF THEM\t\tD.NONE OF THEM");
		if (toupper(getch())=='B')
			{printf("\n\nCorrect!!!");countr++; getch();
			break;}
		else
		       {printf("\n\nWrong!!! The correct answer is B.NO");getch();
			   goto score;
		       break;}	    	  
		case 30:
		printf("\n\n\nWhich of the following is an ternary operator in C?");
		printf("\n\nA. &&\t\tB. %%\n\nC. !=\t\tD.?:");
		if (toupper(getch())=='D')
			{printf("\n\nCorrect!!!");countr++; getch();
			break;}
		else
		       {printf("\n\nWrong!!! The correct answer is D.?:");getch();
			   goto score;
		       break;}	       }
	score:
	    system("cls");
		printf("Your score is : %d",countr);
			 }}}
void help()
	{
		 system("cls");
    printf("\n\n                              HELP");
    printf("\n -------------------------------------------------------------------------");
    printf("\n ......................... C program Quiz Game...........");
    printf("\n >> There are three rounds, WARMUP ROUND & CHALLANGE ROUND");
    printf("\n >> In warmup round you will be asked a total of 3 questions to test your general");
    printf("\n    knowledge. You will be eligible to play the game if you can give atleast 2");
    printf("\n    right answers otherwise you can't play the Game...........");
    printf("\n >> Your game starts with the CHALLANGE ROUND. In this round you will be asked");
    printf("\n    total 10 questions each right answer will be awarded $100,000.");
    printf("\n    By this way you can win upto ONE MILLION cash prize in USD...............");
    printf("\n >> You will be given 4 options and you have to press A, B ,C or D for the");
    printf("\n    right option");
    printf("\n >> You will be asked questions continuously if you keep giving the right answers.");
    printf("\n >> No negative marking for wrong answers");

	printf("\n\n\t*********************BEST OF LUCK*********************************");
	printf("\n\n\t*****C PROGRAM QUIZ GAME is developed by NIT Delhi team********");
	}

