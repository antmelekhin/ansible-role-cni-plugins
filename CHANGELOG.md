# Changelog

## [1.2.3](https://github.com/antmelekhin/ansible-role-cni-plugins/compare/v1.2.2...v1.2.3) (2024-11-30)


### Documentation

* **README:** updated requirements ([d566762](https://github.com/antmelekhin/ansible-role-cni-plugins/commit/d5667629f5f4201bc2fd819874c203c33e2b18f2))

## [1.2.2](https://github.com/antmelekhin/ansible-role-cni-plugins/compare/v1.2.1...v1.2.2) (2024-10-22)


### Fixes

* **version:** CNI plugins updated to `1.6.0` release ([#3](https://github.com/antmelekhin/ansible-role-cni-plugins/issues/3)) ([c106aeb](https://github.com/antmelekhin/ansible-role-cni-plugins/commit/c106aeb345ad92bbb5919974958294cd25d1f3dd))

## [1.2.1](https://github.com/antmelekhin/ansible-role-cni-plugins/compare/v1.2.0...v1.2.1) (2024-10-09)


### Continuous Integration

* use `ubuntu-22.04` instead of `ubuntu-latest` ([b6d5d28](https://github.com/antmelekhin/ansible-role-cni-plugins/commit/b6d5d28090930694b1380e98e910cfd827a9226d))


### Fixes

* add `become: false` to localhost delegated tasks ([e5ea19f](https://github.com/antmelekhin/ansible-role-cni-plugins/commit/e5ea19fac9b0fd7ca1b02127b2a240f257b87bfa))


### Styles

* minor fixes ([c4cd19c](https://github.com/antmelekhin/ansible-role-cni-plugins/commit/c4cd19c65444ea7f35cac53b6af423e0fe4b7b90))

## [1.2.0](https://github.com/antmelekhin/ansible-role-cni-plugins/compare/v1.1.0...v1.2.0) (2024-08-19)


### Features

* add `meta/argument_specs.yml` file ([#2](https://github.com/antmelekhin/ansible-role-cni-plugins/issues/2)) ([145fad2](https://github.com/antmelekhin/ansible-role-cni-plugins/commit/145fad2e31320a6c4b30c4eeae17683a88d9470a))

## [1.1.0](https://github.com/antmelekhin/ansible-role-cni-plugins/compare/v1.0.2...v1.1.0) (2024-08-19)


### Improvements

* minor fixes ([#1](https://github.com/antmelekhin/ansible-role-cni-plugins/issues/1)) ([158a328](https://github.com/antmelekhin/ansible-role-cni-plugins/commit/158a32863a795d662056a3a6db1dedce60e34e76))

## [1.0.2](https://github.com/antmelekhin/ansible-role-cni-plugins/compare/v1.0.1...v1.0.2) (2024-07-16)


### Fixes

* add `check_mode` ([a585aae](https://github.com/antmelekhin/ansible-role-cni-plugins/commit/a585aae2af4bbbf2c4cbba96173dba1ca5741618))
* add `cni_plugins_checksum_url` variable ([86a4f01](https://github.com/antmelekhin/ansible-role-cni-plugins/commit/86a4f012e49dcf59e06f65e58eb67b648a23a084))


### Tests

* add molecule verify ([c77d3a0](https://github.com/antmelekhin/ansible-role-cni-plugins/commit/c77d3a0fca734af1e0aa7fd2b0157fae496878e6))

## [1.0.1](https://github.com/antmelekhin/ansible-role-cni-plugins/compare/v1.0.0...v1.0.1) (2024-07-15)


### Continuous Integration

* add `update-version` workflow ([eaede61](https://github.com/antmelekhin/ansible-role-cni-plugins/commit/eaede612d81430971a9fac4de657cfb5bc06a66e))


### Fixes

* update `cni_plugins_download_url` variable ([4216faf](https://github.com/antmelekhin/ansible-role-cni-plugins/commit/4216faf971468790f8012af00c4e945f296e3491))

## [1.0.0](https://github.com/antmelekhin/ansible-role-cni-plugins/compare/...v1.0.0) (2024-07-15)


### Features

* initial commit ([4e1cf9f](https://github.com/antmelekhin/ansible-role-cni-plugins/commit/4e1cf9ffacebc84c646ac56aa1695f3af7fd54a1))
