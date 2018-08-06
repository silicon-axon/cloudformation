# cloudformation

This is a collection of CloudFormation templates, wrapped around Python Jinja2 templating.

## Introduction

CloudFormation yaml lacks control statements such as for-loops and conditional.
This makes organizing your AWS resources a bit tad repetitive.
Rather than using a 3rd party product like Terraform, which at the point of this writing does not support rollback, we thought we should just wrap CloudFormation files with Jinja templates.

This is not a replacement of CloudFormation. You still have to take the output yaml to CloudFormation whether through the AWS console or CLI.

## How to Use

Install jinja2-cli

    pip install jinja2-cli
    pip install jinja2-cli[yaml]

Fill in your own variables. Example variables can be found in `example.yaml`, then pass it to `jinja2`

    jinja2 stacks/vpc.yaml example.yaml

The `stacks/` folder contains CloudFormation stack templates.
They serve as examples of how to provision various AWS resources.
Your usage and needs may vary, but we hope they can help you in organizing your resources better.
