# 🪛 AutoResolver
Troubleshoot programmatic issues

🏗️ WIP



Arguments used to fine-tune LongCoder for cross-language code clone detection.


output=longcoder_test_dir 
lr=5e-5
batch_size=16
source_length=512
data_dir=./
output_dir=model/$output
train_file=./dataset/pair_train.jsonl
dev_file=./dataset/pair_valid.jsonl
test_file=./dataset/pair_test.jsonl
epochs=3
pretrained_model=microsoft/longcoder-base

python run_con.py --do_train --do_eval --do_test --model_type roberta --model_name_or_path $pretrained_model --train_filename $train_file --dev_filename $dev_file --output_dir $output_dir --max_source_length $source_length --train_batch_size $batch_size --eval_batch_size $batch_size --learning_rate $lr --num_train_epochs $epochs --test_filename $test_file
