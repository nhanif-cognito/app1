podTemplate(label: 'mypod', containers: [
    containerTemplate(name: 'git', image: 'alpine/git', ttyEnabled: true, command: 'cat')
	],
  volumes: [
    hostPathVolume(mountPath: '/var/run/docker.sock', hostPath: '/var/run/docker.sock'),
  ]
  ) {
	node('mypod') {
			stage('update') {
					container('docker') {
							RUN apk add --update nodejs
              COPY package.json /src/package.json
              npm install
              COPY . /src
					}
			}
// Update
//  RUN apk add --update nodejs

//  Install app dependencies
// COPY package.json /src/package.json
// RUN cd /src; npm install

//  Bundle app source
// COPY . /src

    EXPOSE  8080
    CMD ["node", "/src/index.js"]
  }
}
