Clone this project running git clone https://github.com/amoraitis/TodoList.git in your terminal. If you haven't git installed can simply download it and unzip it.

2 - Add your Sendgrid API Key by running dotnet user-secrets set "SendGrid:ServiceApiKey" "your_secret_key".

3 - Run the required infrastructure (PostgreSQL etc) for development purposes

Go to the TodoList/ folder by running the command cd TodoList/
Run the command docker-compose -f docker-dev-compose.yml up to bring up the infrastructure. This will setup and run the PostgreSQL server locally.
Note that a folder pgdata will be created. PostgreSQL data is persisted in this folder and can be used without having to re-create/seed data over and over during development. Delete this folder to remove any data created during development.
4 - Go to the TodoList/TodoList.Web folder by running the command cd TodoList/TodoList.Web or manually navigating into the file system.

5 - Run the command dotnet tool install -g Microsoft.Web.LibraryManager.Cli to install Libman.

6 - Run the command dotnet restore to install all the dependencies.

7 - Run the command dotnet build to compile the project.

8 - Run the command dotnet run to start serving the project.

9 - That it's, your application is running in http://localhost:47818.
