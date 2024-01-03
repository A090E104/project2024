## Getting Started

This is an example of how you may give instructions on setting up your project locally.
To get a local copy up and running follow these simple example steps.

### Prerequisites

- VLC MUST BE DOWNLOADED ON YOUR COMPUTER

In order to install the prerequisites you will need to do:  
* pip
  ```sh
  pip install -r requirements.txt
  ```

### Installation

1. Get a OpenAI API Key at [OpenAPIKey](https://openai.com/api/)
2. Get a Twitch API Token at [TwitchToken](https://twitchtokengenerator.com/)
3. Create a Google Cloud Project with TTS Service enabled and download JSON credentials file. [GoogleCloud](https://cloud.google.com/)
4. Clone the repo
   ```sh
   git clone https://github.com/github_username/repo_name.git
   ```
5. Add the Google Cloud JSON file into the project folder. 
6. Enter API Keys in creds.py:
  ```python
  # You're Twitch Token 
  TWITCH_TOKEN = ""
  # Your TWITCH Channel Name
  TWITCH_CHANNEL = ""
  # Your OpenAI API Key
  OPENAI_API_KEY = ""
  # Your Google Cloud JSON Path
  GOOGLE_JSON_PATH = ""
  ```
10. Download VTube Studio and use VBAudio Cable to route audio coming from the program. 
11. Add the following script into OBS [CaptionsScript](https://gist.github.com/kkartaltepe/861b02882056b464bfc3e0b329f2f174)
12. Create a new text source for captions, and set it to read from a file, select the `output.txt` file from the project folder.
13. In the script options put the name of you're text source.
14. Set the script in transform options to scale to inner bounds, and adjust the size of the captions.
15. Enjoy! For more details watch the attatched video.
16. IN ORDER TO CHANGE THE VOICE OF YOU'RE VTUBER you will need to change the following parameters in main.py
    Here is a list of [supported voices](https://cloud.google.com/text-to-speech/docs/voices)
    
  ```python
    voice = texttospeech.VoiceSelectionParams(
        language_code="en-GB",
        name= "en-GB-Wavenet-B",
        ssml_gender=texttospeech.SsmlVoiceGender.MALE,
    )
   ```





<!-- USAGE EXAMPLES -->
## Usage

Use this space to show useful examples of how a project can be used. Additional screenshots, code examples and demos work well in this space. You may also link to more resources.

_For more examples, please refer to the [Documentation](https://example.com)_

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- ROADMAP -->
## Roadmap

- [ ] Feature 1
- [ ] Feature 2
- [ ] Feature 3
    - [ ] Nested Feature

See the [open issues](https://github.com/github_username/repo_name/issues) for a full list of proposed features (and known issues).

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- CONTRIBUTING -->
## Contributing

Contributions are what make the open source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

If you have a suggestion that would make this better, please fork the repo and create a pull request. You can also simply open an issue with the tag "enhancement".
Don't forget to give the project a star! Thanks again!

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request
