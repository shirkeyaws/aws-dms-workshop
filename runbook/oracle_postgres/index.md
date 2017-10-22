---
title: "AWS Database Migration Services"
subtitle: "Workshop: Oracle to PostgreSQL Migration"
author: [Amazon Web Services]
institute: "Amazon Web Services"
abstract: "This document is © 2017, Amazon Web Services, Inc. or its Affiliates. All rights reserved.

Oracle is a registered trademark of Oracle Corporation and/or its affiliates.

PostgreSQL is a registered trademark of the PostgreSQL Community Association of Canada."
numbersections: yes
numberoffset: 1
papersize: A4
mainfont: Amazon Ember
documentclass: article
geometry: margin=2cm
date: "Revised: 2017.10.22"
toc: true
lot: true
lof: true
subject: ""
tags: [AWS Database Migration Services, AWS DMS, Oracle, PostgreSQL]
titlepage: true
titlepage-color: 146eb4
titlepage-text-color: ffffff
titlepage-rule-color: ffffff
titlepage-rule-height: 1
colorlinks: true
toccolor: cyan
citecolor: cyan
urlcolor: cyan
linkcolor: cyan
bookmarks: true
pdfpagemode: FullScreen
header-includes:
    - \usepackage{graphicx}
    - \graphicspath{{../shared/}{images/}}
...

```include
intro.md
intro_objective.md
intro_dms.md
intro_sct.md
setup.md
setup_key_pair.md
setup_aws_cfn_stack.md
setup_access_appstream.md
setup_jdbc_driver.md
setup_install_sct.md
setup_install_db_mgmt.md
steps.md
teardown.md
teardown_aws_cfn_stack.md
```