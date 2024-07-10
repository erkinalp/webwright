<div align="center">
  <img src="https://raw.githubusercontent.com/MittaAI/webwright/main/logo.png" width="200" alt="Webwright Logo">
</div>

# Webwright: The Ghost in Your Shell 👻💻

Webwright is an AI-driven terminal shell designed to streamline the process of building, deploying, and managing websites.

## 🔑 API Requirements

Webwright requires an API token from either OpenAI or Anthropic to function. You can obtain these tokens from:

- [OpenAI API Keys](https://platform.openai.com/account/api-keys)
- [Anthropic API Keys](https://www.anthropic.com/) or [Anthropic Console](https://console.anthropic.com/)

Please ensure you have at least one of these API keys before proceeding with the installation.

## 🚀 Key Features

- 🌐 **AI-Powered Web Development**: Craft and launch websites with intelligent, AI-driven tools.
- 💻 **Smart Code Generation**: Let AI write code for you, boosting productivity and innovation.
- 📊 **Effortless Project Management**: Seamlessly create and oversee projects with AI assistance.
- 🔄 **Integrated Version Control**: Push your code to GitHub without leaving the terminal.
- 🐳 **Docker at Your Fingertips**: Effortlessly spin up and manage Docker containers.
- 🌐 **Browser Magic**: Automate web tasks and open URLs (or other apps) with simple commands.
- 🔧 **Infinitely Extensible**: Customize your shell with bespoke commands and scripts.

## 🛠️ Installation
Webwright requires Anaconda and Docker to be configured on your system.

1. **Install Webwright**
   ```bash
   pip install webwright
   ```

2. **Set up dependencies**
   Webwright requires Anaconda and Docker to be configured on your system.
  - [Anaconda/Miniconda Installation](https://docs.anaconda.com/miniconda/miniconda-install/)
  - [Docker Desktop Installation](https://www.docker.com/products/docker-desktop/)

3. **Create and activate a Conda environment**
   ```bash
   conda create -n webwright python=3.10
   conda activate webwright
   ```

4. **Install Git**
   Ensure Git is installed in your Conda environment:
   ```bash
   conda install git
   ```

5. **Start Webwright**
   ```bash
   webwright
   ```

## 🔄 System Flow Diagram

```mermaid
graph TD
    A[User] -->|Enters command| B[Webwright Shell]
    B -->|Processes command| C{Function or AI?}
    C -->|Function| D[Execute Local Function]
    C -->|AI Request| E{OpenAI or Anthropic?}
    E -->|OpenAI| F[OpenAI API]
    E -->|Anthropic| G[Anthropic API]
    F -->|Response| H[Process AI Response]
    G -->|Response| H
    H -->|Generate Code/App| I[Code/Application Output]
    H -->|Execute Function| J[Function Execution]
    J -->|Result| K[Process Function Result]
    K -->|Update Context| B
    I -->|Display to User| A
    D -->|Result| K
    B -->|Store/Retrieve Data| L[(Vector Store)]
    B -->|Store/Retrieve Data| M[(Set Store)]
```

This diagram illustrates the flow of Webwright's functionality, showing how user commands are processed, how AI requests are handled, and how data is stored and retrieved.

## Getting Started

Once installed, you can start using Webwright by simply typing `webwright` in your terminal. Here's a quick overview of some commands:

### Open URLs in Your Browser

```bash
rare-parrot@openai ~\code\mitta\webwright $ open hackernews
```

### Create a New Project

```bash
rare-parrot@openai ~\code\mitta\webwright $ create project my-project
```

### Generate Code

```bash
rare-parrot@openai ~\code\mitta\webwright $ generate code --type python --output my_script.py
```

### Commit to GitHub

```bash
rare-parrot@openai ~\code\mitta\webwright $ git commit -m "Initial commit"
```

### Start Docker Containers

```bash
rare-parrot@openai ~\code\mitta\webwright $ docker start my-container
```

### AI-Powered Code Generation

Webwright can generate complex code snippets using AI. For example, to generate an ASCII fractal:

```bash
rare-parrot@openai ~\code\mitta\webwright $ generate fractal --size 20
```

### Example: Fractal Generation

Here's an example of a Python code snippet generated by Webwright to create a mandlebrot fractal:

```python
import matplotlib.pyplot as plt
import numpy as np

# Function to compute the Mandelbrot set
def mandelbrot(c, max_iter):
    z = c
    for n in range(max_iter):
        if abs(z) > 2:
            return n
        z = z*z + c
    return max_iter

# Generate the fractal
def generate_fractal(size):
    # Determine the plot boundaries
    x_min, x_max = -2.5, 1.5
    y_min, y_max = -2.0, 2.0

    width, height = (size*100, size*100)  # Increase resolution by multiplying size by 100
    x, y = np.linspace(x_min, x_max, width), np.linspace(y_min, y_max, height)
    fractal = np.zeros((width, height))

    for i in range(width):
        for j in range(height):
            fractal[i, j] = mandelbrot(complex(x[i], y[j]), 256)

    plt.imshow(fractal.T, extent=[x_min, x_max, y_min, y_max], cmap='hot')
    plt.colorbar()
    plt.title("Mandelbrot Fractal")
    plt.show()

# Generate a fractal of the given size
generate_fractal(20)

```

### Output

<img src="https://raw.githubusercontent.com/MittaAI/webwright/main/fractal.png" alt="Fractal">

## Documentation

For detailed usage instructions and examples, visit the [Webwright Documentation](https://mitta.ai/docs/webwright).

## Contributing

Webwright is an open-source project. We welcome contributions!

## Community and Support

Join our community on [Slack](https://join.slack.com/t/mittaai/shared_invite/zt-2azbcv29i-CL74lmOksgvN54jhvmVWeA) for support, discussions, and to share your ideas and feedback.

## License

Webwright is open-source software licensed under the [MIT License](https://opensource.org/license/mit).

---

With Webwright, harness the power of AI to enhance your development workflow and make building and managing websites easier and more efficient than ever before. Try it today and experience the future of web development!