iterrows() 是 pandas 中用于逐行迭代 DataFrame 的方法。每次迭代返回一个 (index, Series) 元组，其中 index 是行标签，Series 包含行的数据。

> [!CAUTION]
> 注意：当你使用 iterrows() 遍历 DataFrame 时，每次循环得到的那个 row 对象，是原始 DataFrame 中对应行的一个独立副本。iterrows() 在 Pandas 中相对较慢，因为它需要为每一行构建一个 Series 对象。除非没有其他办法，否则应尽量避免在大型数据集上使用它。

**如何正确地在迭代中修改 DataFrame？**
既然不能直接修改 row，正确的方法是使用 .at 或 .loc 方法，它们通过 索引 和 列名 直接定位并修改原始 DataFrame 中的单元格。
现在有一原始 DataFrame:
      Name  Age      City
0    Alice   25  New York
1      Bob   30    London
2  Charlie   35     Tokyo
`for index, row in df.iterrows():
    df.at[index, 'Age'] = row['Age'] + 1`

直接定位到原始 df 的特定单元格进行修改
items()返回结果是类型是dict_items，可以转换为列表list()再进行下一步计算