The `message.toml` is for fanning out communications as per of your release process.

# Use-Cases
##### Problem
- Your release resolves 3 **forum** post, 2 **jira** stories, and you want to **email** a specifc customer once issue is resolved.
##### Solution
- The message.toml allows you to address all these communications in one location.

# How it works
  - In the message.toml you provide the urls to where you want to post.
    - Examples
      - Form post: https://forums.developer.nvidia.com/t/a2f-2021-2-4-is-available-for-download/176436
      - Jira issue: https://nvidia-omniverse.atlassian.net/secure/RapidBoard.jspa?rapidView=25052&projectKey=OM&modal=detail&selectedIssue=OVPUB-25
 - By default, we use your CHANGELOG.md to form the message to these platforms.
 - Alternatively, you can write unique message (independent of the CHANGELOG.md).
  - This is done by adding `override_message = My unique message` to your message.toml

## Post release updates  
 - Post messages on release to Jira, Slack, Email, [forums.developer.nvidia](https://forums.developer.nvidia.com/), and Text Message 
 - Requires a [message.toml](message.toml)
 - By **default** the message will contain contains of CHANGELOG.md
 - Alternatively, you post **custom messages** and override the CHANGELOG.md by adding `override_message = "my custom message"` to your message.toml
    - Allowing for a custom message
  - Ex: `override_message = "OM-27478 Support camera control on multiple viewports. (Jihui Shentu)"`
## Post change updates to Jira  
  - Update Jira Issues once fixes are published
    - Ex: I'm publishing a release that resolves Jira Issue [OM-23030](https://nvidia-omniverse.atlassian.net/browse/OM-23030).
  - Add jira array to [message.toml](message.toml)
    - for one:  `jira = ["OM-26226"]`
    - for multiple: `jira = ["OM-26226", "OM-26227"]`
## Post change updates to Forums    
  - Update [Forums](https://forums.developer.nvidia.com/c/omniverse/300) once fixes are published
    - Ex: I'm publishing a release that resolves Forum [Omniverse-Drive-Installing-Frozen-When-Register-169647](https://forums.developer.nvidia.com/t/omniverse-drive-installing-frozen-when-register/169647).
  - Add forum array to [message.toml](message.toml)
    - you only need to provide the id of the Forums Post
      - In our example its [16947](https://forums.developer.nvidia.com/t/omniverse-drive-installing-frozen-when-register/169647)
    - for one:  `forums = ["169647"]`
    - for multiple: `forums = ["169647", "169648"]`
## Post change updates via Text Message
  - Ex: I want to text client after publishing change.
  - Add sms array to [message.toml](message.toml)
    - _**include country code in number (EX: US is `1`)**_
    - for one:  `text = ["14001234000"]`
    - for multiple: `text = ["14001234000", "14001234030" ]`
## Post change updates Email 
  - Ex: I want to email client after publishing change.
  - ** Emails will be sent to shared-pipeline-myapp@nvidia.com ** 
    - This email is a nvidia dl
  - You can request to add emails to dl via [gitlab issue](https://gitlab-master.nvidia.com/omni-cd/toml-database/-/issues/new?issue%5Bassignee_id%5D=&issue%5Bmilestone_id%5D=) 
  - To do, set email value to true in [message.toml](message.toml)
    - Ex: `email = true`


