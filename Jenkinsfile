node {
   stage('Preparation') { // for display purposes
      // Get some code from a GitHub repository
      sh "echo 'some prep steps'"
   }
   stage('API Tests') {
      sh '/usr/local/bin/node /usr/local/bin/newman run "devchallenge-r2.tests.json" -e "devchallenge-r2.env.json" --export-environment "devchallenge-r2.env.json" -r cli,htmlextra --reporter-htmlextra-export "reports/APITestSummary.html" --reporter-htmlextra-darkTheme'
   }
   stage('Results') {
      archiveArtifacts 'reports/*.html'
      publishHTML([
      	allowMissing: true, 
      	alwaysLinkToLastBuild: false, 
      	keepAll: false, 
      	reportDir: 'reports', 
      	reportFiles: 'APITestSummary.html', 
      	reportName: 'API Test Summary', 
      	reportTitles: ''])
   }
}