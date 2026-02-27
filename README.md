# Assignment-2-PDC

1. Why is message passing required in distributed systems?
In distributed systems, each process runs independently and has its own memory space. Since they cannot directly read or write each other’s data, message passing is necessary for communication. Through sending and receiving messages, processes can exchange information and coordinate their tasks.

2. What happens if one process fails?
When a process fails, other processes might continue waiting for a message that will never arrive. This can cause the program to hang or stop responding. In basic MPI implementations, there is often no built-in fault recovery, so a single failure can cause the entire program to terminate.

3. How does this model differ from shared-memory programming?
In a message-passing model, processes interact only by exchanging messages and do not share memory. In contrast, shared-memory programming allows processes to access the same memory space directly. While shared memory can be faster, it requires careful synchronization to prevent conflicts when multiple processes modify data at the same time.
