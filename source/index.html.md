---
title: PixelPeak API Reference

language_tabs: # must be one of https://git.io/vQNgJ
  - shell

toc_footers:
  - <a href='#'>Sign Up for a Developer Key</a>
  - <a href='https://github.com/slatedocs/slate'>Documentation Powered by Slate</a>

includes:
  - errors

search: true
---

# Introduction

Welcome to the PixelPeak API. The one stop page for all DevOps health checking, network monitoring, and more!

# Authentication

> To authorize, use this code:

```shell
# With API calls you pass the token inline to authorize your request.
curl "api_endpoint_here?token=<token>"
```

PixelPeak uses API keys to allow access to the API. You can register a new API key at our [developer portal](http://example.com/developers).

# Git API

## Add Commit

```shell
curl "http://pixelpeak-dev.aigdev.com/api/git/addcommit?token=<token>&author=<author>&branch=<branch>"
```

> The above command returns a message

```json
Adding Git Commit! Payload: {branch, author}
```

This endpoint adds a commit

### HTTP Request

`GET http://pixelpeak-dev.aigdev.com/api/git/addcommit`
### URL Parameters

Parameter | Required | Description
--------- | -------- | -----------
token  | Yes | Your API Token
author | Yes | Author who made the commit
branch | Yes | The branch the commit was made on

## Get Commits

```shell
curl "http://pixelpeak-dev.aigdev.com/api/git/getcommits?token=<token>"
```

> The above command returns a message in JSON

```json
{
  [  
    id: "1",
    author: "Steve",
    branch: "master"
  ]
}
```
This endpoint returns a JSON array of all commits.

### HTTP Request

`GET http://pixelpeak-dev.aigdev.com/api/git/getcommits`
### URL Parameters

Parameter | Required | Description
--------- | -------- | -----------
token  | Yes | Your API Token

## Set Current Branch

```shell
curl "http://pixelpeak-dev.aigdev.com/api/git/setcurrentbranch?token=<token>&branch=<branch>"
```

> The above command returns a message

```json
Setting Current Branch. Payload: {branch}
```

This endpoint sets the current branch of the deploy cycle

### HTTP Request

`GET http://pixelpeak-dev.aigdev.com/api/git/setcurrentbranch`
### URL Parameters

Parameter | Required | Description
--------- | -------- | -----------
token  | Yes | Your API Token
branch | Yes | The current branch in the deploy cycle

## Set Previous Branch

```shell
curl "http://pixelpeak-dev.aigdev.com/api/git/setpreviousbranch?token=<token>&branch=<branch>"
```

> The above command returns a message

```json
Setting Previous Branch. Payload: {branch}
```

This endpoint sets the previous branch of the deploy cycle

### HTTP Request

`GET http://pixelpeak-dev.aigdev.com/api/git/setpreviousbranch`
### URL Parameters

Parameter | Required | Description
--------- | -------- | -----------
token  | Yes | Your API Token
branch | Yes | The previous branch in the deploy cycle

# Deploy API

## Add Deploy

```shell
curl "http://pixelpeak-dev.aigdev.com/api/git/adddeploy?token=<token>&author=<author>&description=<description>"
```

> The above command returns a message

```json
Adding new deploy! Payload: {description, author}
```

This endpoint adds a deploy

### HTTP Request

`GET http://pixelpeak-dev.aigdev.com/api/git/adddeploy`
### URL Parameters

Parameter | Required | Description
--------- | -------- | -----------
token  | Yes | Your API Token
author | Yes | Author who made the deploy
description | Yes | descripton/details of the deploy

## Get Deploys

```shell
curl "http://pixelpeak-dev.aigdev.com/api/git/getdeploys?token=<token>"
```

> The above command returns a message in JSON

```json
{
  [  
    id: "1",
    author: "Steve",
    description: "Deploying new branch to production"
  ]
}
```
This endpoint returns a JSON array of all deploys.

### HTTP Request

`GET http://pixelpeak-dev.aigdev.com/api/git/getdeploys`
### URL Parameters

Parameter | Required | Description
--------- | -------- | -----------
token  | Yes | Your API Token

# Message API

# Endpoint API