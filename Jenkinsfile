// Ce pipeline Jenkins est un pieline déclaratif pour tester les stages

pipeline {
    
    agent any
    
    environment {
       PRENOM = 'issam'
       NOM = 'Mejri'
    }
    
    parameters {
        
        string(name: 'Name', defaultValue: 'issam', description: "Name of the devops")
        string(name: 'Last_Name', defaultValue: 'mejri', description: "Last Name of the devops")
    }
    
    stages {
        
        stage('affichage de prénom') {
            
            steps {
                
                echo "mon prénom est ${params.Name}"
                
            } // fin steps
        } // fin stage
        
        stage('Affichage de nom de famille') {
            
            steps {
                
                echo "Mon nom de famille est ${params.Last_Name}"
                
            } //steps
        }// stage
        
    } // fin stages
    
    post { 
        success { 
            echo "Notre ingénieur DevOps est ${params.Name} ${params.Last_Name}"
        }
    }
    
} //pipeline