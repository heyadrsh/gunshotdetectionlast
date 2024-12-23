**Title: A Multi-Firearm, Multi-Orientation Audio Dataset of Gunshots**
Authors: Ruksana Kabealo<sup>(a*)</sup>, Steven Wyatt<sup>(a)</sup>, Akshay Aravamudan<sup>(a)</sup>, Xi Zhang<sup>(a)</sup>, David N Acaron<sup>(a)</sup>, Mawaba Pascal Dao<sup>(a)</sup>,
David Elliott<sup>(a)</sup>, Anthony O. Smith<sup>(a)</sup>, Carlos E. Otero<sup>(a)</sup>, Luis D. Otero<sup>(a)</sup>, Adrian M. Peter<sup>(a)</sup>, Wesley Jones<sup>(b)</sup>,  Eric Lam<sup>(b)</sup>
Journal: Data in Brief

<sup>(a)</sup> Center for Advanced Data Analytics & Systems (CADAS) - https://cadas.fit.edu/
<sup>(b)</sup> Air Force Research Laboratory (AFRL)
<sup>(*)</sup> Corresponding author: rkabealo@my.fit.edu

This dataset is composed of audio recordings of four different types of firearms, each shot with three different firing styles. The recordings contained within this dataset have been cropped from the original recordings for ease of use. The original recordings often contained files where gunshots would be separated by several of minutes of background noise. To avoid users having to extract the relevant sections themselves, each original recording was broken up into clips using a method that ensured that every 2 seconds of audio contained at least one
gunshot. For more information on how this was performed, see the Preprocessing section of the paper.  

The data is contained in the included folder ("edge-collected-gunshot-audio"). This folder contains four sub-folders, each containing audio collected from a different firearm type. Within each of these sub-folders are files that follow the following naming convention: 

* A uuid: This identifier uniquely identifies the original audio recording 
* A channel: This is only present for audio recordings collected by multichannel microphones 
* A clip identifier: This identifier identifies a unique clip of the original audio recording

For example, the file "0a07b229-7d2b-4d2b-8f32-c94cbc7b1487_chan5_v1" is the 2nd clip from the 6th channel of the original audio recording "0a07b229-7d2b-4d2b-8f32-c94cbc7b1487".

Not all intermediate clips may exist, intermediate clips may have been deleted due to extremely poor audio quality or lack of gunshot. This also applies to files containing individual audio channels, all channels may not be present due to individual files with extremely poor audio quality being removed.  

Additionally, the mean of any audio collected by multichannel microphones is also included in the dataset for completeness. This mean was created by taking all audio channels and taking the mean of each value to create a mono audio clip. 

Finally, due to an error encountered on-site, the device "P9" (a Raspberry Pi Zero W with an attached 8-Channel Mic Array) recorded no data. This device is shown in the device setup within the paper, but audio from this device is not present within the dataset. 

The timestamps where gunshots occur within the data is denoted in the included file: "gunshot-audio-gunshot-locations-only.csv". 

More information on each individual recording, including the device/microphone used to collect it, can be found in the included file: "gunshot-audio-all-metadata.csv". 
