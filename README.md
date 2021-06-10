# JiraMap
A simple Jira enumerator

### Creating your environment to do local tests
```
docker volume create --name jiraVolume
docker run -v jiraVolume:/var/atlassian/application-data/jira --name="jira" -d -p 8080:8080 atlassian/jira-software
```
## Do an enumeration of available gadgets (some pages require authentication):

/rest/config/1.0/directory
```
