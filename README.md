# Queue-data-structure
Queue data structure

### Overview

FIFI: First In First Out    
LILO: Last In Last Out

This works just like a movie line.  The first person in line will be the first person to get their ticket. Last person will be the last one to get their ticket. 

```
added first                                     added last
    10 -> 20 -> 30 -> 40 -> 50 -> 60 -> 70 -> 80 -> 90
```

It is also possible to reverse the order.  For instance, remove 90 first and then so on down the line.    

Enque: the process of adding an element to the queue.  Use ```.append()``` method.    

Dequeue: the process of removing an element from the queue. To remove the element from the front we use ```.pop(0)``` and to remove from the end ```.pop()```


#### Queues and lists

* A simple queue append example.  This builds a list from left to right.

```
queue = []
queue.append(10)
queue.append(20)
queue.append(30)
queue.append(40)

print(queue)  // [10, 20, 30, 40]
```
* To remove the number 10 from the list

```
queue.pop(0)
```

* A simple insert example.  This builds a list from right to left.
```
queue = []
queue.insert(0, 10)
queue.insert(0, 20)
queue.insert(0, 30)
queue.insert(0, 40)

print(queue) // [40, 30, 20, 10]
```
* To remove the number 10 from the list
```
queue.pop()
```

* To check if the queue is empty
```
not queue
```

#### A simple example with user input
```
queue = []

def enqueue():
    element = input("Enter the element:")
    queue.append(element)
    print(element, "is added to queue")
    
def dequeue():
    if not queue:
        print("the queue is empty")
    else:
        e = queue.pop(0)
        print("removed element: ", e)
        
def display():
    print(queue)
    
while True:
    print("Select the operation 1. add 2. remove 3. show 4. quit")
    choice = int(input())
    if choice == 1:
        enqueue()
    if choice == 2:
        dequeue()
    if choice == 3:
        display()
    if choice == 4:
        break
    else:
        print("Enter the correct operation")
```

### Queue using classes

Adding and deleting elements from the queue comes with choices

```
 appendleft() -> --------------------------------- <- append()
 
 popleft() ->  ----------------------------------- <- pop()

```
So, we can use appendleft() to append items to the right.  We can use append() to append items to the left.    
We can popleft() items off from the left.  We can pop() off items from the right.  
