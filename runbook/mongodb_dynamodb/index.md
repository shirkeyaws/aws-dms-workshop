---
title: "AWS Database Migration Services Lab"
subtitle: "NoSQL Lab: MongoDB to DynamoDB Migration"
author: [Amazon Web Services]
institute: "Amazon Web Services"
abstract: "This document is © 2017, Amazon Web Services, Inc. or its Affiliates. All rights reserved."
numbersections: yes
numberoffset: 1
papersize: A4
mainfont: Amazon Ember
documentclass: article
geometry: margin=2cm
date: "Revised: 2017.10.25"
toc: true
lot: true
lof: true
subject: ""
tags: [AWS Database Migration Services, AWS DMS, DynamoDB, Amazon DynamoDB, MongoDB, NoSQL]
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
```

```include
setup.md
setup_key_pair.md
setup_aws_cfn_stack.md
setup_appstream.md
setup_jdbc_driver.md
setup_install_db_mgmt.md
```

```include
steps.md
step_aws_dms_repl_inst.md
step_aws_dms_endpoint.md
step_aws_dms_task.md
step_aws_dms_troubleshoot.md
step_aws_dms_error_trunc.md
step_aws_dms_error_supp_log.md
```

```include
teardown.md
teardown_aws_dms.md
teardown_aws_cfn_stack.md
teardown_key_pair.md
conclusion.md
```