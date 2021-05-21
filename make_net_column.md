## Creates the values for the NET basis column

# Note: This is an imaginary basis I use in my spreadsheets to make other calculations Easier
# This should be used in the column to the left of the basis # 

=IF(INDIRECT(ADDRESS(ROW(), COLUMN() + 2)) = "NET", VALUE(INDIRECT(ADDRESS(ROW(), COLUMN() + 3))), 0)
