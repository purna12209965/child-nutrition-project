# bmiResult function to print the BMI Categories
def bmiResult(childName,bmi):
    if bmi<16:                        #if bmi<16-Severely Underweight
        print("BMI of {0} is {1} and he (she) is Severely Underweight.".format(childName,bmi))
    elif bmi>=16 and bmi<18.5:        #if bmi>=16 and bmi<18.5- Underweight
        print("BMI of {0} is {1} and he (she) is Underweight.".format(childName,bmi))
    elif bmi>=18.5 and bmi<25:        #if bmi>=18.5 and bmi<25-Healthy
        print("BMI of {0} is {1} and he (she) is Healthy.".format(childName,bmi))
    elif bmi>=25 and bmi<30:          #if bmi>=25 and bmi<30-Overweight
        print("BMI of {0} is {1} and he (she) is Overweight.".format(childName,bmi))
    elif bmi>=30:                     #if bmi>=30-Obese
        print("BMI of {0} is {1} and he (she) is Obese.".format(childName,bmi
                                                            
# Function bmiResult: This function takes a child's name and BMI as inputs, 
# and then prints out the BMI category based on predefined ranges. 
# It categorizes the child as "Severely Underweight," "Underweight," "Healthy," "Overweight," or "Obese" based on their BMI.
                                                                
# If the condition of the previous line is True (i.e., if the BMI is less than 16),
# this line prints a formatted string using the .format() method. 
# It fills in the placeholders {0} and {1} with the values of childName and bmi, respectively.
# This line informs the user that the child is severely underweight.


# caloriesCalculator function to calculate the total calories consumed by child in a day
def caloriesCalculator(calories):
    caloriesCount={"Milk":100,"Vegetables":85,"Meat":143,"Lentils":113,"Egg":155,"Rice":130}
    # dictionary that contains the calories contained in 100 gm of food they consumed
    totalCalories = 0
    for key, value in calories.items():
            calorie=value                      # calorie- total number of calories consumed by child
            while calorie!=0:
                if  calorie- 100 >= 0:        
                #if calories-100 is greater than 0 simply decrease the calorie and add the calories in 100 gm of food
                    calorie-= 100
                    totalCalories += caloriesCount[key]
                else:                             # else add the fraction of calorie
                    fraction = calorie/100
                    totalCalories +=  caloriesCount[key]* fraction
                    calorie = int(calorie - (caloriesCount[key] * fraction))
                    break
             
    return totalCalories   #returing the total calorie
# The caloriesCalculator function is designed to compute the total calories consumed by a child based on the quantities
# of different types of food they have eaten. The function takes a dictionary called calories as input,
# where each key represents a food type (such as "Milk," "Vegetables," "Meat," etc.), and 
# the corresponding value indicates the amount of that food consumed. 
# The function begins by initializing a variable totalCalories to keep track of the overall calorie count.

# It then iterates through each item in the calories dictionary using a loop, 
# where each item consists of a food type and the corresponding quantity consumed. 
# Inside the loop, the function calculates the total calories for each food type by 
# referring to a predefined caloriesCount dictionary. 
# This caloriesCount dictionary contains the calories contained in 100 grams of each food type.

# The function employs a while loop to manage the calculations for each food type. 
# It checks if subtracting 100 calories from the current food's calorie count is possible without going below zero. 
# If so, it deducts 100 calories and adds the predetermined calories for that food type to the totalCalories.

# If subtracting 100 calories would result in a negative value, the function calculates 
# the fraction of calories to be added based on the remaining amount. 
# It then adds the appropriate fraction of calories to totalCalories and updates 
# the remaining calorie count. The loop continues until the entire consumed amount has been processed.

# After iterating through all food types, the function returns the totalCalories value, 
# which represents the cumulative calories consumed by the child, 
# considering both complete 100-gram portions and any remaining fractional portions of food. 
# This function helps provide an accurate estimate of the child's total calorie intake, 
# which is crucial for assessing their nutritional status and well-being.







# nourishmentResult function to print the nourished status of child
def nourishmentResult(childName,childAge,totalCalorie):
    if childAge>=0 and childAge<2:      
        #if childAge>=0 and childAge<2 and totalCalories<800- under-nourished else nourished
        if totalCalories<800:
            print("The daily calorie consumption of {0} is 800 and he (she) is taking {1},he or she required more calories  and he or she is  under-nourished.".format(childName,totalCalories))
        else:
            print("The daily calorie consumption of {0} is 800 and he (she) is taking {1}, he or she is nourished.".format(childName,totalCalories))
    elif childAge>=2 and childAge<4:      
            ##if childAge>=2 and childAge<4 and totalCalories<1400- under-nourished else nourished
        if totalCalories<1400:
            print("The daily calorie consumption of {0} is 1400 and he (she) is taking {1},he or she required more calories  and he or she is  under-nourished.".format(childName,totalCalories))
        else:
            print("The daily calorie consumption of {0} is 1400 and he (she) is taking {1}, he or she is nourished.".format(childName,totalCalories))
    elif childAge>=4 and childAge<8:
            ##if childAge>=4 and childAge<8 and totalCalories<1800- under-nourished else nourished
        if totalCalories<1800:
            print("The daily calorie consumption of {0} is 1800 and he (she) is taking {1},he or she required more calories  and he or she is  under-nourished.".format(childName,totalCalories))
        else:
            print("The daily calorie consumption of {0} is 1800 and he (she) is taking {1}, he or she is nourished.".format(childName,totalCalories))
    else:
        print("He(or She) is not Child!")
                                                                
# The nourishmentResult function is aimed at assessing the nourishment status of a child based on their 
# age and total calorie consumption. This function takes three parameters as inputs: childName (the name of the child), 
# childAge (the age of the child), and totalCalorie (the total number of calories consumed by the child in a day).

# The function starts by evaluating the age of the child in different age ranges: 0-2 years, 2-4 years, and 4-8 years. 
# Within each age range, it assesses whether the child's total calorie consumption is sufficient for adequate nourishment.

# For children aged 0 to 2 years, the function checks if the total calories consumed (totalCalorie) 
# are less than 800. If the condition is met, it prints a message indicating that the child's daily
# calorie consumption should ideally be 800, and the child is taking less than that amount. 
# This suggests that the child requires more calories for proper nourishment, leading to a classification of 
# "under-nourished." If the total calories are greater than or equal to 800, the function concludes that 
#  the child is "nourished."

# Similarly, for children aged 2 to 4 years, the function compares the total calories consumed to a value of 1400. 
# If the calories are below this threshold, the child is considered "under-nourished." 
# If the calories meet or exceed 1400, the child is considered "nourished."

# For children aged 4 to 8 years, the function uses a threshold of 1800 calories to make the same assessment 
# regarding nourishment status.

# If the age of the child does not fall within any of these predefined ranges (0-2 years, 2-4 years, or 4-8 years), 
# the function prints a message stating that the given age does not correspond to that of a child.

# In summary, the nourishmentResult function provides insights into the nourishment status of a child based on 
# their age and total calorie consumption. It helps in determining whether the child is consuming an adequate 
# amount of calories for their age group, thus contributing to an assessment of their nutritional well-being.
#
        
        
#Main Function
#Taking details of child
print("WELCOME TO CHILD NUTRITION CALCULATOR")
childName=input("Name:")                         
childAge=int(input("Age:"))
childHeight=float(input("Height(inches):"))
childWeight=float(input("Weight(lb):"))

print("")

#Taking daily calorie consumption of child
print("Calorie Consumption of child")
calories={}
calories["Milk"]=int(input("Milk:"))
calories["Vegetables"]=int(input("Vegetables:"))
calories["Meat"]=int(input("Meat:"))
calories["Lentils"]=int(input("Lentils:"))
calories["Egg"]=int(input("Egg:"))
calories["Rice"]=int(input("Rice:"))

print("")

#calculating bmi using bmi formula
# The multiplication by 703 is used in the calculation of BMI when the height
# is measured in inches and weight is measured in pounds. 
# The standard BMI formula is calculated using the metric system (weight in kilograms and height in meters squared). 
bmi = (childWeight/(childHeight**2))*703
bmiTwoDecimal= round(bmi, 2)    #rounding bmi to 2 decimal places

#passing child name and bmi to bmiResult to print the BMI Categories
bmiResult(childName,bmiTwoDecimal)   

print("")

#Passing calories dictionary to caloriesCalculator to calculate total calories consumed by child
totalCalories=caloriesCalculator(calories)  
totalCaloriesTwoDecimal= round(totalCalories, 2)   #rounding total calories to 2 decimal places

#passing child name, age and total calories consumed to nourishmentResult to print the nourished status of child
nourishmentResult(childName,childAge,totalCaloriesTwoDecimal)

