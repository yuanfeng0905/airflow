<!--
 Licensed to the Apache Software Foundation (ASF) under one
 or more contributor license agreements.  See the NOTICE file
 distributed with this work for additional information
 regarding copyright ownership.  The ASF licenses this file
 to you under the Apache License, Version 2.0 (the
 "License"); you may not use this file except in compliance
 with the License.  You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

 Unless required by applicable law or agreed to in writing,
 software distributed under the License is distributed on an
 "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY
 KIND, either express or implied.  See the License for the
 specific language governing permissions and limitations
 under the License.
 -->


# Package apache-airflow-backport-providers-slack

Release: 2020.5.20

**Table of contents**

- [Backport package](#backport-package)
- [Installation](#installation)
- [Compatibility](#compatibility)
- [PIP requirements](#pip-requirements)
- [Cross provider package dependencies](#cross-provider-package-dependencies)
- [Provider class summary](#provider-class-summary)
    - [Operators](#operators)
        - [New operators](#new-operators)
        - [Moved operators](#moved-operators)
    - [Hooks](#hooks)
        - [Moved hooks](#moved-hooks)
- [Releases](#releases)
    - [Release 2020.5.20](#release-2020520)

## Backport package

This is a backport providers package for `slack` provider. All classes for this provider package
are in `airflow.providers.slack` python package.

**Only Python 3.6+ is supported for this backport package.**

While Airflow 1.10.* continues to support Python 2.7+ - you need to upgrade python to 3.6+ if you
want to use this backport package.



## Installation

You can install this package on top of an existing airflow 1.10.* installation via
`pip install apache-airflow-backport-providers-slack`

## Compatibility

For full compatibility and test status of the backport packages check
[Airflow Backport Package Compatibility](https://cwiki.apache.org/confluence/display/AIRFLOW/Backported+providers+packages+for+Airflow+1.10.*+series)

## PIP requirements

| PIP package   | Version required   |
|:--------------|:-------------------|
| slackclient   | &gt;=2.0.0,&lt;3.0.0     |

## Cross provider package dependencies

Those are dependencies that might be needed in order to use all the features of the package.
You need to install the specified backport providers package in order to use them.

You can install such cross-provider dependencies when installing from PyPI. For example:

```bash
pip install apache-airflow-backport-providers-slack[http]
```

| Dependent package                                                                                              | Extra   |
|:---------------------------------------------------------------------------------------------------------------|:--------|
| [apache-airflow-backport-providers-http](https://github.com/apache/airflow/tree/master/airflow/providers/http) | http    |

# Provider class summary

All classes in Airflow 2.0 are in `airflow.providers.slack` package.


## Operators


### New operators

| New Airflow 2.0 operators: `airflow.providers.slack` package                                                                     |
|:---------------------------------------------------------------------------------------------------------------------------------|
| [operators.slack.SlackAPIFileOperator](https://github.com/apache/airflow/blob/master/airflow/providers/slack/operators/slack.py) |



### Moved operators

| Airflow 2.0 operators: `airflow.providers.slack` package                                                                                         | Airflow 1.10.* previous location (usually `airflow.contrib`)                                                                                                             |
|:-------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [operators.slack.SlackAPIOperator](https://github.com/apache/airflow/blob/master/airflow/providers/slack/operators/slack.py)                     | [operators.slack_operator.SlackAPIOperator](https://github.com/apache/airflow/blob/v1-10-stable/airflow/operators/slack_operator.py)                                     |
| [operators.slack.SlackAPIPostOperator](https://github.com/apache/airflow/blob/master/airflow/providers/slack/operators/slack.py)                 | [operators.slack_operator.SlackAPIPostOperator](https://github.com/apache/airflow/blob/v1-10-stable/airflow/operators/slack_operator.py)                                 |
| [operators.slack_webhook.SlackWebhookOperator](https://github.com/apache/airflow/blob/master/airflow/providers/slack/operators/slack_webhook.py) | [contrib.operators.slack_webhook_operator.SlackWebhookOperator](https://github.com/apache/airflow/blob/v1-10-stable/airflow/contrib/operators/slack_webhook_operator.py) |







## Hooks



### Moved hooks

| Airflow 2.0 hooks: `airflow.providers.slack` package                                                                                 | Airflow 1.10.* previous location (usually `airflow.contrib`)                                                                                         |
|:-------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [hooks.slack.SlackHook](https://github.com/apache/airflow/blob/master/airflow/providers/slack/hooks/slack.py)                        | [hooks.slack_hook.SlackHook](https://github.com/apache/airflow/blob/v1-10-stable/airflow/hooks/slack_hook.py)                                        |
| [hooks.slack_webhook.SlackWebhookHook](https://github.com/apache/airflow/blob/master/airflow/providers/slack/hooks/slack_webhook.py) | [contrib.hooks.slack_webhook_hook.SlackWebhookHook](https://github.com/apache/airflow/blob/v1-10-stable/airflow/contrib/hooks/slack_webhook_hook.py) |






## Releases

### Release 2020.5.20

| Commit                                                                                         | Committed   | Subject                                                                       |
|:-----------------------------------------------------------------------------------------------|:------------|:------------------------------------------------------------------------------|
| [5cf46fad1](https://github.com/apache/airflow/commit/5cf46fad1e0a9cdde213258b2064e16d30d3160e) | 2020-05-29  | Add SlackAPIFileOperator impementing files.upload from Slack API (#9004)      |
| [0b0e4f7a4](https://github.com/apache/airflow/commit/0b0e4f7a4cceff3efe15161fb40b984782760a34) | 2020-05-26  | Preparing for RC3 relase of backports (#9026)                                 |
| [00642a46d](https://github.com/apache/airflow/commit/00642a46d019870c4decb3d0e47c01d6a25cb88c) | 2020-05-26  | Fixed name of 20 remaining wrongly named operators. (#8994)                   |
| [427257c2e](https://github.com/apache/airflow/commit/427257c2e2ffc886ef9f516e9c4d015a4ede9bbd) | 2020-05-24  | Remove defunct code from setup.py (#8982)                                     |
| [375d1ca22](https://github.com/apache/airflow/commit/375d1ca229464617780623c61c6e8a1bf570c87f) | 2020-05-19  | Release candidate 2 for backport packages 2020.05.20 (#8898)                  |
| [12c5e5d8a](https://github.com/apache/airflow/commit/12c5e5d8ae25fa633efe63ccf4db389e2b796d79) | 2020-05-17  | Prepare release candidate for backport packages (#8891)                       |
| [f3521fb0e](https://github.com/apache/airflow/commit/f3521fb0e36733d8bd356123e56a453fd37a6dca) | 2020-05-16  | Regenerate readme files for backport package release (#8886)                  |
| [92585ca4c](https://github.com/apache/airflow/commit/92585ca4cb375ac879f4ab331b3a063106eb7b92) | 2020-05-15  | Added automated release notes generation for backport operators (#8807)       |
| [578fc514c](https://github.com/apache/airflow/commit/578fc514cd325b7d190bdcfb749a384d101238fa) | 2020-05-12  | [AIRFLOW-4543] Update slack operator to support slackclient v2 (#5519)        |
| [4bde99f13](https://github.com/apache/airflow/commit/4bde99f1323d72f6c84c1548079d5e98fc0a2a9a) | 2020-03-23  | Make airflow/providers pylint compatible (#7802)                              |
| [be2b2baa7](https://github.com/apache/airflow/commit/be2b2baa7c5f53c2d73646e4623cdb6731551b70) | 2020-03-23  | Add missing call to Super class in &#39;http&#39;, &#39;grpc&#39; &amp; &#39;slack&#39; providers (#7826) |
| [97a429f9d](https://github.com/apache/airflow/commit/97a429f9d0cf740c5698060ad55f11e93cb57b55) | 2020-02-02  | [AIRFLOW-6714] Remove magic comments about UTF-8 (#7338)                      |
| [9a04013b0](https://github.com/apache/airflow/commit/9a04013b0e40b0d744ff4ac9f008491806d60df2) | 2020-01-27  | [AIRFLOW-6646][AIP-21] Move protocols classes to providers package (#7268)    |
| [c42a375e7](https://github.com/apache/airflow/commit/c42a375e799e5adb3f9536616372dc90ff47e6c8) | 2020-01-27  | [AIRFLOW-6644][AIP-21] Move service classes to providers package (#7265)      |
