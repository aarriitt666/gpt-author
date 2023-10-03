# gpt-author

This project utilizes GPT-3.5 Turbo to generate original fantasy novels. By accepting an initial prompt and a specified number of chapters from users, the AI crafts an entire novel and outputs it as an EPUB file, ready for e-book readers.

A 15-chapter novel can be generated in mere minutes.

**Examples** of the novels produced are available in this repository. To read one, download its file and view it on an e-book viewer, or transfer it to your e-reader.

## How It Works

1. **Brainstorming**: The AI generates a list of potential plots based on user input.
2. **Plot Selection**: Engaging plots are chosen and refined, and a suitable title is deduced.
3. **Storyline Creation**: A detailed storyline is formed, incorporating the specified number of chapters.
4. **Chapter Writing**: Each chapter is meticulously crafted, adhering to the storyline and ensuring consistency with preceding chapters.
5. **EPUB Compilation**: The novel is compiled into an EPUB format.

### Tiktoken Usage

To manage API usage and avoid unexpected costs, `tiktoken` is employed to count the tokens in a text string without making an API call. The `write_chapter` function dynamically manages the content sent to the API, ensuring it adheres to token limitations by adjusting the content where necessary. This ensures efficient usage of the OpenAI API and aids in maintaining control over the generation process.

## Prerequisites

- Ensure Visual Studio Code is installed. The latest version is recommended.
- Install additional extensions as required (e.g., Jupyter extension).
- Create a virtual environment:
    ```bash
    python -m venv env
    ```
- Store environment variables in a `.env` file in the main project directory. `.env` and `env` are ignored by Git, as specified in the `.gitignore` file.

## Installation & Usage

1. Clone the repository and navigate to the project directory.
2. Activate the virtual environment:
    ```bash
    source env/bin/activate
    ```
3. Install the necessary packages from `requirements.txt`:
    ```bash
    pip install -r requirements.txt
    ```
4. Open the project in Visual Studio Code and run the program.
5. Adjust the `MAX_TOKEN` value in the code to manage the intensity of the API calls.

### Example

```python
prompt = "A story reminiscent of Percy Jackson or Harry Potter but with a unique plot set in the present day. Incorporate technology elements."
num_chapters = 20
writing_style = "Clear and easily understood, akin to a young adult novel. Highly descriptive and occasionally verbose."
novel, title, chapters, chapter_titles = write_fantasy_novel(prompt, num_chapters, writing_style)
Contributions
Contributions, issues, and feature requests are always welcome!

Potential Enhancements
Improve the initial chapter for setting the novel's tone.
Refine prompts for optimized results.
Augment the process with additional checks and generations.
Expand beyond the fantasy genre.
Address issues of chapter truncation.
License
This project is MIT licensed.

Contact
Matt Shumer - @mattshumer_

Project Link

Feel free to modify or expand upon this as needed!