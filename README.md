# Postgres image for backend API
Postgres' extension image that defines API and back-end schemas as well as a low-privileged API user.

## Environement variables
Aside from the environmental variables the official Postgres image specifies, this image uses the following ones:
* `POSTGRES_API_USER` - the name of the API user that will have access to the API schema
* `POSTGRES_API_USER_PASSWORD` - the password of the API user
 
API user is granted `USAGE` permissions to the `api` schema. The initialization script also creates `backend` schema.
