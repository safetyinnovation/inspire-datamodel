# SocialMedia

This entity contains a harmonised description of SocialMedia Posting

## Data Model

- `id`

- `type`

- `country`: The identified country

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

- `sentiment`: Number. The sentiment of the post (e.g negative, positive, neutral, no value)

- `snipppet`: Short extract (snippet) of the social media post


- ` `
  - Attribute type: GeoProperty. `geo:json` Point.
  - Normative References:
        [https://tools.ietf.org/html/rfc7946](https://tools.ietf.org/html/rfc7946)
  - Required.
