# Mars Orbit Modeling 

This repository contains the implementation and results for Assignment 2 of the Mars Orbit module. The project involves modeling Mars's orbit using observational data, optimizing orbital parameters, and minimizing angular errors through iterative search methods.

## **Dataset**
The dataset used in this assignment is `01_data_mars_opposition_updated.csv`, which contains the following information:
- **Date and Time of Opposition**: Year, Month, Day, Hour, and Minute.
- **Longitude Data**:
  - ZodiacIndex: Zodiac position (Aries = 0, Taurus = 1, ..., Pisces = 11).
  - Degree, Minute, Second of Mars's heliocentric longitude.
  - Formula: `Longitude = ZodiacIndex*30 + Degree + Minute/60 + Second/3600` (degrees).
- **Latitude Data**: Degree and Minute of Mars's geocentric latitudinal position.
- **Mean Longitude Data**: These were ignored as per the assignment instructions.

## **Key Features**
The implementation consists of five main functions:
1. **`MarsEquantModel`**:
   - Calculates angular errors for each opposition based on a given set of orbital parameters.
   - Outputs the errors and the maximum angular error.
   
2. **`bestOrbitInnerParams`**:
   - Performs a discretized exhaustive search over parameters \( c, e_1, e_2, z \) to minimize the maximum angular error.
   - Outputs the best parameters, angular errors, and the maximum angular error.

3. **`bestS`**:
   - Searches for the best angular velocity \( s \), keeping \( r \) fixed.
   - Uses the function from question 2 for optimization.
   - Outputs the best \( s \), angular errors, and the maximum angular error.

4. **`bestR`**:
   - Searches for the best radius \( r \), keeping \( s \) fixed.
   - Uses the function from question 2 for optimization.
   - Outputs the best \( r \), angular errors, and the maximum angular error.

5. **`bestMarsOrbitParams`**:
   - A wrapper function that iteratively searches over \( r \) and \( s \), starting from an initial guess.
   - Outputs the best parameters \( c, e_1, e_2, z, r, s \), angular errors, and the maximum angular error.

## **Results**
- **Best Parameters**:
  - The optimal values of \( c, e_1, e_2, z, r, s \) were determined through iterative search and optimization.
- **Errors**:
  - Angular errors were computed for each opposition, and the maximum angular error was minimized.
- **Visualization**:
  - Generated plots of the optimized orbit and the angular error distribution.
  - ![image](https://github.com/user-attachments/assets/17343dba-b7f2-4af2-a70b-95aace410696)
  - ![plot1](https://github.com/user-attachments/assets/880f50bd-6046-4fec-8daf-307e0468ce15)


## **Dependencies**
- Python 3.9.12
- Required Libraries:
  - `numpy`
  - `matplotlib`
  - `pandas`
  - `scipy`

## Contact
If you have any questions or suggestions, please feel free to reach out to me at nvarjunmani07@gmail.com.
