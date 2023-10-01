gpt-author
This project is designed to leverage the capabilities of GPT-3.5 Turbo to generate an original fantasy novel. Users can input an initial prompt and specify the number of chapters desired. The AI then crafts an entire novel, outputting it as an EPUB file suitable for e-book readers.

A 15-chapter novel can be generated in just a few minutes.

Examples of the novels produced are available in this repository. To read one, download its file and view it on fviewer, or transfer it to your e-reader.

How It Works
The AI is prompted to brainstorm a list of potential plots based on the user's input. It then selects an engaging plot, refines it, and deduces a suitable title. Following this, it forms a detailed storyline with the specified number of chapters. Each chapter is meticulously crafted by the AI, adhering to the storyline and ensuring consistency with prior chapters. The novel is then compiled into an EPUB format.

Prerequisites
Ensure you have Visual Studio Code installed. The latest version is recommended.
If required, install additional extensions such as the Jupyter extension when prompted.
Create a virtual environment:
bash
Copy code
python -m venv env
Store environment variables in a .env file in the main project directory.
Remember, .env and env will be ignored by Git, as specified in the .gitignore file.
Installation & Usage
To set up and run the project:

Clone the repository and navigate to the project directory.
Activate the virtual environment:
bash
Copy code
source env/bin/activate
Install the necessary packages from requirements.txt:
bash
Copy code
pip install -r requirements.txt
Open the project in Visual Studio Code and run the program.
In the code, you can fine-tune the MAX_TOKEN value to adjust the intensity of the API calls.

Example of generating a novel:

python
Copy code
prompt = "A story reminiscent of Percy Jackson or Harry Potter but with a unique plot set in the present day. Incorporate technology elements."
num_chapters = 20
writing_style = "Clear and easily understood, akin to a young adult novel. Highly descriptive and occasionally verbose."
novel, title, chapters, chapter_titles = write_fantasy_novel(prompt, num_chapters, writing_style)
Contributions
Contributions, issues, and feature requests are always welcome!

Potential areas of enhancement include:

Bettering the initial chapter, as it sets the tone for the entire novel.
Refining prompts for improved results.
Augmenting the process with additional checks and generations.
Expanding beyond the fantasy genre to include others.
Addressing issues where some chapters might truncate prematurely.
License
This project is MIT licensed.

Contact
Matt Shumer - @mattshumer_

Project Link: https://github.com/mshumer/gpt-author/

Feel free to modify or expand upon this as needed!