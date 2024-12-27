three ways to call REST endpoints from a Spring app: 
1- OpenFeign—A tool offered by the Spring Cloud project. I recommend developers use this feature in new apps for consuming REST endpoints. 
2- RestTemplate—A well-known tool developers have used since Spring 
 to call REST endpoints. RestTemplate is often used today in Spring apps. However, as we’ll discuss in this chapter, OpenFeign is a better alternative to RestTemplate, so if you work on a new app, you’ll probably avoid RestTemplate and use OpenFeign instead. 
 3- WebClient—A Spring feature presented as an alternative to RestTemplate. This feature uses a different programming approach named reactive programming