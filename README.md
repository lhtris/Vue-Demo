## **Commands**

Your Ledis should be able to handle the following. Note that these are modeled after Redis commands, so feel free to refer to Redis manual when you have questions.

### **String**

- `SET key value`: set a string value, always overwriting what is saved under key
- `GET key`: get a string value at key

### **Set**

Set is an unordered collection of unique string values (duplicates not allowed).

- `SADD key value1 [value2...]`: add values to set stored at key
- `SREM key value1 [value2...]`: remove values from set. (Bonus: Show values are not removed (not exist) from set)
- `SMEMBERS` *key*: return an array of all members of a set
- `SINTER [key1] [key2] [key3] ...`: *(bonus)* set intersection among all set stored in specified keys. Return array of members of the result set. Ex: a: [1, 2, 3, 4], b: [2, 3, 4, 5], c: [3, 4, 5, 6]. The result of `SINTER a b c` is [3, 4]

### **Data Expiration**

- `KEYS`: List all available keys
- `DEL key`: delete a key
- `EXPIRE key seconds`: set a timeout on a key, *seconds* is a positive integer (by default a key has no expiration). Return the number of seconds if the timeout is set
- `TTL key`: query the time remaining of a key. Return a message if key does not have timeout.

### **Snapshot (bonus)**

- *SAVE*: save the current state in a snapshot
    - key1: ‘a’
    - key2: 1 2 3 4 5
- *RESTORE*: restore from the last snapshot,
    - 

### **Error Handling**

When an error happens, simply return “ERROR”, together with the cause of the error if possible. Example: *“ERROR: Key not found”*

## **Web CLI**

Please build a simple web-based CLI interface that allows users to enter commands and displays the result (this is just an example, you could build a different UI):