import java.util.Scanner;

// Base class
class Cylinder {
    protected double radius;
    protected double height;
    protected double area;

    // Method to get input and compute the surface area of the Cylinder
    public void Area() {
        Scanner scanner = new Scanner(System.in);
        
        // Get input for radius and height
        System.out.print("Enter the radius of the cylinder: ");
        radius = scanner.nextDouble();
        
        System.out.print("Enter the height of the cylinder: ");
        height = scanner.nextDouble();
        
        // Compute the area using the given formula
        area = 2 * Math.PI * radius * radius + 2 * Math.PI * radius * height;
        
        // Display area
        System.out.println("Area of the cylinder: " + area);
    }
}

// Derived class
class CylinderVol extends Cylinder {
    private double volume;

    // Method to compute the volume of the Cylinder
    public void Volume() {
        // Compute the volume using the given formula
        volume = Math.PI * radius * radius * height;
        
        // Display volume
        System.out.println("Volume of the cylinder: " + volume);
    }
}

// Main class
public class Main {
    public static void main(String[] args) {
        // Create an object of CylinderVol class
        CylinderVol cylinderVol = new CylinderVol();
        
        // Calculate the area of the Cylinder
        cylinderVol.Area();
        
        // Calculate the volume of the Cylinder
        cylinderVol.Volume();
    }
}
