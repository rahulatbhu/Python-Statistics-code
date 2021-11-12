def payme(): 
    #get inputs from user 
    employeeName = input("Enter your name: ") 
    hourlyWage = eval(input("Enter hourly wage: ")) 
    hoursWorked = eval(input("Enter hours worked: ")) 
 
    #calculate wages 
    if hoursWorked > 40: 
        overTimeWages =  (hoursWorked - 40) * hourlyWage * 1.5 
        regularWages = 40 * hourlyWage 
    else: 
        overTimeWages = 0 
        regularWages = hoursWorked * hourlyWage 
 
    #calculate total wages 
    totalWages = overTimeWages + regularWages 
 
    #calculate total wages and medical insurance 
    taxes = totalWages * .20 
    medical = totalWages *.10 
 
    takeHomePay = totalWages - taxes - medical 
 
    print("This paycheck is for: ", employeeName) 
    print("Take home pay is: ", takeHomePay) 
    print("for ", hoursWorked, "hours worked at", hourlyWage) 
    print("Taxes are: ", taxes) 
    print("Medical insurance is: ", medical) 
 
payme() 
