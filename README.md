# 📘 Binus R Programming

**Table of Contents & Materials**

---

## 📍 Pertemuan 1: Introduction to R

🔗 Link to Notebook

1.1 Installing R and RStudio

```r
# Download R: https://cran.r-project.org/
# Download RStudio: https://posit.co/download/rstudio-desktop/
```

1.2 Basic Syntax in R

```r
print("Hello, R!")
```

1.3 R Programming Editor

```r
# Menggunakan RStudio untuk menulis dan menjalankan script R
```

1.4 Creating an R Script

```r
# File > New File > R Script di RStudio
```

1.5 Printing "Hello World"

```r
print("Hello World")
```

---

## 📍 Pertemuan 2: Data Types & Operators

🔗 Link to Notebook

2.1 Data Types in R

```r
# Numeric, Character, Logical
x <- 10
y <- "Hello"
z <- TRUE
```

2.2 Data Type Conversion

```r
as.character(10)
as.numeric("5")
```

2.3 Arithmetic Operators

```r
5 + 3
5 - 3
5 * 3
5 / 3
```

2.4 Assignment Operators

```r
x <- 5
y = 6
```

2.5 Comparison Operators

```r
x == 5
x != 4
x > 3
```

2.6 Logical Operators

```r
(x > 3) & (x < 10)
(x > 3) | (x < 2)
```

---

## 📍 Pertemuan 3: Conditions & Loops

🔗 Link to Notebook

3.1 If Structure in R

```r
if (x > 5) {
  print("Greater than 5")
} else {
  print("Less or equal to 5")
}
```

3.2 If/Else Branching

```r
nilai <- 80
if (nilai >= 90) {
  print("A")
} else if (nilai >= 80) {
  print("B")
} else {
  print("C")
}
```

3.3 For Loops

```r
for (i in 1:5) {
  print(i)
}
```

3.4 While Loops

```r
i <- 1
while (i <= 5) {
  print(i)
  i <- i + 1
}
```

3.5 Repeat Loops

```r
i <- 1
repeat {
  print(i)
  i <- i + 1
  if (i > 5) break
}
```

---

## 📍 Pertemuan 4: Functions in R

🔗 Link to Notebook

4.1 User-Defined Functions

```r
hello <- function() {
  print("Hello World")
}
```

4.2 Functions with Parameters

```r
add <- function(a, b) {
  return(a + b)
}
```

4.3 Returning Values from Functions

```r
multiply <- function(a, b) {
  return(a * b)
}
```

4.4 Variable Scope in R

```r
x <- 10
myFunction <- function() {
  x <- 5
  print(x)
}
myFunction()
print(x)
```

4.5 Common Built-in Functions

```r
mean(c(1, 2, 3))
sum(c(1, 2, 3))
max(c(1, 2, 3))
```

---

## 📍 Pertemuan 5: Vectors and Lists

🔗 Link to Notebook

5.1 Creating Vectors

```r
v <- c(1, 2, 3, 4)
```

5.2 Accessing Vector Elements

```r
v[2]
```

5.3 Modifying Vectors

```r
v[2] <- 10
```

5.4 Vector Operations

```r
v * 2
```

5.5 Creating Lists

```r
myList <- list(Name="John", Age=25)
```

5.6 Accessing and Modifying Lists

```r
myList$Name
myList$Age <- 26
```

5.7 List Operations

```r
length(myList)
```

---

## 📍 Pertemuan 6: Matrices & Data Frames

🔗 Link to Notebook

6.1 Creating Matrices

```r
m <- matrix(1:9, nrow=3)
```

6.2 Accessing Matrix Elements

```r
m[1, 2]
```

6.3 Matrix Operations

```r
m * 2
```

6.4 Creating Data Frames

```r
df <- data.frame(Name=c("A", "B"), Age=c(20, 25))
```

6.5 Accessing and Modifying Data Frames

```r
df$Age[1] <- 21
```

6.6 Data Frame Filtering and Sorting

```r
subset(df, Age > 20)
df[order(df$Age), ]
```

---

## 📍 Pertemuan 7: Factors and Date Handling

🔗 Link to Notebook

7.1 Working with Factors

```r
f <- factor(c("low", "medium", "high"))
```

7.2 Modifying Factor Levels

```r
levels(f)
```

7.3 Creating Date Objects

```r
date <- as.Date("2024-07-05")
```

7.4 Date Arithmetic and Formatting

```r
date + 7
format(date, "%d-%m-%Y")
```

---

## 📍 Pertemuan 8: Data Manipulation with dplyr

🔗 Link to Notebook

8.1 Selecting and Filtering Data

```r
library(dplyr)
filter(df, Age > 20)
select(df, Name)
```

8.2 Sorting Data

```r
arrange(df, desc(Age))
```

8.3 Mutating and Summarizing Data

```r
mutate(df, NewAge = Age + 1)
summarise(df, MeanAge = mean(Age))
```

8.4 Grouping Data

```r
group_by(df, Name)
summarise(df, Count = n())
```

---

## 📍 Pertemuan 9: Data Visualization with ggplot2

🔗 Link to Notebook

9.1 Scatter Plots

```r
library(ggplot2)
ggplot(df, aes(x=Age, y=Name)) + geom_point()
```

9.2 Bar Charts

```r
ggplot(df, aes(x=Name, fill=Name)) + geom_bar()
```

9.3 Histograms

```r
ggplot(df, aes(x=Age)) + geom_histogram(binwidth=1)
```

9.4 Line Charts

```r
ggplot(df, aes(x=Age, y=Age)) + geom_line()
```

9.5 Customizing ggplot2 Visuals

```r
ggplot(df, aes(x=Age, y=Name)) +
  geom_point(color="blue") +
  labs(title="Example Plot", x="Age", y="Name")
```

---

## 📍 Pertemuan 10: Statistical Analysis

🔗 Link to Notebook

10.1 Descriptive Statistics

```r
summary(df)
```

10.2 Correlation Analysis

```r
cor(df$Age, c(30, 35))
```

10.3 Simple Linear Regression

```r
model <- lm(Age ~ Name, data=df)
summary(model)
```

10.4 t-Test and Hypothesis Testing

```r
t.test(df$Age, mu=25)
```

---

## 📍 Pertemuan 11: Machine Learning with R

🔗 Link to Notebook

11.1 Data Partitioning

```r
library(caret)
trainIndex <- createDataPartition(df$Age, p=0.8, list=FALSE)
train <- df[trainIndex, ]
test <- df[-trainIndex, ]
```

11.2 Model Training and Testing

```r
model <- train(Age ~ Name, data=train, method="lm")
```

11.3 Model Evaluation

```r
predictions <- predict(model, test)
postResample(predictions, test$Age)
```

11.4 Confusion Matrix

```r
confusionMatrix(table(predictions, test$Age))
```

11.5 Cross Validation

```r
trainControl(method="cv", number=5)
```

---

## 📍 Pertemuan 12: Shiny Dashboard

🔗 Link to Notebook

12.1 Introduction to Shiny

```r
library(shiny)
```

12.2 UI Layout in Shiny

```r
ui <- fluidPage(
  titlePanel("Simple Shiny App"),
  sidebarLayout(
    sidebarPanel(sliderInput("num", "Choose a number:", 1, 100, 50)),
    mainPanel(textOutput("result"))
  )
)
```

12.3 Server Logic in Shiny

```r
server <- function(input, output) {
  output$result <- renderText({ paste("You selected:", input$num) })
}
```

12.4 Reactive Elements

```r
# Reactive input automatically updates outputs
```

12.5 Interactive Graphs and Filters

```r
# Integrate ggplot2 with shiny for interactive graphs
```

---

## 📍 Pertemuan 13: Final Project

🔗 Link to Notebook

13.1 Data Cleaning and Preprocessing

```r
# Menghapus data kosong
cleaned_data <- na.omit(df)

# Mengisi data kosong dengan rata-rata
# df$Age[is.na(df$Age)] <- mean(df$Age, na.rm = TRUE)
```

13.2 Exploratory Data Analysis

```r
# Menampilkan statistik deskriptif
summary(cleaned_data)

# Visualisasi distribusi data
hist(cleaned_data$Age)
```

13.3 Model Building and Evaluation

```r
# Membuat model regresi sederhana
model <- lm(Age ~ Name, data=cleaned_data)
summary(model)

# Melakukan prediksi
predictions <- predict(model, cleaned_data)

# Evaluasi model
postResample(predictions, cleaned_data$Age)
```

13.4 Dashboard Development

```r
# Membuat Shiny dashboard sederhana
ui <- fluidPage(
  titlePanel("Dashboard Data Final Project"),
  sidebarLayout(
    sidebarPanel(sliderInput("age", "Filter umur minimum:", min=cleaned_data$Age, max=max(cleaned_data$Age), value=min(cleaned_data$Age))),
    mainPanel(tableOutput("filteredData"))
  )
)

server <- function(input, output) {
  output$filteredData <- renderTable({
    subset(cleaned_data, Age >= input$age)
  })
}

shinyApp(ui = ui, server = server)
```
