# AgentSquare
The implementation of the paper "AgentSquare: Automatic LLM Agent Search in Modular Design Space"

## Setup
1. Set up OpenAI API key and store in environment variable ``OPENAI_API_KEY`` (see [here](https://help.openai.com/en/articles/5112595-best-practices-for-api-key-safety)). 

2. Install dependencies
```bash
pip install -r requirements.txt
```

3. Install ``alfworld`` following instructions [here](https://github.com/alfworld/alfworld).


## Quick Start
The following script will choose modules to solve the task of ALFworld:
```bash
cd alfworld
sh run.sh or 
python3 alfworld_run.py \
    --planning deps\
    --reasoning cot\
    --tooluse none\
    --memory dilu\
    --model gpt-3.5-turbo-0125 \
```

