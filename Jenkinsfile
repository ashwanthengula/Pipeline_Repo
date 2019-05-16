properties([
    parameters([
choice(choices: ['IL', 'CA', 'TX'], description: 'Select state', name: 'State'),
string(defaultValue: 'Ash', description: 'Enter your name', name: 'Name', trim: false)

])
])
if(State=='IL')
{
    j_node='master'
}         else {
    j_node='w4'
}
node(j_node)
{
    stage('Build and package'){
    
        echo 'this is build stage'
        sleep 4
        echo "choice: ${params.State}"
    }
    stage('QA test'){
        echo 'this is test stage'
        powershell 'Date'
        powershell 'mvn --version'
        echo "choice: ${params.Name}"
    }
    stage('Deploy in prod'){
        echo 'this is deploy code to prod stage'
    }
}
