// Test pipeline
pipeline
{
  // Which agent?
  agent any

  // Stages
  stages
  {
    stage('Build')
    {
      steps
      {
        echo 'Building..'
        sleep(1)
        mattermostSend (
          color: "#2A42EE",
          channel: 'essai',
          endpoint: 'http://192.168.0.133:8065/hooks/wfoscr4wdiyyie51n17815sxie', 
          message: "Hello from jenkins to essai"
        ) 
        mattermostSend (
          color: "#2A42EE",
          channel: 'channel_private1',
          endpoint: 'http://192.168.0.133:8065/hooks/wfoscr4wdiyyie51n17815sxie', 
          message: "Hello from jenkins to channel_private1"
        ) 

      }
    }
    stage('Test')
    {
      steps
      {
        echo 'Testing..'
        sleep(2)
      }
    }
    stage('Deploy')
    {
      steps
      {
        echo 'Deploying....'
        sleep(3)
      }
    }
  }
}



