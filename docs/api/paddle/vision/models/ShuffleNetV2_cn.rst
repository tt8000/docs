.. _cn_api_paddle_vision_models_ShuffleNetV2:

ShuffleNetV2
-------------------------------

.. py:class:: paddle.vision.models.ShuffleNetV2(num_classes=1000, scale=1.0, act="relu")

 ShuffleNetV2模型，来自论文 `"ShuffleNet V2: Practical Guidelines for Ecient CNN Architecture Design" <https://arxiv.org/pdf/1807.11164.pdf>`_。

参数
:::::::::
  - **num_classes** (int，可选) - 最后一个全连接层输出的维度。如果该值小于0，则不定义最后一个全连接层。默认值：1000。
  - **scale** (float，可选) - 模型架构，可选值[0.25, 0.33, 0.5, 1.0, 1.5, 2.0]。默认值：1.0。
  - **act** (str，可选) - 批归一化后的激活函数。默认值："relu"。

返回
:::::::::
ShuffleNetV2模型，Layer的实例。

代码示例
:::::::::

.. code-block:: python

    import paddle
    from paddle.vision.models import ShuffleNetV2
    
    
    shufflenetv2_x0_25 = ShuffleNetV2(num_classes=1000, scale=0.25, act="relu")
    x = paddle.rand([1, 3, 224, 224])
    out = shufflenetv2_x0_25(x)
    print(out.shape)
