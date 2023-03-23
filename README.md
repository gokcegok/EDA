# EDA
Exploratory Data Analysis

Functions: 

  check_df()
  
    This function prints basic information about given dataframe.
          shape, data types, head of dataframe, tail of dataframe,
          null value counts

      Parameters
      ----------
      dataframe: pandas.DataFrame

      n_head: integer
              number of rows for printing head of df

      n_tail: integer
              number of rows for printing tail of df
  
  cat_summary()
  
    This function prints value counts and class ratio of given
      categorical variable in the given dataframe.

      Parameters
      ----------
      dataframe: pandas.DataFrame

      col_name: string
                the name of the categorical variable
      plot: boolean
            If plot == True:
              plot bar plot of the categorical variable
              
  num_summary()
      
    This function prints descriptive statistics
    of the given numeric variable in the given dataset.

    Parameters
    ----------
    dataframe: pandas.DataFrame

    num_col: string
             the name of the numeric column
    plot: boolean
          If plot == True:
            plot bar plot of the categorical variable
            
  grab_col_names()
  
    This function returns names of categorical, numeric and categorical looking
    cardinal variables in the given dataset. And prints a brief report about dataset.

    Parameters
    ----------
    dataframe: pandas.DataFrame

    cat_th: int, float
            threshold value for numeric looking categorical variables

    car_th: int, float
            threshold value for categorical looking cardinal variables

    Return
    ------
    cat_cols: list
        list of categorical variables
    num_cols: list
        list of numeric variables
    cat_but_car: list
        list of categorical looking cardinal variables

    Notes
    -----
    len(cat_cols) + len(num_cols) + len(cat_but_car) = len(df)
    num_but_cols(numeric looking categorical variables) is in cat_cols
  
  target_summary_with_categorical()
    
    This function prints the means of the target variable
    according to the classes of the given categorical variable

    Parameters
    ----------
    dataframe: pandas.DataFrame

    target: str
            the name of the target/dependent variable
    cat_col: str
            the name of the given categorical variable
  
  target_summary_with_numeric()
  
    This function prints the means of the target variable
    according to the classes of the given numeric variable

    Parameters
    ----------
    dataframe: pandas.DataFrame

    target: str
            the name of the target/dependent variable
    num_col: str
            the name of the given numeric variable
  
  high_correlated_cols()
  
    This function returns the list of the high correlated variables.
    As default if the correlation between two variable bigger than 0.90
    this variables would be "high correlated".

    Parameters
    ----------
    dataframe: pandas.DataFrame

    plot: boolean
          If plot == True:
          plot bar plot of the categorical variable

    corr_th: int, float
             threshold value for high correlated variables

    Returns
    -------
    drop_list: list
               the list of high correlated variables
