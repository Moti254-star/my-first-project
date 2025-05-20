#calculating descriptive statistics
# Create sample data
height <- c(160, 165, 170, 175, 180, 155, 168, 172, 178, 182,
            161, 164, 169, 174, 179, 158, 167, 171, 177, 181)
weight <- c(55, 60, 65, 70, 75, 50, 63, 68, 73, 78,
            56, 59, 64, 69, 74, 53, 62, 66, 72, 76)

# Combine into a data frame
my_data <- data.frame(height, weight)

install.packages("psych")
library(psych)

# Summary statistics
summary(my_data)

# More detailed descriptive stats
describe(my_data)


#Histogram of Heights
hist(my_data$height, main = "Histogram of Heights", xlab = "Height (cm)", col = "skyblue", border = "white")

![image](https://github.com/user-attachments/assets/87b11453-9423-4e3c-9ef4-95780b68cbcf)

#Boxplot of Weights
boxplot(my_data$weight, main = "Boxplot of Weights", ylab = "Weight (kg)", col = "red")

![image](https://github.com/user-attachments/assets/3d97340a-ff9f-42ba-8d6c-dfafb8003958)



#Scatter Plot of Height vs. Weight
plot(my_data$height, my_data$weight, main = "Height vs Weight", xlab = "Height (cm)", ylab = "Weight (kg)", pch = 19, col = "blue")

![image](https://github.com/user-attachments/assets/b3891c9c-0075-408f-8301-147eaeb71146)



# create the model
model <- lm(weight ~ height, data = my_data)  

#Add a Regression Line
plot(my_data$height, my_data$weight,
     main = "Height vs Weight",
     xlab = "Height (cm)", ylab = "Weight (kg)",
     pch = 19, col = "blue")

abline(model, col = "red", lwd = 2)  # now this works


![image](https://github.com/user-attachments/assets/1126ed75-4432-468b-b915-26662c5b5917)



















