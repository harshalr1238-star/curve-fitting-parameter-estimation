# Curve Fitting and Parameter Estimation

## 1. Objective

The objective of this assignment is to find the unknown parameters
`θ`, `M` and `X` in the given parametric equation of a curve.

The given data points are provided in the CSV file `xy_data.csv`.
The aim is to find values of the unknown parameters such that the
generated curve is as close as possible to the given data points.

## 2. Given Parametric Equation

The given curve is represented using the following equations:

### x equation

\[
x = t\cos(\theta) - e^{M|t|}\sin(0.3t)\sin(\theta) + X
\]

### y equation

\[
y = 42 + t\sin(\theta) + e^{M|t|}\sin(0.3t)\cos(\theta)
\]

The unknown parameters are:

- `θ` - Theta
- `M`
- `X`

Here, `t` is used to generate the points on the curve. The value of
`θ` is given in degrees and is converted to radians in the Python
code before calculating the curve.

## 3. Parameter Ranges

The given ranges for the unknown parameters are:

- `0° < θ < 50°`
- `-0.05 < M < 0.05`
- `0 < X < 100`

The parameter `t` is taken from 6 to 60.

## 4. Dataset

The given data points are provided in:

`xy_data.csv`

The CSV file contains two columns:

- `x`
- `y`

These `x` and `y` values are the given data points used for curve
fitting and parameter estimation.

The dataset contains 1500 data points.

I used Python to load the CSV file and work with the given data.

## 5. Approach

I followed the following steps to estimate the unknown parameters:

1. Loaded the CSV file using Pandas.
2. Checked the data and the number of rows and columns.
3. Extracted the `x` and `y` values from the dataset.
4. Plotted the given data points using Matplotlib.
5. Defined the given parametric equations in Python.
6. Defined an error function to compare the generated curve with
   the given data.
7. Set the allowed ranges for `θ`, `M` and `X`.
8. Used Differential Evolution to search for suitable values of
   `θ`, `M` and `X`.
9. Calculated the error for the estimated parameter values.
10. Generated the fitted curve using the estimated parameters.
11. Plotted the original data and fitted curve together.

## 6. Parameter Estimation

For different values of `θ`, `M` and `X`, the parametric equations
generate different curves.

The generated curve is compared with the given data points.

The error is calculated from the difference between the original
data points and the predicted points.

The optimization process searches within the given parameter
ranges and finds parameter values that give a small error.

The parameter values giving the minimum error are taken as the
estimated values of `θ`, `M` and `X`.

## 7. Result

The estimated parameter values obtained from the Python program are:

- **θ = 30.043636301°**
- **M = 0.0299905453**
- **X = 55.015520868**

The Mean L1 Error obtained is approximately:

- **Mean L1 Error = 0.30229127**

## 8. Fitted Curve

After obtaining the parameter values, I used them in the
parametric equations to generate the fitted curve.

The final graph compares:

- Original CSV Data
- Fitted Curve

The fitted curve follows the original data closely, showing that
the estimated parameter values give a good fit to the given points.

## 9. Conclusion

In this assignment, I used Python to perform curve fitting and
parameter estimation.

The given CSV data was loaded and visualized. The parametric
equations were implemented and Differential Evolution was used
to estimate the unknown parameters `θ`, `M` and `X`.

The final estimated values are:

**θ = 30.043636301°**

**M = 0.0299905453**

**X = 55.015520868**

The Mean L1 Error obtained was **0.30229127**.

The original data and fitted curve were plotted together to check
the quality of the fitted result.

## 10. Files

- `UVCE_Assignment.ipynb` - Jupyter Notebook containing the
  Python code, calculations and graphs.
- `xy_data.csv` - Dataset provided for the assignment.
- `README.md` - Explanation of the assignment, equations,
  approach and results.
