18-07-2025

## Progress:
* Understood that in aggregation, one class contains a reference to another class, but does not own its lifecycle.
* Practiced implementation using a Student and Marksheet example, where the Marksheet object was passed into the constructor and managed outside the class.

**AGGREGATION** 
``` java
class College{
	String  collegeName;
	String location;
	
	College(String clgName, String loc){
		this.collegeName = clgName;
		this.location = loc;
	}
}


// College object is created 
// independently outside the Student class
//  and passed into it.

// If the Student is deleted, the College still exists.

// It's a weaker relationship — Student has-a College,
// but doesn’t own it.
class Student{
	String name;
	int rollNumber;
	College college;
	
	Student(String n, int r, College college){
		this.name = n;
		this.rollNumber = r;
		this.college = college;
	}
	
	void displayInfo(){
		System.out.println("Student name: " + name);
		System.out.println("Roll number: " + rollNumber);
		System.out.println("College name: " + college.collegeName);
		System.out.println("College location: " + college.location);
		
	}
}

public class MainAggregation{
	public static void main(String[] args){
		College myClg = new College("SGTB Khalsa College" , "Delhi");
		Student student = new Student("Taran", 18, myClg);
		
		student.displayInfo();
	}
}
```


* Learned that in composition, one class completely owns another class by creating its instance within itself.
* Understood that if the container object is destroyed, the composed object should also be destroyed.
* Practiced a question where Student created a new Marksheet inside its constructor — then learned this was incorrect if a Marksheet was passed in from outside (a mistake that helped deepen clarity).

**COMPOSITION**
``` java
class Marksheet{
	int sub1Marks;
	int sub2Marks;
	
	Marksheet(int sub1Marks, int sub2Marks){
		this.sub1Marks = sub1Marks;
		this.sub2Marks = sub2Marks;
	}
	
	int getTotalMarks(){
		return sub1Marks + sub2Marks;
	}
}


class Student{
	String name;
	int rollNumber;
	private Marksheet marksheet;

	
	Student(String name , int rollNumber, Marksheet marksheet){
		this.name = name;
		this.rollNumber = rollNumber;
		this.marksheet = marksheet;
	}
	
	void displayInfo(){
		System.out.println("Name: " + name);
		System.out.println("Roll number: " + rollNumber);
		System.out.println("Total marks: " + marksheet.getTotalMarks());
	}
}

public class MainComposition{
	public static void main(String[] args){
		Marksheet m = new Marksheet(78,89);
		Student student = new Student("Taran", 23,m);
		
		student.displayInfo();
	}
}
```

## Challenges:
* Solved one question each on aggregation and composition.
* Corrected a mistake in composition implementation, which clarified the difference in object instantiation logic.

## Key Takeaway:
* Aggregation vs Composition is mainly about ownership and object lifecycle.
* Composition = stronger relationship, class creates and manages the contained object.
* Aggregation = weaker relationship, object is shared or passed in from outside.
* The decision between using this.object = new Object() vs this.object = object; depends on whether the class should create the dependency or receive it.
