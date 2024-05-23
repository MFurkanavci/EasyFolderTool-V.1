# EasyFolderTool-V.1

`EasyFolderTool-V.1` is a Unity Editor tool that allows users to create, manage, export, and import custom folder structures. This tool helps streamline the process of setting up project folder hierarchies, making it easier to maintain consistency and organization in your Unity projects.

## Features

- **Create Folder Structures**: Define custom folder structures and save them for reuse.
- **Add Structures**: Apply saved folder structures to any root folder within your project.
- **Bulk Create**: Create multiple folders at once using a saved structure and a list of folder names.
- **Manage Structures**: Export and import folder structures to and from JSON files for easy sharing and backup.

## Installation

1. Clone or download the repository.
2. Place the `CustomFolderCreator.cs` script in an `Editor` folder within your Unity project.

## Usage

### Opening the Tool

1. In the Unity Editor, navigate to `Tools > Custom Folder Creator`.
2. The `Folder Creator` window will appear.

### Creating a Folder Structure

1. Go to the `Create Structure` tab.
2. Enter a name for the new structure.
3. Specify the number of sub-folders and their names.
4. Click `Save Structure` to save the new folder structure.

### Adding a Folder Structure

1. Go to the `Add Structure` tab.
2. Click `Select Root Folder` and choose the root folder where the structure should be created.
3. Select a saved folder structure from the list.
4. Enter the main folder name.
5. Click `Create Folder Structure` to generate the folders.

### Bulk Creating Folders

1. Go to the `Bulk Create` tab.
2. Click `Select Root Folder` and choose the root folder where the structures should be created.
3. Enter folder names in the text area, one name per line.
4. Select a saved folder structure from the list.
5. Click `Create Folder Structure` to generate the folders.

### Managing Folder Structures

1. Go to the `Manage Structures` tab.
2. Click `Export Structures` to save the current structures to a JSON file.
3. Click `Import Structures` to load structures from a JSON file.

## Code Overview

### CustomFolderCreator Class

The `CustomFolderCreator` class extends `EditorWindow` and provides the core functionality for the tool, including UI rendering, structure management, and folder creation.

#### Key Methods

- `ShowWindow()`: Displays the Custom Folder Creator window.
- `OnGUI()`: Renders the UI based on the selected tab.
- `DrawCreateStructureTab()`: Draws the UI for creating a new folder structure.
- `DrawAddStructureTab()`: Draws the UI for adding a saved structure to a root folder.
- `DrawBulkCreateTab()`: Draws the UI for bulk folder creation.
- `DrawManageStructuresTab()`: Draws the UI for managing saved structures.
- `SaveFolderStructure()`: Saves a new folder structure to EditorPrefs.
- `RemoveFolderStructure()`: Removes a saved structure from EditorPrefs.
- `SaveFolderStructuresToPrefs()`: Saves all folder structures to EditorPrefs.
- `LoadFolderStructures()`: Loads folder structures from EditorPrefs.
- `CreateFolderStructure()`: Creates a folder structure in the selected root folder.
- `CreateFolderStructureForBulk()`: Creates a folder structure for each name in the bulk create list.
- `ExportStructures()`: Exports the saved structures to a JSON file.
- `ImportStructures()`: Imports structures from a JSON file.

### Data Classes

- `FolderStructureData`: A serializable class for exporting and importing folder structures.
- `FolderStructure`: A serializable class representing a single folder structure.

## Contributing

Contributions are welcome! If you have suggestions for improvements or new features, feel free to open an issue or submit a pull request.

### License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

### Acknowledgements

Special thanks to the Unity community for their continuous support and contributions to making development tools like this possible.

---

Feel free to customize this README as needed for your project. Happy coding!
