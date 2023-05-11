# sum_of_time_data_on_diff_of_7


# import pandas as pd

# # create a sample dataframe with a values column
# df = pd.DataFrame({'values': [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20]})

# # create a new index starting from 0 and consider the first index as 0
df1.index = df.index

# add a new column with NaN values
df1['values_new'] = pd.np.nan

# add values column in every interval of 7
df1.loc[(df1.index - 1) % 6 == 0, 'values_new'] = df1['downtime'].rolling(window=6, min_periods=1).sum()

# print the resulting dataframe
df1.head(30)
