



# 3. Adding an offline mode for local speech-to-text translation
## Azure speech recognition can be used to execute commands
The Speech CLI is a command-line tool for using the Speech service without writing any code. The Speech CLI requires minimal setup, and it's easy to immediately start experimenting with key features of the Speech service to see if your use-cases can be met. Within minutes, you can run simple test workflows like batch speech-recognition from a directory of files, or text-to-speech on a collection of strings from a file. Beyond simple workflows, the Speech CLI is production-ready and can be scaled up to run larger processes using automated .bat or shell scripts.

Most features in the Speech SDK are available in the Speech CLI, and some advanced features and customizations are simplified in the Speech CLI. Consider the following guidance to decide when to use the Speech CLI or the Speech SDK.

Use the Speech CLI when:

You want to experiment with Speech service features with minimal setup and no code
You have relatively simple requirements for a production application using the Speech service
Use the Speech SDK when:

You want to integrate Speech service functionality within a specific language or platform (for example, C#, Python, C++)
You have complex requirements that may require advanced service requests, or developing custom behavior including response streaming.
