# CODDSOFT
tasks = []

def addTask():
    task = input("Please enter a task:")
    tasks.append(task)
    print(f"Task '{task}' added to the list:")

def listTasks():
    if not tasks:
        print("There are no task currently :")
    else:
        print("Current Tasks:")
        for index, task in enumerate(tasks):
            print(f"Task #{index}. {task}")
            
def deleteTask():
    listTasks()
    try:
        taskToDelete = int(input("Enter the # want to delete:"))    
        if taskToDelete >=0 and taskToDelete < len(tasks):
            tasks.pop(taskToDelete)
            print(f"Task #{taskToDelete} has been removed: ")
        else:
            print(f"Task #{taskToDelete}  not found:")
    except:
        print("Invalid input.")
        
if __name__ == "__main__":
    
    print("Welcome to the To Do List App :) ")

while True:
    print("/n")
    print("Please select one of the following options :")
    print("___________________________________________")
    print("1.Add a new task")
    print("2.Delete a task")
    print("3.Task list")
    print("4.Quit")         # menu options
    
    #creating a variable called choice
    
    choice = input("Enter our choice: ")
    
    if(choice =="1"):
        addTask()
        
    elif(choice =="2"):
        deleteTask()
        
    elif(choice =="3"):
        listTasks()
        
    elif(choice =="4"):
        break  
    else:
        print("Invalid input.Please try again.")
        
    print("Welcome Again")
