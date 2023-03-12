pipelines{
    agent { labels 'docker'}
    triggers { pollSCM('* 23 * * 1-5') }
    stages{
        stage{
            step('vcs'){
                git url: https://github.com/Danish-Ansarii/StudentCoursesRestAPI.git,
                    branch: sprint-1-release
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