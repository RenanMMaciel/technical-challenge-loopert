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
    1. Click on “Configs”
    2. In the “Server” section, click on “Add”
    3. In the “Name” field, fill in “Icecast”
    4. In the “Type” field, choose “Icecast”
    5. In the “Address” field, fill in “localhost”
    6. In the “Port” field, fill in “8000”
    7. In the “Password” field, fill in with “[`source-password`](icecast/icecast.xml#L15)” from the [`icecast.xml`](icecast/icecast.xml) file
    8. In the “Mount” field, fill in “/stream”
    9. In the “Icecast User” field, fill in “source”
    10. Click on "Add"
    11. Close the configuration window
    12. Back on the BUTT home screen, click on the “Play” icon

  - Access [localhost:8000](http://localhost:8000)
    - On [localhost:8000](http://localhost:8000), you can see the Icecast options, such as “Administration”, "Server Status" and "Version".
      1. Click on "Administration"
      2. In the “Username” field, fill in with “[`admin-user`](icecast/icecast.xml#L17)” from the [`icecast.xml`](icecast/icecast.xml) file
      3. In the “Password” field, fill in with “[`admin-password`](icecast/icecast.xml#L18)” from the [`icecast.xml`](icecast/icecast.xml) file
      4. Submit login
      5. On [localhost:8000/admin/](http://localhost:8000/admin/), you can see the Icecast Admin options, such as “Admin Home”, "List Mountpoints", "Move Listeners" and "Index".
      6. Click on "List Mountpoints" and you can see a mount point "[/stream](http://localhost:80/stream)"

  - Access [localhost:80/stream](http://localhost:80/stream)
    - You can see the audio started on BUTT being broadcast by the live player.

### Demo Video of the Application
  <video controls>
  <source src="docs/application.mp4" type="video/mp4">
  </video>

  - If you prefer, download the video [here](docs/application.mp4)
