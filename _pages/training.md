# Training Documentations

This is Training Documentation of PinjamYuk.

```text
Training Session 1
- Flow of PinjamYuk System part 1
Training Session 2
- Flow of PinjamYuk System part 2
Training Session 3
- Basic Framework of PinjamYuk
Training Session 4
- Basic Development Server Configuration
Training Session 5
- Basic Rule, Format and Directory Base Code
```


## Register Process - Session 1

1. Register Process

`Register Process Flowchart`

![Register Flow](../_media/PY-Register-Process.png 'Register Flow')

2. Loan Disbursement

`Loan Disbursement Flowchart`

![Loan Disbursement](../_media/PY-Loan-Disbursement-Repayment.png 'Loan Disbursement Flow')


## Collect User Info & User Credit Process - Session 2

1. Collect User

`Collect User Flowchart`

![Collect User Flow](../_media/PY-Collect-User.png 'Collect User Flow')

2. User Credit Process

`User Credit Process Flowchart`

![Credit Flow](../_media/PY-Credit-Flow.png 'User Credit Process Flow')

3. Cloudun Credit Flow

`Cloudun Credit Flowchart`

![Cloudun Credit Flow](../_media/PY-Cloudun-Credit.png 'Cloudun Credit Flow')


## Framework Layers - Session 3

Basic Framework of PinjamYuk build with PHP Yii.

There are 4 layers we need to considered.

- Controllers
- Models & Pages
- Services
- Dao

Picture represent 4 layers below :
![Basic Framework](../_media/PY-base-code.png '4 laters basic framework')

```
Controllers 

The controller is the part that bridges the model and view. 
The controller contains commands that function to process data and send it to a web page.
```

```
Models (Pages)

Models represent data structures.
The model is the part that is responsible for managing, preparing, manipulating, and organizing data (usually from a database). 
Models performs inserting data into databases, updating data, deleting data, and others. The model performs its tasks based on instructions from the controller.
```

```
Services

Services represent logic business when we want to add business logic into program.
```

```
Dao

DAO / Database Access Object, is a class that contains methods used to access the database
 
DAO performs inserting data into databases, updating data, deleting data, and others.

The DAO performs its tasks based on instructions from the controller.
```

## Preview Environment - Session 4

Preview Environment (Development Server)

Preview Enviroment we use to develop system before go online production.

How to access?

We need to use VPN or private office network to access this environment.

What is inside Preview Environmnet?

There is nginx to make sure preview environment can get any request.

Which we can go to `/home/work/tool/webroot` we can find our `nginx` here.

The main flow of our preview environment is :

```text
nginx -> php-fpm -> index.php->Yii::createWebApplication->run() -> controller/action
```

## Basic Format - Session 5

Basic Rule, Format and Directory

1. Naming Format

1.1 Function/Class Name Format

`CamelCase` is a way to separate the words in a phrase by making the first letter of each word capitalized and not using spaces

```php
<?php

class OjkReconcileBatchDataCommand extends CConsoleCommand
        
{
    // Your code goes here
}
```

1.2 Variable Name Format

In PHP, a `variable` starts with the `$` sign, followed by the name of the variable:

```php
class OjkReconcileBatchDataCommand extends CConsoleCommand
        
{
    // variable goes here
    $date
    // or
    $start_time
}
```

1.3 Constant Name Format

Name of constants must follow the same rules as variable names, 

which means a valid constant name must starts with a letter or underscore, 

followed by any number of letters, numbers or underscores with one exception: the `$` prefix is not required for constant names.

```php
<?php

class OjkReconcileBatchDataCommand extends CConsoleCommand
        
{
    CONST VERSION = 1;
}
```

2. Format

2.1 Indenting

Line code should using 4 spaces instead of using tabs

2.2 Bracket

Opening curly bracket `{}` for class should go on the next line,

for closing curly bracket should go on the next line after body.

```php
<?php

class OjkReconcileBatchDataCommand extends CConsoleCommand
        
{
    private static function curlyBracket()
    {
        // code goes here
    }
}
```



