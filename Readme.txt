Here we are storing element in doubly linked list and we are maintaining the order like last recently used will at first ,after that second last recently used so the least recently used will be stored at last and we are taking map which will store the location of the key .it will help in deleting the key and getting the value of the key.

    when we get the key it will become last used.if the key is not present directly return -1.if key is present so we have to insert at first just after head.so now we need hashmap to store location of the node.so we can acces and dlete from that location and store just after head and update location of key to m[key]=head->next.

    if size of lru catche data structure is less than capacity then there can be two possibilities.

        may be key is present so we insert it just next to head and delete from the previous location and update the location of key in map i.e m[key]=head->next.

        may be key is not present then we will directly insert just after head i.e at first and store the location in map m[key]=head->next.

    here we are always inserting in the order of
    ->last used ->second last used ->third last used->least used

    if the size is equal to capacity so we have to maintain it so here can be two option
        Element we are inserting is present so we delete the node from double linked list and with help of map and insert just after head saying that it is last used and also update the location of the key.
        Element is not present in the cache so to maintain capacity we will delete the least used which will be stored at last i.e before tail .so we will delete that node from there and the new node should be inserted at first i.e just after head and also delete that key from map.

starting configuration of doubly linked list.

Doubly linked list
head<-->tail
Complexity

    Time complexity:O(1)O(1)O(1) Average get and put

    Space complexity:O(n)O(n)O(n)
