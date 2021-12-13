The primary purpose of constness is to provide documentation and prevent programming mistakes. Const allows you to make it clear to yourself and others that something should not be changed. Moreover, it has the added benefit that anything that you declare const will in fact remain const short of the use of forceful methods (which we'll talk about later). It's particularly useful to declare reference parameters to functions as const references:

“Const” uses simply in bullets
•	Make an unchangeable variable
           int const x = 5;
•	Make an unchangeable pointer (what it refers to)
           int x;
int * const p_int = &x;

•	Make an unchangeable pointer (what it contains)
        const int *p_int;

•	Make an unchangeable iteration (to make sure the process will be the same)

std::vector<int> vec;
vec.push_back( 3 );
vec.push_back( 4 );
vec.push_back( 8 );
 
for ( std::vector<int>::const_iterator itr = vec.begin(), end = vec.end(); 
      itr != end;
      ++itr )
{
        // just print out the values...
        std::cout<< *itr <<std::endl;
}

•	Make an unchangeable reference (to const parameters)
1	bool verifyObjectCorrectness (const myObj& obj);





“&” uses simply in bullets
•	Logical-and: if ( ( a>1 ) && (b<0) ) ...
•	Bitwise-and: x = a&b; Corresponding bits are and ‘ed (e.g., 0&1 -> 0)
•	Bitwise-and-assign: x &= y; Means the same as: x = x&y;
•	Address-of operator: p = &x; Read: Assign to p (a pointer) the address of x.
•	The additional use of & (in parameters) in C++
