pipeline
 {
agent any
 
   stages
 {
    stage ('Clone sources')
{
     steps
 {       
      git url: 'https://github.com/RavitejaAdepudi/javawar.git'
           
 }
  }
  stage ('Compile Stage') 
{
  steps 
{
               
 withMaven(maven : 'maven_3_5_0') 
{  
       sh 'mvn -f mavewebappdemo/pom.xml clean install'
             
   }
     
       }
   
     }
       
    stage ('Testing Stage') 
{

      
      steps
 {
      
          withMaven(maven : 'maven_3_5_0') 
{
     
               sh 'mvn -f pom.xml  test'
                
}
      
      }
    

    }
       
stage('Deploy to Tomcat')
{
       
 steps
 {
    
   sh 'cp -r /root/.jenkins/workspace/mymavenmanualpipeline/target/* /opt/apache-tomcat-8.5.29/webapps/'
     
  }
    }

    }

}
