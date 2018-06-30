ProXPN.py Notes:
------------------------------------
The ProXPN.py script is written in Python 2.7 and uses OpenVPN (cli), as well as multiprocessing to allow the user to automatically log onto ProXPN and keep track of his/her IP address (to show when the connection drops).

ProXPN.py uses the auth-user-pass functionality of OpenVPN.
Create your ProXPN/OpenVPN auth-user-pass file as follows:
vi /<your/home/directory>/.openvpn/auth.txt

johndoe@emailprovider.com
<super_secret_password>

Make sure that the username and password are in clear text and that only the two lines 

Side-note, make sure you 'chmod 600' the auth.txt file to prevent other non-root users on your machine from being able to read it.

------------------------------------
Next, in the ProXPN configuration files, replace the line that reads:
auth-user-pass

with this:
auth-user-pass /<your/home/directory>/.openvpn/auth.txt

------------------------------------

The ProXPN.py application also creates a lock file and will automatically switch off wireless using rfkill, restarting it when complete. 

The user will need full sudo rights to use this application.
(%wheel	ALL=(ALL)	NOPASSWD: ALL)

Remember: "It is preferable not to travel with a dead man."
                --Henri Michaux
