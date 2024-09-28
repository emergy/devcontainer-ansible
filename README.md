This is a devcontainer for Visual Studio Code (VSCode) with Ansible and Molecule support.

## Prerequisites

Before using this devcontainer, make sure you have the following installed:

- Docker: You can download and install Docker from the official website: [https://www.docker.com](https://www.docker.com)

## Getting Started

To use this devcontainer, follow these steps:

1. Pull the devcontainer image from Docker Hub by running the following command:

    ```shell
    docker pull emergy/devcontainer-ansible
    ```

2. Open the project in VSCode.

3. Press `Ctrl + Shift + P` (or `Cmd + Shift + P` on macOS) to open the command palette.

4. Type "Remote-Containers: Open Folder in Container" and select it from the list.

5. Choose the root folder of your project.

6. VSCode will now start a new instance inside the devcontainer with Ansible and Molecule pre-installed.

## Usage

Once inside the devcontainer, you can use Ansible and Molecule to manage your infrastructure and test your code.

For more information on how to use Ansible, refer to the official documentation: [https://docs.ansible.com](https://docs.ansible.com)

For more information on how to use Molecule, refer to the official documentation: [https://molecule.readthedocs.io](https://molecule.readthedocs.io)

## Contributing

If you encounter any issues or have suggestions for improvements, feel free to open an issue or submit a pull request on GitHub: [https://github.com/emergy/devcontainer-ansible](https://github.com/emergy/devcontainer-ansible)

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.