# Python_training

def fun(name,delay):
    counter = 0
    while counter <5:
        counter+=1
        print(name)
        print(time.ctime())      
        time.sleep(delay)
    
t1 = threading.Thread(target=fun,args= ("dhoni",2))
t2 = threading.Thread(target=fun,args = ("virat",4))

t1.start()
t2.start()

t1.join()
t2.join()

def fun(name,lock):
    lock.acquire()
    new()
    print(name,token)
    lock.release()

token = 0
def new():
    global token
    token = token +1
    
lock = threading.Lock()    
t1 = threading.Thread(target=fun,args= ("dhoni",lock))
t2 = threading.Thread(target=fun,args = ("virat",lock))

t1.start()
t2.start()

t2.join()
t1.join()
