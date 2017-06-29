# ClientAPI CDK (Client Development Kit)
Development Kit for the ClientAPI

## Setup

The setup is the same as any other forgegradle project. The instructions below are for Intellij IDEA, however you can look up instructions for other IDEs.

- Clone the CDK recursively: `git clone --recursive https://github.com/ZeroMemes/ClientAPI-CDK.git`
  - You may want to remove our git tracking and setup your own. If so, remove `.git`, `.gitmodules` and `src/main/.git` and then run `git init` to set up your own git repo. _TODO: Add a setup script that does this automatically_
- Import the project as a gradle project in Intellij
- Create a run configuration for gradle task `setupDecompWorkspace`
  - Use VM options `-Xmx2g` to assign at least 2GB of ram (4GB recommended)
  - Tick "Single instance only"
- Run your newly created run configuration for `setupDecompWorkspace`
- Once this is complete reload gradle libs by clicking the blue "Refresh all Gradle projects" icon under the gradle tab
- Create client run configurations by running gradle task `genIntellijRuns`

That's it. When the gradle config changes, you will need to re-run your `setupDecompWorkspace` task and refresh gradle projects, but you should never need to run `genIntellijRuns` again.

To build a jar, you should run the `build` gradle task. To debug you can use the generated "Minecraft Client" run configuration.