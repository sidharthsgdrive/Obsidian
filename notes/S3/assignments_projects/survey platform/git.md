`02/10/25` Cloned Royce's work to a local directory, then copied `myapp` to `/opt/tomcat/webapps`. Then I made a local repository for `myapp`, and pushed that to the repo:
```bash
  827  git init
  828  ls
  829  git remote add origin https://github.com/SidharthVJain/survey_platform.git
  830  git add .
  831  git commit -m "Royce's frontend content"
  832  git checkout -b myapp
  833  git push -u origin myapp

```
