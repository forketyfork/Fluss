from:: lobste.rs
url:: [What is io\_uring?](https://matklad.github.io/2024/09/32/-what-is-io-uring.html)
on:: 2024-09-24 14:39

`io_uring` is a new Linux kernel interface for making system calls, it allows to submit the calls asynchronously using batches; the application writes system call codes and arguments to a lock-free shared-memory ring buffer, the kernel writes the results to a second lock-free shared-memory ring buffer where they become available to the application asynchronously. This might improve performance but is not portable, and the feature is rather new.