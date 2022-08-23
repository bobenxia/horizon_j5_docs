.. Copyright (c) 2020 Horizon Robotics.All Rights Reserved.
   The material in this file is confidential and contains trade secrets
   of Horizon Robotics Inc. This is proprietary information owned by
   Horizon Robotics Inc. No part of this work may be disclosed,
   reproduced, copied, transmitted, or used in any way for any purpose,
   without the express written permission of Horizon Robotics Inc.

.. Horizon J5 AI Toolchain User Guide documentation master file, created by
   sphinx-quickstart on Mon Aug 16 13:15:06 2021.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

地平线J5 AI芯片工具链用户手册
==============================================================

J5 AI芯片工具链是基于地平线征程5代芯片研发的AI算法解决方案。
它包含： **模型算法处理** 和 **嵌入式模型预测库** 两大重要组件。
模型算法处理提供PTQ浮点定点模型转换方案，
支持将基于TensorFlow、PyTorch或Caffe等公开框架得到的浮点模型直接转换为定点模型。
使用方案得到的定点模型配合模型编译工具处理后就可以在地平线芯片上执行。
嵌入式模型预测库提供利用定点模型完成推理的系列支持接口。
更多有关芯片工具链的细节，请继续阅读下一章内容。

为了让开发者快速上手体验模型训练/转换、部署、验证、推理等关键步骤，芯片工具链的各组件还提供 **示例包** 
以及配合示例包使用的Docker镜像和模型发布物。 
这些示例包将各工具核心业务逻辑和关键配置参数封装成脚本；模型发布物内置了丰富的算法模型；Docker镜像预置了使用示例包所需的开发环境。

.. note::

  根据开发者使用芯片工具链的步骤，我们建议您这样使用J5 AI芯片工具链提供的文档：  

  * 首选阅读《J5 AI芯片工具链用户手册》（即本手册），全面了解PTQ浮点定点模型转换方案和嵌入式模型预测库等核心模块的实现原理、环境搭建、开发步骤、使用经验和常见问题等内容。
    在从模型处理到部署的过程中，您将需要多次阅读第1，3，4章内容，直至完成芯片工具链使用。
  * 在选择阅读了以上的用户手册之后，如果您选择使用PTQ模型转换方案处理模型，则需要阅读
    `《PTQ模型转换示例包手册》 <../horizon_model_convert_sample/index.html>`_ 和
    `《supported_op_list_and_restrictions》 <../supported_op_list_and_restrictions/supported_op_list_and_restrictions_release.xlsx>`_
    算子列表，以便在Docker环境中，使用PTQ模型转换示例包，完成模型转换 + 编译过程，得到能够部署到J5开发板上的定点模型。
    在这一过程中，您也将学会使用PTQ方案完成模型转换和编译，进而搭建自己的业务pipeline。
  * 在使用PTQ方案得到J5平台支持的模型之后，就要将模型部署到开发板上并进行Runtime应用开发了。在此过程中，

    - `《基础示例包使用说明》 <../basic_sample/index.html>`_ 帮助开发者使用Runtime应用开发基础示例包了解嵌入式API使用、自定义算子推理、多模批量推理等功能。
    - `《ai_benchmark使用说明》 <../ai_benchmark/index.html>`_ 帮助开发者使用 **ai_benchmark** 示例包中的示例脚本对上板模型进行性能和精度评测。
    - `《bpu_sdk_api_doc》 <../bpu_sdk_api_doc/index.html>`_ 介绍应用开发中需要使用的数据的类型、结构、排布、对齐规则、API接口、错误码和配置信息。
    
    在完成模型上板部署后，您将在嵌入式应用开发过程中多次查阅此文档。
  * 最后，当您对芯片工具链各模块有一定了解后，将继续阅读 
    `《J5 AI芯片工具链工具手册》 <../j5_ai_toolchain_tool_guide/index.html>`_ 在开发过程中查阅各工具的使用方法。

.. toctree::
   :numbered:
   :maxdepth: 2
   :caption: 本手册目录结构:

   product_introduction.rst
   env_prepare.rst
   ptq_solution.rst
   application_development.rst
   dsp.rst
   appendix.rst


