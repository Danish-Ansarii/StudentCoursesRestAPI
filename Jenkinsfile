pipelines{
    agent { labels 'docker'}
    triggers { pollSCM('* * * * *') }
    stages{
        stage{
            step('vcs'){
                git url: https://github.com/Danish-Ansarii/StudentCoursesRestAPI.git,
                    branch: develop
            }
        }
        stage{
            step('build'){
                sh 'echo scanning',
                sh docker image push danish/spc:latest

            }
        }
    }
}