[English](README.md)



# 大语言模型提示词优化工具

优化你的提示词，就像PromptPerfect一样，发掘大型语言模型的潜力，获得更精确、更相关的回应。

**万能提示词**: 提供一个强大的模板，帮助你创建准确、有效的提示词，以引导模型产生高质量的回应。



优化prompt的关键思路是，坚守编写提示时的根本规则：

一个提示指令通常包括以下几个要素：

- 指令：你期望AI模型执行的明确任务或者具体指导。
- 上下文示例：涵盖任何外部信息或额外的细节，这些可以帮助AI更准确地产生响应。
- 输入数据：特定的查询或输入，你希望对此得到回答。
- 输出指示：说明期望的响应格式或类型。



使用方式：

- 如果是直接调用LLM的API，可以按照system、user的方式输入
- 如果直接用chatgpt/gpt4进行提问，可以分两次输入



### 示例1

Before：

```
Classify the text into neutral, negative or positive. 
```

After:

```
Prompt: <Analyze the sentiment of the following text snippet and categorize it as either 'neutral', 'negative', or 'positive'. Please provide a brief justification for your classification to offer insight into your reasoning process.>
```

### 示例2

Before:

```
Table departments, columns = [DepartmentId, DepartmentName]
Table students, columns = [DepartmentId, StudentId, StudentName]
Create a MySQL query for all students in the Computer Science Department
```

After:

```
Write a MySQL query to retrieve all records of students who are part of the Computer Science Department. Assume there are two tables involved: one named 'departments' with columns 'DepartmentId' and 'DepartmentName', and another named 'students' with columns 'DepartmentId', 'StudentId', and 'StudentName'. The 'DepartmentId' column in the 'students' table references the 'DepartmentId' in the 'departments' table as a foreign key. The query should list all students where 'DepartmentName' is "Computer Science". Ensure that the query is syntactically correct and properly formatted for use in a MySQL database.
```

### 示例3

Before:

```
translate the following English content into Chinese, 并润色
```

After:

```
<Please translate the following English text into Chinese, ensuring not only accuracy in translation but also enhancing the prose to flow naturally and elegantly in Chinese. The translation should read as if originally written by a native speaker, with attention to cultural nuances and idiomatic expressions.>
```

### 示例4

Before:

```
完善句子
```

After:

```
请根据以下的中文句子开头，完善每个句子。你的句子补全应当语法正确，上下文恰当，并且展现出一定的创造性或有趣的思考，使句子吸引人。请确保遵循每个句子开头提供的风格或语气指示。
```



## 许可证

此项目采用MIT许可证。

