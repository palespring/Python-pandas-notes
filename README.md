# Python-pandas-notes
something notes about pandas
## 1、切片
### ① df.loc[index, column_name]
    df.loc[0,'name']  //0 为index值，非序号
    df.loc[0:2, ['name','age']]
    df.loc[[2,3],['name','age']]
### ② df.iloc[row_index, column_index]
    内容几乎同上
## 2、列
### ① column_name = df.columns[0]
    取序号为0的列的名称
### ② column_data = df[column_name]
    取名称为‘column_name’列的数据
### ③ df[column_name] = df[column_name].apply()
    对名称为'column_name'列的数据进行操作，括号中可用lamda x:x 或者置入方法
### ④ columns = df.columns
    取所有列名称
### ⑤ df.columns = df.columns.map()
    对所有列名称进行操作，括号中可用lamda x:x 或者置入方法
## 3、索引
### ① df.index = df.index.map()
    对所有index进行操作，括号中可用lamda x:x 或者置入方法
### ② df.set_index(column_name,inplace=True)
    重置索引（将列名称为‘column_name’的列置为索引，并且在原df上生效（implace=True））
## 4、删除
### ① df.drop(df.columns[[0]], axis=1, inplace=True)
    删除序号为0的列，axis=1表示列（不填表示 行）
## 5、新增
### ① df.insert(0, df_unit_name, df_unit_data)
    新插入列，在序号为0的列的位置
## 6、合并
### ① pd.concat()
    df_qty_total = pd.concat([df_qty_total, df_qty])
   合并以前
![df_qty](https://github.com/palespring/Python-pandas-notes/blob/master/df_qty.png)
![df_qty](https://github.com/palespring/Python-pandas-notes/blob/master/df_qty_total.png)
   合并以后
![df_qty](https://github.com/palespring/Python-pandas-notes/blob/master/df_qty_total2.png)
