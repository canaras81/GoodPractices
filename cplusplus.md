1) Use ++i instead of i++ if i value is not used before the increment.
2) Class getters should be const functions.
3) Class setters' input parameters should be const references (e.g. const int &)
4) If you have a user-defined destructor, then you most probably need a user-defined copy constructor and assignment operator too.
