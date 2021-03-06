**PRACTICES**
1) Use ++i instead of i++ if i value is not used before the increment.
2) Class getters should be const functions.
3) Class setters' input parameters should be const references (e.g. const int &)
4) If you have a user-defined destructor, then you most probably need a user-defined copy constructor and assignment operator too.
5) If you have a continuous enumeration (e.g. 0,1,2,...) without any special value assignments, then add <ENUM_NAME>\_LAST as the last element so that any value larger than that can right away be rejected by the users of the enum by comparing with <ENUM_NAME>\_LAST value.
6) Do a final review of your newly created classes to answer the questions: Should your objects be copy-able? Assignable? Compareable? If the answer to any is NO, then declare the related member function as private in the class.
7) If a function takes both input and output parameters in its parameter list, its signature should list the output variables first.
8) If a free function is only locallyy being used (that is only called by the other functions in the same file), then consider defining the free function as "static".
9) If you are writing to a database in a transactional mode (that is multiple related records in one commit), consider the failure scenarios for which you may have to "rollback". See your database documentation as every database may have different approaches to various issues during write-query execution.
10) Do NOT use the word *new* in naming functions/services/requests/etc. After all, everything new becomes old at some point. Use names that provide information about the context.
11) Do NOT simply name a function/request as *DataRequest*. Be specific and as verbose as necessary.

**GOOD TO KNOW**
1) "inline" specifier can be used to tell a confused compiler (multiply-defined symbols) to trust the developer and use any of the symbol's instances for a function that is "defined, not just declared" in a header file.
2) "explicit" specifier specifies that a conversion function (a constructor with a single non-default parameter since C++11) of a class is explicit, that is, it CANNOT be used for implicit conversions and copy-initialization.
