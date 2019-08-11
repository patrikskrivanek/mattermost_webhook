# Mattermost Webhook
This bash program is used to for sending messages to your Mattermost instance
using Mattermost Webhook URL.

### Installation
```bash
# installing dependencies
sudo apt update
sudo apt install curl git

# clone repository
git clone https://github.com/patrikskrivanek/mattermost_webhook.git

# run mattermost_webhook program with help and learn how to use
mattermost_webhook --help
```

### Arguments
Argument | Description | Required
------------ | ------------- | -------------
--url | Webhook url for sending requests to Mattermost | yes
--channel | Name of channel in Mattermost | yes
--message | Message text | yes
--username | Username to notify as | no [default: Mattermost Webhook]
--iconUrl | URL of icon for a message | no [default: Mattermost logo]
--debug | Run program in debug mode | 
-V --version | Show program version | 
-h --help | Show program help and usage | 

### Examples
```bash
# send a simple message 
mattermost_webhook --url <webhook_url> --channel <your_channel> --message "<your_message>"

# with a debug flag
mattermost_webhook --url <webhook_url> --channel <your_channel> --message "<your_message>" --debug

# post with a special icon
mattermost_webhook --url <webhook_url> --channel <your_channel> --message "<your_message>" --iconUrl <url_to_img_icon>

# different username
mattermost_webhook --url <webhook_url> --channel <your_channel> --message "<your_message>" --username <username>
```
