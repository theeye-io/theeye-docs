# Script Task

##  Runtime Information

During runtime, you can access basic information of the job being executed via environment variables.

The information is storead as JSON Strings or as JSON encoded Key-Value structures.
All the environment variables belonging to TheEye runtime are prefixed with *THEEYE_* keyword

### THEEYE_JOB

Contains information of the current job.

| Name | Type | Description |
| ---  | --- | --- |
| id | string | the id of the job. you can fetch the API with it |
| task_id | string | task definition id. can fetch the API with it |

### THEEYE_JOB_USER

This is the uses that executes the Task. This env can take diferent form depending on how the task was executed.

* Automatic Execution: the user will be always an internal user.      
* Play Button: When the task is executed via User Interface, this will be the user that pushed the Play Button.
* API Calls: Api calls can be done using Integration Keys (bot user) or Access Tokens (human user).

| Name | Type | Description |
| ---  | --- | --- |
| id | string | the user id |
| email | string | the user email |

### THEEYE_JOB_WORKFLOW

When Tasks belongs to Workflows, this constains information of the Workflow.

| Name | Type | Description |
| ---  | --- | --- |
| id | string | the workflow schema id |
| job_id | string | the workflow job execution instance |

### THEEYE_API_URL (string)

This is the API URL.

### THEEYE_ORGANIZATION_NAME (string)

This is the organization name or project running the current script.

## Examples

###  Get THEEYE_JOB_USER information from DOS / BAT scripts

The following script shows how to get user id and email information, it can be replicated to get information for THEEYE_JOB and THEEYE_JOB_WORKFLOW:
[Download Recipe](https://github.com/theeye-io/theeye-docs/blob/master/docs/assets/recipes/check_theeye_env_vars.json)


