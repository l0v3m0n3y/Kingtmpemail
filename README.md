# Temp_mail_best
web api for temp-mail.best Forget about spam, advertising mailings, hacking and attacking robots. Keep your real mailbox clean and secure. Temp Mail provides temporary, secure, anonymous, free, disposable email address.
# main
```cpp
#include "Temp_mail_best.h"
#include <iostream>

int main() {
   Temp_mail_best api;
    auto email = api.generate_email().then([](json::value result) {
        std::cout << result<< std::endl;
    });
    email.wait();
    
    return 0;
}
```

# Launch (your script)
```
g++ -std=c++11 -o main main.cpp -lcpprest -lssl -lcrypto -lpthread -lboost_system -lboost_chrono -lboost_thread
./main
```
