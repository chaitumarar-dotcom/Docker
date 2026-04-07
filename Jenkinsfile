pipeline{
  agent any
  stages{
    
      stage('1. checkout'){
        steps{
          git url:'https://github.com/chaitumarar-dotcom/Docker.git',branch:'main'
        }
      }
      
      stage('2. Build Image'){
        steps{
          bat 'docker build -t hello .'
        }
      }
  
      stage('3. Stop/Remove old Containers'){
        steps{
          bat 'docker stop mycont || exit 0'
          bat 'docker rm mycount || exit 0'
        }
      }
  
      stage('4. Run the Image Containerize'){
        steps{
          bat 'docker run -d -p 5000:80 --name mycount hello'
        }
      }

    
  } 
}
