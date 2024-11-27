## Kurzbeschreibung
Dies sind die Installations- und Konfigurationsdaten der CI-CD-Pipeline für das Hauptrojekt (siehe <a href="https://github.com/lb-bewerbung/jobscraper-jenkins">Jobscraper-Jenkins</a>). 

### Dateien
1. install_docker.sh 
   - Installiert aktuellste Docker Engine 
2. run_docker_in_docker.sh
   - Erstellt und startet einen Jenkins-side-container, der es ermöglicht Dockerbefehle in einem Container auszuführen
3. Dockerfile.jenkins-install
   - Erstellt ein Image für einen Jenkins-in-Docker-container 
   - Enthält alle benötigten Pakete und Jenkins Plugins
4. run_jenkins_in_container.sh
   - Startet Jenkins
   - Konfiguriert Volumes, Umgebungsvariablen und Ports
5. CommitPipeline
   - Build und Test einer neuen Softwareversion
   - Erstellt ein Docker image
6. DeployPipeline
   - Webserverkonfiguration, Deploy und Start einer Softwareversion in einem Container
