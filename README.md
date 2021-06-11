# JiraMap
A simple Jira enumerator

### Creating your environment to do local tests
```
docker volume create --name jiraVolume
docker run -v jiraVolume:/var/atlassian/application-data/jira --name="jira" -d -p 8080:8080 atlassian/jira-software
```

### Get all Jiras from wordlist hosts
```
httpx -l todosPagosUp -path '/rest/config/1.0/directory.json' -match-string 'com.atlassian.jira.gadgets' -threads 400 | anew todosJiras
```
---
### Enumeration of available gadgets (some pages require authentication):

#### All Gadgets
jiraurl/rest/config/1.0/directory.json

#### Get Jira version
jiraurl/rest/api/2/serverInfo

#### Get All endpoints from specified version
https://docs.atlassian.com/software/jira/docs/api/REST/{{VERSION}}

## Resources
https://github.com/elfarsaouiomar/scan-jira-endpoints

https://github.com/0x48piraj/Jiraffe/blob/4d7634557e708a58ea2857fb18d1ffe4c7f74546/jiraffe/exploits.py
