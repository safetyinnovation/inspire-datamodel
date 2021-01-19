# SocialMedia

This entity contains a harmonised description of SocialMedia Postings

## Data Model

- `id`: Unique identifier

- `type`: SocialMedia

- `country`: Text. The identified country of the post

- `createdBy`: The SocialMediaUser who created the post

- `dateIssued`: The timestamp when the Social Media post was posted. Type: DateTime

- `location`
  - Type: String Array: Identified locations from the post

  - `media`:
    - Type: `StructuredValue`
    - `imageUrls`: String Array of URL pointing to an image
    - `videoUrls`: String Array of URL pointing to a video

- `message`: Text Full text of the posting, if available

- `network`: The name of the Social Media Network where the post was published (e.g. Facebook)

- `searchIds`: String Array indicating to which crawler/social media search this post belongs

- `sentiment`: Number. The sentiment of the post (e.g. negative, positive, neutral, no value)

- `snipppet`: Text. Short extract (snippet) of the social media post

- `viralityTotalScore`: Number. Virality indicator of the post
