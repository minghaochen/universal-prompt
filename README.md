

[中文](README.zh.md)

# Large Language Model Prompt Optimization Tool

Optimize your prompts like PromptPerfect to unlock the potential of large language models and achieve more accurate and relevant responses.

**Universal Prompts**: Provides a robust template for crafting precise and effective prompts to guide models towards high-quality responses.



The **core concept** of optimizing prompts is to adhere to the fundamental principles of prompt construction:

A prompt may consist of the following elements:

- Instruction: This is a clear task or directive you wish the AI model to undertake.
- Context: It includes any external information or added details that can guide the AI towards generating more accurate responses.
- Input Data: This is the specific inquiry or input for which you are seeking an answer.
- Output Indicator: It specifies the desired format or type of response.



Usage:

- If you are directly calling the LLM's API, you can input in the format of system, user.
- If you are asking questions directly to chatgpt/gpt4, you may input in two separate turns.



### Example 1

Before：

```
Classify the text into neutral, negative or positive. 
```

After:

```
Prompt: <Analyze the sentiment of the following text snippet and categorize it as either 'neutral', 'negative', or 'positive'. Please provide a brief justification for your classification to offer insight into your reasoning process.>
```

### Example 2

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

### Example 3

Before:

```
translate the following English content into Chinese, 并润色
```

After:

```
<Please translate the following English text into Chinese, ensuring not only accuracy in translation but also enhancing the prose to flow naturally and elegantly in Chinese. The translation should read as if originally written by a native speaker, with attention to cultural nuances and idiomatic expressions.>
```

### Example 4

Before:

```
完善句子
```

After:

```
请根据以下的中文句子开头，完善每个句子。你的句子补全应当语法正确，上下文恰当，并且展现出一定的创造性或有趣的思考，使句子吸引人。请确保遵循每个句子开头提供的风格或语气指示。
```





## License

This project is licensed under the MIT License.