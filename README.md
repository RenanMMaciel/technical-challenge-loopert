### DevOps Challenge

### Requirements
  - [Docker](https://docs.docker.com/get-started/get-docker/)
  - [BUTT](https://danielnoethen.de/butt/)

### Configurations
  - Cloning and accessing the repository:
    ```bash
    git clone https://github.com/RenanMMaciel/devops-challenge.git && cd devops-challenge
    ```

  - Downloading images, building and up Icecast and Nginx containers.
    ```bash
    docker compose up -d
    ```

  - After downloading [BUTT](https://danielnoethen.de/butt/)
    - Click on “Configs”
    - In the “Server” section, click on “Add”
    - In the “Name” field, fill in “Icecast”
    - In the “Type” field, choose “Icecast”
    - In the “Address” field, fill in “localhost”
    - In the “Port” field, fill in “8000”
    - In the “Password” field, fill in with “[`source-password`](icecast/icecast.xml#L15)” from the [`icecast.xml`](icecast/icecast.xml) file
    - In the “Mount” field, fill in “/stream”
    - In the “Icecast User” field, fill in “source”
    - Click on "Add"
    - Close the configuration window
    - Back on the BUTT home screen, click on the “Play” icon

  - Access [localhost:8000](http://localhost:8000)
    - On [localhost:8000](http://localhost:8000), you can see the Icecast options, such as “Administration”, "Server Status" and "Version".
      - Click on "Administration"
      - In the “Username” field, fill in with “[`admin-user`](icecast/icecast.xml#L17)” from the [`icecast.xml`](icecast/icecast.xml) file
      - In the “Password” field, fill in with “[`admin-password`](icecast/icecast.xml#L18)” from the [`icecast.xml`](icecast/icecast.xml) file
      - Submit login
      - On [localhost:8000/admin/](http://localhost:8000/admin/), you can see the Icecast Admin options, such as “Admin Home”, "List Mountpoints", "Move Listeners" and "Index".
      - Click on "List Mountpoints" and you can see a mount point "[/stream](http://localhost:80/stream)"

  - Access [localhost:80/stream](http://localhost:80/stream)
    - You can see the audio started on BUTT being broadcast by the live player.

### Demo Video of the Application
https://github.com/user-attachments/assets/36dcd05a-b038-4c7a-9f65-f44b26b2714f

