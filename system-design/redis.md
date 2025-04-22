## Redis

#### Why redis is fast

##### In-memory storage (RAM-based)
- Redis primarily stores data in RAM, enabling near-instantaneous access speeds (microseconds).
- While it supports persistence (RDB, AOF) for saving to disk, this is for backup purposes, not for primary access.
- Compared to disk-based databases (like PostgreSQL), Redis experiences less I/O bottleneck.

##### Single-threaded + Event loop
- Redis utilizes a single-threaded event loop based on the I/O multiplexing model (epoll/kqueue/select).
Advantages:
- No need for locking/access control like in multi-threaded systems → avoids context switching.
- Suitable for small, fast operations, such as incrementing counters, session storage, and lightweight queues.
- Redis can handle millions of requests per second with just one thread due to extremely low scheduling overhead.

##### Efficient data structures
- Redis supports various specialized data structures:
- String, Hash, List, Set, Sorted Set, HyperLogLog, Bitmap, Stream
- Each type is individually optimized for speed, memory usage, and access methods.
- For example: Sorted Sets use Skip Lists, Hashes use compact hash tables, Lists use quicklists (linked list + array).
