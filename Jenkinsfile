node('master') {
   ws('/disk/docker/docker-elk') {
      stage('Git checkout') {
         ansiColor('xterm') {
	        checkout scm
         }
      }
   
      stage('Compose pull') {
         ansiColor('xterm') {
            sh('docker-compose pull')
         }
      }

      stage('Compose pull') {
         ansiColor('xterm') {
            sh('docker-compose build')
         }
      }
   
      stage('Compose up') {
         ansiColor('xterm') {
            sh('docker-compose up -d --force-recreate')
         }
      }
   }
}
