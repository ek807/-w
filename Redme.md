本项目使用Python的`pandas`库来处理这个任务。将一个.xlsx文件分成多份，每份的数据量如下：前四份1000条，最后一份562条的步骤。可以进行自由修改

1. 安装`pandas`和`openpyxl`（如果你还没有安装）：

   ```bash
   pip install pandas openpyxl
   ```



1. `pd.read_excel('your_file.xlsx')`：读取你提供的Excel文件。
2. `chunks.append(df[i * split_size: (i + 1) * split_size])`：将数据每1000行分割一次，前四份分别包含1000条数据。
3. `chunk.to_excel(f'output_part_{idx + 1}.xlsx', index=False)`：将每个分块保存成新的.xlsx文件。

记得将代码中的`'your_file.xlsx'`替换成你文件的路径。如果你有具体的表格文件，代码将会把数据分割成多个文件并保存。