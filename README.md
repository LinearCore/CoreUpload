# CoreUpload

Packaged upload file. Zipped, encrypted.
Bundler and Patcher

Requirements:
  - Upload the zipped file through the web interface.
  - Seperate service watches the folder it gets uploaded to then starts the update.
  - Delayed time/start time setting in the setting/init file.
  - Package contains:
    - Settings file, serialized, contains the info needs to run the update and the order to run the data objects
    - Site files to be updated
    - Service files to be updated
    - EF comparison checker, run or check any migrations to the database. Should be bound in Core
    - Data objects, such as SQL scripts, 
    - Code files that need to be loaded as plugins and ran, these contain the commands to be executed into the core
  
  - Site notification and warning to users about the site going down
  - Progress indication and feedback, somewhere? Log file, Error log in DB.
    

Bundler:
  - Takes the zipped file, and updates the system based on the rules and data in the package.
  
