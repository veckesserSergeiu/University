public class University {

    static Teacher tech1 = new Teacher(1, "Ana");
    static Teacher tech2 = new Teacher(2, "Anatoliy");
    static Teacher tech3 = new Teacher(3, "Vladislav");
    static Teacher[] tech = new Teacher[3];

    public static void list() {
        tech[0] = tech1;
        tech[1] = tech2;
        tech[2] = tech3;
    }

    void goWork() {
        for (int i = 0; i < 3; i++) {
            tech[i].getGroop();
            tech[i].getName();
        }
    }

    public static void main(String[] args) {
        Teacher.list();
        Teacher.list2();
        Teacher.list3();
        University.list();
        System.out.println("Techers:");
        for (int i = 0; i < 3; i++) {
            System.out.print("Name: ");
            tech[i].getName();
            System.out.print(" Groop: ");
            tech[i].getGroop();
            System.out.println();
        }
        System.out.println();
        System.out.println("Students");
        System.out.println();
        System.out.println("1 groop:");
        Teacher.chekAgeName();
        System.out.println();
        System.out.println("2 groop:");
        Teacher.chekAgeName2();
        System.out.println();
        System.out.println("3 groop:");
        Teacher.chekAgeName3();
        System.out.println();
        System.out.println("Students metods:");
        System.out.println();
        Student stu = new Student(16, "Zeeman",5);
        stu.ageStudent();
        stu.markStudent();
        System.out.println();
        System.out.println("Teachers metod:");
        System.out.println();
        tech1.studentsMetods();
        System.out.println();
        tech3.studentsMetods3();
        System.out.println();
        tech2.studentsMetods2();
    }
}


public class Teacher {
    int groop;
    String name;

    static Student s1 = new Student(16, "Zeeman",5);
    static Student s2 = new Student(18, "Nazzy", 4);
    static Student s3 = new Student(21, "Yan", 3);
    static Student[] students = new Student[3];

    static void list() {
        students[0] = s1;
        students[1] = s2;
        students[2] = s3;
    }

    public static void chekAgeName() {
        for (int i = 0; i < 3; i++) {
            students[i].getAge();
            students[i].getName();
            students[i].getMarks();
            System.out.println();
        }
    }
    public void studentsMetods() {
        for (int i = 0; i < 3; i++) {
            students[i].markStudent();
            students[i].ageStudent();
        }
    }
    static Student s12 = new Student(25, "Danil",4);
    static Student s22 = new Student(27, "Hizen", 5);
    static Student s32 = new Student(30, "Yanoly", 3);
    static Student[] students2 = new Student[3];

    public static void list2() {
        students2[0] = s12;
        students2[1] = s22;
        students2[2] = s32;
    }

    public static void chekAgeName2() {

        for (int i = 0; i < 3; i++) {
            students2[i].getAge();
            students2[i].getName();
            students2[i].getMarks();
            System.out.println();
        }
    }
    public void studentsMetods2() {
        for (int i = 0; i < 3; i++) {
            students2[i].markStudent();
            students2[i].ageStudent();
        }
    }
    static Student s13 = new Student(27, "Roman",3);
    static Student s23 = new Student(30, "Mack", 4);
    static Student s33 = new Student(26, "Yango", 5);
    static Student[] students3 = new Student[3];

    public static void list3() {
        students3[0] = s13;
        students3[1] = s23;
        students3[2] = s33;
    }

    public static void chekAgeName3() {
        for (int i = 0; i < 3; i++) {
            students3[i].getAge();
            students3[i].getName();
            students3[i].getMarks();
            System.out.println();
        }
    }
    public void studentsMetods3() {
        for (int i = 0; i < 3; i++) {
            students3[i].markStudent();
            students3[i].ageStudent();
        }
    }

    Teacher(int inputGroop,String inputName){
        this.groop = inputGroop;
        this.name = inputName;
    }
    int getGroop() {
        System.out.print(this.groop+" ");
        return this.groop;
    }

    String getName() {
        System.out.print(this.name+" ");
        return this.name;
    }
}



public class Student {
    int marks;// поле
    private int age;
    String name;

    Student(int inputAge, String inputName, int inputMarks) {// конструктор
        this.age = inputAge;
        this.name = inputName;
        this.marks = inputMarks;
    }

    void markStudent() {
        System.out.println("my name is " + this.name + " and my mark is " + this.marks);
    }


    void ageStudent() {
        int retirement = 65 - this.age;
        System.out.println("my age is " + this.age + ". " + "And I'm " + retirement + " years old before retirement");
        System.out.println();
    }
    int getAge() {
        System.out.print("Age:"+this.age + " ");
        return this.age;
    }

    String getName() {
        System.out.print("Name:"+this.name + " ");
        return this.name;
    }

    int getMarks() {
        System.out.print("Marks:"+this.marks + " ");
        return this.marks;
    }
}


