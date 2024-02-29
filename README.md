# hetzner-cloud-js

[![StandardJS](https://img.shields.io/badge/code--style-standard-yellowgreen.svg?style=flat)](https://standardjs.com)
[![License](https://img.shields.io/badge/license-MIT-blue.svg?style=flat)](LICENSE.md)
[![Documentation Status](https://readthedocs.org/projects/hetzner-cloud-js/badge/?version=latest)](http://hetzner-cloud-js.readthedocs.io/en/latest/?badge=latest)
[![Travis](https://img.shields.io/travis/dennisbruner/hetzner-cloud-js.svg?style=flat)](https://travis-ci.org/dennisbruner/hetzner-cloud-js)
[![Known Vulnerabilities](https://snyk.io/test/github/dennisbruner/hetzner-cloud-js/badge.svg?targetFile=package.json)](https://snyk.io/test/github/dennisbruner/hetzner-cloud-js?targetFile=package.json)

A Node.js module for the Hetzner Cloud API

## Example

### Create a client instance

```javascript
const HetznerCloud = require('hetzner-cloud-js')
let client = new HetznerCloud.Client('API_TOKEN')
```

### Build and create a server

```javascript
const { server } = await client.servers.build('my-awesome-server')
  .serverType('cx11')
  .location('nbg1')
  .image('debian-9')
  .sshKey('work')
  .create()
```

## Documentation

 - [hetzner-cloud-js documentation page](https://hetzner-cloud-js.readthedocs.org/)
 - [Official Hetzner Cloud API documentation](https://docs.hetzner.cloud/)

## Development

### Quick setup

* Clone this repo with `git clone https://github.com/boxexchanger/hetzner-cloud-js.git`
* `cd hetzner-cloud-js`
* Run `npm install` to install dependencies
* Copy `.env.dist` to `.env` file and setup your access token. [You can use this guide by Hetzner.](https://docs.hetzner.cloud/#getting-started)


## License

[MIT](LICENSE.md)
