{
 "cells": [
  {
   "cell_type": "code",
   "execution_count": 1,
   "id": "62912264-965a-4abc-a0b4-beff28b1a1d9",
   "metadata": {},
   "outputs": [],
   "source": [
    "import pandas as pd\n",
    "import matplotlib.pyplot as plt\n",
    "import seaborn as sns\n"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 2,
   "id": "4b0771c7-b305-4fea-bb19-c83dfd1507f3",
   "metadata": {},
   "outputs": [],
   "source": [
    "data=pd.read_csv(\"test.csv\")"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 3,
   "id": "5de29ae2-6a55-45f6-b33a-97bcb08f9094",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "<div>\n",
       "<style scoped>\n",
       "    .dataframe tbody tr th:only-of-type {\n",
       "        vertical-align: middle;\n",
       "    }\n",
       "\n",
       "    .dataframe tbody tr th {\n",
       "        vertical-align: top;\n",
       "    }\n",
       "\n",
       "    .dataframe thead th {\n",
       "        text-align: right;\n",
       "    }\n",
       "</style>\n",
       "<table border=\"1\" class=\"dataframe\">\n",
       "  <thead>\n",
       "    <tr style=\"text-align: right;\">\n",
       "      <th></th>\n",
       "      <th>PassengerId</th>\n",
       "      <th>Pclass</th>\n",
       "      <th>Name</th>\n",
       "      <th>Sex</th>\n",
       "      <th>Age</th>\n",
       "      <th>SibSp</th>\n",
       "      <th>Parch</th>\n",
       "      <th>Ticket</th>\n",
       "      <th>Fare</th>\n",
       "      <th>Cabin</th>\n",
       "      <th>Embarked</th>\n",
       "    </tr>\n",
       "  </thead>\n",
       "  <tbody>\n",
       "    <tr>\n",
       "      <th>0</th>\n",
       "      <td>892</td>\n",
       "      <td>3</td>\n",
       "      <td>Kelly, Mr. James</td>\n",
       "      <td>male</td>\n",
       "      <td>34.5</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>330911</td>\n",
       "      <td>7.8292</td>\n",
       "      <td>NaN</td>\n",
       "      <td>Q</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>1</th>\n",
       "      <td>893</td>\n",
       "      <td>3</td>\n",
       "      <td>Wilkes, Mrs. James (Ellen Needs)</td>\n",
       "      <td>female</td>\n",
       "      <td>47.0</td>\n",
       "      <td>1</td>\n",
       "      <td>0</td>\n",
       "      <td>363272</td>\n",
       "      <td>7.0000</td>\n",
       "      <td>NaN</td>\n",
       "      <td>S</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>2</th>\n",
       "      <td>894</td>\n",
       "      <td>2</td>\n",
       "      <td>Myles, Mr. Thomas Francis</td>\n",
       "      <td>male</td>\n",
       "      <td>62.0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>240276</td>\n",
       "      <td>9.6875</td>\n",
       "      <td>NaN</td>\n",
       "      <td>Q</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>3</th>\n",
       "      <td>895</td>\n",
       "      <td>3</td>\n",
       "      <td>Wirz, Mr. Albert</td>\n",
       "      <td>male</td>\n",
       "      <td>27.0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>315154</td>\n",
       "      <td>8.6625</td>\n",
       "      <td>NaN</td>\n",
       "      <td>S</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>4</th>\n",
       "      <td>896</td>\n",
       "      <td>3</td>\n",
       "      <td>Hirvonen, Mrs. Alexander (Helga E Lindqvist)</td>\n",
       "      <td>female</td>\n",
       "      <td>22.0</td>\n",
       "      <td>1</td>\n",
       "      <td>1</td>\n",
       "      <td>3101298</td>\n",
       "      <td>12.2875</td>\n",
       "      <td>NaN</td>\n",
       "      <td>S</td>\n",
       "    </tr>\n",
       "  </tbody>\n",
       "</table>\n",
       "</div>"
      ],
      "text/plain": [
       "   PassengerId  Pclass                                          Name     Sex  \\\n",
       "0          892       3                              Kelly, Mr. James    male   \n",
       "1          893       3              Wilkes, Mrs. James (Ellen Needs)  female   \n",
       "2          894       2                     Myles, Mr. Thomas Francis    male   \n",
       "3          895       3                              Wirz, Mr. Albert    male   \n",
       "4          896       3  Hirvonen, Mrs. Alexander (Helga E Lindqvist)  female   \n",
       "\n",
       "    Age  SibSp  Parch   Ticket     Fare Cabin Embarked  \n",
       "0  34.5      0      0   330911   7.8292   NaN        Q  \n",
       "1  47.0      1      0   363272   7.0000   NaN        S  \n",
       "2  62.0      0      0   240276   9.6875   NaN        Q  \n",
       "3  27.0      0      0   315154   8.6625   NaN        S  \n",
       "4  22.0      1      1  3101298  12.2875   NaN        S  "
      ]
     },
     "execution_count": 3,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "data.head()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 4,
   "id": "f7c38a31-ba13-4e59-aa7d-d41856ea5e5d",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "<div>\n",
       "<style scoped>\n",
       "    .dataframe tbody tr th:only-of-type {\n",
       "        vertical-align: middle;\n",
       "    }\n",
       "\n",
       "    .dataframe tbody tr th {\n",
       "        vertical-align: top;\n",
       "    }\n",
       "\n",
       "    .dataframe thead th {\n",
       "        text-align: right;\n",
       "    }\n",
       "</style>\n",
       "<table border=\"1\" class=\"dataframe\">\n",
       "  <thead>\n",
       "    <tr style=\"text-align: right;\">\n",
       "      <th></th>\n",
       "      <th>PassengerId</th>\n",
       "      <th>Pclass</th>\n",
       "      <th>Name</th>\n",
       "      <th>Sex</th>\n",
       "      <th>Age</th>\n",
       "      <th>SibSp</th>\n",
       "      <th>Parch</th>\n",
       "      <th>Ticket</th>\n",
       "      <th>Fare</th>\n",
       "      <th>Cabin</th>\n",
       "      <th>Embarked</th>\n",
       "    </tr>\n",
       "  </thead>\n",
       "  <tbody>\n",
       "    <tr>\n",
       "      <th>413</th>\n",
       "      <td>1305</td>\n",
       "      <td>3</td>\n",
       "      <td>Spector, Mr. Woolf</td>\n",
       "      <td>male</td>\n",
       "      <td>NaN</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>A.5. 3236</td>\n",
       "      <td>8.0500</td>\n",
       "      <td>NaN</td>\n",
       "      <td>S</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>414</th>\n",
       "      <td>1306</td>\n",
       "      <td>1</td>\n",
       "      <td>Oliva y Ocana, Dona. Fermina</td>\n",
       "      <td>female</td>\n",
       "      <td>39.0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>PC 17758</td>\n",
       "      <td>108.9000</td>\n",
       "      <td>C105</td>\n",
       "      <td>C</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>415</th>\n",
       "      <td>1307</td>\n",
       "      <td>3</td>\n",
       "      <td>Saether, Mr. Simon Sivertsen</td>\n",
       "      <td>male</td>\n",
       "      <td>38.5</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>SOTON/O.Q. 3101262</td>\n",
       "      <td>7.2500</td>\n",
       "      <td>NaN</td>\n",
       "      <td>S</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>416</th>\n",
       "      <td>1308</td>\n",
       "      <td>3</td>\n",
       "      <td>Ware, Mr. Frederick</td>\n",
       "      <td>male</td>\n",
       "      <td>NaN</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>359309</td>\n",
       "      <td>8.0500</td>\n",
       "      <td>NaN</td>\n",
       "      <td>S</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>417</th>\n",
       "      <td>1309</td>\n",
       "      <td>3</td>\n",
       "      <td>Peter, Master. Michael J</td>\n",
       "      <td>male</td>\n",
       "      <td>NaN</td>\n",
       "      <td>1</td>\n",
       "      <td>1</td>\n",
       "      <td>2668</td>\n",
       "      <td>22.3583</td>\n",
       "      <td>NaN</td>\n",
       "      <td>C</td>\n",
       "    </tr>\n",
       "  </tbody>\n",
       "</table>\n",
       "</div>"
      ],
      "text/plain": [
       "     PassengerId  Pclass                          Name     Sex   Age  SibSp  \\\n",
       "413         1305       3            Spector, Mr. Woolf    male   NaN      0   \n",
       "414         1306       1  Oliva y Ocana, Dona. Fermina  female  39.0      0   \n",
       "415         1307       3  Saether, Mr. Simon Sivertsen    male  38.5      0   \n",
       "416         1308       3           Ware, Mr. Frederick    male   NaN      0   \n",
       "417         1309       3      Peter, Master. Michael J    male   NaN      1   \n",
       "\n",
       "     Parch              Ticket      Fare Cabin Embarked  \n",
       "413      0           A.5. 3236    8.0500   NaN        S  \n",
       "414      0            PC 17758  108.9000  C105        C  \n",
       "415      0  SOTON/O.Q. 3101262    7.2500   NaN        S  \n",
       "416      0              359309    8.0500   NaN        S  \n",
       "417      1                2668   22.3583   NaN        C  "
      ]
     },
     "execution_count": 4,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "data.tail()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 5,
   "id": "bf30416b-1ae9-4fa6-9172-8a02f93a3de8",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "<div>\n",
       "<style scoped>\n",
       "    .dataframe tbody tr th:only-of-type {\n",
       "        vertical-align: middle;\n",
       "    }\n",
       "\n",
       "    .dataframe tbody tr th {\n",
       "        vertical-align: top;\n",
       "    }\n",
       "\n",
       "    .dataframe thead th {\n",
       "        text-align: right;\n",
       "    }\n",
       "</style>\n",
       "<table border=\"1\" class=\"dataframe\">\n",
       "  <thead>\n",
       "    <tr style=\"text-align: right;\">\n",
       "      <th></th>\n",
       "      <th>PassengerId</th>\n",
       "      <th>Pclass</th>\n",
       "      <th>Age</th>\n",
       "      <th>SibSp</th>\n",
       "      <th>Parch</th>\n",
       "      <th>Fare</th>\n",
       "    </tr>\n",
       "  </thead>\n",
       "  <tbody>\n",
       "    <tr>\n",
       "      <th>count</th>\n",
       "      <td>418.000000</td>\n",
       "      <td>418.000000</td>\n",
       "      <td>332.000000</td>\n",
       "      <td>418.000000</td>\n",
       "      <td>418.000000</td>\n",
       "      <td>417.000000</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>mean</th>\n",
       "      <td>1100.500000</td>\n",
       "      <td>2.265550</td>\n",
       "      <td>30.272590</td>\n",
       "      <td>0.447368</td>\n",
       "      <td>0.392344</td>\n",
       "      <td>35.627188</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>std</th>\n",
       "      <td>120.810458</td>\n",
       "      <td>0.841838</td>\n",
       "      <td>14.181209</td>\n",
       "      <td>0.896760</td>\n",
       "      <td>0.981429</td>\n",
       "      <td>55.907576</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>min</th>\n",
       "      <td>892.000000</td>\n",
       "      <td>1.000000</td>\n",
       "      <td>0.170000</td>\n",
       "      <td>0.000000</td>\n",
       "      <td>0.000000</td>\n",
       "      <td>0.000000</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>25%</th>\n",
       "      <td>996.250000</td>\n",
       "      <td>1.000000</td>\n",
       "      <td>21.000000</td>\n",
       "      <td>0.000000</td>\n",
       "      <td>0.000000</td>\n",
       "      <td>7.895800</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>50%</th>\n",
       "      <td>1100.500000</td>\n",
       "      <td>3.000000</td>\n",
       "      <td>27.000000</td>\n",
       "      <td>0.000000</td>\n",
       "      <td>0.000000</td>\n",
       "      <td>14.454200</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>75%</th>\n",
       "      <td>1204.750000</td>\n",
       "      <td>3.000000</td>\n",
       "      <td>39.000000</td>\n",
       "      <td>1.000000</td>\n",
       "      <td>0.000000</td>\n",
       "      <td>31.500000</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>max</th>\n",
       "      <td>1309.000000</td>\n",
       "      <td>3.000000</td>\n",
       "      <td>76.000000</td>\n",
       "      <td>8.000000</td>\n",
       "      <td>9.000000</td>\n",
       "      <td>512.329200</td>\n",
       "    </tr>\n",
       "  </tbody>\n",
       "</table>\n",
       "</div>"
      ],
      "text/plain": [
       "       PassengerId      Pclass         Age       SibSp       Parch        Fare\n",
       "count   418.000000  418.000000  332.000000  418.000000  418.000000  417.000000\n",
       "mean   1100.500000    2.265550   30.272590    0.447368    0.392344   35.627188\n",
       "std     120.810458    0.841838   14.181209    0.896760    0.981429   55.907576\n",
       "min     892.000000    1.000000    0.170000    0.000000    0.000000    0.000000\n",
       "25%     996.250000    1.000000   21.000000    0.000000    0.000000    7.895800\n",
       "50%    1100.500000    3.000000   27.000000    0.000000    0.000000   14.454200\n",
       "75%    1204.750000    3.000000   39.000000    1.000000    0.000000   31.500000\n",
       "max    1309.000000    3.000000   76.000000    8.000000    9.000000  512.329200"
      ]
     },
     "execution_count": 5,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "data.describe()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 6,
   "id": "d98e1959-bc9f-43ef-9e21-479f6d7f9903",
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "<class 'pandas.core.frame.DataFrame'>\n",
      "RangeIndex: 418 entries, 0 to 417\n",
      "Data columns (total 11 columns):\n",
      " #   Column       Non-Null Count  Dtype  \n",
      "---  ------       --------------  -----  \n",
      " 0   PassengerId  418 non-null    int64  \n",
      " 1   Pclass       418 non-null    int64  \n",
      " 2   Name         418 non-null    object \n",
      " 3   Sex          418 non-null    object \n",
      " 4   Age          332 non-null    float64\n",
      " 5   SibSp        418 non-null    int64  \n",
      " 6   Parch        418 non-null    int64  \n",
      " 7   Ticket       418 non-null    object \n",
      " 8   Fare         417 non-null    float64\n",
      " 9   Cabin        91 non-null     object \n",
      " 10  Embarked     418 non-null    object \n",
      "dtypes: float64(2), int64(4), object(5)\n",
      "memory usage: 36.0+ KB\n"
     ]
    }
   ],
   "source": [
    "data.info()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 7,
   "id": "fc0c724f-6f0b-4717-974b-477bf8276cee",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "PassengerId      0\n",
       "Pclass           0\n",
       "Name             0\n",
       "Sex              0\n",
       "Age             86\n",
       "SibSp            0\n",
       "Parch            0\n",
       "Ticket           0\n",
       "Fare             1\n",
       "Cabin          327\n",
       "Embarked         0\n",
       "dtype: int64"
      ]
     },
     "execution_count": 7,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "data.isnull().sum()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 8,
   "id": "e26efc7f-828e-4afe-825e-526cd89f178d",
   "metadata": {},
   "outputs": [],
   "source": [
    "data.dropna(subset=[\"Embarked\"],inplace=True)\n",
    "data[\"Cabin\"].fillna(\"Unknown\",inplace=True)\n",
    "data[\"Age\"].fillna(data[\"Age\"].mean(),inplace=True)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 9,
   "id": "453501c2-6f5d-4387-a8a9-17d7f3cd21a9",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "PassengerId    0\n",
       "Pclass         0\n",
       "Name           0\n",
       "Sex            0\n",
       "Age            0\n",
       "SibSp          0\n",
       "Parch          0\n",
       "Ticket         0\n",
       "Fare           1\n",
       "Cabin          0\n",
       "Embarked       0\n",
       "dtype: int64"
      ]
     },
     "execution_count": 9,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "data.isnull().sum()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 10,
   "id": "e8d13499-04c0-4dfe-bf85-5bd5263281e2",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "0"
      ]
     },
     "execution_count": 10,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "data.duplicated().sum()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 11,
   "id": "c96c6bd3-9d39-4877-9e2d-78be5906f566",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "image/png": "iVBORw0KGgoAAAANSUhEUgAAAhwAAAE8CAYAAACLumjXAAAAOXRFWHRTb2Z0d2FyZQBNYXRwbG90bGliIHZlcnNpb24zLjguMiwgaHR0cHM6Ly9tYXRwbG90bGliLm9yZy8g+/7EAAAACXBIWXMAAA9hAAAPYQGoP6dpAABLoUlEQVR4nO3deVzU1f4/8Nfs7LsMoKCIKO6aC5ItmiSVmpaVdrU0zcqwNL2V/sosb2W2eL2ZaXVL7ZtmWWq2aYaF18QNd0UFRUFlQJZh2GaY5fz+ICcnoRBmmMXX8/H4PGQ+n8+ceR9Hx5dnzud8JEIIASIiIiIHkjq7ACIiIvJ8DBxERETkcAwcRERE5HAMHERERORwDBxERETkcAwcRERE5HAMHERERORwDBxERETkcAwcRERE5HAMHETUYs6ePQuJRIKVK1c6/LVWrlwJiUSCs2fPWve1a9cOw4cPd/hr20NL/l4RtQQGDiI38/7770MikSAxMdHZpUAikVg3uVyOkJAQ9OnTB9OnT8fx48ft9jrvv/++y/7D68q1EbkSCe+lQuReBg4ciIsXL+Ls2bPIzs5Ghw4dnFaLRCLB7bffjocffhhCCJSXl+PQoUNYt24dqqqqsHDhQsycOdN6vhACBoMBCoUCMpms0a/TrVs3hIWF4ddff230c8xmM4xGI1QqFSQSCYC6EY5u3brhu+++a3Q7jqitMc6ePYvY2FisWLECEydOtGvbRM7AEQ4iN5Kbm4udO3di0aJFaNWqFVavXu3sktCxY0eMHz8eDz30EKZNm4aPPvoIp0+fRr9+/TBr1iz88MMP1nMlEgm8vLyuKWxcq6qqKgCATCaDl5eXNWwQkXMxcBC5kdWrVyM4OBjDhg3Dfffd12DgKCkpwUMPPYSAgAAEBQVhwoQJOHToUL1zAk6cOIH77rsPISEh8PLyQt++fbFp06Zm1RkaGoq1a9dCLpfjtddes+6vb16CRqPBI488gjZt2kClUiEyMhIjR460zr1o164djh07hvT0dOvXN4MGDQLwxzyN9PR0PPnkkwgPD0ebNm1sjl05h+Oyn376Cb169YKXlxe6dOmC9evX2xx/+eWX6w0qf27zr2oDAK1WixkzZiA6OhoqlQodOnTAwoULYbFYbNrVarWYOHEiAgMDre+XVqtt3G82kZuQO7sAImq81atX495774VSqcSDDz6IZcuWYe/evejXr5/1HIvFghEjRmDPnj2YOnUqEhIS8M0332DChAlXtXfs2DEMHDgQrVu3xuzZs+Hr64svv/wSo0aNwtdff4177rmnybXGxMTg1ltvxS+//AKdToeAgIB6zxs9ejSOHTuGp556Cu3atUNRURG2bt2KvLw8tGvXDosXL8ZTTz0FPz8/vPDCCwAAtVpt08aTTz6JVq1a4aWXXrKOcDQkOzsbY8aMwRNPPIEJEyZgxYoVuP/++7F582bcfvvt19THv6qturoat956Ky5cuIDHH38cMTEx2LlzJ+bMmYOCggIsXrwYQN3XTCNHjsSOHTvwxBNPoHPnztiwYUO97xeRWxNE5Bb27dsnAIitW7cKIYSwWCyiTZs2Yvr06Tbnff311wKAWLx4sXWf2WwWt912mwAgVqxYYd0/ZMgQ0b17d6HX6637LBaLuPHGG0V8fPzf1gRApKamNnh8+vTpAoA4dOiQEEKI3NxcmxrKysoEAPHWW2/95et07dpV3HrrrVftX7FihQAgbrrpJmEymeo9lpuba93Xtm1bAUB8/fXX1n3l5eUiMjJS9O7d27pv3rx5or6Px/rabKi2f/3rX8LX11ecOnXKZv/s2bOFTCYTeXl5QgghNm7cKACIN99803qOyWQSN99881XvF5E741cqRG5i9erVUKvVGDx4MIC6+RBjxozB2rVrYTabredt3rwZCoUCU6ZMse6TSqVITU21aa+0tBTbtm3DAw88gIqKChQXF6O4uBglJSVISUlBdnY2Lly40Kya/fz8AAAVFRX1Hvf29oZSqcSvv/6KsrKyJr/OlClTGj0vJCoqymbkJiAgAA8//DAOHDgAjUbT5Br+bN26dbj55psRHBxs/b0tLi5GcnIyzGYztm/fDgD44YcfIJfLMXXqVOtzZTIZnnrqKbvVQuQK+JUKkRswm81Yu3YtBg8ejNzcXOv+xMREvPPOO0hLS8PQoUMBAOfOnUNkZCR8fHxs2vjz1Sw5OTkQQmDu3LmYO3duva9bVFSE1q1bN7nuyspKAIC/v3+9x1UqFRYuXIhZs2ZBrVZjwIABGD58OB5++GFEREQ0+nViY2MbfW6HDh2ump/RsWNHAHVzTK7ldf9KdnY2Dh8+jFatWtV7vKioCMAf79flcHZZp06d7FIHkatg4CByA9u2bUNBQQHWrl2LtWvXXnV89erV1sDRWJcnLv7zn/9ESkpKvec095Lbo0ePQiaT/WUgmDFjBkaMGIGNGzdiy5YtmDt3LhYsWIBt27ahd+/ejXodb2/vZtX5Zw1d2XLlSNLfsVgsuP322/Hcc8/Ve/xyyCG6XjBwELmB1atXIzw8HEuXLr3q2Pr167FhwwYsX74c3t7eaNu2LX755RdUV1fbjHLk5OTYPK99+/YAAIVCgeTkZLvXnJeXh/T0dCQlJTU4wnFZXFwcZs2ahVmzZiE7Oxu9evXCO++8g88++wxAwwGgKS6P7FzZ5qlTpwDUXXUCAMHBwQDqrh4JCgqynnfu3Lmr2muotri4OFRWVv7t723btm2RlpaGyspKm1GOkydPNqo/RO6CcziIXFxNTQ3Wr1+P4cOH47777rtqmzZtGioqKqyXsqakpMBoNOKjjz6ytmGxWK4KK+Hh4Rg0aBA++OADFBQUXPW6ly5danLNpaWlePDBB2E2m61Xb9Snuroaer3eZl9cXBz8/f1hMBis+3x9fe12mejFixexYcMG62OdTodPP/0UvXr1sn6dEhcXBwDWeRZA3foeq1atuqq9hmp74IEHkJGRgS1btlx1TKvVwmQyAQDuuusumEwmLFu2zHrcbDZjyZIlTesgkYviCAeRi9u0aRMqKipw991313t8wIAB1kXAxowZg1GjRqF///6YNWsWcnJykJCQgE2bNqG0tBSA7f/Ily5diptuugndu3fHlClT0L59exQWFiIjIwPnz5/HoUOH/ra+U6dO4bPPPoMQAjqdzrrSaGVlJRYtWoQ77rjjL587ZMgQPPDAA+jSpQvkcjk2bNiAwsJCjB071npenz59sGzZMrz66qvo0KEDwsPDcdtttzX2t9BGx44dMXnyZOzduxdqtRqffPIJCgsLsWLFCus5Q4cORUxMDCZPnoxnn30WMpkMn3zyCVq1aoW8vDyb9hqq7dlnn8WmTZswfPhwTJw4EX369EFVVRWOHDmCr776CmfPnkVYWBhGjBiBgQMHYvbs2Th79qx1XZDy8vIm9Y/IZTn5Khki+hsjRowQXl5eoqqqqsFzJk6cKBQKhSguLhZCCHHp0iXxj3/8Q/j7+4vAwEAxceJE8dtvvwkAYu3atTbPPX36tHj44YdFRESEUCgUonXr1mL48OHiq6+++tvaAFg3qVQqgoKCRO/evcX06dPFsWPHrjr/z5fFFhcXi9TUVJGQkCB8fX1FYGCgSExMFF9++aXN8zQajRg2bJjw9/cXAKyXoV6+THXv3r1XvVZDl8UOGzZMbNmyRfTo0UOoVCqRkJAg1q1bd9XzMzMzRWJiolAqlSImJkYsWrSo3jYbqk0IISoqKsScOXNEhw4dhFKpFGFhYeLGG28Ub7/9tqitrbWeV1JSIh566CEREBAgAgMDxUMPPSQOHDjAy2LJo/BeKkTXiY0bN+Kee+7Bjh07MHDgQGeXQ0TXGQYOIg9UU1Njc+WG2WzG0KFDsW/fPmg0Grtf1UFE9Hc4h4PIAz311FOoqalBUlISDAYD1q9fj507d+L1119n2CAip+AIB5EHWrNmDd555x3k5ORAr9ejQ4cOmDp1KqZNm+bs0ojoOsXAQURERA7HdTiIiIjI4Rg4iIiIyOE4aRR1qzBevHgR/v7+dl1CmYiIyNMJIVBRUYGoqChIpQ2PYzBwoG6p4+joaGeXQURE5Lby8/PRpk2bBo8zcOCPW2fn5+cjICDAydUQERG5D51Oh+jo6L+9SSMDB/64t0RAQAADBxERURP83ZQETholIiIih2PgICIiIodj4CAiIiKHY+AgIiIih2PgICIiIodj4CAiIiKHc2rg2L59O0aMGIGoqChIJBJs3LjResxoNOL5559H9+7d4evri6ioKDz88MO4ePGiTRulpaUYN24cAgICEBQUhMmTJ6OysrKFe0JERER/xanrcFRVVaFnz56YNGkS7r33Xptj1dXV2L9/P+bOnYuePXuirKwM06dPx9133419+/ZZzxs3bhwKCgqwdetWGI1GPPLII3jsscewZs2alu4OkcvLy8tDcXGxXdoKCwtDTEyMXdoiIs/nMrenl0gk2LBhA0aNGtXgOXv37kX//v1x7tw5xMTEICsrC126dMHevXvRt29fAMDmzZtx11134fz584iKimrUa+t0OgQGBqK8vJwLf5HHysvLQ0LnzqiprrZLe94+PjiRlcXQQXSda+y/oW610mh5eTkkEgmCgoIAABkZGQgKCrKGDQBITk6GVCrF7t27cc8999TbjsFggMFgsD7W6XQOrZvIFRQXF6Omuhrjnn8L6pi4ZrVVmHcaqxc+i+LiYgYOImoUtwkcer0ezz//PB588EFrgtJoNAgPD7c5Ty6XIyQkBBqNpsG2FixYgFdeecWh9RK5KnVMHNrEd3V2GUR0nXGLq1SMRiMeeOABCCGwbNmyZrc3Z84clJeXW7f8/Hw7VElEREQNcfkRjsth49y5c9i2bZvN90MREREoKiqyOd9kMqG0tBQRERENtqlSqaBSqRxWMxEREdly6RGOy2EjOzsbP//8M0JDQ22OJyUlQavVIjMz07pv27ZtsFgsSExMbOlyiYiIqAFOHeGorKxETk6O9XFubi4OHjyIkJAQREZG4r777sP+/fvx3XffwWw2W+dlhISEQKlUonPnzrjjjjswZcoULF++HEajEdOmTcPYsWMbfYUKEREROZ5TA8e+ffswePBg6+OZM2cCACZMmICXX34ZmzZtAgD06tXL5nm//PILBg0aBABYvXo1pk2bhiFDhkAqlWL06NF49913W6R+IiIiahynBo5Bgwbhr5YBacwSISEhIVzki4iIyMW59BwOIiIi8gwMHERERORwDBxERETkcAwcRERE5HAMHERERORwDBxERETkcAwcRERE5HAMHERERORwDBxERETkcAwcRERE5HAMHERERORwDBxERETkcAwcRERE5HAMHERERORwDBxERETkcAwcRERE5HAMHERERORwDBxERETkcAwcRERE5HAMHERERORwDBxERETkcAwcRERE5HAMHERERORwDBxERETkcAwcRERE5HBODRzbt2/HiBEjEBUVBYlEgo0bN9ocF0LgpZdeQmRkJLy9vZGcnIzs7Gybc0pLSzFu3DgEBAQgKCgIkydPRmVlZQv2goiIiP6OUwNHVVUVevbsiaVLl9Z7/M0338S7776L5cuXY/fu3fD19UVKSgr0er31nHHjxuHYsWPYunUrvvvuO2zfvh2PPfZYS3WBiIiIGkHuzBe/8847ceedd9Z7TAiBxYsX48UXX8TIkSMBAJ9++inUajU2btyIsWPHIisrC5s3b8bevXvRt29fAMCSJUtw11134e2330ZUVFSL9YWIiIga5rJzOHJzc6HRaJCcnGzdFxgYiMTERGRkZAAAMjIyEBQUZA0bAJCcnAypVIrdu3c32LbBYIBOp7PZiIiIyHFcNnBoNBoAgFqtttmvVqutxzQaDcLDw22Oy+VyhISEWM+pz4IFCxAYGGjdoqOj7Vw9ERERXcllA4cjzZkzB+Xl5dYtPz/f2SURERF5NJcNHBEREQCAwsJCm/2FhYXWYxERESgqKrI5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HngA06dPh8lkQmRkJNatW4dBgwZh9uzZ+P7773HkyBHr+S+++CJee+01lJWVISgoCI8++ihkMhk++OAD6zk7duzArbfeiqqqKnh5eTmjW0TUAI5wEFGLO3nyJPbs2YMHH3wQACCXyzFmzBh8/PHH1uP9+vWzeU7//v1tHh86dAgrV66En5+fdUtJSYHFYkFubm7LdISIGk3u7AKI6Prz8ccfw2Qy2UwSFUJApVLhvffea1QblZWVePzxx/H0009fdSwmJsZutRKRfTBwEFGLMplM+PTTT/HOO+9g6NChNsdGjRqFzz//HJ06dcIPP/xgc2zv3r02j2+44QYcP34cHTp0cHjNRNR8nMNBRC1q48aNGDNmDIqKihAYGGhz7Pnnn8e2bdvw5ZdfolOnTnjmmWcwefJkHDx4ELNmzcL58+eh1WoRGBiIw4cPY8CAAZg0aRIeffRR+Pr64vjx49i6dWujR0mIqOVwDgcRtaiPP/4YycnJV4UNABg9ejT27duHiooKfPXVV1i/fj169OiBZcuWWa9SUalUAIAePXogPT0dp06dws0334zevXvjpZde4loeRC6KIxxE5BZee+01LF++HPn5+c4uhYiagHM4iMglvf/+++jXrx9CQ0Px22+/4a233uIaG0RujIGDiFxSdnY2Xn31VZSWliImJgazZs3CnDlznF0WETURv1IhIiIih+OkUSIiInI4Bg4iIiJyOAYOIiIicjgGDiIiInI4Bg4iIiJyOAYOIiIicjgGDiIiInI4Bg4iIiJyuP8Pho+yGWL43gYAAAAASUVORK5CYII=",
      "text/plain": [
       "<Figure size 600x300 with 1 Axes>"
      ]
     },
     "metadata": {},
     "output_type": "display_data"
    }
   ],
   "source": [
    "plt.figure(figsize=(6,3))\n",
    "sns.histplot(data[\"Age\"],kde=True)\n",
    "plt.title(\"Age Distributed\")\n",
    "plt.xlabel(\"Age\")\n",
    "plt.ylabel(\"Count\")\n",
    "plt.show()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 19,
   "id": "a514af92-c2fc-460b-b2d4-86fdece07e81",
   "metadata": {},
   "outputs": [
    {
     "name": "stderr",
     "output_type": "stream",
     "text": [
      "No artists with labels found to put in legend.  Note that artists whose label start with an underscore are ignored when legend() is called with no argument.\n"
     ]
    },
    {
     "data": {
      "image/png": "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",
      "text/plain": [
       "<Figure size 600x300 with 1 Axes>"
      ]
     },
     "metadata": {},
     "output_type": "display_data"
    }
   ],
   "source": [
    "plt.figure(figsize=(6,3))\n",
    "sns.countplot(data=data,x=\"Sex\",hue=\"Sex\")\n",
    "plt.title(\"Survival by Gender\")\n",
    "plt.xlabel(\"Gender\")\n",
    "plt.ylabel(\"Count\")\n",
    "plt.legend(title=\"Survived\",loc=\"upper right\")\n",
    "plt.show()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 20,
   "id": "be0057bb-72ff-4d59-b366-fdf7dfcfe3ed",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "image/png": "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8AJDhw4lOjqamTNn8uCDDyKTyXj33XcjBjT9+/fnww8/5OGHH2bgwIEYjUauvfZaMjMziYqK4q233sJkMmEwGBg8eDDp6en897//ZeLEifTo0YM777yTDh06cPz4cb777jvMZjNffvnlBX0WXq+XsWPHctNNN7F//37eeOMNhg8fznXXXVfvMffccw//+te/uOOOO9iyZQudO3fm448/Zt26dbzyyiuYTCagtlk9JyeHDz/8kK5duxITE0PPnj3rzcP47W9/y/vvv8/EiRN58MEHiYmJYd68eeTl5fHJJ5+c98RRHo+HTz75hPHjx6PVaiPuc9111/Hqq69SWlpKQkICzzzzDA888ABXXnklN910E/n5+cydO5fMzMywlozbbruNjz76iHvvvZfvvvuOYcOGEQgE2LdvHx999BHLli0LtZidLTs7m8zMTB555BGOHz+O2Wzmk08+adT8J/W59tprGTZsGL/97W/Jz88nJyeHTz/99IJyiM50zTXX8Nxzz3HnnXcydOhQdu7cyfz588nIyGjU8XK5vMW/y8IlrM3GxwhCC1u6dKn0i1/8QsrOzpaMRqOkVqulrKws6YEHHpBKSkrq7P+///1P6tu3r6TRaKTo6Ghp1KhR0vLly0Pl69atk4YMGSLpdDopJSUlNMwWkL777rvQfna7Xbr11lulqKgoCQgbIvv5559LOTk5klKprDOM8aeffpKmTp0qxcbGShqNRkpLS5NuuukmacWKFaF9Tg2LLSsra9RncGpY7OrVq6V77rlHio6OloxGozRjxgypoqIibN+zh8VKkiSVlJRId955pxQXFyep1WqpV69eEYderl+/Xurfv7+kVqsbNUT28OHD0vTp06WoqChJq9VKgwYNkhYvXlxnPxoxLPaTTz6RAOntt9+ud59Vq1ZJgPTqq6+Gtr322mtSWlqapNFopEGDBknr1q2T+vfvL1199dVhx3q9XunPf/6z1KNHj9B3o3///tKzzz4rVVdXN1i3PXv2SOPGjZOMRqMUFxcn3X333dL27dvr/O5nzpwpGQyGOsef+n2fqaKiQrrtttsks9ksWSwW6bbbbpN++umn8xoWu3Dhwojlbrdb+vWvfy0lJydLOp1OGjZsmLRhw4Y6341znacx32Wh/ZFJUiNmDRIE4ZI0d+5c7rzzTjZt2lTvk7hQKxgMEh8fz9SpUyN2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",
      "text/plain": [
       "<Figure size 600x300 with 1 Axes>"
      ]
     },
     "metadata": {},
     "output_type": "display_data"
    }
   ],
   "source": [
    "plt.figure(figsize=(6,3))\n",
    "sns.scatterplot(data=data,x=\"Age\",y=\"Fare\", hue=\"Age\")\n",
    "plt.title(\"Scatter plot of Age and Fare\")\n",
    "plt.xlabel(\"Age\")\n",
    "plt.ylabel(\"Fare\")\n",
    "plt.legend(title=\"Survived\")\n",
    "plt.show()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "id": "c3b345f9-6cfd-4ded-914b-9cbbf3164077",
   "metadata": {},
   "outputs": [],
   "source": []
  }
 ],
 "metadata": {
  "kernelspec": {
   "display_name": "Python 3 (ipykernel)",
   "language": "python",
   "name": "python3"
  },
  "language_info": {
   "codemirror_mode": {
    "name": "ipython",
    "version": 3
   },
   "file_extension": ".py",
   "mimetype": "text/x-python",
   "name": "python",
   "nbconvert_exporter": "python",
   "pygments_lexer": "ipython3",
   "version": "3.10.11"
  },
  "widgets": {
   "application/vnd.jupyter.widget-state+json": {
    "state": {},
    "version_major": 2,
    "version_minor": 0
   }
  }
 },
 "nbformat": 4,
 "nbformat_minor": 5
}

