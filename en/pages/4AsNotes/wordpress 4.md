# wordpress meetup and wp 4 preview

- wordpress nyc meetup 
- every third tuesday
- wpnyc.org
	- job board
	- helpdesk open
- plugins
	- tablepress
	- nextgen gallery
	- pods
- aram zucker-scharff
	- pressforward
		- rss feeds
		- opml files
	- aggregated curated posts from a collection of blogs
	- readbility library (instapaper)
	- post will go to the original author
		- with permission full conntent
		- type a summary
	- edit flow plugin cfo.com
	- use of template tags
	- pressthis bookmarket
	- open source
	- rss is being replaced by json

# wordpress 4 preview

@helenhousandi

- oembed previews
	- youtube, tweets, media from the urls
	- insert from url , not just image, finds the embed code automatically
	- whitelist for embedded
	- then we cache the response into post "meta"
		- just text
	- outside of post in a widget ?
		-  where is it cached - *need to investgate this*
- plug in installs easier
	- 30k plugins
	- now will load featured plugins with info cards
	- create favorite collections
	- can read reviews in the interface
	- *cf note - get list of complex site managers and developers in pro editorial space*
- keep the edit tools with the text in the editor area
- media library improvements
	- bulk select, multi select
	- attachment details
		- details, properties
	-preview media that is not just images
	- full fledge media library
	- view modal
		- edit more details
			- taxonomies here
		- attachment post type
- "customizer" -*need to investigate this*
	- edit widget preview 
	- can navigate in the preview window
	- "panels"
- muliple "order by" statements now available
- media element. js
- jquery update
- **4.0 is just another incremental release**
	- backward compatibility still most important
- database
	- plugins for database drivers
	- still written for MySQL
- no new migration tools
- beta testing tab is for plugins
- compatability
	- php versions? usually the problem for plugins
	- we dont alert - pro need, not typical user
- security?
	- from 3.92
	- expiring nonces
	- coordinated with Drupal
-tinyMcE
	- we dont have a real html mode *check out - still need special plugin?*
- svg ?
	- xml so they are by definition insecure, not supported
- ***cf note - need to study multisite!!!***
- we have long term roadmap for taxonomies
- plugins
	- multisite
		- manage plugins, not install plugins
	- hosts have white list plugins etc
- biggest difference 3.9 and 4.0
	- **think version 39 and 40**
	- customizer came in 34 for instance
	- no particularly dramatic diffs for developers
- ***cf note - still oriented toward lone users?***

# experience of leading a release
- still a volunteer effort
- mostly reading commits, tickets, forums, devchats
- mostly communication, bugging, alert, reporting
- *cf note - getting involvment includes "visualizing"*
- *cf note - need to really schedule the team for preview/reviews of design, workflow, user action flow*
- decision making on features and prioritization most important
- trust *cf note-need trust quotient monitor for team*
- *cf note - need to ask stakeholders "what do you think your role is."*
