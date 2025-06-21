# Customer Service Agents Demo

[![MIT License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
![NextJS](https://img.shields.io/badge/Built_with-NextJS-blue)
![OpenAI API](https://img.shields.io/badge/Powered_by-OpenAI_API-orange)

This repository contains a demo of a Customer Service Agent interface built on top of the [OpenAI Agents SDK](https://openai.github.io/openai-agents-python/).
It is composed of two parts:

1. A python backend that handles the agent orchestration logic, implementing the Agents SDK [customer service example](https://github.com/openai/openai-agents-python/tree/main/examples/customer_service)

2. A Next.js UI allowing the visualization of the agent orchestration process and providing a chat interface.

![Demo Screenshot](screenshot.jpg)

## How to use

### Setting your OpenAI API key

You can set your OpenAI API key in your environment variables by running the following command in your terminal:

```bash
export OPENAI_API_KEY=your_api_key
```

You can also follow [these instructions](https://platform.openai.com/docs/libraries#create-and-export-an-api-key) to set your OpenAI key at a global level.

Alternatively, you can set the `OPENAI_API_KEY` environment variable in an `.env` file at the root of the `python-backend` folder. You will need to install the `python-dotenv` package to load the environment variables from the `.env` file.

### Install dependencies

Install the dependencies for the backend by running the following commands:

```bash
cd python-backend
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

For the UI, you can run:

```bash
cd ui
npm install
```

### Run the app

You can either run the backend independently if you want to use a separate UI, or run both the UI and backend at the same time.

#### Run the backend only

```bash
cd python-backend
python main.py
```

This will start the FastAPI backend on `http://localhost:8000`.

#### Run both the backend and UI

```bash
cd python-backend
python main.py &  # Run backend in background
cd ../ui
npm run dev  # Run UI in foreground
```

The UI will be available at `http://localhost:3000`.

### Usage

1. Open your browser and navigate to `http://localhost:3000`.
2. You'll see the Customer Service Agent interface.
3. Start a conversation by typing a message in the chat box.
4. Watch the agent orchestration process in real-time as different agents handle your request.

## Project Structure

- `python-backend/` - FastAPI backend with agent orchestration
- `ui/` - Next.js frontend application
- `screenshot.jpg` - Demo screenshot

## Features

- Real-time chat interface
- Agent orchestration visualization
- Customer service workflow demonstration
- Built with OpenAI Agents SDK

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.