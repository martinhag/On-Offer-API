# On offer - API

## Use
- AWS Lambda for REST API AND Worker to crawl sites for new products on offer
- DynamoDB for the database
-- looking for ORM for DynamboDB, might be dynamoose (https://www.npmjs.com/package/dynamoose)

## TL;DR
Users creates profile, and saves searchwords for products they want to survay, eg. `'i9-'`.
We store the searchwords and crawl predefined URL's. If any matches are found, we store these products with what info we can get.
Then the system notifies the user. The user can now see a list of every match, ordered by URL/location, on his profile.

## Responsibilities
- API takes searchwords/queries and URL's to search
- API returns all products which matches given queries, ordered by location/store
- API also stores contact info to be able to notify user if a product is found?
- Worker Crawls defined URL's after products that matches queries
- Worker stores all matches in DynamoDB, with data from where and product info
- User management, user searchwords and other data is stored and managed on another site/repo
- The other site fetches products from API when showing products on offer to the user