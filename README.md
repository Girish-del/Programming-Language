Take pull from the above branch
|
# Setup tools
1. sudo apt update
2. sudo apt install default-jre python3-pip -y
3. pip install antlr4-python3-runtime

# Go to working folder
wget https://www.antlr.org/download/antlr-4.13.0-complete.jar

# Generate ANTLR parser
java -Xmx500M -cp ".:antlr-4.13.0-complete.jar" org.antlr.v4.Tool -Dlanguage=Python3 -visitor -listener MarathiCode.g4

# Run the program
python3 main.py sample.mc
