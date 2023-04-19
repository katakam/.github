# .github
## GitHub Template Repo

## 🚦 Pipeline Workflow
This repository store the SES workflow templates.

```mermaid
graph TD;
    main-->Setup-Environment;
    main--docker-compose-->Test-Application;
    main--code-quality-->SonarQube-Scan;    
    Setup-Environment-->Build-and-Push;
    Test-Application-->Build-and-Push;
    SonarQube-Scan-->Build-and-Push;    
    Build-and-Push--security-gateway-->Trivy-Scan;
    Trivy-Scan-->GitOps-Deploy;
    GitOps-Deploy--notify-->Slack;
```

## feature tests 
## release build-and-push, deploy
## hotfix tests , build-and-push, deploy
## main promote
