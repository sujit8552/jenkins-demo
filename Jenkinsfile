pipeline{
  agent{
    node{
      label 'built-in'
      customWorkspace '/home/ec2-user'
    }
  }
  stages{
    stage('SCM checkout'){
      steps{
        sh '''
        git clone https://github.com/Dee601/game-of-life.git
        cd game-of-life
        '''
      }
    }
    stage('BUILD'){
      steps{
        sh '''
        cd /home/ec2-user/game-of-life
        mvn clean install
        '''
      }
    }
    stage('Deploy'){
      steps{
        sh '''
        cp game-of-life/game-of-life-web/target/gameoflife.war /mnt/apache-tomcat-9.0.80/webapps
        '''
      }
    }
  }
}
