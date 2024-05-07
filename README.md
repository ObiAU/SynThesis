# SynThesis: Synthetic Dataset Generator

## Overview
Welcome to the Repo for SynThesis, a synthetic data generator that incorporates LLMs such as Claude-3-Haiku, Claude-3-Opus and GPT-3.5-Turbo. This tool is designed to create datasets based on user specifications!

### Core Components

1. Actor (Claude-3-Haiku) - The actor model processes user queries to extract context and essential parameters such as entry count, labeling, class distinctions etc. It then generates a preliminary dataset in JSON format. It incorporates RAG using DSPy for improved task-specific natural language understanding.
   
2. Curator (Function) - The curator serves to post-process this dataset; removing noise and formatting inconsistencies, returning a curated dataset in DataFrame format.
   
3. Critique (GPT-3.5-Turbo) - The critique (or critic) model takes in as input, a tuple of (context, prompt, response dataset) and generates a critique. This critique aims to assess the respoonse dataset against the user's initial query based on the given context. Should the response dataset fail the critique's evaluation, a regeneration process is triggered.

## Notes

SynThesis is still a work in progress, and is undergoing rigorous testing and refinement processes.

I'm looking to integrate a React frontend and release fully by summer!

Stay tuned for updates!
