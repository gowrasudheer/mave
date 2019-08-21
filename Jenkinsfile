pipeline{
	agent any
	stages{
	stage('compilestage'){
	steps{
	withmaven(maven : maven){
	sh 'mvn compile'
	}
     }
}
}
}
