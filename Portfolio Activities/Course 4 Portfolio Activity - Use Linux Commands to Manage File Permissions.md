File Permissions in Linux

Project Description:
The research team at my organization needs to update the permissions for certain files and directories within the “projects” directory.
The existing permissions do not reflect the level of authorization that should be given for these files and directories.
Checking and updating these permissions will aid in keeping the systems secure.
The completion of this task is outlined in the sections below.



Check File and Directory Details:
The following image demonstrates how I used Linux commands to determine the existing permissions for a specific directory within the file system.

![LinuxPermission1](https://github.com/GVTH8K/GoogleCybersecurityCertificate/blob/main/Portfolio%20Activities/Images/LinuxPermission1.png?raw=true)

The first line in this image displays the command that I entered to check the contents and permissions of the “projects” directory and any files within it.
The lines that follow this command represent the output.
Since the “ls” command was used with the “-la” switch, the output included a detailed listing of the contents of this directory including any files that were hidden.
The output of this command indicates that the “projects” directory contains one directory named drafts, one hidden file named “.project_x.txt”, and five other project files.
The ten-character string in the first column represents the current permission set for each file or directory.



Describe the Permissions String:
The ten-character string can be used to determine who is authorized to access the file or directory, and what specific permissions they have. The characters and what they represent are as follows:

  ●	1st character: This character is either a d or hyphen (-) and indicates the file type.
    If it’s a d, it’s a directory. If it’s a hyphen (-), it’s a regular file.

  ●	2nd-4th characters: These characters indicate the read (r), write (w), and execute (x) permissions for the user.
    When one of these characters is a hyphen (-) instead, it indicates that this permission is not granted to the user.

  ●	5th-7th characters: These characters indicate the read (r), write (w), and execute (x) permissions for the group.
    When one of these characters is a hyphen (-) instead, it indicates that this permission is not granted for the group.

  ●	8th-10th characters: These characters indicate the read (r), write (w), and execute (x) permissions for other.
    This owner type consists of all other users on the system apart from the user and the group.
    When one of these characters is a hyphen (-) instead, that indicates that this permission is not granted for other.

For example, the permissions for “project_t.txt” are “-rw-rw-r--”.
Since the first character is a hyphen, we are dealing with a regular file rather than a directory.
The second, fifth, and eighth characters are all “r”, indicating that the user, group, and other all have read permissions.
The third and sixth characters are “w”, which indicates that the user and group have write permissions, while other does not.
Based on the permissions string, no one has the ability to execute this file.



Change File Permissions:
The organization determined that group should not have write access for any of their files.
To comply with this, I referred to the file permissions that were gathered previously.
Based on these permissions, I was able to determine that “project_k.txt” file must have write access removed for other.
The following image demonstrates how I used Linux commands to adjust the permission.

![LinuxPermission2](https://github.com/GVTH8K/GoogleCybersecurityCertificate/blob/main/Portfolio%20Activities/Images/LinuxPermission2.png?raw=true)

The first two lines display the commands that were entered, while the lines following this demonstrate the output from the second command.
The “chmod” command is used to update permissions for files and directories in Linux.
The first argument “o-w” indicates that the write permission should be removed from other, while the second argument indicates the target file.
In this example, I removed write permissions for other from the “project_k.txt” file in order to comply with business requirements.
Following this, I used the “ls -la” command to review the updates that were made.



Change File Permissions on a Hidden File:
The research team at my organization recently archived “.project_x.txt”.
They do not want anyone to have write access for this file, however the user and group should have read access.
The following image demonstrates how I used Linux commands to update these permissions.

![LinuxPermission3](https://github.com/GVTH8K/GoogleCybersecurityCertificate/blob/main/Portfolio%20Activities/Images/LinuxPermission3.png?raw=true)

The first two lines display the commands that were entered, while the lines following this demonstrate the output from the second command.
It can be identified that “.project_x.txt” is a hidden file due to the fact that the name starts with a “.”.
In this example, I removed write permissions from the user and group, and added the read permission to group.
The write permission for user was removed using the “u-w” argument, and the write permission for group were removed using the “g-w” argument.
The read permission was added to group using the “g+r” argument.



Change Directory Permissions:
My organization determined that only the researcher2 user should have access to the “drafts” directory and its contents.
This means that no one other than researcher2 should have execute permissions, so the execute permission will need to be removed from group.
The following image demonstrates how I used Linux commands to update these permissions.

![LinuxPermission4](https://github.com/GVTH8K/GoogleCybersecurityCertificate/blob/main/Portfolio%20Activities/Images/LinuxPermission4.png?raw=true)

The first two lines display the commands that were entered, while the lines following this demonstrate the output from the second command.
Since it was previously determined that group had execute permissions for this directory, I used the “chmod” command with the “g-x” argument to remove them.
The researcher2 user already had the necessary permissions, so none needed to be added.



Summary:
In this scenario, I updated multiple permissions for both files and directories within the “projects” directory to match the level of authorization deemed appropriate by the organization.
The first step was to use the “ls- la” command to view the existing permissions for the directory and its contents.
This provided the information necessary to determine what needed to be updated based on the organization’s requirements.
I then updated the permissions using the “chmod” command along with the necessary arguments.
These changes were then validated using the “ls -la” command.
