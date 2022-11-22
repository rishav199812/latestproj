pipeline {
    agent {
          docker {
               image 'qnib/pytest'
          }
     }
     stages{
       stage('test') {
         steps {
            sh 'virtualenv venv && . venv/bin/activate && pip install -r requirements.txt && python tests.py'
     }
     }
}
}