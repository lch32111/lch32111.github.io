---
layout: distill
title: Portfolio One Pager
description: My Portfolio
importance: 1
category: work
related_publications: false
toc:
  - name: 경력
    subsections:
      - name: Ubisoft La Forge
      - name: LG AI Research
      - name: Com2us
  - name: 개인 프로젝트
    subsections:
      - name: ChLib
      - name: MeshOptimization
      - name: MarchingCubeSDF
      - name: ChanGameEngine
      - name: GJK Collision Detection
---



# 경력



## Ubisoft La Forge

* 재직기간: 2022.11 - 2024.08
* 직무: Generalist Programmer (R&D 인턴쉽 프로그램. 학교 석사 연구와 함께 진행)

Ubisoft La Forge Montreal에서 연구를 했었습니다. 게임같은 실시간 어플리케이션에 cloth deformation을 적용하기 위해 neural cloth synthesis를 연구 했습니다. 이 연구는 저의 석사 학위 프로그램과 함께 진행되었습니다. 연구 논문 Real-Time Neural Cloth Deformation using a Compact Latent Space and a Latent Vector Predictor가 ECCV 2024 [CV2](https://sites.google.com/nvidia.com/cv2/home) Workshop에 승인되었습니다. 워크샵 논문이 업로드 되기전까지 해당 논문에 대한 것을 [졸업 논문](https://spectrum.library.concordia.ca/id/eprint/994526/)에서 참조가능 합니다.

{% details 논문 Abstract %}

We propose a method for real-time cloth deformation using neural networks, especially for draping a garment on a human body. The computational overhead of most of the existing learning methods for cloth deformation often limits their use in interactive applications. Employing a two-stage training process, our method predicts garment deformations in real-time. In the first stage, a graph neural network extracts cloth vertex features which are compressed into a latent vector with a mesh convolution network. We then decode the latent vector to blend shape weights, which are fed to a trainable blend shape module. In the second stage, we freeze the latent extraction and train a latent predictor network. The predictor uses a subset of the inputs from the first stage, ensuring that inputs are restricted to those which are readily available in a typical game engine. Then, during inference, the latent predictor predicts the compacted latent which is processed by the decoder and blend shape networks from the first stage. Our experiments demonstrate that our method effectively balances computational efficiency and realistic cloth deformation, making it suitable for real-time use in applications such as games.

{% enddetails %}



## LG AI Research

* 재직기간: 2022.05 - 2022.08
* 직무: 프리랜서 소프트웨어 엔지니어

사용자가 화학 정보 파일을 볼 수 있고, 렌더링 결과를 수정할 수 있고, 그 결과에 대한 labeled data를 얻을 수 있는 프로그램을 개발했습니다. 회사의 머신러닝 프로젝트의 많은 훈련 데이터셋을 생성하기 위한 프로그램입니다. 이 프로그램은 한 유명한 화학 정보 렌더링 라이브러리를 기반으로 만들어 졌습니다. Windows와 Ubuntu를 포함하여 크로스 플랫폼으로 작동하게 하고, cmake와 c++를 통해 빌드되어 집니다.

* 병렬로 많은 훈련 데이터셋을 생성할 수 있는 CLI  프로그램 개발했습니다. Windows와 Ubuntu에서 작동합니다.
* 사용자가 렌더링 결과를 수정하고, labeled data를 얻을 수 있는 GUI 프로그램을 개발했습니다. 이 프로그램은 화학 정보 파일들을 병렬로 처리하는 것과 멀티 윈도우 렌더링을 지원합니다. DirectX11이 렌더링에 사용되었습니다.
* 훈련 데이터셋을 생성하기 위해 화학 정보 렌더링 라이브러리를 분석하고 커스터마이징 했습니다.



## Com2us

* 재직기간: 2019.03 - 2021.06
* 직무: 게임 엔진 프로그래머

렌더러와, 그 렌더러를 위한 다른 시스템들을 개발했습니다. 이 프로젝트는 Windows, Mac, Android, 그리고 iOS를 포함하는 cross-platforms를 타겟으로 했었습니다. cmake build system과 C++11로 프로젝트가 빌드되었습니다. 렌더링과 관련된 다양한 측면 뿐만 아니라, 엔진이 튼튼하게 작동하기 위해 유용한 도구들을 다루었습니다.

* OpenGL ES, Vulkan, Metal를 이용하여 **통합 그래픽스 API**를 개발했습니다.
* Godot 엔진에 영향을 받은 **Material/Shader 시스템**을 개발했습니다. 이것은 사용자가 엔진에서 **쉐이더 프로그래밍**을 가능하게 합니다. 이 시스템은 쉐이더 변환을 위해 주로 glslang 라이브러리를 사용합니다.
* Game Scene과 Editor Viewport를 렌더링 할 수 있는 **forward shading renderer**를 개발했습니다. 이 렌더러는 에디터를 위한 **multi-window rendering**도 지원합니다. 렌더러의 아키텍쳐는 Unreal Enigne 4 (UE4)의 [Mesh Drawing Pipeline](https://youtu.be/qx1c190aGhs)을 참조했습니다.
* 게임 엔진의 **asset system**을 공동 기획했고, 그 asset system의 중요 부분들을 구현했습니다.
* 게임 엔진 파일의 **직렬화(serialization) 시스템**을 공동 기획했습니다.
* UE4에 영향을 받은 **자동화 테스트 프레임 워크**를 구현했습니다. 이것은 테스트 요청과 결과를 프로세스끼리 주고 받기 위해 Socket API를 이용합니다. 





# 개인 프로젝트



## ChLib

* 기간: 2021 ~
* 관련 링크:
  * [Full Reference](/blog/2024/ChLib-Full-Credits)
  * [Building GUI from scratch](/blog/2024/Building-GUI-from-scratch)

ChLib의 저의 개인 라이브러리로, 미래 계획을 위해 게임엔진과 다른 어플리케이션을 만들기 위해 사용됩니다. 이 라이브러리는 다음의 것들로 개발되고 있습니다:

* C99
* [Unity Build](https://en.wikipedia.org/wiki/Unity_build)
* [4coder editor](https://4coder.net/)
* [raddebugger](https://github.com/EpicGamesExt/raddebugger)

위의 개발 환경은 빠른 빌드타임을 갖게 해주고 코드를 즐겁게 작성할 수 있게 합니다. 코드 스타일을 보여주기 위해, `chrender_vulkan_texture.c` 파일을 여기에 공개합니다.

<details>
<summary> chrender_vulkan_texture.c </summary>
<pre style="font-family:monospace;color: rgb(201, 209, 217); background-color: rgb(13, 17, 23); font-weight: 400; "><span style="color: rgb(121, 192, 255); font-weight: 400;">#<span style="color: rgb(255, 123, 114); font-weight: 400;">include</span> <span style="color: rgb(165, 214, 255); font-weight: 400;">"chrender/vulkan/chrender_vulkan.h"</span></span>
<span style="color: rgb(121, 192, 255); font-weight: 400;">#<span style="color: rgb(255, 123, 114); font-weight: 400;">include</span> <span style="color: rgb(165, 214, 255); font-weight: 400;">"chrender/vulkan/chrender_vulkan_library.h"</span></span>

ChRenderTexture* <span style="color: rgb(210, 168, 255); font-weight: 400;">chrender_vulkan_texture_create</span><span style="color: rgb(201, 209, 217); font-weight: 400;">(ChRenderContext* ctx, ChRenderTextureParam* param)</span>
{
    ChAllocator allocator = param-&gt;allocator ? *param-&gt;allocator : ctx-&gt;permanent_buddy_allocator;
    ChRenderContextVulkan* vctx = (ChRenderContextVulkan*)ctx-&gt;handle;
    
    <span style="color: rgb(255, 123, 114); font-weight: 400;">const</span> u64 memory_size = <span style="color: rgb(255, 123, 114); font-weight: 400;">sizeof</span>(ChRenderTexture) + <span style="color: rgb(255, 123, 114); font-weight: 400;">sizeof</span>(ChRenderTextureVulkan);
    u8* memory = (u8*)allocator.alloc_func(allocator.object, memory_size, CH_PLATFORM_MIN_MALLOC_ALIGNMENT);
    <span style="color: rgb(255, 123, 114); font-weight: 400;">if</span> (memory == <span style="color: rgb(121, 192, 255); font-weight: 400;">NULL</span>)
        <span style="color: rgb(255, 123, 114); font-weight: 400;">return</span> <span style="color: rgb(121, 192, 255); font-weight: 400;">NULL</span>;
    <span style="color: rgb(255, 166, 87); font-weight: 400;">memset</span>(memory, <span style="color: rgb(121, 192, 255); font-weight: 400;">0</span>, memory_size);
    
    ChRenderTexture* rt_handle = (ChRenderTexture*)memory;
    ChRenderTextureVulkan* rtv = (ChRenderTextureVulkan*)(memory + <span style="color: rgb(255, 123, 114); font-weight: 400;">sizeof</span>(ChRenderTexture));
    rtv-&gt;allocator = allocator;
    
    rt_handle-&gt;type = param-&gt;type;
    rt_handle-&gt;format = param-&gt;format;
    rt_handle-&gt;width = param-&gt;width;
    rt_handle-&gt;height = param-&gt;height;
    rt_handle-&gt;depth = param-&gt;depth;
    rt_handle-&gt;handle = rtv;
    
    VkFormat texture_format = chrender_vulkan_get_vkformat(param-&gt;format);
    VkFormatProperties format_properties;
    vkGetPhysicalDeviceFormatProperties(vctx-&gt;physical_device, texture_format, &amp;format_properties);
    
    <span style="color: rgb(139, 148, 158); font-weight: 400;">/*
    * I am gonna always create a texture with the optimal tiling.
    * So, I validate the format feature support here
    * TODO : add more validation code here for usage and format feature
    */</span>
    VkImageUsageFlags image_usage = chrender_vulkan_get_vkimageusage(param-&gt;usage);
    <span style="color: rgb(255, 123, 114); font-weight: 400;">bool</span> wrong_usage = <span style="color: rgb(121, 192, 255); font-weight: 400;">false</span>;
    wrong_usage |= (image_usage &amp; VK_IMAGE_USAGE_SAMPLED_BIT) &amp;&amp; 
    (format_properties.optimalTilingFeatures &amp; VK_FORMAT_FEATURE_SAMPLED_IMAGE_BIT) == <span style="color: rgb(121, 192, 255); font-weight: 400;">0</span>;
    wrong_usage |= (image_usage &amp; VK_IMAGE_USAGE_COLOR_ATTACHMENT_BIT) &amp;&amp;
    (format_properties.optimalTilingFeatures &amp; VK_FORMAT_FEATURE_COLOR_ATTACHMENT_BIT) == <span style="color: rgb(121, 192, 255); font-weight: 400;">0</span>;
    wrong_usage |= (image_usage &amp; VK_IMAGE_USAGE_DEPTH_STENCIL_ATTACHMENT_BIT) &amp;&amp;
    (format_properties.optimalTilingFeatures &amp; VK_FORMAT_FEATURE_DEPTH_STENCIL_ATTACHMENT_BIT) == <span style="color: rgb(121, 192, 255); font-weight: 400;">0</span>;
    wrong_usage |= (image_usage &amp; VK_IMAGE_USAGE_TRANSFER_SRC_BIT) &amp;&amp;
    (format_properties.optimalTilingFeatures &amp; VK_FORMAT_FEATURE_TRANSFER_SRC_BIT) == <span style="color: rgb(121, 192, 255); font-weight: 400;">0</span>;
    wrong_usage |= (image_usage &amp; VK_IMAGE_USAGE_TRANSFER_DST_BIT) &amp;&amp;
    (format_properties.optimalTilingFeatures &amp; VK_FORMAT_FEATURE_TRANSFER_DST_BIT) == <span style="color: rgb(121, 192, 255); font-weight: 400;">0</span>;
    <span style="color: rgb(255, 123, 114); font-weight: 400;">if</span> (wrong_usage == <span style="color: rgb(121, 192, 255); font-weight: 400;">true</span>)
        <span style="color: rgb(255, 123, 114); font-weight: 400;">goto</span> FAIL;
    
    VkImageType image_type = chrender_vulkan_get_vkimagetype(param-&gt;type);
    
    VkImageCreateInfo image_create_info =
    {
        .sType = VK_STRUCTURE_TYPE_IMAGE_CREATE_INFO,
        .pNext = <span style="color: rgb(121, 192, 255); font-weight: 400;">NULL</span>,
        .flags = <span style="color: rgb(121, 192, 255); font-weight: 400;">0</span>, <span style="color: rgb(139, 148, 158); font-weight: 400;">// @TODO : Do I need a param for this?</span>
        .imageType = image_type,
        .format = texture_format,
        .extent = {.width = param-&gt;width, .height = param-&gt;height, .depth = param-&gt;depth},
        .mipLevels = param-&gt;mip_levels,
        .arrayLayers = param-&gt;array_layers,
        .samples = param-&gt;samples, <span style="color: rgb(139, 148, 158); font-weight: 400;">// same as vulkan</span>
        .tiling = VK_IMAGE_TILING_OPTIMAL,
        .usage = image_usage,
        .sharingMode = VK_SHARING_MODE_EXCLUSIVE,
        .queueFamilyIndexCount = <span style="color: rgb(121, 192, 255); font-weight: 400;">0</span>,
        .pQueueFamilyIndices = <span style="color: rgb(121, 192, 255); font-weight: 400;">NULL</span>,
        .initialLayout = VK_IMAGE_LAYOUT_PREINITIALIZED
    };
    VkResult result = vkCreateImage(vctx-&gt;logical_device, &amp;image_create_info, <span style="color: rgb(121, 192, 255); font-weight: 400;">NULL</span>, &amp;rtv-&gt;image);
    <span style="color: rgb(255, 123, 114); font-weight: 400;">if</span> (result != VK_SUCCESS)
        <span style="color: rgb(255, 123, 114); font-weight: 400;">goto</span> FAIL;
    
    VkMemoryRequirements mem_req;
    vkGetImageMemoryRequirements(vctx-&gt;logical_device, rtv-&gt;image, &amp;mem_req);
    
    VkMemoryPropertyFlags mem_priorities[<span style="color: rgb(121, 192, 255); font-weight: 400;">1</span>] =
    {
        VK_MEMORY_PROPERTY_DEVICE_LOCAL_BIT
    };
    s32 mem_type_index = chrender_vulkan_find_memory_property_index(&amp;vctx-&gt;device_mem_properties, mem_req.memoryTypeBits, mem_priorities[<span style="color: rgb(121, 192, 255); font-weight: 400;">0</span>]);
    <span style="color: rgb(255, 123, 114); font-weight: 400;">if</span> (mem_type_index == <span style="color: rgb(121, 192, 255); font-weight: 400;">-1</span>)
        <span style="color: rgb(255, 123, 114); font-weight: 400;">goto</span> FAIL;
    
    VkMemoryAllocateInfo mem_alloc_info =
    {
        .sType = VK_STRUCTURE_TYPE_MEMORY_ALLOCATE_INFO,
        .pNext = <span style="color: rgb(121, 192, 255); font-weight: 400;">NULL</span>,
        .allocationSize = mem_req.size,
        .memoryTypeIndex = mem_type_index
    };
    result = vkAllocateMemory(vctx-&gt;logical_device, &amp;mem_alloc_info, <span style="color: rgb(121, 192, 255); font-weight: 400;">NULL</span>, &amp;rtv-&gt;image_memory);
    <span style="color: rgb(255, 123, 114); font-weight: 400;">if</span> (result != VK_SUCCESS)
        <span style="color: rgb(255, 123, 114); font-weight: 400;">goto</span> FAIL;
    
    result = vkBindImageMemory(vctx-&gt;logical_device, rtv-&gt;image, rtv-&gt;image_memory, <span style="color: rgb(121, 192, 255); font-weight: 400;">0</span>);
    <span style="color: rgb(255, 123, 114); font-weight: 400;">if</span> (result != VK_SUCCESS)
        <span style="color: rgb(255, 123, 114); font-weight: 400;">goto</span> FAIL;
    
    <span style="color: rgb(139, 148, 158); font-weight: 400;">// just view image as it is</span>
    VkImageViewType view_type = <span style="color: rgb(121, 192, 255); font-weight: 400;">0</span>;
    <span style="color: rgb(255, 123, 114); font-weight: 400;">switch</span> (image_type)
    {
        <span style="color: rgb(255, 123, 114); font-weight: 400;">case</span> VK_IMAGE_TYPE_1D:
        {
            <span style="color: rgb(255, 123, 114); font-weight: 400;">if</span> (param-&gt;array_layers == <span style="color: rgb(121, 192, 255); font-weight: 400;">1</span>)
                view_type = VK_IMAGE_VIEW_TYPE_1D;
            <span style="color: rgb(255, 123, 114); font-weight: 400;">else</span>
                view_type = VK_IMAGE_VIEW_TYPE_1D_ARRAY;
            
            <span style="color: rgb(255, 123, 114); font-weight: 400;">break</span>;
        }
        <span style="color: rgb(255, 123, 114); font-weight: 400;">case</span> VK_IMAGE_TYPE_2D:
        {
            <span style="color: rgb(255, 123, 114); font-weight: 400;">if</span> (param-&gt;array_layers == <span style="color: rgb(121, 192, 255); font-weight: 400;">1</span>)
                view_type = VK_IMAGE_VIEW_TYPE_2D;
            <span style="color: rgb(255, 123, 114); font-weight: 400;">else</span>
                view_type = VK_IMAGE_VIEW_TYPE_2D_ARRAY;
            <span style="color: rgb(255, 123, 114); font-weight: 400;">break</span>;
        }
        <span style="color: rgb(255, 123, 114); font-weight: 400;">case</span> VK_IMAGE_TYPE_3D:
        {
            <span style="color: rgb(255, 123, 114); font-weight: 400;">if</span> (param-&gt;array_layers == <span style="color: rgb(121, 192, 255); font-weight: 400;">1</span>)
            {
                view_type = VK_IMAGE_VIEW_TYPE_3D;
                <span style="color: rgb(255, 123, 114); font-weight: 400;">break</span>;
            }
            <span style="color: rgb(255, 123, 114); font-weight: 400;">else</span>
            {
                <span style="color: rgb(139, 148, 158); font-weight: 400;">// wrong parameter</span>
                CH_ASSERT(<span style="color: rgb(121, 192, 255); font-weight: 400;">0</span>);
            }
        }
        <span style="color: rgb(255, 123, 114); font-weight: 400;">default</span>: <span style="color: rgb(139, 148, 158); font-weight: 400;">// @TODO : CUBE_TYPE...</span>
        {
            CH_ASSERT(<span style="color: rgb(121, 192, 255); font-weight: 400;">0</span>);
        }
    }
    
    <span style="color: rgb(255, 123, 114); font-weight: 400;">bool</span> is_depth, is_stencil;
    chrender_vulkan_check_render_depthstencil(param-&gt;format, &amp;is_depth, &amp;is_stencil);
    VkImageAspectFlags image_aspects = VK_IMAGE_ASPECT_NONE;
    <span style="color: rgb(255, 123, 114); font-weight: 400;">if</span> (is_depth || is_stencil)
    {
        <span style="color: rgb(255, 123, 114); font-weight: 400;">if</span> (is_depth)
            image_aspects |= VK_IMAGE_ASPECT_DEPTH_BIT;
        
        <span style="color: rgb(255, 123, 114); font-weight: 400;">if</span> (is_stencil)
            image_aspects |= VK_IMAGE_ASPECT_STENCIL_BIT;
    }
    <span style="color: rgb(255, 123, 114); font-weight: 400;">else</span>
    {
        image_aspects = VK_IMAGE_ASPECT_COLOR_BIT;
    }
    
    VkImageViewCreateInfo imageview_create_info =
    {
        .sType = VK_STRUCTURE_TYPE_IMAGE_VIEW_CREATE_INFO,
        .pNext = <span style="color: rgb(121, 192, 255); font-weight: 400;">NULL</span>,
        .flags = <span style="color: rgb(121, 192, 255); font-weight: 400;">0</span>,
        .image = rtv-&gt;image,
        .viewType = view_type,
        .format = texture_format,
        .components = 
        {
            .r = VK_COMPONENT_SWIZZLE_IDENTITY,
            .g = VK_COMPONENT_SWIZZLE_IDENTITY,
            .b = VK_COMPONENT_SWIZZLE_IDENTITY,
            .a = VK_COMPONENT_SWIZZLE_IDENTITY
        },
        <span style="color: rgb(139, 148, 158); font-weight: 400;">// @TODO : mipmapping</span>
        .subresourceRange = 
        {
            .aspectMask = image_aspects,
            .baseMipLevel = <span style="color: rgb(121, 192, 255); font-weight: 400;">0</span>,
            .levelCount = <span style="color: rgb(121, 192, 255); font-weight: 400;">1</span>,
            .baseArrayLayer = <span style="color: rgb(121, 192, 255); font-weight: 400;">0</span>,
            .layerCount = <span style="color: rgb(121, 192, 255); font-weight: 400;">1</span>
        }
    };
    result = vkCreateImageView(vctx-&gt;logical_device, &amp;imageview_create_info, <span style="color: rgb(121, 192, 255); font-weight: 400;">NULL</span>, &amp;rtv-&gt;imageview);
    <span style="color: rgb(255, 123, 114); font-weight: 400;">if</span> (result != VK_SUCCESS)
        <span style="color: rgb(255, 123, 114); font-weight: 400;">goto</span> FAIL;
    
    rtv-&gt;layout = VK_IMAGE_LAYOUT_PREINITIALIZED;
    
    <span style="color: rgb(255, 123, 114); font-weight: 400;">return</span> rt_handle;
    
    FAIL:
    <span style="color: rgb(255, 123, 114); font-weight: 400;">if</span> (rtv-&gt;imageview != <span style="color: rgb(121, 192, 255); font-weight: 400;">NULL</span>)
    {
        vkDestroyImageView(vctx-&gt;logical_device, rtv-&gt;imageview, <span style="color: rgb(121, 192, 255); font-weight: 400;">NULL</span>);
    }
    
    <span style="color: rgb(255, 123, 114); font-weight: 400;">if</span> (rtv-&gt;image_memory != <span style="color: rgb(121, 192, 255); font-weight: 400;">NULL</span>)
    {
        vkFreeMemory(vctx-&gt;logical_device, rtv-&gt;image_memory, <span style="color: rgb(121, 192, 255); font-weight: 400;">NULL</span>);
    }
    
    <span style="color: rgb(255, 123, 114); font-weight: 400;">if</span> (rtv-&gt;image != <span style="color: rgb(121, 192, 255); font-weight: 400;">NULL</span>)
    {
        vkDestroyImage(vctx-&gt;logical_device, rtv-&gt;image, <span style="color: rgb(121, 192, 255); font-weight: 400;">NULL</span>);
    }
    
    <span style="color: rgb(255, 123, 114); font-weight: 400;">if</span> (memory != <span style="color: rgb(121, 192, 255); font-weight: 400;">NULL</span>)
    {
        allocator.free_func(allocator.object, memory);
    }
    
    <span style="color: rgb(255, 123, 114); font-weight: 400;">return</span> <span style="color: rgb(121, 192, 255); font-weight: 400;">NULL</span>;
}

<span style="color: rgb(255, 123, 114); font-weight: 400;">bool</span> <span style="color: rgb(210, 168, 255); font-weight: 400;">chrender_vulkan_texture_destroy</span><span style="color: rgb(201, 209, 217); font-weight: 400;">(ChRenderContext* ctx, ChRenderTexture* texture)</span>
{
    ChRenderContextVulkan* vctx = (ChRenderContextVulkan*)ctx-&gt;handle;
    ChRenderTextureVulkan* rtv = (ChRenderTextureVulkan*)texture-&gt;handle;
    ChAllocator allocator = rtv-&gt;allocator;
    
    vkDestroyImageView(vctx-&gt;logical_device, rtv-&gt;imageview, <span style="color: rgb(121, 192, 255); font-weight: 400;">NULL</span>);
    vkFreeMemory(vctx-&gt;logical_device, rtv-&gt;image_memory, <span style="color: rgb(121, 192, 255); font-weight: 400;">NULL</span>);
    vkDestroyImage(vctx-&gt;logical_device, rtv-&gt;image, <span style="color: rgb(121, 192, 255); font-weight: 400;">NULL</span>);
    
    allocator.free_func(allocator.object, texture);
    
    <span style="color: rgb(255, 123, 114); font-weight: 400;">return</span> <span style="color: rgb(121, 192, 255); font-weight: 400;">true</span>;
}

<span style="color: rgb(255, 123, 114); font-weight: 400;">bool</span> <span style="color: rgb(210, 168, 255); font-weight: 400;">chrender_vulkan_texture_update</span><span style="color: rgb(201, 209, 217); font-weight: 400;">(ChRenderContext* ctx, ChRenderTexture* texture, ChRenderTextureUpdateParam* param)</span>
{
    ChRenderContextVulkan* rctxv = (ChRenderContextVulkan*)ctx-&gt;handle;
    ChRenderTextureVulkan* rtv = (ChRenderTextureVulkan*)texture-&gt;handle;
    ChRenderCommandBufferVulkan* rcbv = (ChRenderCommandBufferVulkan*)param-&gt;command_buffer-&gt;handle;
    VkCommandBuffer cur_command_buffer = rcbv-&gt;command_buffers[rctxv-&gt;submission_index];
    
    <span style="color: rgb(139, 148, 158); font-weight: 400;">/*
    * 1. Transfer the image layout of the texture from its oldLayout to TRANSFER_DST_OPTIMAL,
    *    in order to update its content.
    * 2. Create a staging texture buffer that is visible to the cpu and update the user's texture to the staging texture buffer
    * 3. Copy the staging buffer data to the texture
    * 4. Transfer the image layout of the texture from TRANSFER_DST_OPTIMAL to VK_IMAGE_LAYOUT_SHADER_READ_ONLY_OPTIMAL, so that
    *    a shader can read this texture.
    */</span>
    
    <span style="color: rgb(139, 148, 158); font-weight: 400;">// @TODO : add the texture update dependency to the param?</span>
    VkImageMemoryBarrier image_memory_barrier =
    {
        .sType = VK_STRUCTURE_TYPE_IMAGE_MEMORY_BARRIER,
        .pNext = <span style="color: rgb(121, 192, 255); font-weight: 400;">NULL</span>,
        .srcAccessMask = <span style="color: rgb(121, 192, 255); font-weight: 400;">0</span>,
        .dstAccessMask = VK_ACCESS_TRANSFER_WRITE_BIT,
        .oldLayout = rtv-&gt;layout,
        .newLayout = VK_IMAGE_LAYOUT_TRANSFER_DST_OPTIMAL,
        .srcQueueFamilyIndex = VK_QUEUE_FAMILY_IGNORED,
        .dstQueueFamilyIndex = VK_QUEUE_FAMILY_IGNORED,
        .image = rtv-&gt;image,
        .subresourceRange =
        {
            .aspectMask = VK_IMAGE_ASPECT_COLOR_BIT, <span style="color: rgb(139, 148, 158); font-weight: 400;">// @TODO</span>
            .baseMipLevel = <span style="color: rgb(121, 192, 255); font-weight: 400;">0</span>,
            .levelCount = <span style="color: rgb(121, 192, 255); font-weight: 400;">1</span>,
            .baseArrayLayer = <span style="color: rgb(121, 192, 255); font-weight: 400;">0</span>,
            .layerCount = <span style="color: rgb(121, 192, 255); font-weight: 400;">1</span>,
        }
    };
    
    <span style="color: rgb(139, 148, 158); font-weight: 400;">// VkPipelineStageFlags src_stage_mask = VK_PIPELINE_STAGE_TOP_OF_PIPE_BIT means</span>
    <span style="color: rgb(139, 148, 158); font-weight: 400;">// no stage of execution when specified in the first scope.</span>
    VkPipelineStageFlags src_stage_mask = VK_PIPELINE_STAGE_TOP_OF_PIPE_BIT; 
    VkPipelineStageFlags dst_stage_mask = VK_PIPELINE_STAGE_TRANSFER_BIT;
    vkCmdPipelineBarrier
    (
     cur_command_buffer,
     src_stage_mask,
     dst_stage_mask,
     <span style="color: rgb(121, 192, 255); font-weight: 400;">0</span>,
     <span style="color: rgb(121, 192, 255); font-weight: 400;">0</span>, <span style="color: rgb(121, 192, 255); font-weight: 400;">NULL</span>,
     <span style="color: rgb(121, 192, 255); font-weight: 400;">0</span>, <span style="color: rgb(121, 192, 255); font-weight: 400;">NULL</span>,
     <span style="color: rgb(121, 192, 255); font-weight: 400;">1</span>, &amp;image_memory_barrier
     ); <span style="color: rgb(139, 148, 158); font-weight: 400;">// Step 1 Done</span>
    
    VkBuffer staging_buffer = VK_NULL_HANDLE;
    <span style="color: rgb(255, 123, 114); font-weight: 400;">if</span> (<span style="color: rgb(121, 192, 255); font-weight: 400;">false</span> == chrender_vulkan_staging_texture_buffer_get(rctxv, param, texture-&gt;format, &amp;staging_buffer))
        <span style="color: rgb(255, 123, 114); font-weight: 400;">return</span> <span style="color: rgb(121, 192, 255); font-weight: 400;">false</span>;
    <span style="color: rgb(139, 148, 158); font-weight: 400;">// Step 2 Done</span>
    
    VkBufferImageCopy buffer_image_copy =
    {
        .bufferOffset = <span style="color: rgb(121, 192, 255); font-weight: 400;">0</span>,
        .bufferRowLength = param-&gt;width,
        .bufferImageHeight = param-&gt;height,
        .imageSubresource =
        {
            .aspectMask = VK_IMAGE_ASPECT_COLOR_BIT, <span style="color: rgb(139, 148, 158); font-weight: 400;">// @TODO</span>
            .mipLevel = <span style="color: rgb(121, 192, 255); font-weight: 400;">0</span>,
            .baseArrayLayer = <span style="color: rgb(121, 192, 255); font-weight: 400;">0</span>,
            .layerCount = <span style="color: rgb(121, 192, 255); font-weight: 400;">1</span>,
        },
        .imageOffset = {.x = <span style="color: rgb(121, 192, 255); font-weight: 400;">0</span>, .y = <span style="color: rgb(121, 192, 255); font-weight: 400;">0</span>, .z = <span style="color: rgb(121, 192, 255); font-weight: 400;">0</span>},
        .imageExtent =
        {
            .width = param-&gt;width,
            .height = param-&gt;height,
            .depth = <span style="color: rgb(121, 192, 255); font-weight: 400;">1</span>,
        }
    };
    vkCmdCopyBufferToImage
    (
     cur_command_buffer,
     staging_buffer,
     rtv-&gt;image,
     VK_IMAGE_LAYOUT_TRANSFER_DST_OPTIMAL,
     <span style="color: rgb(121, 192, 255); font-weight: 400;">1</span>,
     &amp;buffer_image_copy
     );
    <span style="color: rgb(139, 148, 158); font-weight: 400;">// Step 3 Done</span>
    
    image_memory_barrier.srcAccessMask = VK_ACCESS_TRANSFER_WRITE_BIT;
    image_memory_barrier.dstAccessMask = VK_ACCESS_SHADER_READ_BIT;
    image_memory_barrier.oldLayout = VK_IMAGE_LAYOUT_TRANSFER_DST_OPTIMAL;
    image_memory_barrier.newLayout = VK_IMAGE_LAYOUT_SHADER_READ_ONLY_OPTIMAL;
    src_stage_mask = VK_PIPELINE_STAGE_TRANSFER_BIT;
    <span style="color: rgb(139, 148, 158); font-weight: 400;">// TODO(@CHAN): If this texture is read in vertex shader, then this sync is wrong. </span>
    <span style="color: rgb(139, 148, 158); font-weight: 400;">// So, On 20241111 I convert dst_stage_mask from VK_PIPELINE_STAGE_FRAGMENT_SHADER_BIT to</span>
    <span style="color: rgb(139, 148, 158); font-weight: 400;">// VK_PIPELINE_STAGE_VERTEX_SHADER_BIT for general usage</span>
    <span style="color: rgb(139, 148, 158); font-weight: 400;">// I should add one more additional update hint parameter for this.</span>
    dst_stage_mask = VK_PIPELINE_STAGE_VERTEX_SHADER_BIT; 
    vkCmdPipelineBarrier
    (
     cur_command_buffer,
     src_stage_mask,
     dst_stage_mask,
     <span style="color: rgb(121, 192, 255); font-weight: 400;">0</span>,
     <span style="color: rgb(121, 192, 255); font-weight: 400;">0</span>, <span style="color: rgb(121, 192, 255); font-weight: 400;">NULL</span>,
     <span style="color: rgb(121, 192, 255); font-weight: 400;">0</span>, <span style="color: rgb(121, 192, 255); font-weight: 400;">NULL</span>,
     <span style="color: rgb(121, 192, 255); font-weight: 400;">1</span>, &amp;image_memory_barrier
     );
    <span style="color: rgb(139, 148, 158); font-weight: 400;">// Step 4 Done</span>
    
    rtv-&gt;layout = VK_IMAGE_LAYOUT_SHADER_READ_ONLY_OPTIMAL;
    
    <span style="color: rgb(255, 123, 114); font-weight: 400;">return</span> <span style="color: rgb(121, 192, 255); font-weight: 400;">true</span>;
}

ChRenderFormat <span style="color: rgb(210, 168, 255); font-weight: 400;">chrender_vulkan_get_renderformat</span><span style="color: rgb(201, 209, 217); font-weight: 400;">(VkFormat format)</span>
{
    <span style="color: rgb(255, 123, 114); font-weight: 400;">switch</span> (format)
    {
        <span style="color: rgb(255, 123, 114); font-weight: 400;">case</span> VK_FORMAT_R8_UNORM: <span style="color: rgb(255, 123, 114); font-weight: 400;">return</span> CHRENDER_FORMAT_R8_UNORM;
        <span style="color: rgb(255, 123, 114); font-weight: 400;">case</span> VK_FORMAT_R8_UINT: <span style="color: rgb(255, 123, 114); font-weight: 400;">return</span> CHRENDER_FORMAT_R8_UINT;
        <span style="color: rgb(255, 123, 114); font-weight: 400;">case</span> VK_FORMAT_R8G8B8_UNORM: <span style="color: rgb(255, 123, 114); font-weight: 400;">return</span> CHRENDER_FORMAT_R8G8B8_UNORM;
        <span style="color: rgb(255, 123, 114); font-weight: 400;">case</span> VK_FORMAT_R8G8B8A8_UNORM: <span style="color: rgb(255, 123, 114); font-weight: 400;">return</span> CHRENDER_FORMAT_R8G8B8A8_UNORM;
        <span style="color: rgb(255, 123, 114); font-weight: 400;">case</span> VK_FORMAT_R8G8B8A8_SNORM: <span style="color: rgb(255, 123, 114); font-weight: 400;">return</span> CHRENDER_FORMAT_R8G8B8A8_SNORM;
        <span style="color: rgb(255, 123, 114); font-weight: 400;">case</span> VK_FORMAT_R8G8B8A8_UINT: <span style="color: rgb(255, 123, 114); font-weight: 400;">return</span> CHRENDER_FORMAT_R8G8B8A8_UINT;
        <span style="color: rgb(255, 123, 114); font-weight: 400;">case</span> VK_FORMAT_R8G8B8A8_SINT: <span style="color: rgb(255, 123, 114); font-weight: 400;">return</span> CHRENDER_FORMAT_R8G8B8A8_SINT;
        <span style="color: rgb(255, 123, 114); font-weight: 400;">case</span> VK_FORMAT_R8G8B8A8_SRGB: <span style="color: rgb(255, 123, 114); font-weight: 400;">return</span> CHRENDER_FORMAT_R8G8B8A8_SRGB;
        <span style="color: rgb(255, 123, 114); font-weight: 400;">case</span> VK_FORMAT_B8G8R8A8_UNORM: <span style="color: rgb(255, 123, 114); font-weight: 400;">return</span> CHRENDER_FORMAT_B8G8R8A8_UNORM;
        <span style="color: rgb(255, 123, 114); font-weight: 400;">case</span> VK_FORMAT_R32_UINT: <span style="color: rgb(255, 123, 114); font-weight: 400;">return</span> CHRENDER_FORMAT_R32_UINT;
        <span style="color: rgb(255, 123, 114); font-weight: 400;">case</span> VK_FORMAT_R32_SFLOAT: <span style="color: rgb(255, 123, 114); font-weight: 400;">return</span> CHRENDER_FORMAT_R32_SFLOAT;
        <span style="color: rgb(255, 123, 114); font-weight: 400;">case</span> VK_FORMAT_R32G32_SFLOAT: <span style="color: rgb(255, 123, 114); font-weight: 400;">return</span> CHRENDER_FORMAT_R32G32_SFLOAT;
        <span style="color: rgb(255, 123, 114); font-weight: 400;">case</span> VK_FORMAT_R32G32B32_SFLOAT: <span style="color: rgb(255, 123, 114); font-weight: 400;">return</span> CHRENDER_FORMAT_R32G32B32_SFLOAT;
        <span style="color: rgb(255, 123, 114); font-weight: 400;">case</span> VK_FORMAT_R32G32B32A32_UINT: <span style="color: rgb(255, 123, 114); font-weight: 400;">return</span> CHRENDER_FORMAT_R32G32B32A32_UINT;
        <span style="color: rgb(255, 123, 114); font-weight: 400;">case</span> VK_FORMAT_R32G32B32A32_SINT: <span style="color: rgb(255, 123, 114); font-weight: 400;">return</span> CHRENDER_FORMAT_R32G32B32A32_SINT;
        <span style="color: rgb(255, 123, 114); font-weight: 400;">case</span> VK_FORMAT_R32G32B32A32_SFLOAT: <span style="color: rgb(255, 123, 114); font-weight: 400;">return</span> CHRENDER_FORMAT_R32G32B32A32_SFLOAT;
        <span style="color: rgb(255, 123, 114); font-weight: 400;">case</span> VK_FORMAT_D16_UNORM: <span style="color: rgb(255, 123, 114); font-weight: 400;">return</span> CHRENDER_FORMAT_D16_UNORM;
        <span style="color: rgb(255, 123, 114); font-weight: 400;">case</span> VK_FORMAT_D32_SFLOAT: <span style="color: rgb(255, 123, 114); font-weight: 400;">return</span> CHRENDER_FORMAT_D32_SFLOAT;
        <span style="color: rgb(255, 123, 114); font-weight: 400;">case</span> VK_FORMAT_D16_UNORM_S8_UINT: <span style="color: rgb(255, 123, 114); font-weight: 400;">return</span> CHRENDER_FORMAT_D16_UNORM_S8_UINT;
        <span style="color: rgb(255, 123, 114); font-weight: 400;">case</span> VK_FORMAT_D24_UNORM_S8_UINT: <span style="color: rgb(255, 123, 114); font-weight: 400;">return</span> CHRENDER_FORMAT_D24_UNORM_S8_UINT;
        <span style="color: rgb(255, 123, 114); font-weight: 400;">case</span> VK_FORMAT_D32_SFLOAT_S8_UINT: <span style="color: rgb(255, 123, 114); font-weight: 400;">return</span> CHRENDER_FORMAT_D32_SFLOAT_S8_UINT;
    }
    <span style="color: rgb(255, 123, 114); font-weight: 400;">return</span> CHRENDER_FORMAT_UNDEFINED;
}

VkFormat <span style="color: rgb(210, 168, 255); font-weight: 400;">chrender_vulkan_get_vkformat</span><span style="color: rgb(201, 209, 217); font-weight: 400;">(ChRenderFormat format)</span>
{
    <span style="color: rgb(255, 123, 114); font-weight: 400;">switch</span> (format)
    {
        <span style="color: rgb(255, 123, 114); font-weight: 400;">case</span> CHRENDER_FORMAT_R8_UNORM: <span style="color: rgb(255, 123, 114); font-weight: 400;">return</span> VK_FORMAT_R8_UNORM;
        <span style="color: rgb(255, 123, 114); font-weight: 400;">case</span> CHRENDER_FORMAT_R8_UINT: <span style="color: rgb(255, 123, 114); font-weight: 400;">return</span> VK_FORMAT_R8_UINT;
        <span style="color: rgb(255, 123, 114); font-weight: 400;">case</span> CHRENDER_FORMAT_R8G8B8_UNORM: <span style="color: rgb(255, 123, 114); font-weight: 400;">return</span> VK_FORMAT_R8G8B8_UNORM;
        <span style="color: rgb(255, 123, 114); font-weight: 400;">case</span> CHRENDER_FORMAT_R8G8B8A8_UNORM: <span style="color: rgb(255, 123, 114); font-weight: 400;">return</span> VK_FORMAT_R8G8B8A8_UNORM;
        <span style="color: rgb(255, 123, 114); font-weight: 400;">case</span> CHRENDER_FORMAT_R8G8B8A8_SNORM: <span style="color: rgb(255, 123, 114); font-weight: 400;">return</span> VK_FORMAT_R8G8B8A8_SNORM;
        <span style="color: rgb(255, 123, 114); font-weight: 400;">case</span> CHRENDER_FORMAT_R8G8B8A8_UINT: <span style="color: rgb(255, 123, 114); font-weight: 400;">return</span> VK_FORMAT_R8G8B8A8_UINT;
        <span style="color: rgb(255, 123, 114); font-weight: 400;">case</span> CHRENDER_FORMAT_R8G8B8A8_SINT: <span style="color: rgb(255, 123, 114); font-weight: 400;">return</span> VK_FORMAT_R8G8B8A8_SINT;
        <span style="color: rgb(255, 123, 114); font-weight: 400;">case</span> CHRENDER_FORMAT_R8G8B8A8_SRGB: <span style="color: rgb(255, 123, 114); font-weight: 400;">return</span> VK_FORMAT_R8G8B8A8_SRGB;
        <span style="color: rgb(255, 123, 114); font-weight: 400;">case</span> CHRENDER_FORMAT_B8G8R8A8_UNORM: <span style="color: rgb(255, 123, 114); font-weight: 400;">return</span> VK_FORMAT_B8G8R8A8_UNORM;
        <span style="color: rgb(255, 123, 114); font-weight: 400;">case</span> CHRENDER_FORMAT_R32_UINT: <span style="color: rgb(255, 123, 114); font-weight: 400;">return</span> VK_FORMAT_R32_UINT;
        <span style="color: rgb(255, 123, 114); font-weight: 400;">case</span> CHRENDER_FORMAT_R32_SFLOAT: <span style="color: rgb(255, 123, 114); font-weight: 400;">return</span> VK_FORMAT_R32_SFLOAT;
        <span style="color: rgb(255, 123, 114); font-weight: 400;">case</span> CHRENDER_FORMAT_R32G32_SFLOAT: <span style="color: rgb(255, 123, 114); font-weight: 400;">return</span> VK_FORMAT_R32G32_SFLOAT;
        <span style="color: rgb(255, 123, 114); font-weight: 400;">case</span> CHRENDER_FORMAT_R32G32B32_SFLOAT: <span style="color: rgb(255, 123, 114); font-weight: 400;">return</span> VK_FORMAT_R32G32B32_SFLOAT;
        <span style="color: rgb(255, 123, 114); font-weight: 400;">case</span> CHRENDER_FORMAT_R32G32B32A32_UINT: <span style="color: rgb(255, 123, 114); font-weight: 400;">return</span> VK_FORMAT_R32G32B32A32_UINT;
        <span style="color: rgb(255, 123, 114); font-weight: 400;">case</span> CHRENDER_FORMAT_R32G32B32A32_SINT: <span style="color: rgb(255, 123, 114); font-weight: 400;">return</span> VK_FORMAT_R32G32B32A32_SINT;
        <span style="color: rgb(255, 123, 114); font-weight: 400;">case</span> CHRENDER_FORMAT_R32G32B32A32_SFLOAT: <span style="color: rgb(255, 123, 114); font-weight: 400;">return</span> VK_FORMAT_R32G32B32A32_SFLOAT;
        <span style="color: rgb(255, 123, 114); font-weight: 400;">case</span> CHRENDER_FORMAT_D16_UNORM: <span style="color: rgb(255, 123, 114); font-weight: 400;">return</span> VK_FORMAT_D16_UNORM;
        <span style="color: rgb(255, 123, 114); font-weight: 400;">case</span> CHRENDER_FORMAT_D32_SFLOAT: <span style="color: rgb(255, 123, 114); font-weight: 400;">return</span> VK_FORMAT_D32_SFLOAT;
        <span style="color: rgb(255, 123, 114); font-weight: 400;">case</span> CHRENDER_FORMAT_D16_UNORM_S8_UINT: <span style="color: rgb(255, 123, 114); font-weight: 400;">return</span> VK_FORMAT_D16_UNORM_S8_UINT;
        <span style="color: rgb(255, 123, 114); font-weight: 400;">case</span> CHRENDER_FORMAT_D24_UNORM_S8_UINT: <span style="color: rgb(255, 123, 114); font-weight: 400;">return</span> VK_FORMAT_D24_UNORM_S8_UINT;
        <span style="color: rgb(255, 123, 114); font-weight: 400;">case</span> CHRENDER_FORMAT_D32_SFLOAT_S8_UINT: <span style="color: rgb(255, 123, 114); font-weight: 400;">return</span> VK_FORMAT_D32_SFLOAT_S8_UINT;
    }
    
    <span style="color: rgb(255, 123, 114); font-weight: 400;">return</span> VK_FORMAT_UNDEFINED;
}

u64 <span style="color: rgb(210, 168, 255); font-weight: 400;">chrender_vulkan_get_vkformat_size</span><span style="color: rgb(201, 209, 217); font-weight: 400;">(VkFormat format)</span>
{
    <span style="color: rgb(255, 123, 114); font-weight: 400;">switch</span> (format)
    {
        <span style="color: rgb(255, 123, 114); font-weight: 400;">case</span> VK_FORMAT_R8_UNORM:
        <span style="color: rgb(255, 123, 114); font-weight: 400;">case</span> VK_FORMAT_R8_UINT:
        <span style="color: rgb(255, 123, 114); font-weight: 400;">return</span> <span style="color: rgb(121, 192, 255); font-weight: 400;">1</span>;
        <span style="color: rgb(255, 123, 114); font-weight: 400;">case</span> VK_FORMAT_D16_UNORM:
        <span style="color: rgb(255, 123, 114); font-weight: 400;">return</span> <span style="color: rgb(121, 192, 255); font-weight: 400;">2</span>;
        <span style="color: rgb(255, 123, 114); font-weight: 400;">case</span> VK_FORMAT_R8G8B8_UNORM:
        <span style="color: rgb(255, 123, 114); font-weight: 400;">case</span> VK_FORMAT_D16_UNORM_S8_UINT:
        <span style="color: rgb(255, 123, 114); font-weight: 400;">return</span> <span style="color: rgb(121, 192, 255); font-weight: 400;">3</span>;
        <span style="color: rgb(255, 123, 114); font-weight: 400;">case</span> VK_FORMAT_R8G8B8A8_UNORM: 
        <span style="color: rgb(255, 123, 114); font-weight: 400;">case</span> VK_FORMAT_R8G8B8A8_SNORM: 
        <span style="color: rgb(255, 123, 114); font-weight: 400;">case</span> VK_FORMAT_R8G8B8A8_UINT: 
        <span style="color: rgb(255, 123, 114); font-weight: 400;">case</span> VK_FORMAT_R8G8B8A8_SINT: 
        <span style="color: rgb(255, 123, 114); font-weight: 400;">case</span> VK_FORMAT_R8G8B8A8_SRGB: 
        <span style="color: rgb(255, 123, 114); font-weight: 400;">case</span> VK_FORMAT_B8G8R8A8_UNORM: 
        <span style="color: rgb(255, 123, 114); font-weight: 400;">case</span> VK_FORMAT_R32_UINT:
        <span style="color: rgb(255, 123, 114); font-weight: 400;">case</span> VK_FORMAT_R32_SFLOAT:
        <span style="color: rgb(255, 123, 114); font-weight: 400;">case</span> VK_FORMAT_D32_SFLOAT:
        <span style="color: rgb(255, 123, 114); font-weight: 400;">case</span> VK_FORMAT_D24_UNORM_S8_UINT:
        <span style="color: rgb(255, 123, 114); font-weight: 400;">return</span> <span style="color: rgb(121, 192, 255); font-weight: 400;">4</span>;
        <span style="color: rgb(255, 123, 114); font-weight: 400;">case</span> VK_FORMAT_D32_SFLOAT_S8_UINT:
        <span style="color: rgb(255, 123, 114); font-weight: 400;">return</span> <span style="color: rgb(121, 192, 255); font-weight: 400;">5</span>;
        <span style="color: rgb(255, 123, 114); font-weight: 400;">case</span> VK_FORMAT_R32G32_SFLOAT: 
        <span style="color: rgb(255, 123, 114); font-weight: 400;">return</span> <span style="color: rgb(121, 192, 255); font-weight: 400;">8</span>;
        <span style="color: rgb(255, 123, 114); font-weight: 400;">case</span> VK_FORMAT_R32G32B32_SFLOAT: 
        <span style="color: rgb(255, 123, 114); font-weight: 400;">return</span> <span style="color: rgb(121, 192, 255); font-weight: 400;">12</span>;
        <span style="color: rgb(255, 123, 114); font-weight: 400;">case</span> VK_FORMAT_R32G32B32A32_UINT: 
        <span style="color: rgb(255, 123, 114); font-weight: 400;">case</span> VK_FORMAT_R32G32B32A32_SINT: 
        <span style="color: rgb(255, 123, 114); font-weight: 400;">case</span> VK_FORMAT_R32G32B32A32_SFLOAT: 
        <span style="color: rgb(255, 123, 114); font-weight: 400;">return</span> <span style="color: rgb(121, 192, 255); font-weight: 400;">16</span>;
    }
    
    <span style="color: rgb(255, 123, 114); font-weight: 400;">return</span> <span style="color: rgb(121, 192, 255); font-weight: 400;">0</span>;
}

ChRenderTextureUsageFlags <span style="color: rgb(210, 168, 255); font-weight: 400;">chrender_vulkan_get_textureusage</span><span style="color: rgb(201, 209, 217); font-weight: 400;">(VkImageUsageFlags in_flags)</span>
{
    <span style="color: rgb(139, 148, 158); font-weight: 400;">// ChRenderTextureUsageFlags are defined the same as vulkan</span>
    ChRenderTextureUsageFlags flags = (ChRenderTextureUsageFlags)in_flags; 
    <span style="color: rgb(255, 123, 114); font-weight: 400;">return</span> flags;
}

VkImageUsageFlags <span style="color: rgb(210, 168, 255); font-weight: 400;">chrender_vulkan_get_vkimageusage</span><span style="color: rgb(201, 209, 217); font-weight: 400;">(ChRenderTextureUsageFlags in_flags)</span>
{
    VkImageUsageFlags flags = (VkImageUsageFlags)in_flags;
    <span style="color: rgb(255, 123, 114); font-weight: 400;">return</span> flags;
}

ChRenderTextureType <span style="color: rgb(210, 168, 255); font-weight: 400;">chrender_vulkan_get_imagetype</span><span style="color: rgb(201, 209, 217); font-weight: 400;">(VkImageType type)</span>
{
    <span style="color: rgb(255, 123, 114); font-weight: 400;">switch</span> (type)
    {
        <span style="color: rgb(255, 123, 114); font-weight: 400;">case</span> VK_IMAGE_TYPE_1D: <span style="color: rgb(255, 123, 114); font-weight: 400;">return</span> CHRENDER_TEXTURE_TYPE_1D;
        <span style="color: rgb(255, 123, 114); font-weight: 400;">case</span> VK_IMAGE_TYPE_2D: <span style="color: rgb(255, 123, 114); font-weight: 400;">return</span> CHRENDER_TEXTURE_TYPE_2D;
        <span style="color: rgb(255, 123, 114); font-weight: 400;">case</span> VK_IMAGE_TYPE_3D: <span style="color: rgb(255, 123, 114); font-weight: 400;">return</span> CHRENDER_TEXTURE_TYPE_3D;
    }
    
    <span style="color: rgb(255, 123, 114); font-weight: 400;">return</span> <span style="color: rgb(121, 192, 255); font-weight: 400;">0</span>;
}

VkImageType <span style="color: rgb(210, 168, 255); font-weight: 400;">chrender_vulkan_get_vkimagetype</span><span style="color: rgb(201, 209, 217); font-weight: 400;">(ChRenderTextureType type)</span>
{
    <span style="color: rgb(255, 123, 114); font-weight: 400;">switch</span> (type)
    {
        <span style="color: rgb(255, 123, 114); font-weight: 400;">case</span> CHRENDER_TEXTURE_TYPE_1D: <span style="color: rgb(255, 123, 114); font-weight: 400;">return</span> VK_IMAGE_TYPE_1D;
        <span style="color: rgb(255, 123, 114); font-weight: 400;">case</span> CHRENDER_TEXTURE_TYPE_2D: <span style="color: rgb(255, 123, 114); font-weight: 400;">return</span> VK_IMAGE_TYPE_2D;
        <span style="color: rgb(255, 123, 114); font-weight: 400;">case</span> CHRENDER_TEXTURE_TYPE_3D: <span style="color: rgb(255, 123, 114); font-weight: 400;">return</span> VK_IMAGE_TYPE_3D;
    }
    
    <span style="color: rgb(255, 123, 114); font-weight: 400;">return</span> VK_IMAGE_TYPE_MAX_ENUM;
}

<span style="color: rgb(255, 123, 114); font-weight: 400;">void</span> <span style="color: rgb(210, 168, 255); font-weight: 400;">chrender_vulkan_check_render_depthstencil</span><span style="color: rgb(201, 209, 217); font-weight: 400;">(ChRenderFormat format, <span style="color: rgb(255, 123, 114); font-weight: 400;">bool</span>* is_depth, <span style="color: rgb(255, 123, 114); font-weight: 400;">bool</span>* is_stencil)</span>
{
    <span style="color: rgb(255, 123, 114); font-weight: 400;">switch</span> (format)
    {
        <span style="color: rgb(255, 123, 114); font-weight: 400;">case</span> CHRENDER_FORMAT_D16_UNORM:
        {
            <span style="color: rgb(255, 123, 114); font-weight: 400;">if</span> (is_depth) *is_depth = <span style="color: rgb(121, 192, 255); font-weight: 400;">true</span>;
            <span style="color: rgb(255, 123, 114); font-weight: 400;">if</span> (is_stencil) * is_stencil = <span style="color: rgb(121, 192, 255); font-weight: 400;">false</span>;
            <span style="color: rgb(255, 123, 114); font-weight: 400;">return</span>;
        }
        <span style="color: rgb(255, 123, 114); font-weight: 400;">case</span> CHRENDER_FORMAT_D32_SFLOAT:
        {
            <span style="color: rgb(255, 123, 114); font-weight: 400;">if</span> (is_depth) *is_depth = <span style="color: rgb(121, 192, 255); font-weight: 400;">true</span>;
            <span style="color: rgb(255, 123, 114); font-weight: 400;">if</span> (is_stencil) *is_stencil = <span style="color: rgb(121, 192, 255); font-weight: 400;">false</span>;
            <span style="color: rgb(255, 123, 114); font-weight: 400;">return</span>;
        }
        <span style="color: rgb(255, 123, 114); font-weight: 400;">case</span> CHRENDER_FORMAT_D16_UNORM_S8_UINT:
        {
            <span style="color: rgb(255, 123, 114); font-weight: 400;">if</span> (is_depth) *is_depth = <span style="color: rgb(121, 192, 255); font-weight: 400;">true</span>;
            <span style="color: rgb(255, 123, 114); font-weight: 400;">if</span> (is_stencil) *is_stencil = <span style="color: rgb(121, 192, 255); font-weight: 400;">true</span>;
            <span style="color: rgb(255, 123, 114); font-weight: 400;">return</span>;
        }
        <span style="color: rgb(255, 123, 114); font-weight: 400;">case</span> CHRENDER_FORMAT_D24_UNORM_S8_UINT:
        {
            <span style="color: rgb(255, 123, 114); font-weight: 400;">if</span> (is_depth) *is_depth = <span style="color: rgb(121, 192, 255); font-weight: 400;">true</span>;
            <span style="color: rgb(255, 123, 114); font-weight: 400;">if</span> (is_stencil) *is_stencil = <span style="color: rgb(121, 192, 255); font-weight: 400;">true</span>;
            <span style="color: rgb(255, 123, 114); font-weight: 400;">return</span>;
        }
        <span style="color: rgb(255, 123, 114); font-weight: 400;">case</span> CHRENDER_FORMAT_D32_SFLOAT_S8_UINT:
        {
            <span style="color: rgb(255, 123, 114); font-weight: 400;">if</span> (is_depth) *is_depth = <span style="color: rgb(121, 192, 255); font-weight: 400;">true</span>;
            <span style="color: rgb(255, 123, 114); font-weight: 400;">if</span> (is_stencil) * is_stencil = <span style="color: rgb(121, 192, 255); font-weight: 400;">true</span>;
            <span style="color: rgb(255, 123, 114); font-weight: 400;">return</span>;
        }
    }
    
    <span style="color: rgb(255, 123, 114); font-weight: 400;">if</span> (is_depth) *is_depth = <span style="color: rgb(121, 192, 255); font-weight: 400;">false</span>;
    <span style="color: rgb(255, 123, 114); font-weight: 400;">if</span> (is_stencil) *is_stencil = <span style="color: rgb(121, 192, 255); font-weight: 400;">false</span>;
}


<span style="color: rgb(255, 123, 114); font-weight: 400;">void</span> <span style="color: rgb(210, 168, 255); font-weight: 400;">chrender_vulkan_check_vkdepthstencil</span><span style="color: rgb(201, 209, 217); font-weight: 400;">(VkFormat format, <span style="color: rgb(255, 123, 114); font-weight: 400;">bool</span>* is_depth, <span style="color: rgb(255, 123, 114); font-weight: 400;">bool</span>* is_stencil)</span>
{
    <span style="color: rgb(255, 123, 114); font-weight: 400;">switch</span>(format)
    {
        <span style="color: rgb(255, 123, 114); font-weight: 400;">case</span> VK_FORMAT_D16_UNORM:
        {
            <span style="color: rgb(255, 123, 114); font-weight: 400;">if</span> (is_depth) *is_depth = <span style="color: rgb(121, 192, 255); font-weight: 400;">true</span>;
            <span style="color: rgb(255, 123, 114); font-weight: 400;">if</span> (is_stencil) *is_stencil = <span style="color: rgb(121, 192, 255); font-weight: 400;">false</span>;
            <span style="color: rgb(255, 123, 114); font-weight: 400;">return</span>;
        }
        <span style="color: rgb(255, 123, 114); font-weight: 400;">case</span> VK_FORMAT_X8_D24_UNORM_PACK32:
        {
            <span style="color: rgb(255, 123, 114); font-weight: 400;">if</span> (is_depth) *is_depth = <span style="color: rgb(121, 192, 255); font-weight: 400;">true</span>;
            <span style="color: rgb(255, 123, 114); font-weight: 400;">if</span> (is_stencil) *is_stencil = <span style="color: rgb(121, 192, 255); font-weight: 400;">false</span>;
            <span style="color: rgb(255, 123, 114); font-weight: 400;">return</span>;
        }
        <span style="color: rgb(255, 123, 114); font-weight: 400;">case</span> VK_FORMAT_D32_SFLOAT:
        {
            <span style="color: rgb(255, 123, 114); font-weight: 400;">if</span> (is_depth) *is_depth = <span style="color: rgb(121, 192, 255); font-weight: 400;">true</span>;
            <span style="color: rgb(255, 123, 114); font-weight: 400;">if</span> (is_stencil) *is_stencil = <span style="color: rgb(121, 192, 255); font-weight: 400;">false</span>;
            <span style="color: rgb(255, 123, 114); font-weight: 400;">return</span>;
        }
        <span style="color: rgb(255, 123, 114); font-weight: 400;">case</span> VK_FORMAT_D16_UNORM_S8_UINT:
        {
            <span style="color: rgb(255, 123, 114); font-weight: 400;">if</span> (is_depth) *is_depth = <span style="color: rgb(121, 192, 255); font-weight: 400;">true</span>;
            <span style="color: rgb(255, 123, 114); font-weight: 400;">if</span> (is_stencil) *is_stencil = <span style="color: rgb(121, 192, 255); font-weight: 400;">true</span>;
            <span style="color: rgb(255, 123, 114); font-weight: 400;">return</span>;
        }
        <span style="color: rgb(255, 123, 114); font-weight: 400;">case</span> VK_FORMAT_D24_UNORM_S8_UINT:
        {
            <span style="color: rgb(255, 123, 114); font-weight: 400;">if</span> (is_depth) *is_depth = <span style="color: rgb(121, 192, 255); font-weight: 400;">true</span>;
            <span style="color: rgb(255, 123, 114); font-weight: 400;">if</span> (is_stencil) *is_stencil = <span style="color: rgb(121, 192, 255); font-weight: 400;">true</span>;
            <span style="color: rgb(255, 123, 114); font-weight: 400;">return</span>;
        }
        <span style="color: rgb(255, 123, 114); font-weight: 400;">case</span> VK_FORMAT_D32_SFLOAT_S8_UINT:
        {
            <span style="color: rgb(255, 123, 114); font-weight: 400;">if</span> (is_depth) *is_depth = <span style="color: rgb(121, 192, 255); font-weight: 400;">true</span>;
            <span style="color: rgb(255, 123, 114); font-weight: 400;">if</span> (is_stencil) *is_stencil = <span style="color: rgb(121, 192, 255); font-weight: 400;">true</span>;
            <span style="color: rgb(255, 123, 114); font-weight: 400;">return</span>;
        }
    }
    
    <span style="color: rgb(255, 123, 114); font-weight: 400;">if</span> (is_depth) *is_depth = <span style="color: rgb(121, 192, 255); font-weight: 400;">false</span>;
    <span style="color: rgb(255, 123, 114); font-weight: 400;">if</span> (is_stencil) *is_stencil = <span style="color: rgb(121, 192, 255); font-weight: 400;">false</span>;
}
</pre>
</details>


구현한 것들 강조하고 싶은 것들의 리스트입니다.

* ChSTL: 커스텀 Allocator를 사용하는 모든 자료구조들
  * BuddyBlock and Arena Allocator
  * Robin HOOD Hash Map
  * Linear Algebra: Cholesky Decomposition, Conjugate Gradient Method.
* ChRender: Vulkan 1.3를 이용한 Rendering API
* ChImage
  * PNG Decoder (+ ZLIB Deflation)
  * BMP Decoder
* ChFontCook
  * OpenType/TrueType Font Decoder
  * Font Rasterizer (Scaline Algorithm)
* ChGUI
  * Immediate Mode GUI
  * One draw call GUI rendering, inspired by Our Machinery
* ChModelData
  * Obj File Parser



진행상황 스크린샷들 입니다:

* GUI: 버튼과 텍스트 위젯, 그리고 overlapped 멀티 윈도우들.

  {% include figure.liquid loading="eager" path="assets/img/chgui_window_overlapping.gif" class="img-fluid rounded z-depth-1" zoomable=true %}

* Obj 파일 파싱과 렌더링

  {% include figure.liquid loading="eager" path="assets/img/chlib_background.png" class="img-fluid rounded z-depth-1" zoomable=true %}

* Disney Principled BRDF

  {% include figure.liquid loading="eager" path="assets/img/chlib_pbr.png" class="img-fluid rounded z-depth-1" zoomable=true %}



## MeshOptimization

* 기간: 2023.01 - 2023.05
* [깃헙](https://github.com/lch32111/MeshOptimization)

{% include figure.liquid path="https://github.com/lch32111/MeshOptimization/raw/main/titleshot.png" class="img-fluid rounded z-depth-1" zoomable=true %}

{% include figure.liquid path="https://github.com/lch32111/MeshOptimization/raw/main/titlevideo.gif" class="img-fluid rounded z-depth-1" zoomable=true %}

 [Hoppe](https://hhoppe.com/) et al.의 Mesh Optimization 논문을 학교 수업 (COMP 6381 - Geometric Modeling)을 위해 공부했습니다. Hoppe의 [코드](https://github.com/hhoppe/Mesh-processing-library/blob/main/Meshfit/Meshfit.cpp)를 복사하여 제 코드 베이스에서 작동되게 만들었습니다. 학교 수업 제출물로서 논문을 이해하기 위해 코드를 작성헀고, mesh vertices를 무작위로 샘플된 points에 fitting하는 논문의 알고리즘의 첫 번째 단계에서 non-linear solvers를 적용하려고 했습니다 ([AMPL](https://ampl.com/) 사용). 논문에서는 simplificaiton operation이 한 번에 한 vertex에 대해서만 작동하기 때문에 linear least-squares problem을 locally하게 풀어나갔습니다. non-linear solvers를 적용하려는 저의 시도는 optimization 결과에 눈에 띄는 차이를 만들진 못했습니다. 그렇기에 이 구현물을 수업 제출물로 사용했습니다. 이 논문은 linear least-squares problem을 실제 적으로 적용하는 것을 공부하고 mesh의 HalfEdge 자료구조로 edge collapse, edge split, 그리고 edge swap같은 topological operations을 하는 것을 배우기에 매우 교육적입니다.



## MarchingCubeSDF

* 기간: 2022.09 - 2022.12
* [깃헙](https://github.com/lch32111/MarchingCubeSDF)

{% include figure.liquid path="https://github.com/lch32111/MarchingCubeSDF/raw/main/result.png" class="img-fulid rounded z-depth-1" zoomable=true %}

mesh로부터 SDF values를 계산하고, 이것을 OpenGL API로 marching cubes algorithm으로 렌더링 하는 것을 공부하기 위해 이 프로젝트를 했습니다. 이 프로그램은 연습만을 위한 것이고 최적화 되어있지 않습니다. 여기에서 사용된 코드 스타일은 빠른 구현을 위한 것입니다.

SDF values를 계산할 때, mesh의 한 triangle를 가지는 leaf node가 있는 AABB tree를 사용했습니다. BVH구조를 통해 grid point에 대해 가장 가까운 triangle를 탐색합니다. 한 query (grid) point에 대해 가장 가까운 삼각형을 얻고나서, 그 query point에서 삼각형에 있는 가장 가까운 point를 알 수 있습니다. closest point에서 query point로 향하는 vector는 triangle normal과 함께 grid point가 삼각형의 true plane에 있는지를 아는데 사용됩니다. 만약 true plane에 있다면, 그 query point는 메쉬 밖에 있고, 이것은 SDF value가 양수라는 것을 의미합니다. 만약 그렇지 않다면, SDF value는 음수(바깥)입니다. 이 프로세스를 더 가속화하기 위해 ThreadPool를 사용합니다.



## ChanGameEngine

* 기간: 2018-2021
* [깃헙](https://github.com/lch32111/ChanGameEngine)
* [영상](https://www.youtube.com/watch?v=KSpS1TO2YgM)

{% include figure.liquid path="https://github.com/lch32111/ChanGameEngine/raw/master/img/firstResult.png" class="img-fulid rounded z-depth-1" zoomable=true %}

{% include figure.liquid path="https://github.com/lch32111/ChanGameEngine/raw/master/img/firstResult.gif" class="img-fulid rounded z-depth-1" zoomable=true %}

컴퓨터 그래픽스, 물리, 그리고 게임엔진을 공부하기 위해 시작했던 첫 번째 개인 라이브러리 입니다. Deferred Shading, Lighting, Shadow Cast, Post Processing (HDR, Tone Mapping, Bloom, SSAO), Perlin noise로 Terrain Rendering과 같은 다양한 그래픽스 기능들을 구현했습니다. 물리 부분에 대해선, 충돌을 탐지하고 접점을 해결하는 간단한 물리엔진을 구현했습니다. 그 물리 엔진을 위해 Rigidbody Dynamics와 Sequential Impulse Constraint Solver를 공부했었습니다. 그 이후에, Bounding Volume Hierarchy를 이용한 multi-threaded ray tracer를 구현했습니다.



## GJK Collision Detection

* 기간: 2019
* [깃헙](https://github.com/lch32111/GJKPracticeBasedBox2D)

{% include figure.liquid path="https://github.com/lch32111/GJKPracticeBasedBox2D/raw/master/GJKResult.PNG" class="img-fulid rounded z-depth-1" zoomable=true %}

Box2D의 개발자인 Erin Catto의 Game Developer Conference (GDC) 발표 자료로 충돌 탐지에서 자주 사용되는 알고리즘을 공부하고 구현했습니다.
