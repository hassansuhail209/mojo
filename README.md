# mojo
Mojo is a inter-process communication (IPC) system used to  communicate  different processes. The Mojo Interface Defined Language (IDL) is an essential component of the Mojo framework, allowing developers to define interfaces for communication between different programming languages, such as TypeScript and C++.
The Mojo IDL tells the messages and their formats, ensuring that all parties involved understand how to communicate.

How to make communication channel between two languages using the mojo IDL.

1) Create a mojom inteface

        interface MessagingService {
          ConnectToChannelHandle(string name) => (Handle handle);
          SendMessage(string message);
        };
   
3) Generate stub and proxy
 
     **Stub** is the client side representation of remote , stub is an autogenerated file created by tools like mojom_bindings_generator (generate various types of 
     fils based on mojo interface like cpp , java , js etc ).

     **Proxy** acts as a server-side component that receives messages sent by client-side stubs.
   
