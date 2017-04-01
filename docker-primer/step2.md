
## Useful commands in Docker
---
### General wrappers for classic Linux commands

Check running containers:
`docker ps`{{execute}}

Check running processes in specific container:
`docker top <name>`

Forward sync - from host to guest:
`docker cp ./ <name>:/`

Backward sync - from guest to host:
`docker cp <name>:/<some_file> ./`
  

**The basics** of Docker (other than this): [zeroturnaround.com/rebellabs/docker-commands-and-best-practices-cheat-sheet/](https://zeroturnaround.com/rebellabs/docker-commands-and-best-practices-cheat-sheet/)  
**Slightly more than needed**, you can find more useful commands here: [github.com/wsargent/docker-cheat-sheet](https://github.com/wsargent/docker-cheat-sheet)

