## 🌎 Setup
1. Set up OpenAI API key and store in environment.
```bash
export OPENAI_API_KEY=<YOUR KEY HERE>
```
2. Install dependencies
```bash
git clone https://github.com/tsinghua-fib-lab/AgentSquare.git
conda create -n agentsquare python=3.9.12
conda activate agentsquare
cd AgentSquare
pip install -r requirements.txt
```

## 🚀 Quick Start: Demo with ALFWorld
An exemplar script combining different agent modules to solve the task of ALFworld:
```bash
export ALFWORLD_DATA=<Your path>/AgentSquare/tasks/alfworld
cd tasks/alfworld
sh run.sh or 
python3 alfworld_run.py \
    --planning deps\
    --reasoning cot\
    --tooluse none\
    --memory dilu\
    --model gpt-3.5-turbo-0125 \
```

## 🔎 Run Other Tasks
### Install dependencies
```bash
cd tasks
pip install -r requirements.txt
```

<details>
  
<summary> Webshop </summary>
  
Install `webshop` environment following instructions [here](https://github.com/princeton-nlp/WebShop) and launch the `WebShop` webpage.
```bash
cd tasks/webshop
sh run.sh
```
</details>

<details>

<summary> M3Tooleval </summary>

```bash
cd tasks/m3tooleval
sh run.sh
```
</details>

<details>

<summary> Sciworld </summary>

Install `Sciworld` environment following instructions [here](https://github.com/hkust-nlp/AgentBoard) .
```bash
cd tasks/sciworld/agentboard
python3 eval_main_sci.py \
    --cfg-path ../eval_configs/main_results_all_tasks.yaml     --tasks scienceworld     --wandb     --log_path ../results/gpt-4o-2024-08-06    --project_name evaluate-gpt-4o-2024-08-06     --baseline_dir ../data/baseline_results \
    --model gpt-4o-2024-08-06 \
    --planning none \
    --reasoning cot \
    --tooluse none \
    --memory none \
```
</details>



