ECG Data Augmentation with Conditional (by heart rate) CNN GAN:


data:

https://www.physionet.org/content/challenge-2017/1.0.0/

please download training2017.zip

please look at ecgGAN.ipynb

training:

![alt text](https://github.com/abbasloo/dnnHealth/blob/master/AF/GAN_Loss_per_Epoch_final.png)

synthetic ECG (AF heart condition)

![alt text](https://github.com/abbasloo/dnnHealth/blob/master/AF/result.png)


load the model (gan.h5 and gan.json):

    print('loaded model from disk')
    json_file = open('gan.json', 'r')
    loaded_model_json = json_file.read()
    json_file.close()
    loaded_model = model_from_json(loaded_model_json)
    loaded_model.load_weights('gan.h5')
