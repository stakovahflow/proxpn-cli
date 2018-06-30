ProXPN.py Notes:
------------------------------------
The ProXPN.py script is written in Python 2.7 and uses OpenVPN (cli), as well as multiprocessing to allow the user to automatically log onto ProXPN and keep track of his/her IP address (to show when the connection drops).

The ProXPN.py application also creates a lock file and will automatically switch off wireless using rfkill, restarting it when complete. 

The user will need full sudo rights to use this application.
(%wheel	ALL=(ALL)	NOPASSWD: ALL)

Remember: "It is preferable not to travel with a dead man."
                --Henri Michaux
