# Angular in nodeenv

This procedure describes how to create a nodeenv on Windows for developing Angular applications.

## Procedure

1. Create a python virtual environment:

    ```
    $ python -m venv <venv_name>
    ```

1. Activate the python virtual environment:

    * Linux-based terminal (e.g., Git Bash):

        ```
        $ source <path_to_venv>/Scripts/activate
        ```

    * Windows cmmand prompt:
        
        ```
        $ <path_to_venv>/Scripts/activate
        ```

1. Run the following command to upgrade pip:

    ```
    (venv) $ python -m pip install --upgrade pip
    ```

1. Run the following command to install nodeenv:

    ```
    (venv) $ pip install nodeenv
    ```

1. Run the following comment to install the latest version of Node.js:

    ```
    (venv) $ nodeenv -p
    ```

    **Note**: To install a specific version of node, use the `--node` command-line option; for example:

    ```
    (venv) $ nodeenv -p --node=<node_version>
    ```

    Where `node_version` is the version of node.js that you want to install.

1. Run the following command to confirm the node version within your virtual environment: 
    
    ```
    (venv) $ node -v
    ```

    **Note**: Node.js and Angular versions must be compatible; to determine which versions of Node.js and Angular to use, refer to [Version compatibility](https://angular.io/guide/versions).

1. With your virtual environment activate, run the following command to create an Angular application:

    ```
    (venv) $ npx @angular/cli@<version> new <project_name>
    ```

    Where `<version>` is the version of Angular to install and `<project_name>` is the name of the Angular project to create.

1. Change into the application folder, and run the following command to build and serve the application:

    ```
    (venv) $ ng serve
    ```

1. Access the application at `http://localhost:4200/`.
