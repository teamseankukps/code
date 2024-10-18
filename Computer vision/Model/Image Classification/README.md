
# Transfer Learning ด้วย ResNet-50 ใน PyTorch

โค้ดนี้เป็นใช้การเรียนรู้ถ่ายโอน (Transfer Learning) ด้วยสถาปัตยกรรม ResNet-50 ใน PyTorch โดยจะแสดงวิธีการปรับแต่งโมเดล ResNet-50 ที่ได้รับการฝึกฝนมาแล้ว

## ข้อกำหนดเบื้องต้น

เพื่อใช้งานโน้ตบุ๊คนี้ คุณจะต้องติดตั้งไลบรารีต่อไปนี้:

- Python 3.x
- PyTorch
- Torchvision
- Numpy
- Matplotlib
- Pillow (PIL)
  
คุณสามารถติดตั้งไลบรารีเหล่านี้ด้วย pip:

```bash
pip install torch torchvision numpy matplotlib Pillow
```



**ชุดข้อมูล**:

   โน้ตบุ๊คนี้ได้รับการตั้งค่าให้ทำงานร่วมกับชุดข้อมูลของคุณเอง โดยให้คุณจัดชุดข้อมูลตามโครงสร้างดังนี้:
   
   ```
   data/
   ├── train/
   │   ├── class1/
   │   ├── class2/
   └── val/
       ├── class1/
       ├── class2/
   ```

   ให้แทนที่ `class1`, `class2` ด้วยชื่อคลาสที่คุณต้องการ โน้ตบุ๊คนี้ใช้คลาส `ImageFolder` ของ PyTorch เพื่อโหลดข้อมูล

## ภาพรวมของการเรียนรู้ถ่ายโอน

ในโน้ตบุ๊คนี้ เราใช้การเรียนรู้ถ่ายโอนเพื่อปรับแต่งโมเดล ResNet-50 ที่ได้รับการฝึกฝนมาก่อนจากไลบรารี `torchvision` โดยมีขั้นตอนดังนี้:

1. โหลดโมเดล ResNet-50 ที่ได้รับการฝึกฝนมาก่อน
2. Freeze ชั้นเริ่มต้นเพื่อรักษาคุณลักษณะที่เรียนรู้มาแล้ว
3. ปรับแต่งชั้น Fully Connected สุดท้ายให้ตรงกับจำนวนคลาสในชุดข้อมูล
4. ฝึกฝนโมเดลกับชุดข้อมูลใหม่เป็นจำนวน epochs

## ผลลัพธ์

โน้ตบุ๊คจะแสดงวิธีการประเมินผลโมเดลที่ได้รับการปรับแต่ง และแสดงภาพกราฟการสูญเสีย (Loss) และความแม่นยำ (Accuracy) บนชุดข้อมูลการตรวจสอบ

## อ้างอิง

- [เอกสาร PyTorch](https://pytorch.org/docs/stable/index.html)
- [โมเดล Torchvision](https://pytorch.org/vision/stable/models.html)



# Transfer Learning with ResNet-50 in PyTorch

This repository contains a tutorial for performing transfer learning using the ResNet-50 architecture in PyTorch. The notebook demonstrates how to fine-tune a pre-trained ResNet-50 model on a custom dataset.

## Requirements

To run this notebook, you will need the following dependencies:

- Python 3.x
- PyTorch
- Torchvision
- Numpy
- Matplotlib
- Pillow (PIL)
  
You can install the necessary libraries using pip:

```bash
pip install torch torchvision numpy matplotlib Pillow
```

## How to Use

**Dataset**:

   The notebook is set up to work with a custom dataset. You need to organize your dataset in the following directory structure:
   
   ```
   data/
   ├── train/
   │   ├── class1/
   │   ├── class2/
   └── val/
       ├── class1/
       ├── class2/
   ```

   Replace `class1`, `class2`, etc., with your actual class names. The notebook uses PyTorch's `ImageFolder` class to load the data.

## Transfer Learning Overview

In this notebook, we use transfer learning to leverage a pre-trained ResNet-50 model from the `torchvision` library. We fine-tune the model on a custom dataset by following these steps:

1. Load a pre-trained ResNet-50 model.
2. Freeze the initial layers to retain pre-learned features.
3. Modify the final fully connected layer to match the number of classes in the custom dataset.
4. Train the model on the new dataset for a few epochs.

## Results

The notebook shows how to evaluate the fine-tuned model and visualize the performance on the validation dataset using plots for loss and accuracy.

## References

- [PyTorch Documentation](https://pytorch.org/docs/stable/index.html)
- [Torchvision Models](https://pytorch.org/vision/stable/models.html)

