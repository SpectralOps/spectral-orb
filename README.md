<p>
    <br/>
    <br/>
    <a href="http://spectralops.io"> 
        <img alt="SpectralOps logo" src="./logo.svg" width="300"/>
    </a>
    <h1>Spectral Orb</h1> 
</p>

[![CircleCI](https://circleci.com/gh/SpectralOps/spectral-orb/tree/main.svg?style=svg)](https://circleci.com/gh/SpectralOps/spectral-orb/tree/main)
[![CircleCI Orb Version](https://img.shields.io/badge/version-2.0.0-brightgreen)](https://circleci.com/orbs/registry/orb/spectralops/spectral)
[![GitHub License](https://img.shields.io/badge/license-MIT-brightgreen)](https://raw.githubusercontent.com/SpectralOps/spectral/master/LICENSE)

The Spectral CircleCI Orb can be used with any linux based docker image that includes the command line tools curl.

To connect your Spectral account on [spectralops.io](https://spectralops.io) you need to set up `SPECTRAL_DSN` and `SPECTRAL_ENV` (e.g https://get.spectralops.io) as environment variables.  
- We recommend to set up a CircleCI context in your organization named `credentials` that contains a variable with key `SPECTRAL_DSN` and the `dsn` as the value, and `SPECTRAL_ENV` as well.

## Installation

```yaml
  version: 2.1
  orbs:
    spectral: spectralops/spectral@2.0.0
  jobs:
    build:
      docker:
        - image: cimg/base:stable
      steps:
        - checkout
        - spectral/scan
  workflows:
    test-env-vars:
      jobs:
        - build:
            context: credentials
```

## Resources

[CircleCI Orb Registry Page](https://circleci.com/orbs/registry/orb/spectralops/spectral) - The official registry page of this orb for all versions, executors, commands, and jobs described.
[CircleCI Orb Docs](https://circleci.com/docs/2.0/orb-intro/#section=configuration) - Docs for using and creating CircleCI Orbs.

### How to Contribute

We welcome [issues](https://github.com/SpectralOps/spectral-orb/issues) to and [pull requests](https://github.com/SpectralOps/spectral-orb/pulls) against this repository!

## License

This project is licensed under the MIT License. See [LICENSE](LICENSE) for further details.



