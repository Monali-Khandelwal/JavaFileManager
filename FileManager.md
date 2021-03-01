# FileManager

An amazingly useful tool!

We have 3 classes in this package. 
Console
FileManager
FileOperator

Our main method is in FileManager class. We are creating a fileManager object called app. Now we are calling the handleUserInput by the object app and returning it to the int status. 

In the handleUserInput method, a sendIntro method
is called. The sendIntro method is printing a string of commands through class Console, sendMessage method. Then there is a while loop with an argument this.running. Then the promptForString is called from thr Console class.

The promptForString method is using the scanner object s to take user input by a prompt message. The input is accepted in lower case and is trimmed. If the promptforString msg is null or empty, then a message is sent "Did nothing, as you commanded."; else if the user inputs help, then the sendIntro method will be called; else processCommand method will be called. 

The processCommand method has switch statement. 
first case is "list":
it is using fileops object and calling .list method from the class FileOperator. 
The list method has an object named path1. There is an if statement which says that if path1 exists and path1 is a directory then add a list to an array called lista. If the length of lista is 0 then output "Folder is empty.". For each string in the array lista, output a message, else send message "Wrong path entered!"

The second case in the switch statement is "info" which is calling .info method from the FileOperator class. This is using an if condition. If the object path1 exists, then the method returns name, absolute path, relative path, length, created and updated date of the file, else it will display "Wrong path entered!"

The third case is "mkdir" which creates the directory if the name is valid and doesn't contain any of these special characters "\\ / : ? * \" < > |". This also checks that the folder doesn't exist with the same name. 

Next is the rename command which takes the old file name and new file name as input and renames it. Before renaming, it also checks if the new file name already exists. 

The 5th and 6th case is "copy" and "move" which executes in conjunction. This first calls the method performCopyMove, which asks the user to Enter a path of file/folder they would like to copy/move. The copyCutDir method is called. If the destination folder doesn't exist, it will create one. 
It also asks to Enter destination path. If the command is a move, then it will delete the file from the original location and move it to the new location. If the command is a copy, then it will just create another copy at the new location without deleting the existing. 
The "delete" case first checks if it is a directory or a file. If file exists, it deletes it, else the directory is deleted by calling the deletedir method. 

The "quit" case checks if the user has entered a quit command no more action is needed. 