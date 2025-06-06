1.Car Java

 Public class car {

    Private string plateNumber;

    Private string model;

    Private Boolean isavailable;



    Public car (string plateNumber, string model) {

        This.platenumber = platenumber;

        This.Model = model;

        This.isavailable = true;

    }



    Public string getplatenumber () {

        Return to platinambar;

    }



    Public string getmodel () {

        Return model;

    }



    Public Boolean Isavailable () {

        Return Isavailable;

    }



    Public zero rental () {

        Isavailable = wrong;

    }



    Public zero returns () {

        Isavailable = truth;

    }



    @Override

    Public string tostring () {

        Return Model + “(“ + Platenumber + “) –“ + (Isavailable? “Available”: “on rent”));

    }

}



2.Rental Transaction Java

Import java.time.localdate;



Public rent on rent {

    Private customer customer;

    Private car car;

    Private local rentaldate;



    Public Rentalization (Customer Customer, Car Car) {

        This.customer = customer;

        This.car = car;

        This.Rentaldate = localdate.Now ();

        This.car.Rentcar ();

    }



    Public zero returns () {

        Car.returncar ();

    }



    @Override

    Public string tostring () {

        Customer + “Returned” + Car + “” “ + Retaldate;

    }

}



3.Rental Agency Java

Import java.util.ArrayList;



Public class RentalAgency {

    Private ArrayList<Car> cars = new ArrayList<>();

    Private ArrayList<RentalTransaction> transactions = new ArrayList<>();



    Public void addCar(Car car) {

        Cars.add(car);

    }



    Public void rentCar(String plateNumber, Customer customer) {

        For (Car car : cars) {

            If (car.getPlateNumber().equals(plateNumber) && car.isAvailable()) {

                RentalTransaction rt = new RentalTransaction(customer, car);

                Transactions.add(rt);

                System.out.println(“Car rented: “ + rt);

                Return;

            }

        }

        System.out.println(“Car not available.”);

    }



    Public void displayCars() {

        For (Car car : cars) {

            System.out.println(car);

        }

    }

}



4.Customer Java

Public class Customer {

    Private String name;

    Private String licenseNumber;



    Public Customer(String name, String licenseNumber) {

        This.name = name;

        This.licenseNumber = licenseNumber;

    }



    Public String getName() {

        Return name;

    }



    Public String getLicenseNumber() {

        Return licenseNumber;

    }



    @Override

    Public String toString() {

        Return name + “ (License: “ + licenseNumber + “)”;

    }

}



5.Login System 

Import java.Io.Console,. 

Import java.Util.Scanner,. 





Public class main {. 

String username = “admin”; 

String password = “1234”; 





Public static void main(string[] args) {. 

If (Login() == false) return; 





newRentalAgency(): 

Agency.Addcar(new car(“kdg123a”, “toyota corolla”)),. 

Agency.Addcar(new car(“kaa456b”, “honda fit”)),. 





Customer customer = new customer(“alice”, “dl12345”); 





System.Console.WriteLine(“\navailable cars:”),. 

```:





System.Console.WriteLine(“\nrenting a car..”); 

```: 



System.Console.WriteLine(“\nupdated car list:”),. 

AgencyDisplaycars(),: 

} 



Public static boolean login() {. 

Scanner scanner = new Scanner(System.in); 

Console console = system.Console(),. 

Int attempts = 3,. 



While (attempts > 0) { 

System.Console.Write(“enter username: “),. 

String inputUser = scanner.NextLine(),; 



String inputPassed = “”;

If (console!= null) { console.log(“Result”); } 

Char[] passwordchars = console.Readpassword(“enter password: “),. 

Inputpass = new string(passwordchars),. 

} 

System.Console.Write(“enter password: “),. 

Inputpass = maskpassword(),. 

} 



If (inputuser == username && inputpass == password) {. 

System.Console.WriteLine(“login successful.\n”); 

Return true, 

} 

Attempts--,: 

System.Console.WriteLine(“incorrect login.”); “ + attempts),. 

} 

} 



System.Console.WriteLine(“Too many failed attempts. Exiting”),:

Return false; 

} 



Public static string maskpassword() {. 

Scanner scanner = new Scanner(System.in); 

StringBuilder password = new stringbuilder(),; 

Try {. 

While (accurate) {. 

Int ch = system.In.Read(),. 

If (ch == ‘\n’) break,. 

Password.Append((char) ch),. 

SystemOutPrint(“”);: 

} 

} catch (exception e) { 

System.Console.WriteLine(“error reading password.”),. 

} 

Return password.tostring().trim(),. 

} 
