This projects hosts the source code for a implementation of the known Livewire algorithm for image segmentation using graphic processing units, through NVidia's CUDA API.

## Video showing GPU based segmentation running CUDA and Qt on Linux ##

There's a small video showing one of the results of the project [here](http://www.youtube.com/watch?v=eH_Jojw9NWw)

## GPGPU BASED IMAGE SEGMENTATION LIVEWIRE ALGORITHM IMPLEMENTATION ##


### Master Thesis Abstract ###

This thesis presents a GPU implementation of the Livewire algorithm. Instead of using traditional architectures, like the CPU, this implementation focus advantages obtained using Single Instruction Multiple Data (SIMD) architectures. The algorithm is divided in three phases: Sobel or Laplacian ﬁlter convolution, image modeling as a grid graph and solving the non-negative weighted edges single source shortest path problem. In order to calculate the shortest path, a parallel approach is made through the development of an adapted version of the ∆-stepping algorithm for GPUs. Each part of the algorithm was programmed as a single kernel, which is executed and compiled to the GPU, using CUDA ( Compute Uniﬁed Device Architecture), available on NVidia GeForce 8 series. GPUs have been the ﬁrst SIMD commodity devices widely available on several desktops. Although originally designed for applications highly focused on rendering, GPGPU ( General Purpose Computing on Graphic Processing Units) researchers have shown that the huge processing power available on these devices as well as the recent advent of a programmable pipeline have made of GPUs an attractive option for low cost high performance platforms. Even though the implementation has used CUDA API, several other approaches are pointed out, showing a wide variety of alternatives such as other platforms – multicore CPUs, Cell processor –, other graphic APIs, such as Cg, OpenGL and DirectX, or even
different approaches like RapidMind and Brook, which make GPU access transparent. The conclusion of this thesis highlights a successful implementation of the algorithm using the GPU architecture showing advantages and disadvantages of this approach. A critical result analysis shows that intense speedups are seen in image ﬁltering algorithms. On the other hand, the wide use of dependent device memory look-ups has constrained ∆-stepping
algorithm from achieving higher performance than CPU implementation although a better performance is expected for wider graphs. If device memory access latency was decreased or if more threads were available, a huge increase in performance would be expected. Besides showing the viability of the Livewire algorithm implementation, this thesis makes available an open-source image segmentation GPU based application, which can be used as example for future GPU algorithm implementations at http://code.google.com/p/gpuwire/.

### Resumo da tese ###

Esta tese apresenta a implementação do algoritmo de segmentação de imagens Livewire em uma placa de vídeo, que é uma arquitetura Single Instruction Multiple Data(SIMD), ao invés da utilização tradicional da CPU. O algoritmo é dividido em três fases: aplicação do ﬁltro Sobel ou Laplaciano sobre a imagem, seguido de modelagem da mesma através de grafos do tipo grid e posterior resolução do menor caminho a partir de um dado nó. Para tal cálculo uma abordagem paralela feita através do desenvolvimento de uma versão adaptada do algoritmo ∆-stepping para placas de vídeo. Cada uma das partes
do algoritmo foi transformada em um núcleo que é executado e compilado na própria placa de vídeo, utilizando-se a arquitetura CUDA (Compute Uniﬁed Device Architecture) disponível na série 8 da NVidia GeForce. As placas de vídeo são os primeiros dispositivos SIMD amplamente disponíveis em diversos computadores. Embora originalmente desenvolvidos para aplicações de renderização, pesquisadores da área de GPGPU (General Purpose Computing on Graphic Processing Units) têm demonstrado que o imenso poder computacional destes dispositivos e a sua recente capacidade de programação fazem deles
uma alternativa atrativa como plataforma de alta-performance. A implementação foi focada na arquitetura CUDA, mas diversas outras abordagens são comentadas e referenciadas mostrando grande parte das alternativas disponíveis, como outras plataformas - CPUs com multicore, processador Cell -, outras APIs gráﬁcas como Cg e OpenGL, ou mesmo abordagens que deixam transparente o uso de GPUs, como RapidMind e Brook. A conclusão coloca em evidência o sucesso da implementação do algoritmo para a plataforma de GPUs ressaltando os aspectos positivos e negativos da abordagem utilizada. Uma análise crítica dos resultados demonstra que o processamento de imagens através de ﬁltros tem grande ganho de desempenho com relação a uma CPU, no entanto, devido a muitos acessos à memória do dispositivo, o algoritmo ∆-stepping não mostrou performance superior em tal arquitetura com os tamanhos de grafos testados, apontando uma maior melhora quanto maior o tamanho do grafo. Uma menor demora no acesso à memória local ou mesmo um maior número de threads poderiam aumentar muito a performance do algoritmo. Além da demonstração de viabilidade de implementação do algoritmo, esta tese
contribui disponibilizando uma aplicação open-source de segmentação de imagens através da GPU (em http://code.google.com/p/gpuwire/), servindo como base para futuras implementações na mesma arquitetura.