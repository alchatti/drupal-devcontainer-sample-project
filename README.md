# Drupal devcontainer sample project

This is a sample project using Drupal 9 & PHP 8 for demonstrating [Drupal Devcontainer](https://github.com/alchatti/drupal-devcontainer) project.

## Usage

1.Clone this project with its submodule to `drupal-dev-1` folder.

```bash
git clone --recurse-submodules https://github.com/alchatti/drupal-devcontainer-sample-project.git drupal-dev-1
```

2.Create `pnpm-store` Docker volume

```bash
docker volume create pnpm-store
```


2.Using `devcontainer cli` access `drupal-dev-1` folder and start the project.

```bash
cd drupal-dev-1
devcontainer open .
```

3.Inside the devcontainer using VS Code integrated terminal install dependencies using the container script.

```bash
# Option (A) project composer dependencies version [Not Up to date]
composer install
# Option (B) Install & update composer dependencies [Latest version]
yes | composer update
```

4.In the browser visit http://localhost and start drupal installation using standard profile.

5.Fill in the site information.

## References

- https://github.com/alchatti/drupal-devcontainer for more information on the devcontainer project
- https://www.drupal.org/docs/develop/using-composer/manage-dependencies for Using Composer to Install Drupal and Manage Dependencies
