[![Build status](https://ci.appveyor.com/api/projects/status/q31a2qtgi4bw3e9b/branch/develop?svg=true)](https://ci.appveyor.com/project/dotnetgeek/dng-syndication/branch/develop)
[![Build status](https://ci.appveyor.com/api/projects/status/80gqbde41fru5wlb/branch/master?svg=true)](https://ci.appveyor.com/project/dotnetgeek/dng-syndication/branch/master)
[![NuGet](https://img.shields.io/nuget/v/dng.Syndication.svg)](https://www.nuget.org/packages/dng.Syndication)
![MIT License](https://img.shields.io/badge/license-MIT-orange.svg)

# dng.Syndication

A feed generator which can be used to create valid RSS 2.0 ([spec](http://cyber.harvard.edu/rss/rss.html))  and Atom([spec](https://tools.ietf.org/html/rfc4287)) syndication  feeds. It is written in C# and available as NuGet-Package.

### Supports:
* .NET Standard 2.0
* .NET 4.5.x

# Objects and Fields description


## Feed

This is the main object which description the general information about the feed.

| Field  | RSS 2.0 | ATOM  | Description |
|--------|---------|-------|-------------|
| Title | title (*) | title | The name for the feed.|
| Author | author | author | The author element is used to specify the e-mail address of the author of an item. |
| Link | link (*) | id | Defines the hyperlink to the channel |
| FeedEntries | item | entry | Each <item> element defines an article or "story" in an RSS feed. |
| Language | language | - | Specifies the language the feed is written in |
| Copyright | copyright | rights | - |
| Published | pubDate | published | Defines the publication date for the feed |
| UpdatedDate | lastBuildDate | updated |  Defines the last-modified date of the content of the feed. |
| Generator | generator | generator | The program used to generate the feed |
| Description | description (*) | subtitle |  Describes the feed |
| Image | image | logo |  Allows an image to be displayed when aggregators present a feed |
| WebMaster | webMaster | - | Defines the e-mail address to the webmaster of the feed | 


* required

## Author

| Field | RSS 2.0 | Atom |
|-------|---------|------|
| name  | author | name |
| email [RFC 2822](http://tools.ietf.org/html/rfc2822) | emailauthor | email |


## FeedEntry

| Field | RSS 2.0 | Atom | Description |
|-------|---------|------|-------------|
| Title | title (*) | title | Title of the item. |
| Link | link (*) | link | The hyperlink to the item. |
| Summary | - | summary |
| Content | description (*) | content | Content the item. |
| Author | author | author | Author is used to specify the e-mail address of the author of an item. |
| PublishDate | pubDate | published | Last publication date for the item. |
| Updated | - | updated | Defines the last-modified date of the content of the feed. |
| Enclosure | enclosure  | - | 

# ToDo

* Documentation
* Validate Atom-Feed
* Implement 'image' 
* Code Samples and Demo Application
* Validation of input parameter, required fields,...
