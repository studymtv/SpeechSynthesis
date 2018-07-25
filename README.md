# Text-to-Speech Synthesis
딥러닝을 이용한 음성합성 관련 자료 모음

## Lectures & Seminars
* [책 읽어주는 딥러닝 (김태훈, 2017.11)](http://tv.naver.com/v/2292650)
  * Tacotron에 대해 쉽게 이해할 수 있도록 DEVIEW 2017에서 발표한 영상
* [모두의 연구소 WaveNet 스터디 영상 (김승일, 2017.10)](https://youtu.be/GyQnex_DK2k)
  * WaveNet에 대해 이해한 것을 설명 및 온라인 토론내용이 담긴 영상
* [Generative Model-Based Text-to-Speech Synthesis (Heiga Zen, 2017.02)](https://youtu.be/nsrSrYtKkT8)
  * WaveNet 논문 저자 중 1명인 Heiga Zen이 소개하는 TTS 전반적인 기술 및 WaveNet 소개 영상
  
## Dataset
* [CMU_ARCTIC (en)](http://festvox.org/cmu_arctic/)
  * CMU의 Language Technologies Institute에서 음성합성 연구를 위해 만든 US English 데이터셋
* [The LJ Speech Dataset (en)](https://keithito.com/LJ-Speech-Dataset/)
  * Keith Ito란 사람의 웹사이트에 올라와 있지만 어디서, 왜 만들었는지에 대한 내용은 찾지 못함
* [Blizzard 2012 (en)](http://www.cstr.ed.ac.uk/projects/blizzard/2012/phase_one/)
  * Blizzard Challenge 2012라는 코퍼스기반 음성합성 챌린지에서 사용된 데이터셋
* [CSTR VCTK Corpus (en)](http://homepages.inf.ed.ac.uk/jyamagis/page3/page58/page58.html)
  * English Multi-speaker Corpus for CSTR Voice Cloning Toolkit
### 한국어 코퍼스
* [KSS Dataset: Korean Single speaker Speech Dataset](https://www.kaggle.com/bryanpark/korean-single-speaker-speech-dataset)
  
## WaveNet
### Paper
* [WaveNet: A Generative Model for Raw Audio (2016.09)](https://arxiv.org/abs/1609.03499)
* [HybridNet: A Hybrid Neural Architecture to Speed-up Autoregressive Models (2018.02)](https://openreview.net/forum?id=rJoXrxZAZ) - Yanqi Zhou et al.
  * WaveNet보다 MOS가 높고, 오디오 생성속도는 2~4배까지 빠르다고 함.
  
### Articles
* [WaveNet: A Generative Model for Raw Audio (DeepMind Blog)](https://deepmind.com/blog/wavenet-generative-model-raw-audio/)

### Source Code
* https://github.com/ibab/tensorflow-wavenet
* https://github.com/r9y9/wavenet_vocoder (PyTorch)
* https://github.com/kan-bayashi/PytorchWaveNetVocoder (PyTorch)
  * [WaveNet Vocoder Samples](https://kan-bayashi.github.io/WaveNetVocoderSamples/)

#### Multi-GPU
WaveNet 학습시간이 너무 오래 걸려서 멀티 GPU를 이용하지 않으면 답이 나오지 않는 것 같다. 그와 관련된 코드 링크를 정리하였다.
* https://github.com/nakosung/tensorflow-wavenet/tree/multigpu (Tensorflow)
  * WaveNet multi GPU 구현 버전
* https://github.com/nakosung/tensorflow-wavenet/tree/model_parallel (Tensorflow)
  * WaveNet model parallelism 구현 버전

## Fast WaveNet
### Paper
* [Fast Wavenet Generation Algorithm (2016.11)](https://arxiv.org/abs/1611.09482)

### Articles

### Source Code
* https://github.com/tomlepaine/fast-wavenet
* https://github.com/dhpollack/fast-wavenet.pytorch (PyTorch)

## Parallel WaveNet
### Paper
* [Parallel WaveNet: Fast High-Fidelity Speech Synthesis (2017.11)](https://arxiv.org/abs/1711.10433)

### Articles
* [High-fidelity speech synthesis with WaveNet (DeepMind Blog)](https://deepmind.com/blog/high-fidelity-speech-synthesis-wavenet/) 
### Source Code
* https://github.com/kensun0/Parallel-Wavenet (not a complete implement)

## WaveRNN
### Paper
* [Efficient Neural Audio Synthesis (2018.02)](https://arxiv.org/abs/1802.08435)

## Deep Voice
### Paper
* [Deep Voice: Real-time Neural Text-to-Speech (2017.02)](https://arxiv.org/abs/1702.07825)

## Deep Voice 2
### Paper
* [Deep Voice 2: Multi-Speaker Neural Text-to-Speech (2017.05)](https://arxiv.org/abs/1705.08947)

## Deep Voice 3
### Paper
* [Deep Voice 3: Scaling Text-to-Speech with Convolutional Sequence Learning (2017.10)](https://arxiv.org/abs/1710.07654)

### Source Code
* https://github.com/Kyubyong/deepvoice3
* https://github.com/r9y9/deepvoice3_pytorch (PyTorch)

## Tacotron
### Paper
* [Tacotron: Towards End-to-End Speech Synthesis (2017.05)](https://arxiv.org/abs/1703.10135)

### Source Code
* https://github.com/keithito/tacotron
* https://github.com/Kyubyong/tacotron
* https://github.com/barronalex/Tacotron
* https://carpedm20.github.io/tacotron/ (Multi-speaker Tacotron in TensorFlow)
  * Tactron 1과 Deep Voice 2의 Multi-speaker를 구현한 프로젝트

## Tacotron 2
### Paper
* [Natural TTS Synthesis by Conditioning WaveNet on Mel Spectrogram Predictions (2017.12)](https://arxiv.org/abs/1712.05884)

### Articles
* [Tacotron 2: Generating Human-like Speech from Text (Google Research Blog)](https://research.googleblog.com/2017/12/tacotron-2-generating-human-like-speech.html)
### Source Code
* https://github.com/riverphoenix/tacotron2 (구현됨)
* https://github.com/Rayhane-mamah/Tacotron-2 (구현중)
* https://github.com/selap91/Tacotron2 (구현중)
* https://github.com/CapstoneInha/Tacotron2-rehearsal
* https://github.com/A-Jacobson/tacotron2 (PyTorch)
* https://github.com/maozhiqiang/tacotron_cn (구현 확인 필요/중국어)
* https://github.com/LGizkde/Tacotron2_Tao_Shujie (체크 필요)
* https://github.com/ruclion/tacotron_with_style_control (Style Control)

## Voice Cloning
* [ISPEECH VOICE CLONING DEMOS](https://www.ispeech.org/voice-cloning)
  * 유명한 사람들의 voice cloning 데모를 들어볼 수 있음
### Paper
* [Neural Voice Cloning with a Few Samples (2018.02)](https://arxiv.org/abs/1802.06006)

## Speed Up 전략
* [Fast Generation for Convolutional Autoregressive Models (2017.04)](https://arxiv.org/abs/1704.06001) - Prajit Ramachandran et al.
  * 이 기법을 Wavenet과 PixelCNN++ 모델에 적용하여 각각 최대 21배, 183배의 속도향상이 있었다고 함. 어디까지나 특정 상황에 대한 성능향상 최대치 이므로 실제 환경에서는 속도향상이 생각보다 크지 않을 수 있다는 것에 주의 필요.
