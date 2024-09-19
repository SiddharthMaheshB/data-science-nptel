
  **Lists and Vectors in R are 1 indexed, as in the elements are indexed with 1,2,3...**

### Vectors:
   - created using c() (concat) function
   - only consists of homogenous elements

### Lists:
   - created using list() function
   - non homogenous elements

### Dataframes:
   - created using data.frame() function, which takes n vectors as arguments
   - can also use read.table(path) to read from a csv file
   - values are accessed using `df[i,j]` where i refers to row, j refers to column
   - default is column, if `df[i]` is passed then i refers to ith column
   - i and j can be range of values, ex: `df[1:2,1:3]` returns the rows 1,2 and columns 1-3
   - df can be edited using the edit(df) function this creates a pop up window with an editable table of the df
   - to append rows, use the `rbind(df,data.frame(vec1,vec2,vec3))` where vec1 vec2 vec3 are column names (or values of the column in this row)
   - to append columns, use the `cbind(df,vec4=c(x1,x2,x3))` where vec4 is the name of the new column
   - rows and columns can be deleted by using `df[-i,-j]` where i and j are the indices of the rows/cols to be deleted

### Recasting and Joining Dataframes
#### Recasting dataframes:
- manipulating df based on variables
- also includes reshaping df
- Identifier variables are the variables which are not numeric values
- measurement variables are numeric values
- recasting is done by melting and casting the df, both functions availabe in reshape2 lib
- `melt(df, id.vars, measure.vars, variable.name="variable", value.name = "value")`
- `dcast(df, formula, value.var = col with values)`
- recasting can also be done by using the `recast()` function
- `recast(data, formula, id.var, measure.var)`
- `mutate` function from the `dplyr` library can be used to create new columns by applying formulas on existing columns
- `mutate(df, formula)`
- dataframes can be combined using dplyr library, supporting `left_join(), right_join(), inner_join(), full_join()`

### Arithmatic operations in R
- OR -> |
- AND -> &
- isTRUE -> boolean check

### Matrix Operations in R
- Matrix is created by `matrix(vector, nrow, ncol)`
- to create matrix of same element k, `matrix(k, nrow,ncol)`
- get matrix dimensions with `dim(matrix)`
- accessing is same as df
- `colnames(matrix)` and `rownames(matrix)` can be used to define row and column names, similar to dict in py
- `rbind` and `colbind` work the same as in df
- deleting rows works same as in df
- Matrix Multiplication: `A*B`-> element wise multiplication, `A#*#B`-> regular matrix multiplication

### Data Visualisation
   - **scatter plot** puts all the points on the graph without connecting them
   - [line plot] connects all the plots in a line
   - [bar plot] generates a bar graph