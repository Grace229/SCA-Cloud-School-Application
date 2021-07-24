Syntax for defining jenkins file (using declarative syntax)

there are three main steps when declaring a jenkins file with this syntax 
the agent directive -this is used to to declare the environment in which the pipeline will run in in the sample below it is set to any;

the stages directive - this is used to declare discrete parts of the continuous delivery process, such as Build, Test, 
and Deploy. they are used to group tasks performed at these stages together

the steps directive - this section defines a series of one or more steps to be executed in a given stage directive. 

the steps described above are shown in the dummy jenkins file illustration below. 

```
pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
              //
            }
        }
        stage('Test') {
            steps {
               //
            }
        }
        stage('Deploy') {
            steps {
               //
            }
        }
    }
}
```
#Source Control

Create a pipeline project,
on the pipeline configuration page selecte the pipeline script from SCM option on the description field,
From the SCM field, choose git as the source control system and enter your git repository url and the script path.
On github, click setings on the project repository and click webhook, 
then click on add webhook, paste your Jenkins environment URL on the payload field and select the event that should trigger the webhook,
Finally click Add webhook. 


