# Important Files

#### [`description.toml`](description.toml)
A toml file that describes the application intergating with Launcher.
- You will fill [template](description.toml) with your application's information.
- [Visualize how each attribute will look in Launcher.](toml.md#how-the-toml-attributes-are-displayed)
- [Breakdown of content-pack Requirements](content-pack.md)

#### [`package.toml`](package.toml)
A toml file where you provide your build executables and images in `.zip` format per `OS`.
- **Supported OS** 
   - windows-x86
   - windows-x86_64
   - windows-aarch64
   - linux-x86
   - linux-x86_64
   - linux-aarch64
- **Images size requirements**
   - Card: 220x124
   - Main image: 1920x1080
   - Background: 1920x1080
   - Featured: 175x273
   - Icon: 32x32
- [Fill in the template](package.toml), with your application's information.
- [Thin packages vs Thick packages](thin-vs-thick.md)

#### [`requirements.toml`](requirements.toml)
- A toml file that defines the system requires for your application to be used.  
- [Fill in the template](requirements.toml), with your application's system requirements.
- [Visualize how each attribute will look in Launcher.](images/requirements.JPG)

#### [`CHANGELOG.md`](CHANGELOG.md)
A markdown file that documents changes for your release.
- [Fill in the template](CHANGELOG.md), with your application's changes.

#### [`message.toml`](CHANGELOG.md)
A toml file that allows to send message to multiple platforms ([Forums](https://forums.developer.nvidia.com/c/omniverse/300), [Jira](https://nvidia-omniverse.atlassian.net/jira/projects), Slack, text messages, or email) as part of your release.
- [Fill in the template](message.toml), with your application's system requirements.
- [Click for more details on implementation](message-toml-doc.md).
