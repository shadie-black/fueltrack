pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                // sh 'composer install --no-scripts'
                 sh 'composer install --no-interaction'

                // sh 'php artisan key:generate'
                // sh 'php artisan migrate --force'
            }
        }
        stage('Test') {
            steps {
                sh 'phpunit'
            }
        }
        stage('Deploy') {
            steps {

                // echo "deploying "
                sh 'rsync -avz -e "ssh -p22" --exclude-from="rsync-exclude.txt" . ubuntu@54.158.64.65:/var/www/html/fueltrack; \

                 sh composer install --no-interaction; \

                 php artisan migrate --force; \
                 php artisan cache:clear; \
                 php artisan config:cache; \
                //  '
            }
        }
    }
}


































// pipeline {
//    agent any

//     stages {
//         stage('Build') {
//             steps {

//                                 echo 'building'




//                 //  sh 'php --version'
//                 // sh 'composer install'
//                 // sh 'composer --version'
//                 // sh 'cp .env.example .env'
//                 // sh 'php artisan key:generate'
// //                git 'https://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@github.com/hasin0/fueltrack.git'
//             //  sh  'sudo mv composer.phar /usr/local/bin/composer'

//         //     //     sh 'composer install --no-interaction'
//         //       sh 'chmod +x scripts/jenkins-build.sh'
//         //  sh './scripts/jenkins-build.sh'
//         //         // sh 'cp .env.example .env'
//         //         // sh 'php artisan key:generate'
//             }
//         }
//         stage('Test') {
//             steps {
//                 // sh './vendor/bin/phpunit'
//                                 echo 'test'

//             }
//         }
//     }

//   }

