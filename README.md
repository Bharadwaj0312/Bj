(app js) -
const express = require('express');
const app = express();
app.get('/',(req,res) => {
res.send("Hello World, I am from Nodejs");
});
app.listen(3020,() => {
console.log("Server is running on port 3020")
});

(pipeline for app.js)
pipeline {
 agent any
 stages {
 stage('Clone Repository') {
 steps {
 git branch: 'main', url: 'https://github.com/deepak574/nodejsexample.git'
 }
 }
 stage('Install Dependencies') {
 steps {
 bat 'npm install'
 }
 }
 stage('Run Application') {
 steps {
 bat 'node app.js'
 }
 }
 }
}
