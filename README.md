#Using the API for the Best of's
---

##Get requests
#####Routes
/api/lists : Acess the top 5 lists by aggreagate vote
/api/list?page=2 : Acess next 5 lists by aggregate vote
/api/post/:id : Access the show page for the list at that ID number.

Lists can be replaced with votes, users, and items. Items, users, or votes show all, not the top 5.

###Sample
Api call : http://localhost:3000/api/lists/1

```{
  "id": 1,
  "image_ref": "#",
  "source_ref": "http://www.imdb.com/chart/top",
  "list_desc": "A user curated list of the top two-hundred and fifty movies in the databse",
  "list_title": "The Internet Movie Database top movies.",
  "user_id": 1,
  "created_at": "2016-04-10T20:22:43.102Z",
  "updated_at": "2016-04-10T20:22:43.102Z",
  "list_type": "Movies",
  "items": [
    {
      "id": 1,
      "one": "The Shawshank Redemption",
      "two": "The Godfather",
      "three": "The Godfather: Part II",
      "four": "The Dark Knight",
      "five": "Schindler's List",
      "six": "12 Angry Men",
      "seven": "Pulp Fiction",
      "eight": "The Lord of the Rings: The Return of the King",
      "nine": "The Good, the Bad and the Ugly",
      "ten": "Fight Club",
      "list_id": 1,
      "created_at": "2016-04-10T20:22:43.123Z",
      "updated_at": "2016-04-10T20:22:43.123Z"
    }
  ]
}
```
##Put requests
Api call : put api/posts/:id
Api call : put api/items/:id
Api call : put api/users/:id
Api call : put api/votes/:id

####Sample of params needed
#####Users

username : The desired username change
password : The desired password change

#####Votes

user_id : The user id associated eith the vote
list_id : The user id associated eith the vote
up_vote : If the vote was positive this should be 1, else 0
down_vote : If the vote was negative this should be 1, else 0

#####Items

Each item corresponds to an item on a top ten list.
item[one]
item[two]
item[three]
item[four]
item[five]
item[six]
item[seven]
item[eight]
item[nine]
item[ten]

#####Lists

list_title : The title of the list being submitted.

