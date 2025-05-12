#### Some specifics about this infrastructure
- **A server** is a computer that provides information to other computers called "clients" a computer network. The role of a server is to share data as well as to share resources and distribute work. It hosts *a web server*, and *application server*, *the application code* and *a database*

- **The role of the domain name** is to be human redeable adress mapped to an IP like `www.foobar.com` if mapping to `8.8.8.8`<br>
Here `www.foobar.com` is a **Type A** (HTTP / Address)

- **The web server** is the entry point for all requests, litsenning for incoming web trafic, serves the static files and is linked to the application server forwarding the dynamic requests for processing

- **The application server** runs the back-end and communicate with the database ith queries, processes dynamic requests (login, ...) and responses to the web server

- **The database** is the storage for your application's persistent data

- The server is using **HTTP(S) protocol to communicate** with the computer of the user requesting website


#### Issues with this infrastructure:
 - **SPOF**: If the server runs goes down, the wgole website is off
 - If there if a **maintenance needed** the website will be unavailable during it.
 - **If too much incoming traffic**, the server could reach the limit of the server performance
