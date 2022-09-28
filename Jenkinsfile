pipeline{

agent {  
        label 'built-in'
}

stages{

stage ('install apache') {

steps {
        sh "yum install httpd -y"

}
}
}
stage ('start apache') {

steps {
        sh "service start"

}
}


stage ('deploy index'){

steps {
        sh "cp -r index.html /var/www/html/"
        sh "chmod -R 777 /var/www/html/index.html"
}
}
}
