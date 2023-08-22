# Visual and Semantic Guided Scene Text Retrieval
The project is based on the source code of maskrcnn-benchmark (https://github.com/facebookresearch/maskrcnn-benchmark) and TDSL (https://github.com/lanfeng4659/STR-TDSL.).
![framework](https://github.com/lhl2xju/VSSTR/assets/113302250/a963e404-153b-43bb-b349-175787465daf)



These were inspired by 
@inproceedings{VSTR,
  title={Visual Matching is Enough for Scene Text Retrieval},
  author={Wen, Lilong and Wang, Yingrong and Zhang, Dongxiang and Chen, Gang},
  booktitle={Proceedings of the Sixteenth ACM International Conference on Web Search and Data Mining},
  pages={447--455},
  year={2023}
} and 
@inproceedings{TDSL,
  title={Scene text retrieval via joint text detection and similarity learning},
  author={Wang, Hao and Bai, Xiang and Yang, Mingkun and Zhu, Shenggao and Wang, Jing and Liu, Wenyu},
  booktitle={Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition},
  pages={4558--4567},
  year={2021}
}
. Many thanks for their help!

Next I will talk about how to set up the environment, test, train and visualize.

1. Build the environment
   1) My cuda version is 10.0.0 and I don't know if other versions will be compatible.
   2) conda create -n xxx python=3.7.0
   3) conda activate xxx
   4) pip install -r requirement.txt
   5) unzip 6af....zip (apex)
   6) cd apex...
   7) python setup.py install
   8) cd vsstr
   9) python setup.py bulid develop
2. For Testing (It's a must before training.)
   1) Download the trained model.
   2) cd tools
   3) python test_net.py --ckpt **.pth --congif-file **.yaml --gpu 0 --dataset s(svt)/c(coco-text)/t(total-text)/3(iiit-str)/h(csvtr)/i(icdar-mlt)(retrieval multilingual)
   4) A *.json file will be generated in the RR_*dataset folder in the current directory, which is necessary for the visualization.
3. For Training
   

   
