# lint-staged hook for pre-commit

## Configuration

1. Configure your project with a [lint-staged configuration file](https://www.npmjs.com/package/lint-staged#configuration)
1. Add the following to your `.pre-commit-config.yaml` file:
    ```yaml
    - repo: https://github.com/jwbennet/lint-staged-pre-commit-hook
      rev: <tag>
      hooks:
        - id: lint-staged
          stages: [ pre-commit ]
    ```
1. Add any additional dependencies needed with the `additional_dependencies` parameter of the hook. For example, the following adds [Prettier](https://prettier.io/) for use with `lint-staged`
    ```yaml
    - repo: https://github.com/jwbennet/lint-staged-pre-commit-hook
      rev: <tag>
      hooks:
        - id: lint-staged
          stages: [ pre-commit ]
          additional_dependencies: [ prettier ]
    ```
1. Install the hook in your repository:
   ```sh
   pre-commit install
   ```
