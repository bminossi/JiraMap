# JiraMap
A simple Jira enumerator

### Creating your environment to do local tests
```
docker volume create --name jiraVolume
docker run -v jiraVolume:/var/atlassian/application-data/jira --name="jira" -d -p 8080:8080 atlassian/jira-software
```
---
### Enumeration of available gadgets (some pages require authentication):

#### Unknown
/rest/config/1.0/directory

#### Get Jira version
jiraurl/rest/api/2/serverInfo

#### Get All endpoints from specified version
https://docs.atlassian.com/software/jira/docs/api/REST/{{VERSION}}

## Resources
https://github.com/elfarsaouiomar/scan-jira-endpoints
