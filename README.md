# Huggingface Inference Api With Curl

A simple bash script that utilizes the Hugging Face API to generate images based on textual descriptions. This script sends a POST request to the Hugging Face inference API for the `facebook/bart-large-cnn` model with a given input text, and retrieves the generated image data.

![huggingface inference api with curl](https://github.com/Munya-Marinda/huggingface-inference-api-with-curl/assets/84540577/f07da5b7-4c74-4c85-9bcc-ce4efd59d70f)

## Requirements

- `curl` installed on your system
- An API token from Hugging Face

## Usage

1. **Get your Hugging Face API token:**

   If you don't have an API token, you need to create an account on [Hugging Face](https://huggingface.co/) and obtain your API token.

2. **Clone the repository:**

   ```bash
   git clone https://github.com/yourusername/fusion-image-generator.git
   cd fusion-image-generator
   ```

3. **Update the script with your API token:**

   Open the `fusion_image_generator.sh` file in your preferred text editor and replace `xxxxxxxxxxxxxxxx` with your Hugging Face API token.

   ```bash
   -H "Authorization: Bearer xxxxxxxxxxxxxxxx"
   ```

4. **Run the script:**

   ```bash
   ./fusion_image_generator.sh
   ```

## Example

Here is an example of what the script does:

```bash
curl https://api-inference.huggingface.co/models/facebook/bart-large-cnn \
    -X POST \
    -d '{"inputs": "The tower is 324 metres (1,063 ft) tall, about the same height as an 81-storey building, and the tallest structure in Paris. Its base is square, measuring 125 metres (410 ft) on each side. During its construction, the Eiffel Tower surpassed the Washington Monument to become the tallest man-made structure in the world, a title it held for 41 years until the Chrysler Building in New York City was finished in 1930. It was the first structure to reach a height of 300 metres. Due to the addition of a broadcasting aerial at the top of the tower in 1957, it is now taller than the Chrysler Building by 5.2 metres (17 ft). Excluding transmitters, the Eiffel Tower is the second tallest free-standing structure in France after the Millau Viaduct."}' \
    -H 'Content-Type: application/json' \
    -H "Authorization: Bearer xxxxxxxxxxxxxxxx"
```

## Note

- Make sure you replace the placeholder `xxxxxxxxxxxxxxxx` with your actual Hugging Face API token.
- The input text provided in the example is a description of the Eiffel Tower. You can modify this text to generate images based on different descriptions.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contributing

Contributions are welcome! Please open an issue or submit a pull request if you have any improvements or suggestions.

## Contact

For any questions or support, please contact [yourname@example.com].

---

*This README.md file was generated with the assistance of GPT-4.*
