# docker-livebook

A Docker Compose-based Livebook setup.


# Instructions

Requires Docker to be installed. Just run `docker compose up` to get started.

You may keep your Livebooks in `./data`, e.g. `./data/hello-world.livemd`. Not that these files are gitignored by default.


# Authentication

By default, the password is `password1234`. There are 2 ways to override the password:
  - (Recommended) Create a `.env` file in the root directory of the project with the environment variable `LIVEBOOK_PASSWORD=your_desired_password`
  - (Not recommended) Override the `docker-compose.yml` file so that the default value for `LIVEBOOK_PASSWORD` is no longer `password1234`
    - WARNING: If you edit the password here, it will end up in your git repository.

# Updating

To update the container, run the following commands from the project root directory:

- Stop the container: `docker compose down`
- Update the image: `docker compose pull`
- Start the container: `docker compose up`

