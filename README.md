
Download https://storage.googleapis.com/bert_models/2018_10_18/uncased_L-12_H-768_A-12.zip and rename the folder to chinese_L-12_H-768_A-12 and put it inn this directory<br>
```shell
cd 
mkdir tmp
cd tmp
mkdir 
```
In terminal, excute
```shell
export BERT_BASE_DIR=./chinese_L-12_H-768_A-12
export MY_DATASET=./data
```
then,
```shell
python ./run_classifier_multi.py \
  --task_name=kerry \
  --do_train=true \
  --do_eval=true \
  --do_predict=true \
  --data_dir=$MY_DATASET \
  --vocab_file=$BERT_BASE_DIR/vocab.txt \
  --bert_config_file=$BERT_BASE_DIR/bert_config.json \
  --init_checkpoint=$BERT_BASE_DIR/bert_model.ckpt \
  --max_seq_length=128 \
  --train_batch_size=32 \
  --learning_rate=5e-5 \
  --num_train_epochs=2.0 \
  --output_dir=./tmp/Ecommerce_output
```
