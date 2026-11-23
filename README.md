# mlk-nts-ai

Get-WinEvent -FilterHashtable @{LogName='Application'; ProviderName='Application Error'} -MaxEvents 2 | Format-List TimeCreated, Message

(Get-Item C:\Windows\System32\msvcp140.dll).VersionInfo.FileVersion

https://aka.ms/vs/17/release/vc_redist.x64.exe

https://drive.google.com/file/d/11wrk5Tyq6NFVzTELbbawUcNDzxbnIV-X/view

cd C:\microinfer
curl.exe -L -o models\LFM3-1.7B-Q4_K_M.gguf https://huggingface.co/LiquidAI/LFM3-1.7B-GGUF/resolve/main/LFM3-1.7B-Q4_K_M.gguf
dir models

C:\llama\llama-server.exe -m models\LFM3-1.7B-Q4_K_M.gguf --host 127.0.0.1 --port 8080 -np 2 -c 8192 -t 2 --jinja --reasoning-format deepseek --reasoning-budget 0 --metrics

cd C:\microinfer
python -m mi_eval bench-batch --base-url http://127.0.0.1:8080/v1 --ns 1,2 --timeout 900

cd C:\microinfer
python -m mi_eval run --task sql --mode free,cascade --base-url http://127.0.0.1:8080/v1 --profile lfm3-1.7b --n 2 --limit 5 --timeout 900
