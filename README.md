# cicd-test-ci

A tiny ASP.NET (net8.0) test service for the cicd-bootstrap CI / CI+CD / CD agents.

```
GET /greeting?name=<name>   ->   {"message": "Hello, <name>!"}
```

It has **no CI/CD workflows** on purpose — point the agents at it to generate them.
The included Dockerfile runs `DotnetService.dll` and listens on **port 8092**, so a
CD deploy serves a real response at http://localhost:8092/greeting?name=Bob
