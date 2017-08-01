# mtcnn-align-crop
It is a python code of mtcnn with alignment and crop added

source code and models are from: https://github.com/DuinoDu/mtcnn

add align and crop:
    using similarity transform in skimage

example:

    A = FaceAlignmentor(caffe_model_path)
    
    #return the aligned and cropped image
    wrapimage = A.run(image)
    
    #just return box and landmarks
    boxes, points = A.detectface(image)
    
    #align and crop
    warpimage = A.alignment(image,points,ref_points='your reference points',ref_shape = 'your reference image shape')
