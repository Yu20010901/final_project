## MNIST模型訓練
* 訓練要在網頁中部署的模型
* 將訓練出來的模型轉為onnx格式

# 安裝環境
* 首先安裝我們所需的環境，"<env_name>"可自由替換
  ```bash
    conda create -n <env_name> python=3.8
  ```
* 進入我們設定好的環境
  ```bash
    conda activate <env_name>
  ```

# 安裝環境所需的套件
* 需要pytorch,PyAML,tqdm 在此資料夾中運行
  ```bash
    conda install pytorch==1.8.0 torchvision==0.9.0 cpuonly -c pytorch
  ```

  ```bash
    pip install -r requirements.txt
  ```

# 訓練data
* 它將會把每個epoch儲存到ckpts裡面
  ```bash
    python train.py
  ```

# 轉換檔案類型
* 將ckpt轉換成onnx,"<output_filename.onnx>"可自由替換想要的名稱
  ```bash
    python convert.py -c <checkpoint_filename.pt> -o <output_filename.onnx>
  ```