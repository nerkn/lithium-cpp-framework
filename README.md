# Experinces with lithium framework
A backend framework should provide 
* auth (user login/logout/)
* db connectivity
* easy access to url params
* json tools
* developer friendly
It seems lithium first 4 of those, compiled program failed without error and lack of examples to follow.


## My code is NOT working.

* while compiling I got error : [MySql connection read error: expected primary-expression before ',' token #107](https://github.com/matt-42/lithium/discussions/107)

    auto [name, age] = connection("select name, age from users where id = 42;").read<std::string, int>();



* Could compile after changing function 

    std::string email; int balance;
    connection("select email, balance from users limit 1 ").read(email, balance);

    but now I got no error but program quits abnormally, without any error.
