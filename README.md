# ECR Impact Matrix

The ECR Impact Matrix project implements a simplified version of the Express ECO Impact Matrix onto the ECR, and adds an item action to convert an ECR to an ECN. It's compatible with Aras Innovator 11 SP12 out-of-the-box, as well as Aras Innovator with PE 11.0 R4 installed.

## History

Release | Notes
--------|--------
[v1.0.0](https://github.com/ArasLabs/ecr-impact-matrix/releases/tag/v1.0.0) | First release.

#### Supported Aras Versions

Project | Aras
--------|------
[v1.0.0](https://github.com/ArasLabs/ecr-impact-matrix/releases/tag/v1.0.0) | 11.0 SP12

## Installation

#### Important!
**Always back up your code tree and database before applying an import package or code tree patch!**

### Pre-requisites

1. Aras Innovator installed (version 11.0 SP12+)
2. Aras Package Import Utility
3. ECR Impact Matrix import packages
4. Code Tree overlay

### Install Steps

#### The Code Tree
1. Backup your code tree and store the backup in a safe place.
2. Copy the `Innovator` folder from `\CodeTree` in your local repository.
3. Paste this folder to the root install directory of your code tree.
	* This should be the same folder that contains the `InnovatorServerConfig.xml`.

#### The Database
1. Backup your database and store the BAK file in a safe place.
2. Open up the Aras Package Import tool.
3. Enter your login credentials and click **Login**
    * _Note: You must login as root for the package import to succeed!_
4. Enter the package name in the TargetRelease field.
    * Optional: Enter a description in the Description field.
5. Enter the path to your local `..\ecr-impact-matrix\Import\1-Pre\imports.mf` file in the Manifest File field.
6. Select the following in the Available for Import field.
    * **com.aras.innovator.solution.PLM**
7. Select Type = **Merge** and Mode = **Thorough Mode**.
8. Click **Import** in the top left corner.
9. Enter the path to your local `..\ecr-impact-matrix\Import\2-Post\imports.mf` file in the Manifest File field.
10. Select the following in the Available for Import field.
    * **com.aras.innovator.solution.PLM**
11. Click **Import** in the top left corner.
12. Close the Aras Package Import tool.

You are now ready to login to Aras and check out the ECR Impact Matrix.

## Usage



## Contributing

1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -am 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request

For more information on contributing to this project, another Aras Labs project, or any Aras Community project, shoot us an email at araslabs@aras.com.

## Credits

Created by Mike Gavlak, Aras Corporation. 

## License

Aras Labs projects are published to Github under the MIT license. See the [LICENSE file](./LICENSE.md) for license rights and limitations.