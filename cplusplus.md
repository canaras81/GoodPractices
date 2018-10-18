1) Use ++i instead of i++ if i value is not used before the increment.
2) Class getters should be const functions.
3) Class setters' input parameters should be const references (e.g. const int &)
4) If you have a user-defined destructor, then you most probably need a user-defined copy constructor and assignment operator too.
5) If you have a continuous enumeration (e.g. 0,1,2,...) without any special value assignments, then add <ENUM_NAME>\_LAST as the last element so that any value larger than that can right away be rejected by the users of the enum by comparing with <ENUM_NAME>\_LAST value.
6) Do a final review of your newly created classes to answer the questions: Should your objects be copy-able? Assignable? Compareable? If the answer to any is NO, then declare the related member function as private in the class.
7) Good Knowledge: "inline" keyword can be used to tell a confused compiler (multiply-defined symbols) to trust the developer and use any of the symbol's instances for a function that is "defined, not just declared" in a header file.
