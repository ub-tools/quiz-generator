# CSE 220 Handout Quiz Generator

## Running the Quiz Generator

The quiz generator requires a python3 installation with the `yattag`
library. It is recommended that you use a virtual environement for
python, specifically python3 venv.

## Quiz Generator Inputs

The quiz generator expects a file called questions.json. This file
contains the questions for the quiz and will be passed into the
generator to generate a key for the grader and a form to allow students
to enter their answers.

### Question Types

 * `tf`: True/False
 * `mc`: Multiple Choice
 * `sa`: Short Answer

### Format for questions.json

```json
{
    'name' : 'Quiz Name',
    'version' : 'Quiz version string',
    'questions': [
        {
            "type" : "sa",
            "name" : "sa_question",
            "prompt" : "Question Prompt",
            "answer" : "Question Answer",
            "help" : "Failed Question Response"
        },
        {
            "type" : "tf"
            "name" : "tf_question",
            "prompt" : "Question Prompt",
            "answer" : true,
            "help" : "failed question response"
        },
        {
            "type" : "mc",
            "name" : "mc_question",
            "prompt" : "Question Prompt",
            "options" : [
                "Option 1",
                "Option 2",
                "Option 3"
            ],
            "answer" : [ "1", "3" ],
            "help": "failed question response"
        }
    ]
}
```

## Steps to run the program
1. python3 -m venv env
2. source env/bin/activate
3. pip install wheel
4. pip install -r python_libraries.txt
5. cd src
6. python generate_quiz

## Authors

This quiz generator is originally by Vikram Singh
<vsingh23@buffalo.edu>.  It has been substantially modified by Ethan
Blanton <eblanton@buffalo.edu>.
