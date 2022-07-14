## Cloudinary

(Cyqur is not affiliated to Cloudinary)

If your device is compromised, the use of cloud service providers can help mitigate against Bad Actors having access to your fragments. There are many cloud services that can be used to save encrypted fragments to. Few have client only APIs (this means you can upload to a cloud without using a server) but one we like is Cloudinary.

https://cloudinary.com/

To save fragments to the cloud, open a free account at Cloudinary. Cloudinary allows you to create your own cloud CDN (publicly available files) and allows you to upload images and videos. For Cyqur, data files like text files can also be uploaded via the Browser.

#### How do I do this?

![Cloudinary](/images/cloudinary.png)

Go to Cloudinary settings (Cog at the top), the "upload" tab and then scroll to the Upload Presets. Here you can create a simple api key for easy uploads. Click Add Upload Preset and enter the Upload Preset Name (cloud name), the folder the files will be sent to and the preset api token which is the Preset Name. Make sure Signing Mode = Unsigned.

Enter the details into Cyqur Settings. Test out by adding a random secret. You should find in the Vault under Packets, clouded packets which have been uploaded to Cloudinary.