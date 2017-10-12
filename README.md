# AutomationTest

package javaOne;

import java.util.Scanner;

public class ChapterTwoExercise
{
	public static void main(String args[])
	{
		int i, j, k;
		i = j = k = 2;
		System.out.println(i + " " + j + " " + k);

		System.out.println("25/4 is " + 25/4);

		System.out.println();

		//2.1 
		System.out.println("2.1");
		System.out.println("Enter a degree in Celsius: ");
		Scanner input = new Scanner(System.in);
		double celsius = input.nextDouble();
		double fahrenheit = 9.0 / 5.0 * celsius + 32.0;
		System.out.println(celsius + " Celsius is " + fahrenheit + " Fahrenheit.");

		System.out.println();

		//2.2
		System.out.println("2.2");
		System.out.println("Enter the radius and length of a cylinder: ");
		//Scanner input2 = new Scanner(System.in);
		double radius = input.nextDouble();
		double length = input.nextDouble();

		final double PI = 3.14159;
		double area = radius * radius * PI;
		double volume = area * length;

		System.out.println("The area is " + area + ".");
		System.out.println("The volume is " + volume + ".");

		System.out.println();

		//2.3
		System.out.println("2.3");
		System.out.println("Enter a value for feet: ");
		double feet = input.nextDouble();
		double feetToMeter = feet * 0.305; 
		System.out.println(feet + " feet is " + feetToMeter + " meters.");

		System.out.println();

		//Converting meters to feet
		System.out.println("Enter a value for meter: ");
		double meter = input.nextDouble();
		double meterToFeet = meter * 1.0 / 0.305;
		System.out.println(meter + " meter is " + meterToFeet + " feets.");

		System.out.println();

		//2.4
		System.out.println("2.4");
		System.out.println("Enter a number in pounds: ");
		double pound = input.nextDouble();
		double poundToKilogram = pound * 0.454;
		System.out.println(pound + " pounds is " + poundToKilogram + " kilograms.");

		System.out.println();

		//Converting kilograms to pounds
		System.out.println("Enter a number in kilograms: ");
		double kilogram = input.nextDouble();
		double kilogramToPound = kilogram * 1.0 / 0.454;
		System.out.println(kilogram + " kilograms is " + kilogramToPound + " pounds.");

		System.out.println();

		//2.5
		System.out.println("2.5");
		System.out.println("Enter the subtotal and a gratuity rate: ");
		double subTotal = input.nextDouble();
		double gratuity = input.nextDouble();
		double gratuityRate = gratuity / 100 * subTotal;			
		double total = subTotal + gratuityRate; 
		System.out.println("The gratuity is $" + gratuityRate + " and total is $" + total + ".");

		System.out.println();

		//2.6
		System.out.println("2.6");
		System.out.println("Enter a number between 0 and 1000: ");
		int integer = input.nextInt();
		int first = integer / 10; //first stores the quotient (the result: ex: 24/6 = 4 is the quotient)
		int remainder1 = integer % 10; //remainder 1 stores the remainder. Ex: 93/10, the remainder is 3
		int second = first / 10; //second takes the quotient from first variable and divides it by 10
		int remainder2 = first % 10; //remainder2 takes remainder from the quotient of first variable divides it by 10 
		int sum = remainder1 + remainder2 + second; 
		System.out.println("The sum of the digits is " + sum + ".");

		System.out.println();

		//2.7
		System.out.println("2.7");
		System.out.println("Enter the number of minutes: ");
		int minute = input.nextInt();
		int year = minute / 525600; // (1 / 60) * (1 / 24) * (1 / 365) 
		int remainingMinutes = minute % 525600;
		int day = remainingMinutes / 1440; //(1 / 60) * (1 / 24)
		System.out.println(minute + " minutes is approximately " + year + " years and " + day + " days.");

		System.out.println(); 

		//2.8????????
		//System.out.println("Enter the time zone offset to GMT: ");




		System.out.println();

		//2.9
		System.out.println("2.9");
		System.out.println("Enter v0, v1, and t: ");
		double initialVelocity = input.nextDouble();
		double finalVelociy = input.nextDouble();
		double time = input.nextDouble();
		double averageAcceleration = (finalVelociy - initialVelocity) / time;
		System.out.println("The average acceleration is: " + averageAcceleration); 

		System.out.println();

		//2.10
		System.out.println("2.10");
		System.out.println("Enter the amount of water in kilograms: ");
		double M = input.nextDouble(); //M = weight of water in kilograms							
		System.out.println("Enter the initial temperature: ");
		double initialTemperature = input.nextDouble(); //Temperatures are in Celsius
		System.out.println("Enter the final temperature: ");
		double finalTemperature = input.nextDouble();
		double Q = M * (finalTemperature - initialTemperature) * 4184;
		System.out.println("The energy needed is: " + Q + "."); 

		System.out.println();

		//2.11 
		System.out.println("2.11");
		double birthRateInSeconds = 7.0;
		double deathRateInSeconds = 13.0;
		double newImmigrantInSeconds = 45.0;
		double currentPopulation = 312032486;

		System.out.println("Enter the number of years: ");
		int yearA = input.nextInt();

		double secondsInYears = 60 * 60 * 24 * 365; //(60 sec/1 min) * (60 min/1 sec) * (24 hr/1 day) * (365 day/1 year)

		double numBirths = secondsInYears / birthRateInSeconds;
		double numDeaths = secondsInYears / deathRateInSeconds;
		double numImmigrants = secondsInYears / newImmigrantInSeconds;

		//currentPopulation += year * (numBirths + numImmigrants - numDeaths);
		//System.out.println("The population in " + year + " years is " + (int)currentPopulation + ".");

		//lines 150 and line 151 can be replaced by lines 154 and 155
		double population = currentPopulation + yearA * (numBirths + numImmigrants - numDeaths);
		System.out.println("The population in " + yearA + " years is " + (int)population + "."); 

		System.out.println();

		//2.12
		System.out.println("2.12");
		System.out.println("Enter speed: ");
		double speed = input.nextDouble();
		System.out.println("Enter the acceleration: ");
		double acceleration = input.nextDouble();
		double lengthA = (speed * speed ) / (2 * acceleration);
		System.out.println("The minimum runway length for this airplane is " + lengthA + "."); 

		System.out.println();

		//2.13
		System.out.println("2.13");
		System.out.println("Enter the monthly saving amount: ");
		double principal = input.nextInt();
		double firstMonth = principal * (1 + 0.00417);
		double secondMonth = (principal + firstMonth) * (1 + 0.00417);
		double thirdMonth = (principal + secondMonth) * (1 + 0.00417);
		double fourthMonth = (principal + thirdMonth) * (1 + 0.00417);
		double fifthMonth = (principal + fourthMonth) * (1 + 0.00417);
		double sixthMonth = (principal + fifthMonth) * (1 + 0.00417);

		System.out.println("After the sixth month, the account value is " + sixthMonth + "."); 

		System.out.println();

		//2.14
		System.out.println("2.14");
		System.out.println("Enter weight in pounds: ");
		double weightInPounds = input.nextDouble();
		double weightInKilograms = weightInPounds * 0.45359237;		
		System.out.println("Enter height in inches: ");
		double heightInInches = input.nextDouble();
		double heightInMeters = heightInInches * 0.0254; 
		double BMI = weightInKilograms / (heightInMeters * heightInMeters); 

		System.out.println("BMI is " + BMI); 

		System.out.println();

		//2.15
		System.out.println("2.15");
		System.out.println("Enter x1 and y1: ");
		double x1 = input.nextDouble();
		double y1 = input.nextDouble();
		System.out.println("Enter x2 and y2: ");
		double x2 = input.nextDouble();
		double y2 = input.nextDouble();

		double distance = Math.sqrt((x2 - x1) * (x2 - x1) + (y2 - y1) * (y2 - y1)); 
		//or use double distance = Math.pow(Math.pow(x2 - x1, 2) + Math.pow(y2 - y1, 2), 0.5);
		System.out.println("The distance between the two points is " + distance + "."); 

		System.out.println();

		//2.16
		System.out.println("2.16");
		System.out.println("Enter the side: ");
		double side = input.nextDouble();
		double areaOfHexagon = ((3 * Math.sqrt(3)) / 2) * (side * side);
		System.out.println("The area of the hexagon is " + areaOfHexagon + "."); 

		System.out.println();

		//2.17
		System.out.println("2.17");
		System.out.println("Enter the temperature in Fahrenheit between -58°F and 41°F: ");
		double temperature = input.nextDouble();
		System.out.println("Enter the wind speed (>=2) in miles per hour: ");
		double windSpeed = input.nextDouble();
		double windChill = 35.74 + 0.6215 * temperature - 35.75 * Math.pow(windSpeed, 0.16) + 0.4275 * temperature * Math.pow(windSpeed, 0.16);
		System.out.println("The wild chill index is " + windChill); 

		System.out.println();

		//2.18
		System.out.println("2.18");
		System.out.println("a   b   pow(a, b)");
		System.out.println("1   2   " + (int)Math.pow(1, 2));
		System.out.println("2   3   " + (int)Math.pow(2, 3));
		System.out.println("3   4   " + (int)Math.pow(3, 4));
		System.out.println("4   5   " + (int)Math.pow(4, 5));
		System.out.println("5   6   " + (int)Math.pow(5, 6)); //this way doesn't work: Math.pow((int)5, (int)6);
		System.out.println("6   7   " + (int)Math.pow(6, 7)); 
		
		System.out.println();
		
		//2.19
		System.out.println("2.19");
		System.out.println("Enter three points for a triangle: ");
		double x1A = input.nextDouble();
		double y1A = input.nextDouble();
		double x2A = input.nextDouble();
		double y2A = input.nextDouble();		
		double x3 = input.nextDouble();
		double y3 = input.nextDouble();
		
		//double side1 = Math.pow(Math.pow(x2 - x1, 2) + Math.pow(y2 - y1, 2), 0.5);
		//double side2 = Math.pow(Math.pow(x3 - x2, 2) + Math.pow(y3 - y2, 2), 0.5);
		//double side3 = Math.pow(Math.pow(x1 - x3, 2) + Math.pow(y1 - y3, 2), 0.5);
		
		//or use:
		double side1 = Math.sqrt((x2A - x1A) * (x2A - x1A) + (y2A - y1A) * (y2A - y1A)); 
		double side2 = Math.sqrt((x3 - x2A) * (x3 - x2A) + (y3 - y2A) * (y3 - y2A)); 
		double side3 = Math.sqrt((x1A - x3) * (x1A - x3) + (y1A - y3) * (y1A - y3)); 
		
		double sideA = (side1 + side2 + side3) / 2;
		double areaA = Math.sqrt(sideA * (sideA - side1) * (sideA - side2) * (sideA - side3));
		System.out.println("The area of the triangle is: " + areaA); 
		
		System.out.println();
		
		//2.20
		System.out.println("2.20");
		System.out.println("Enter balance and interest rate (e.g., 3 for 3%): ");
		double balance = input.nextDouble();
		double annualInterestRateA = input.nextDouble();
		double interest = balance * (annualInterestRateA / 1200);
		System.out.println("The interest is: " + interest); 
		
		System.out.println();
		
		//2.21
		System.out.println("2.21");
		System.out.println("Enter investment amount: ");
		double investmentAmount = input.nextDouble();
		System.out.println("Enter annual interest rate in percentage: ");
		double annualInterestRate = input.nextDouble();
		double monthlyInterestRate = annualInterestRate / 1200; //1200 because monthlyInterestRate = annualInterestRate / (100 * 12 months)
		System.out.println("Enter number of years: ");
		double numberOfYears = input.nextDouble();
		double futureInvestmentValue = investmentAmount * Math.pow(1 + monthlyInterestRate, numberOfYears * 12);
		
		System.out.println("Accumulate value is: " + futureInvestmentValue); 
		
		System.out.println();
		
		//2.22
		System.out.println("2.22");
		System.out.println("Enter an amount, for example 1156: ");
		double amount = input.nextDouble();
		double remainingAmount = amount / 100; //0.56 left
		
		//Find the number of one dollars
		int numberOfOneDollars = (int) remainingAmount; //11 dollars
		double remainingAmountInCents = amount % 100; //store 56 cents
		
		System.out.println(amount + " represents " + numberOfOneDollars + " dollars and " + remainingAmountInCents + " cents.");
		
		//Find the number of quarters in the remaining amount
		int numberOfQuarters = (int) (remainingAmountInCents / 25); //stores 2 quarters
		remainingAmountInCents = remainingAmountInCents % 25; //store 6 cents
		
		//Find the number of dimes in the remaining amount
		int numberOfDimes = (int) (remainingAmountInCents / 10);
		remainingAmountInCents = remainingAmountInCents % 10; 
		
		//Find the number of nickels in the remaining amount
		int numberOfNickels = (int) (remainingAmountInCents / 5); 
		remainingAmountInCents = remainingAmountInCents % 5;
		
		//Find the number of pennies in the remaining amount
		int numberOfPennies = (int) remainingAmountInCents;
		
		System.out.println("Your amount " + amount + " consists of");
		System.out.println("     " + numberOfOneDollars + " dollars");
		System.out.println("     " + numberOfQuarters + " quarters ");
		System.out.println("     " + numberOfDimes + " dimes");
		System.out.println("     " + numberOfNickels + " nickels");
		System.out.println("     " + numberOfPennies + " pennies"); 
		
		System.out.println();
		
		//2.23
		System.out.println("2.23");
		System.out.println("Enter the driving distance: ");
		double drivingDistance = input.nextDouble();
		System.out.println("Enter miles per gallon: ");
		double milesPerGallon = input.nextDouble();
		System.out.println("Enter price per gallon: ");
		double pricePerGallon = input.nextDouble();
		double costOfDriving = (drivingDistance / milesPerGallon) * pricePerGallon;
		
		System.out.println("The cost of driving is: $" + costOfDriving);

	}
}
