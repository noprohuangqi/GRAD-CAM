# GRAD-CAM
已经有了非常简洁的实现：https://github.com/jacobgil/pytorch-grad-cam  但是该实现以torchvision库中的VGG的feature和classifier属性为基础，不太适用于新的自定义的网络。

因此新写一个函数，实现给自定义加载的model增加feature和classifier的功能。

但是注意事项较多：
1.自定义网络的forward和init的顺序必须一致，比如你把fc层在init时最先定义了，那么就会报错，一定要严格按照顺序定义init。
