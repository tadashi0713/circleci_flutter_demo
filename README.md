# circleci_flutter_demo

[![CircleCI](https://circleci.com/gh/tadashi0713/circleci_flutter_demo/tree/main.svg?style=svg&circle-token=4b7a45cbf68aec16634634e7504e653d7b77b235)](https://circleci.com/gh/tadashi0713/circleci_flutter_demo/tree/main)

Demo for CI/CD pipeline for Flutter app using CircleCI.

* All config as code
    * [CircleCI config file](.circleci/config.yml)
* Unit Test using `cirrusci/flutter` docker image
    * Convert & upload junit test report
* iOS integration(UI) test using iOS simulator on CircleCI macos machine
    * https://circleci.com/docs/2.0/testing-ios/
* Android integration(UI) test using Android emulator on CircleCI Android machine
    * https://circleci.com/docs/2.0/android-machine-image/
* Generate HTML report with screenshots of integration(UI) test
    * https://pub.dev/packages/ozzie
    * [Link of HTML report from CircleCI Artifacts](https://388-380987153-gh.circle-artifacts.com/0/ozzie/index.html)

![](./ozzie.png)

* Build & distribute app to Firebase App Distribution using Fastlane(Only android)
    * [Fastfile](android/fastlane/Fastfile)