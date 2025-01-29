## Public Access Modifier

````java[]

class Teacher {
    public String name;
    
    public void teach() {
        System.out.println(name + " is teaching.");
    }
}

class Student {
    public String studentName;

    public void study() {
        System.out.println(studentName + " is studying.");
    }
}

public class Main {
    public static void main(String[] args) {
        Teacher teacher = new Teacher();
        teacher.name = "Mr.Sri";  // Accessing public variable
        teacher.teach();  // Accessing public method

        Student student = new Student();
        student.studentName = "Ram";  // Accessing public variable
        student.study();  // Accessing public method
    }
}


````

## Private Access Modifier:


````java[]

class Teacher {
    private String name;  // This cannot be accessed from outside the class
    
    private void teach() {
        System.out.println(name + " is teaching.");
    }
    
    public void setName(String name) {
        this.name = name;  // Setting the value using a public method
    }

    public void getName() {
        System.out.println(name);  // Getting the value using a public method
    }
}

class Student {
    private String studentName;
    
    public void setStudentName(String studentName) {
        this.studentName = studentName;
    }

    public void study() {
        System.out.println(studentName + " is studying.");
    }
}

public class Main {
    public static void main(String[] args) {
        Teacher teacher = new Teacher();
        teacher.setName("Mr. Sri");  // Accessing private variable through a setter method
        teacher.getName();  // Accessing private variable through a getter method

        Student student = new Student();
        student.setStudentName("Ram");  // Accessing private variable through a setter method
        student.study();  // Accessing public method
    }
}


````

## Protected Access Modifier:

````java[]

class Teacher {
    protected String name;

    protected void teach() {
        System.out.println(name + " is teaching.");
    }
}

class Student extends Teacher {
    public void study() {
        name = "Mr. Sri";  // Accessing protected variable from superclass
        teach();  // Accessing protected method from superclass
        System.out.println("Student is studying.");
    }
}

public class Main {
    public static void main(String[] args) {
        Student student = new Student();
        student.study();
    }
}


````

## Default Access Modifier

````java[]

class Teacher {
    String name;  // Default access modifier
    
    void teach() {  // Default access modifier
        System.out.println(name + " is teaching.");
    }
}

class Student {
    public void study() {
        Teacher teacher = new Teacher();
        teacher.name = "Mr. Sri";  // Accessing default variable within the same package
        teacher.teach();  // Accessing default method within the same package
        System.out.println("Student is studying.");
    }
}

public class Main {
    public static void main(String[] args) {
        Student student = new Student();
        student.study();
    }
}


````


