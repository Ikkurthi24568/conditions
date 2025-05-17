pipeline{
    agent any
    stages{
        stage('parallel Running Stage'){
            parallel{
                stage('stage1'){
                    steps{
                        echo "Stage1 Excute"
                        sleep 10
                    }
                }
                stage('stage2'){
                    steps{
                        echo "Stage2 Excute"
                        sleep 10
                    }
                }
                stage('stage3'){
                    steps{
                        echo "Stage3 Excute"
                        sleep 10
                    }
                }
            }
        }
    }
}
