- What is the meaning of the JSON attribute 'timestamp'?
the current date and time (when the script is executed) in UTC.
example, 
```
"timestamp": 1585645013.13614
```

- What is the meaning of the JSON attribute 'updated_on'?
extracted Github item - 'updated_at' (UTC), converted to UNIX timestamp format
example, 
```
"updated_on": 1451929343.0
```

- What is the meaning of the JSON attribute 'origin'?
base_url + owner + repository
example, 
```
"origin": "https://github.com/grimoirelab/perceval"
```

- What is the meaning of the JSON attribute 'category'?
the category from a GitHub item - backend generates two categories of item which are 'issue' and 'pull_request'
example, 
```
"category": "issue"
```

- How many categories do the GitHub and GitLab backends have?
GitHub : 'issue', 'pull_request', 'repository'
Gitlab : 'issue', 'merge_request'

- What is the meaning of the JSON attribute 'uuid'?
generated uuid (universal unique identifier) based on given parameters
example, 
```
"uuid": "c403532b196ed4020cc86d001feb091c009d3d26"
```

- What is the meaning of the JSON attribute search_fields?
adds the values of the fields defined in `SEARCH_FIELDS` class attribute with their corresponding keys
example,
```
"search_fields": {
    "item_id": "124679251",
    "owner": "grimoirelab",
    "repo": "perceval"
}   
```

- What is stored in the attribute data of each JSON document produced by Perceval?
data attribute stores the extracted values of parameters, which are later fed into indexes
example, 
```
"data": {
    "assignee": null,
    "assignee_data": {},
    "assignees": [],
    "assignees_data": [],
    "author_association": "CONTRIBUTOR",
    "body": "Based on Sphynx, prepared for ReadTheDocs.\n\nRight now, this produces (from jgbarah/perceval repository) [this documentation in ReadTheDocs](http://perceval.readthedocs.org). Once this PR is accepted, I plan to switch ReadTheDocs to point to this repostory (master branch), so that the documentation gets rebuilt every time changes are made to the source code.\n\nThe configuration (docs/conf.py) include lines for running sphinx-apidoc, which generates automatically the docs/perceval.rst file, which is the entry point for the automatically generated documentation, produced based on the docstring comments in the source code.\n\nThe file index.rst is still a bare bones schema. It should be completed in a later patch, with more detailed information about Perceval itself.\n",
    "closed_at": "2016-01-04T13:51:56Z",
    "comments": 0,
    "comments_data": [],
    "comments_url": "https://api.github.com/repos/chaoss/grimoirelab-perceval/issues/3/comments",
    "created_at": "2016-01-03T23:46:04Z",
    "events_url": "https://api.github.com/repos/chaoss/grimoirelab-perceval/issues/3/events",
    "html_url": "https://github.com/chaoss/grimoirelab-perceval/pull/3",
    "id": 124679251,
    "labels": [],
    "labels_url": "https://api.github.com/repos/chaoss/grimoirelab-perceval/issues/3/labels{/name}",
    "locked": false,
    "milestone": null,
    "node_id": "MDExOlB1bGxSZXF1ZXN0NTQ5MzUxODA=",
    "number": 3,
    "pull_request": {
        "diff_url": "https://github.com/chaoss/grimoirelab-perceval/pull/3.diff",
        "html_url": "https://github.com/chaoss/grimoirelab-perceval/pull/3",
        "patch_url": "https://github.com/chaoss/grimoirelab-perceval/pull/3.patch",
        "url": "https://api.github.com/repos/chaoss/grimoirelab-perceval/pulls/3"
    },
    "reactions": {
        "+1": 0,
        "-1": 0,
        "confused": 0,
        "eyes": 0,
        "heart": 0,
        "hooray": 0,
        "laugh": 0,
        "rocket": 0,
        "total_count": 0,
        "url": "https://api.github.com/repos/chaoss/grimoirelab-perceval/issues/3/reactions"
    },
    "reactions_data": [],
    "repository_url": "https://api.github.com/repos/chaoss/grimoirelab-perceval",
    "state": "closed",
    "title": "Config files for a documentation, using Sphinx.",
    "updated_at": "2016-01-04T17:42:23Z",
    "url": "https://api.github.com/repos/chaoss/grimoirelab-perceval/issues/3",
    "user": {
        "avatar_url": "https://avatars3.githubusercontent.com/u/1039693?v=4",
        "events_url": "https://api.github.com/users/jgbarah/events{/privacy}",
        "followers_url": "https://api.github.com/users/jgbarah/followers",
        "following_url": "https://api.github.com/users/jgbarah/following{/other_user}",
        "gists_url": "https://api.github.com/users/jgbarah/gists{/gist_id}",
        "gravatar_id": "",
        "html_url": "https://github.com/jgbarah",
        "id": 1039693,
        "login": "jgbarah",
        "node_id": "MDQ6VXNlcjEwMzk2OTM=",
        "organizations_url": "https://api.github.com/users/jgbarah/orgs",
        "received_events_url": "https://api.github.com/users/jgbarah/received_events",
        "repos_url": "https://api.github.com/users/jgbarah/repos",
        "site_admin": false,
        "starred_url": "https://api.github.com/users/jgbarah/starred{/owner}{/repo}",
        "subscriptions_url": "https://api.github.com/users/jgbarah/subscriptions",
        "type": "User",
        "url": "https://api.github.com/users/jgbarah"
    },
    "user_data": {
        "avatar_url": "https://avatars3.githubusercontent.com/u/1039693?v=4",
        "bio": null,
        "blog": "http://gsyc.es/~jgb",
        "company": null,
        "created_at": "2011-09-09T21:47:40Z",
        "email": null,
        "events_url": "https://api.github.com/users/jgbarah/events{/privacy}",
        "followers": 91,
        "followers_url": "https://api.github.com/users/jgbarah/followers",
        "following": 0,
        "following_url": "https://api.github.com/users/jgbarah/following{/other_user}",
        "gists_url": "https://api.github.com/users/jgbarah/gists{/gist_id}",
        "gravatar_id": "",
        "hireable": null,
        "html_url": "https://github.com/jgbarah",
        "id": 1039693,
        "location": null,
        "login": "jgbarah",
        "name": "Jesus M. Gonzalez-Barahona",
        "node_id": "MDQ6VXNlcjEwMzk2OTM=",
        "organizations": [
            {
                "avatar_url": "https://avatars3.githubusercontent.com/u/1843608?v=4",
                "description": null,
                "events_url": "https://api.github.com/orgs/MetricsGrimoire/events",
                "hooks_url": "https://api.github.com/orgs/MetricsGrimoire/hooks",
                "id": 1843608,
                "issues_url": "https://api.github.com/orgs/MetricsGrimoire/issues",
                "login": "MetricsGrimoire",
                "members_url": "https://api.github.com/orgs/MetricsGrimoire/members{/member}",
                "node_id": "MDEyOk9yZ2FuaXphdGlvbjE4NDM2MDg=",
                "public_members_url": "https://api.github.com/orgs/MetricsGrimoire/public_members{/member}",
                "repos_url": "https://api.github.com/orgs/MetricsGrimoire/repos",
                "url": "https://api.github.com/orgs/MetricsGrimoire"
            },
            {
                "avatar_url": "https://avatars3.githubusercontent.com/u/1918070?v=4",
                "description": null,
                "events_url": "https://api.github.com/orgs/Bitergia/events",
                "hooks_url": "https://api.github.com/orgs/Bitergia/hooks",
                "id": 1918070,
                "issues_url": "https://api.github.com/orgs/Bitergia/issues",
                "login": "Bitergia",
                "members_url": "https://api.github.com/orgs/Bitergia/members{/member}",
                "node_id": "MDEyOk9yZ2FuaXphdGlvbjE5MTgwNzA=",
                "public_members_url": "https://api.github.com/orgs/Bitergia/public_members{/member}",
                "repos_url": "https://api.github.com/orgs/Bitergia/repos",
                "url": "https://api.github.com/orgs/Bitergia"
            },
            {
                "avatar_url": "https://avatars2.githubusercontent.com/u/2191340?v=4",
                "description": null,
                "events_url": "https://api.github.com/orgs/VizGrimoire/events",
                "hooks_url": "https://api.github.com/orgs/VizGrimoire/hooks",
                "id": 2191340,
                "issues_url": "https://api.github.com/orgs/VizGrimoire/issues",
                "login": "VizGrimoire",
                "members_url": "https://api.github.com/orgs/VizGrimoire/members{/member}",
                "node_id": "MDEyOk9yZ2FuaXphdGlvbjIxOTEzNDA=",
                "public_members_url": "https://api.github.com/orgs/VizGrimoire/public_members{/member}",
                "repos_url": "https://api.github.com/orgs/VizGrimoire/repos",
                "url": "https://api.github.com/orgs/VizGrimoire"
            },
            {
                "avatar_url": "https://avatars2.githubusercontent.com/u/3017044?v=4",
                "description": null,
                "events_url": "https://api.github.com/orgs/AlertProject/events",
                "hooks_url": "https://api.github.com/orgs/AlertProject/hooks",
                "id": 3017044,
                "issues_url": "https://api.github.com/orgs/AlertProject/issues",
                "login": "AlertProject",
                "members_url": "https://api.github.com/orgs/AlertProject/members{/member}",
                "node_id": "MDEyOk9yZ2FuaXphdGlvbjMwMTcwNDQ=",
                "public_members_url": "https://api.github.com/orgs/AlertProject/public_members{/member}",
                "repos_url": "https://api.github.com/orgs/AlertProject/repos",
                "url": "https://api.github.com/orgs/AlertProject"
            },
            {
                "avatar_url": "https://avatars0.githubusercontent.com/u/16151805?v=4",
                "description": "",
                "events_url": "https://api.github.com/orgs/grimoirelab/events",
                "hooks_url": "https://api.github.com/orgs/grimoirelab/hooks",
                "id": 16151805,
                "issues_url": "https://api.github.com/orgs/grimoirelab/issues",
                "login": "grimoirelab",
                "members_url": "https://api.github.com/orgs/grimoirelab/members{/member}",
                "node_id": "MDEyOk9yZ2FuaXphdGlvbjE2MTUxODA1",
                "public_members_url": "https://api.github.com/orgs/grimoirelab/public_members{/member}",
                "repos_url": "https://api.github.com/orgs/grimoirelab/repos",
                "url": "https://api.github.com/orgs/grimoirelab"
            }
        ],
        "organizations_url": "https://api.github.com/users/jgbarah/orgs",
        "public_gists": 0,
        "public_repos": 38,
        "received_events_url": "https://api.github.com/users/jgbarah/received_events",
        "repos_url": "https://api.github.com/users/jgbarah/repos",
        "site_admin": false,
        "starred_url": "https://api.github.com/users/jgbarah/starred{/owner}{/repo}",
        "subscriptions_url": "https://api.github.com/users/jgbarah/subscriptions",
        "type": "User",
        "updated_at": "2020-03-26T22:56:01Z",
        "url": "https://api.github.com/users/jgbarah"
    }
}
```
