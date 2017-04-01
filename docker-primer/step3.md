
## Dockerfiles

### Anatomy of a Dockerfile

```
FROM nodesource/node:4.4

ADD package.json package.json  
RUN npm install  
ADD . .

EXPOSE  8081
CMD ["npm","start"]  #CMD ["node","app.js"]  
```

So, line by line, what does this file do ?

`FROM nodesource/node:4.4` - specifies that the base image should be from the `nodesource` provider, `node` image, version/tag `4.4`
`ADD package.json package.json` - adds the file from source (left) with the same name in the destination (right)
`RUN npm install` - runs the command after the keyword `RUN` (setup)
`ADD . .` - adds all files from current directory (source - left) to the destination (right)
`EXPOSE  8081` - exposes port 8081 outside the container
`CMD ["npm","start"]  #CMD ["node","app.js"]` - runs the service you need

<!-- ### Docker Compose -->


