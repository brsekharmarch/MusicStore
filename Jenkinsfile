node('dotnet') {
    stage('version control') {
        git url: 'https://github.com/brsekharmarch/MusicStore.git',
          branch: 'scripted'
    }
    stage('build the code') {
        sh 'dotnet restore ./MusicStore/MusicStore.csproj && dotnet build ./MusicStore/MusicStore.csproj'
    }
    stage('test') {
       sh 'dotnet test ./MusicStoreTest/MusicStoreTest.csproj --logger:"junit;LogFilePath=test-result.xml"'
    }
}