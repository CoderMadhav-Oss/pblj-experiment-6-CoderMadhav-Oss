[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/pAwhWXY5)
import java.util.*;

class Employee implements Comparable<Employee> {
    int id;
    String name;
    double salary;

    // Constructor
    public Employee(int id, String name, double salary) {
        this.id = id;
        this.name = name;
        this.salary = salary;
    }

    // Implement compareTo for sorting by salary
    @Override
    public int compareTo(Employee other) {
        return Double.compare(this.salary, other.salary);
    }

    // Display method
    @Override
    public String toString() {
        return "Employee { ID: " + id + ", Name: " + name + ", Salary: " + salary + " }";
    }
}

public class EmployeeSort {
    public static void main(String[] args) {
        // Creating a list of employees
        List<Employee> employees = new ArrayList<>();
        employees.add(new Employee(101, "Alice", 50000));
        employees.add(new Employee(102, "Bob", 70000));
        employees.add(new Employee(103, "Charlie", 60000));

        // Sorting employees by salary
        Collections.sort(employees);

        // Display sorted employees
        System.out.println("Sorted Employee List (by Salary):");
        for (Employee e : employees) {
            System.out.println(e);
        }
    }
}
