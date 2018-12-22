## Release procedure
1. Run **Build** script; ```build -b release -y``` or ```build -b release -y --auto_color``` (_Script not updated to this format yet._)
1. Run **Build** script for public build; ```build -b release -p -y``` or ```build -b release -p -y --auto_color``` (_Script not updated to this format yet._)
1. Run **Deploy** ```deploy -r full``` or ```deploy -r full --auto_color``` (_Script is not created yet)
1. Create patch release