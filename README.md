# aug-29-task-2
This Repo Contains task 2 files and folders
1. Created the new repo in the git hub 
   name : aug-29-task-2

2. Add the java program 
   
        class calculator {
    public static void main(String[] args) {
        if (args.length < 3) {
            System.out.println("Usage: java SimpleCalculator <operation> <num1> <num2>");
            return;
        }

        int choice = Integer.parseInt(args[0]);
        double num1 = Double.parseDouble(args[1]);
        double num2 = Double.parseDouble(args[2]);

        double result = 0;
        
        switch (choice) {
            case 1:
                result = num1 + num2;
                break;
            case 2:
                result = num1 - num2;
                break;
            case 3:
                result = num1 * num2;
                break;
            case 4:
                if (num2 != 0) {
                    result = num1 / num2;
                } else {
                    System.out.println("Error: Division by zero is not allowed.");
                    return;
                }
                break;
            default:
                System.out.println("Invalid choice.");
                return;
        }

        System.out.println("Result: " + result);
    }
}

   * to compile the program i use the command as 
     javac calculator.java
   * to run the program
     java calculator (opt: 1) (num1: 20) + (num2: 30)


3. Create a new jenkins freestyle project
   -- i created the new job in jenkins named as
      name : calculator project
   -- check out the git repo.
      i check the repo by cloning the repo by using 
      Source Code Management
      i selected the git and i configured it.
   -- compile and run the java program.
      by selecting the -> Build Steps
                          Execute shell
                             ->  to compile 
                                 javac calculator.java
                             ->  to run the program
                                 java calculator (opt: 1) (num1: 20) + (num2: 30)
 		 
