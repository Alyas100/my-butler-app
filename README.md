# My Butler Project - Setup Guide
## Prerequisites

Make sure you have Dart and Flutter installed on your machine.

###Step 1: Verify Installation

Check if Flutter and Dart are correctly installed in your machine:

flutter doctor

###Step 2: Start the Server (Serverpod)

Navigate to your server project folder:

cd my_butler_project_server


Then run:

docker-compose up -d


Apply migrations and start the Serverpod server:

dart bin/main.dart --apply-migrations

-run the above command only once in inital setup, then after that just run: dart bin/main.dart

###Step 3: Run the Flutter UI

Navigate to your Flutter project folder:

cd ../my_butler_project_flutter


Run the app in Chrome:

flutter run -d chrome

-for running using real device emulator, can use android studio

-for developing code, only edit related file under 'my_butler_project_server' for backend and 'my_butler_project_flutter' for frontend.


After finished doing a feature (frontend and corresponding backend), create test and run.

-for frontend, go to 'test' folder under 'my_butler_project_flutter', create ur test in a new file (each feature, one test file) and run this below:

flutter test


-for backend, go to 'my_butler_project_server' folder, and find 'test' folder, then add ur correspoding test file for the feature in backend, under the 'integration' folder. NOTE that only if u are testing indviudal functions or anything that relates to unit test, then only create a folder called 'unit test', and add ur test code there, othrwise, just create a file for the feature under 'integration' folder. To run backend test use this command below:

-dart test

## Command to push to main branch remote from the current local feature branch is:

git push origin <<your-feature-branch name here>>:main



Pro Tip: Run in debug mode to enable hot reload. This allows the UI to update automatically after saving code changes.

NOTES-- we develop for phone layout so make sure use screen layout if develop using chrome. 
