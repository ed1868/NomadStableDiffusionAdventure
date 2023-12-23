# Stable Diffusion Adventure Story Game

## Overview
This project is a Flask-based web application that creates an interactive choose-your-own-adventure (CYOA) story game using OpenAI's GPT models and Stable Diffusion for image generation. Users make choices that influence the story's direction, and the app generates corresponding narrative text and images.

## Features
- Interactive storytelling with choices affecting the story's progression.
- Dynamic image generation using Stable Diffusion based on story context.
- Customizable story prompts and choice-driven narrative flow.
- Robust error handling with retries for API calls.
- Efficient and detailed logging for debugging and monitoring.

## Requirements
- Python 3.x
- Flask web framework
- OpenAI API key for GPT model access
- Stable Diffusion API key for image generation
- Dotenv for environment variable management

## Installation
1. Clone the repository to your local machine.
2. Install the required packages:
   ```bash
   pip install flask openai requests python-dotenv


## How It Works
-The Flask app serves a web page where users can start their adventure.
-Users' choices are sent to the backend, which uses OpenAI's GPT model to generate   the next part of the story.
-The app then uses either DALL-E or Stable Diffusion to generate images based on the narrative.
-The story progresses with each user choice, creating a unique adventure.

## Error Handling
- Handles API errors such as APIConnectionError, APIError, RateLimitError, and ServiceUnavailableError.
- Uses the tenacity library for retrying failed API requests.

## Configuration
-Modify the system_directive for different story themes or structures.
-Adjust the parameters for image generation to change the style or resolution.

## Flask Endpoints
-POST /cyoa: Endpoint to generate the next part of the story and the corresponding image.
-GET /: Main page of the web application.