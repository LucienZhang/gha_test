# gha_test
GitHub Action trigger test

|                                         Action                                         |                    Triggered                     |
| :------------------------------------------------------------------------------------: | :----------------------------------------------: |
|               check `This is a pre-release` and publish as a pre-release               |         published, created, prereleased          |
| check `This is a pre-release`, save as a draft and publish as a pre-release from draft | published(github.event.release.prerelease==true) |
|                               directly publish a release                               |           published, created, released           |
|                              publish a release from draft                              |               published, released                |

Conclusion: Always subscribe to `published`
