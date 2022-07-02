### Why?
    The purpose of the EDA is to get insights into the features of House Prices Data. The EDA should include cleaning the features, putting them in proper formats and asking pertinent questions. At the end of the EDA, one should be left with proper actionable insights i.e. Insights which can help the Data Scientist on making proper judgements regarding building the ML model.

### How?
* Give data a preliminary look - Done
* List down all the features - Done
* Look at the types of different features - categorical, continuous - Done
* Look at the summary of features - Done
  * Mean, median, mode, max, min, variance, type
* Find the missing values in the features - nan values, 0 values etc - Done
* Figure out a Strategy for filling the missing values - Done
  * Central Tendency - Mode, Mean, Median etc

* Club the similar features into groups - So that cleaning, and further processing gets easier. - Done
* Check the distribution of Target Variable - Done
  * Target vs Samples 2-D graph
* Check the skewness of the features - Done
  * Distribution of feature values across samples
* Implement the ‘Filling Missing Values’ strategy for all the groups of features - Done
* Check the correlation of the features with the Target Variable - Done
  * Plot the Feature-Target (x-y) points on a 2-D plane
  * List down the highly correlated features
  * Articulate all the plots and distributions
  * Suggest ways to use that distribution in building a model

* Curate the features - 
  * Remove the Unnecessary OR Redundant features - name, etc
  * Skip the complex features for the Next Iteration
  * Features which needs to be grouped into classes - age, dates, etc



### Features
    Column         Non-Null Count  Dtype  
    0   Id             1168 non-null   int64  
    1   MSSubClass     1168 non-null   int64  
    2   MSZoning       1168 non-null   object
    3   LotFrontage    982 non-null    float64
    4   LotArea        1168 non-null   int64  
    5   Street         1168 non-null   object
    6   Alley          74 non-null     object
    7   LotShape       1168 non-null   object
    8   LandContour    1168 non-null   object
    9   Utilities      1168 non-null   object
    10  LotConfig      1168 non-null   object
    11  LandSlope      1168 non-null   object
    12  Neighborhood   1168 non-null   object
    13  Condition1     1168 non-null   object
    14  Condition2     1168 non-null   object
    15  BldgType       1168 non-null   object
    16  HouseStyle     1168 non-null   object
    17  OverallQual    1168 non-null   int64  
    18  OverallCond    1168 non-null   int64  
    19  YearBuilt      1168 non-null   int64  
    20  YearRemodAdd   1168 non-null   int64  
    21  RoofStyle      1168 non-null   object
    22  RoofMatl       1168 non-null   object
    23  Exterior1st    1168 non-null   object
    24  Exterior2nd    1168 non-null   object
    25  MasVnrType     1161 non-null   object
    26  MasVnrArea     1161 non-null   float64
    27  ExterQual      1168 non-null   object
    28  ExterCond      1168 non-null   object
    29  Foundation     1168 non-null   object
    30  BsmtQual       1135 non-null   object
    31  BsmtCond       1135 non-null   object
    32  BsmtExposure   1134 non-null   object
    33  BsmtFinType1   1135 non-null   object
    34  BsmtFinSF1     1168 non-null   int64  
    35  BsmtFinType2   1135 non-null   object
    36  BsmtFinSF2     1168 non-null   int64  
    37  BsmtUnfSF      1168 non-null   int64  
    38  TotalBsmtSF    1168 non-null   int64  
    39  Heating        1168 non-null   object
    40  HeatingQC      1168 non-null   object
    41  CentralAir     1168 non-null   object
    42  Electrical     1168 non-null   object
    43  1stFlrSF       1168 non-null   int64  
    44  2ndFlrSF       1168 non-null   int64  
    45  LowQualFinSF   1168 non-null   int64  
    46  GrLivArea      1168 non-null   int64  
    47  BsmtFullBath   1168 non-null   int64  
    48  BsmtHalfBath   1168 non-null   int64  
    49  FullBath       1168 non-null   int64  
    50  HalfBath       1168 non-null   int64  
    51  BedroomAbvGr   1168 non-null   int64  
    52  KitchenAbvGr   1168 non-null   int64  
    53  KitchenQual    1168 non-null   object
    54  TotRmsAbvGrd   1168 non-null   int64  
    55  Functional     1168 non-null   object
    56  Fireplaces     1168 non-null   int64  
    57  FireplaceQu    614 non-null    object
    58  GarageType     1103 non-null   object
    59  GarageYrBlt    1103 non-null   float64
    60  GarageFinish   1103 non-null   object
    61  GarageCars     1168 non-null   int64  
    62  GarageArea     1168 non-null   int64  
    63  GarageQual     1103 non-null   object
    64  GarageCond     1103 non-null   object
    65  PavedDrive     1168 non-null   object
    66  WoodDeckSF     1168 non-null   int64  
    67  OpenPorchSF    1168 non-null   int64  
    68  EnclosedPorch  1168 non-null   int64  
    69  3SsnPorch      1168 non-null   int64  
    70  ScreenPorch    1168 non-null   int64  
    71  PoolArea       1168 non-null   int64  
    72  PoolQC         3 non-null      object
    73  Fence          222 non-null    object
    74  MiscFeature    40 non-null     object
    75  MiscVal        1168 non-null   int64  
    76  MoSold         1168 non-null   int64  
    77  YrSold         1168 non-null   int64  
    78  SaleType       1168 non-null   object
    79  SaleCondition  1168 non-null   object
    80  SalePrice      1168 non-null   int64 

    COLOR -> Features where missing values need to be filled

###  NAN Columns to be Handeled
    3   LotFrontage    982 non-null    float64 []
    6   Alley          74 non-null     object []
    25  MasVnrType     1161 non-null   object []
    26  MasVnrArea     1161 non-null   float64 []
    30  BsmtQual       1135 non-null   object []
    31  BsmtCond       1135 non-null   object []
    32  BsmtExposure   1134 non-null   object []
    33  BsmtFinType1   1135 non-null   object [] 
    35  BsmtFinType2   1135 non-null   object []
    57  FireplaceQu    614 non-null    object []
    58  GarageType     1103 non-null   object []
    59  GarageYrBlt    1103 non-null   float64 []
    60  GarageFinish   1103 non-null   object []
    63  GarageQual     1103 non-null   object []
    64  GarageCond     1103 non-null   object []
    72  PoolQC         3 non-null      object []
    73  Fence          222 non-null    object []
    74  MiscFeature    40 non-null     object []


### Groups of Features
#### Group A - All the categorical
    1   MSSubClass     1168 non-null   int64  
    2   MSZoning       1168 non-null   object
    5   Street         1168 non-null   object
    6   Alley          74 non-null     object
    7   LotShape       1168 non-null   object
    8   LandContour    1168 non-null   object
    9   Utilities      1168 non-null   object
    10  LotConfig      1168 non-null   object
    11  LandSlope      1168 non-null   object
    12  Neighborhood   1168 non-null   object
    13  Condition1     1168 non-null   object
    14  Condition2     1168 non-null   object
    15  BldgType       1168 non-null   object
    16  HouseStyle     1168 non-null   object
    17  OverallQual    1168 non-null   int64  
    18  OverallCond    1168 non-null   int64  
    21  RoofStyle      1168 non-null   object
    22  RoofMatl       1168 non-null   object
    23  Exterior1st    1168 non-null   object
    24  Exterior2nd    1168 non-null   object
    25  MasVnrType     1161 non-null   object
    26  MasVnrArea     1161 non-null   float64
    27  ExterQual      1168 non-null   object
    28  ExterCond      1168 non-null   object
    29  Foundation     1168 non-null   object
    30  BsmtQual       1135 non-null   object
    31  BsmtCond       1135 non-null   object
    32  BsmtExposure   1134 non-null   object
    33  BsmtFinType1   1135 non-null   object
    35  BsmtFinType2   1135 non-null   object
    39  Heating        1168 non-null   object
    40  HeatingQC      1168 non-null   object
    41  CentralAir     1168 non-null   object
    42  Electrical     1168 non-null   object
    47  BsmtFullBath   1168 non-null   int64  
    48  BsmtHalfBath   1168 non-null   int64  
    49  FullBath       1168 non-null   int64  
    50  HalfBath       1168 non-null   int64  
    51  BedroomAbvGr   1168 non-null   int64  
    52  KitchenAbvGr   1168 non-null   int64  
    53  KitchenQual    1168 non-null   object
    54  TotRmsAbvGrd   1168 non-null   int64  
    55  Functional     1168 non-null   object
    56  Fireplaces     1168 non-null   int64  
    57  FireplaceQu    614 non-null    object
    58  GarageType     1103 non-null   object
    60  GarageFinish   1103 non-null   object
    61  GarageCars     1168 non-null   int64  
    63  GarageQual     1103 non-null   object
    64  GarageCond     1103 non-null   object
    65  PavedDrive     1168 non-null   object
    71  PoolArea       1168 non-null   int64  
    72  PoolQC         3 non-null      object
    73  Fence          222 non-null    object
    74  MiscFeature    40 non-null     object
    76  MoSold         1168 non-null   int64  
    78  SaleType       1168 non-null   object
    79  SaleCondition  1168 non-null   object

#### Group B - Continueous
    37  BsmtUnfSF      1168 non-null   int64  
    38  TotalBsmtSF    1168 non-null   int64  
    43  1stFlrSF       1168 non-null   int64  
    44  2ndFlrSF       1168 non-null   int64  
    45  LowQualFinSF   1168 non-null   int64  
    46  GrLivArea      1168 non-null   int64  
    59  GarageYrBlt    1103 non-null   float64
    62  GarageArea     1168 non-null   int64  
    66  WoodDeckSF     1168 non-null   int64  
    67  OpenPorchSF    1168 non-null   int64  
    68  EnclosedPorch  1168 non-null   int64  
    69  3SsnPorch      1168 non-null   int64  
    70  ScreenPorch    1168 non-null   int64  
    75  MiscVal        1168 non-null   int64  
    77  YrSold         1168 non-null   int64  
    80  SalePrice      1168 non-null   int64 

### References
- [Titanic: Anuj Chauhan](https://github.com/hanchau/titanic-survivor/blob/master/decission_trees.ipynb)
- [Kaggle Titanic](https://www.kaggle.com/code/dejavu23/titanic-eda-to-ml-beginner/notebook)
- [House Price Prediction: Barker31](https://www.kaggle.com/code/bakar31/eda-house-price-prediction)
- [House Price Prediction: Siddhesh Pujari](https://www.kaggle.com/code/siddheshpujari/eda-and-prediction-of-house-price/notebook)
- [House Price Prediction: Dejavu23](https://www.kaggle.com/code/dejavu23/house-prices-eda-to-ml-beginner/notebook)
- [House Price Prediction: Ekami66](https://www.kaggle.com/code/ekami66/detailed-exploratory-data-analysis-with-python/notebook)

