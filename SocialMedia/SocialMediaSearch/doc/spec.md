# SocialMediaSearch

This data model desribes a search for crawling/monitoring social media networks.

## Data model

- `id`: Unique identifier
- `type`: SocialMediaSearch
- `active`: Boolean. Is the search active or inactive (e.g. due to an error)?
- `dateLastModified`: DateTime. Timestamp when the search was last modified.
- `deleted`: Boolean. Indicator if a user deleted the search
- `errorMessage`: Text. Placeholder for error messages from the search
- `name`: Text. Name of the search
- `parentSearchId`: Id of the parent search.
- `searchMode`: Enum. Supported search modes. Valid value `advanced`
- `searchPhrase`: Text. The search phrase
- `searchId`: Number. The internal id of the search
- `missionId` : Relationship. The mission with which this search is associcated.
- `facebookAccounts`: String Array. Optional. List of Facebook accounts (e.g. page names) to monitor
- `twitterAccounts`: String Array. Optional. List of Twitter accounts (e.g. page names) to monitor
- `instagramAccounts` : String Array. Optional. List of Instagram accounts (e.g. page names) to monitor
