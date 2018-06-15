# Gorails forum mini series

Start with models

## Database Structure

1. User
- Devise gem
* email:string
* password:string

has_many :forum_threads
has_many :forum_post

2. ForumThread
* user_id:integer
* subject:string

belongs_to :user
has_many :forum_posts

3. ForumPost
* forum_thread_id:integer
* user_id:integer
* body:text

belongs_to :forum_thread_id
belongs_to :user