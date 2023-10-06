# openapi-example

**version 1.1.0**

This is an OpenAPIv3 description of a video game journaling API.

**[Click here for SwaggerUI](https://handoniumumumum.github.io/openapi-JournalExample)**

## Usage

> This is an interface, so you need to implement the logic for each endpoint interaction.

### Adding a game to the database

Add games to the database by sending a POST request to the `/game/` endpoint.

```
// example game to send in the POST request

{
  "name": "Super Mario 64",
  "platform": [
  {
    "id": 4
  }
  ],
  "photoUrls": ["https://imgur.com/a/hDcGArh"],
  "tags": [
  {
    "name": "platformer"
  }
  ]
}
```

### Creating a journal entry

Create journal entries by sending a POST request to the `/entry/` endpoint.

To create a new journal entry for a game, nothing is required. If an empty entry is sent, it will be associated with the user as a draft with a unique id.

```
// example entry to send in the POST request

{
  "gameId": "128",
  "status": "draft",
  "entryDate": "2022-03-10T13:45:43+0000",
  "entryText": "Though The Legend of Zelda: Breath of the Wild (BotW) usually excels at keeping my attention, I found myself zoning out during its cutscenes."
  "playStatus": "playing"
}
```
