swagger: "2.0"
x-collection-name: Reddit
x-complete: 1
info:
  title: Reddit
  version: 1.0.0
host: www.reddit.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  '{/r/subreddit}/wiki/discussions/page':
    get&nbsp;:
      summary: Get Subreddit Wiki Discussions Page
      description: Retrieve a list of discussions about this wiki page
      operationId: get&nbsp;RSubredditWikiDiscussionsPage
      x-api-path-slug: rsubredditwikidiscussionspage-getnbsp
      parameters:
      - in: query
        name: after
        description: fullname of a thing
        type: string
      - in: query
        name: before
        description: fullname of a thing
        type: string
      - in: query
        name: count
        description: 'a positive integer (default: 0)'
        type: string
      - in: query
        name: limit
        description: 'the maximum number of items desired (default: 25, maximum: 100)'
        type: string
      - in: query
        name: page
        description: the name of an existing wiki page
        type: string
      - in: query
        name: show
        description: (optional) the string all
        type: string
      - in: query
        name: sr_detail
        description: (optional) expand subreddits
        type: string
      responses:
        200:
          description: OK
      tags:
      - Subreddit
      - Wiki
      - Discussions
      - Page
  '{/r/subreddit}/wiki/revisions/page':
    get&nbsp;:
      summary: Get Subreddit Wiki Revisions Page
      description: Retrieve a list of revisions of this wiki page
      operationId: get&nbsp;RSubredditWikiRevisionsPage
      x-api-path-slug: rsubredditwikirevisionspage-getnbsp
      parameters:
      - in: query
        name: after
        description: fullname of a thing
        type: string
      - in: query
        name: before
        description: fullname of a thing
        type: string
      - in: query
        name: count
        description: 'a positive integer (default: 0)'
        type: string
      - in: query
        name: limit
        description: 'the maximum number of items desired (default: 25, maximum: 100)'
        type: string
      - in: query
        name: page
        description: the name of an existing wiki page
        type: string
      - in: query
        name: show
        description: (optional) the string all
        type: string
      - in: query
        name: sr_detail
        description: (optional) expand subreddits
        type: string
      responses:
        200:
          description: OK
      tags:
      - Subreddit
      - Wiki
      - Revisions
      - Page
  '{/r/subreddit}/wiki/settings/page':
    get&nbsp;:
      summary: Get Subreddit Wiki Settings Page
      description: Retrieve the current permission settings for page
      operationId: get&nbsp;RSubredditWikiSettingsPage
      x-api-path-slug: rsubredditwikisettingspage-getnbsp
      parameters:
      - in: query
        name: page
        description: the name of an existing wiki page
        type: string
      responses:
        200:
          description: OK
      tags:
      - Subreddit
      - Wiki
      - Settings
      - Page
    post&nbsp;:
      summary: Add Subreddit Wiki Settings Page
      description: Update the permissions and visibility of wiki page
      operationId: post&nbsp;RSubredditWikiSettingsPage
      x-api-path-slug: rsubredditwikisettingspage-postnbsp
      parameters:
      - in: query
        name: /r/subreddit
        description: subreddit
        type: string
        format: string
      - in: query
        name: listed
        description: boolean value
        type: string
      - in: query
        name: page
        description: the name of an existing wiki page
        type: string
      - in: query
        name: permlevel
        description: an integer
        type: string
      - in: query
        name: uh / X-Modhash header
        description: a modhash
        type: string
      responses:
        200:
          description: OK
      tags:
      - Subreddit
      - Wiki
      - Settings
      - Page
  '{/r/subreddit}/wiki/page':
    get&nbsp;:
      summary: Get Subreddit Wiki Page
      description: Return the content of a wiki page
      operationId: get&nbsp;RSubredditWikiPage
      x-api-path-slug: rsubredditwikipage-getnbsp
      parameters:
      - in: query
        name: page
        description: the name of an existing wiki page
        type: string
      - in: query
        name: v
        description: a wiki revision ID
        type: string
      - in: query
        name: v2
        description: a wiki revision ID
        type: string
      responses:
        200:
          description: OK
      tags:
      - Subreddit
      - Wiki
      - Page