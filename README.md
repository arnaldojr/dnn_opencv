# Módulo DNN OpenCV

DNN é o módulo de **Deep Neural Network** da OpenCV que está disponivel a partir da versão 3.3 na instalação padrão da OpenCV. 

Trata-se de um módulo para realizar a **infêrncias** através de redes neurais pré-treinadas de imagens e videos. ***Tenha em mente que não é possivel realizar treinamento  usando esse módulo***, se o objetivo é realizar treinamento de uma rede neural, use frameworks como TensorFlow ou Pytorch.
 
Tem suporte para os principais frameworks:
    
  - Caffe
  - TensorFlow
  - Torch
  - Darknet
  - Formato ONNX

Com relação as funcionalidades, permite trabalhar com:

- Classificação de Imagens
- Detecção de Objetos
- Segmentação de Imagem
- Detecção e reconhecimento de Texto
- Pose e Depth estimation
- entre outros...

A tabela abaixo exibe alguns exemplos possiveis, vale a pena explorar outras combinações de arquiteturas pre-treinadas. Uma lista mais completa é encontrada na [wiki da OpenCV](https://github.com/opencv/opencv/wiki/Deep-Learning-in-OpenCV). 

Classificação de Imagens|Detecção de Objetos|Segmentação de Imagem|Detecção e reconhecimento de Texto|Human Pose estimation|Detecção de face e pessoas
:---:|:---:|:---:|:---:|:---:|:---:
Alexnet|MobileNet| SSD|	DeepLab|	Easy OCR	|Open Pose|	Open Face
GoogLeNet|	VGG SSD|	UNet|	CRNN|	Alpha Pose|	Torchreid
VGG	|Faster R-CNN	|FCN| | |Mobile FaceNet
ResNet|	EfficientDet|	|	| |		OpenCVFaceDetector
SqueezeNet	|				
DenseNet		|			
ShuffleNet	|				
EfficientNet|					

[fonte da tabela](https://learnopencv.com/deep-learning-with-opencvs-dnn-module-a-definitive-guide/)


## Exemplos módulo DNN OpenCV

 Para rodar o módulo DNN vamos seguir um passo-a-passo, uma "receita de bolo":

1. Carregar o arquivo com o nome das classes da rede pre-treinada, esse arquivo deve ser baixado previamente do repositório da rede.
2. Carregar o arquivo com os pesos da rede pre-treinada, esse arquivo tambem deve ser baixado previamente do repositório da rede.
3. Carregar a imagem e preparar no formato correto para passar na entrada rede. 
4. Realizar a progragação na rede e obter a saida da rede.

Alguns notebooks de exemplo:

- [MaskRCNN.ipynb](MaskRCNN.ipynb)
- [Yolo.ipynb](Yolo.ipynb)
- [ssd_tensorflw.ipynb](ssd_tensorflw.ipynb)
- [ImageNet_DenseNet_Caffemodel.ipynb](ImageNet_DenseNet_Caffemodel.ipynb)

O download dos modelos pre-treinados da rede podems ser baixados nos links:

- [frozen_inference_graph_V1.pb](https://drive.google.com/open?id=1sDn1guYV6oj-AeYuC-riGRh4kv9XBTMz)

- [frozen_inference_graph_V2.pb](https://drive.google.com/open?id=1EU6tVcDNLNwv-pbJUXL7wYUchFHxr5fw )

- [DenseNet-Caffe](https://github.com/shicai/DenseNet-Caffe)

- [Yolo - Darknet](https://pjreddie.com/darknet/yolo/)
