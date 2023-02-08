node {
stage("Git Clone"){

git branch: 'main', url: 'https://github.com/chanakyad/eurekaserver1.git'
}
stage("Docker build"){
sh 'docker build -t claimsui .'
sh 'docker images'
stage("Deploy"){
sh 'docker rm -f claimsui||true'
sh ' docker run -d -p 8000:80 --name claimsui claimsui'
}
}
}
