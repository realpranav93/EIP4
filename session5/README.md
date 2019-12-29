- VGG base code accuracy for multiple labels

    `gender - val: 0.4378, train_acc: 0.4378
    image_quality- val: 55.34, train_acc: 0.5530
    age - val: 0.3993, train_acc: 0.3991
    weight - val: 0.6368, train_acc: 0.6366
    bag: val: 0.5628, train_acc: 0.5628
    footwear- val: 0.4440, train_acc: 0.4438
    pose- val: 0.6173, train_acc: 0.6171
    emotion- val: 0.7138,, train_acc: 0.7135
    `
- Its an Resnet50 Implementation. 
- Following strategies has been used 
  - Cutout 
  - Keras RESNet Preprocess 
  - Image Standardization 
  - One Cycle LR 
### Best Model Performance 
`
loss: 7.9069 - gender_output_loss: 0.6893 - image_quality_output_loss: 0.9889 - age_output_loss: 1.4333 - weight_output_loss: 0.9867 - bag_output_loss: 0.9203 - footwear_output_loss: 1.0454 - pose_output_loss: 0.9313 - emotion_output_loss: 0.9116 - gender_output_acc: 0.5568 - image_quality_output_acc: 0.5513 - age_output_acc: 0.3975 - weight_output_acc: 0.6349 - bag_output_acc: 0.5648 - footwear_output_acc: 0.4274 - pose_output_acc: 0.6173 - emotion_output_acc: 0.7107 - val_loss: 7.8284 - val_gender_output_loss: 0.6866 - val_image_quality_output_loss: 0.9678 - val_age_output_loss: 1.4208 - val_weight_output_loss: 0.9849 - val_bag_output_loss: 0.9240 - val_footwear_output_loss: 1.0392 - val_pose_output_loss: 0.9202 - val_emotion_output_loss: 0.8849 - val_gender_output_acc: 0.5585 - val_image_quality_output_acc: 0.5645 - val_age_output_acc: 0.4078 - val_weight_output_acc: 0.6381 - val_bag_output_acc: 0.5559 - val_footwear_output_acc: 0.4536 - val_pose_output_acc: 0.6205 - val_emotion_output_acc: 0.7218`
` 
