# matrix [![Build Status](https://travis-ci.org/Exilor/matrix.svg?branch=master)](https://travis-ci.org/Exilor/matrix)


This is a Matrix class for [Crystal](https://github.com/crystal-lang/crystal).
There are a few ways to create a Matrix:
```crystal
# Creates a Matrix of Int32 with 3 rows and 2 columns. A Tuple of rows can also 
# be used instead of an array. Each row must have the same number of elements.
Matrix.rows([[1, 2], [3, 4], [5, 6]]) 
# 1, 2
# 3, 4
# 5, 6

# Creates a Matrix with 2 rows and 3 columns. Like with Matrix.rows, the columns 
# must have the same number of elements.
Matrix.columns([[1, 2], [3, 4], [5, 6]])
# 1, 3, 5
# 2, 4, 6

# A Matrix can also be created by giving its number of columns and rows, just 
# like an Array can be created by giving it a starting size. This constructor 
# will yield the linear index, the current row and the current column.
Matrix.new(2, 2) { |idx, row, col| idx  }
# 0, 1
# 2, 3
Matrix.new(2, 2) { |idx, row, col| row  }
# 0, 0
# 1, 1
Matrix.new(2, 2) { |idx, row, col| col  }
 # 0, 1
 # 0, 1
```

Most methods are documented in the matrix.cr file itself.
