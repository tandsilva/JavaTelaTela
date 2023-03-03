# JavaTelaTela
- Curso oficial do google sobre Machine Learning for Web Developers (Web ML): https://youtube.com/playlist?list=PLOU2XLYxmsILr3HQpqjLAUkIPa5EaZiui
- Projetos feitos com TensorFlow: https://youtube.com/playlist?list=PLQY2H8rRoyvzSZZuF0qJpoJxZR1NgzcZw
- Treinando ML no Google: https://teachablemachine.withgoogle.com/

## Aula01
- Codigo do Calculo: https://github.com/monaca-samples/blink-to-text/blob/f3d578ff641298913833b04e98e854bf1cfe38e1/src/js/blinkPrediction.js
- Dependencias do worker.js
```js
    import "https://unpkg.com/@tensorflow/tfjs-core@2.4.0/dist/tf-core.js"
    import "https://unpkg.com/@tensorflow/tfjs-converter@2.4.0/dist/tf-converter.js"
    import "https://unpkg.com/@tensorflow/tfjs-backend-webgl@2.4.0/dist/tf-backend-webgl.js"
    import "https://unpkg.com/@tensorflow-models/face-landmarks-detection@0.0.1/dist/face-landmarks-detection.js"
```
- base de dados usada: https://www.kaggle.com/code/vikassingh1996/netflix-movies-and-shows-plotly-recommender-sys/data
- Converter video para canvas: https://stackoverflow.com/questions/64249599/how-to-run-handpose-tfjs-model-in-web-worker
- blog tensorflow sobre deteccao de iris: https://blog.tensorflow.org/2020/11/iris-landmark-tracking-in-browser-with-MediaPipe-and-TensorFlowJS.html
- tensorflow lib: face-landmarks-detection: https://github.com/tensorflow/tfjs-models/blob/master/face-landmarks-detection
- workers api: https://developer.mozilla.org/en-US/docs/Web/API/Web_Workers_API/Using_web_workers
- module workers: https://web.dev/module-workers/
- verificar compatibilidade: caniuse.com
- outro exemplo fazendo blink detection: https://selvamsubbiah.com/mediapipe-iris-detection-in-tensorflow-js/
- identificando codigo morse com eye detection: https://medium.com/the-web-tub/recognising-eye-blinking-with-tensorflow-js-3c02b738850d
- layout usado: https://codepen.io/Gunnarhawk/pen/vYJEwoM
- Explicação do porque webgl, cpu, webassembly: https://youtu.be/3ive-w7oUis?t=333

## Aula02 
- Arquivo Gestures para copiar: https://github.com/andypotato/rock-paper-scissors/blob/54add341dbe83287c8ede69fbb006149a8145dd9/src/js/Gestures.js
- Imports do arquivo handGestureFactory:
```js
    import "https://cdn.jsdelivr.net/npm/@tensorflow/tfjs-core@4.2.0/dist/tf-core.min.js"
    import "https://unpkg.com/@tensorflow/tfjs-backend-webgl@3.7.0/dist/tf-backend-webgl.min.js"
    import "https://cdn.jsdelivr.net/npm/@mediapipe/hands@0.4.1646424915/hands.min.js"
    import "https://cdn.jsdelivr.net/npm/@tensorflow-models/hand-pose-detection@2.0.0/dist/hand-pose-detection.min.js"
    import "https://cdn.jsdelivr.net/npm/fingerpose@0.1.0/dist/fingerpose.min.js"
```
- Problema que encontrei na hora de usar webworker no hands.js: https://github.com/tensorflow/tfjs/issues/7380
- PR aberto no fingerpose: https://github.com/andypotato/fingerpose/pull/25
- Meu fingerpose: https://github.com/ErickWendel/fingerpose
- Jokenpo: https://github.com/andypotato/rock-paper-scissors
- Diagrama do TensorFlow HandPoseDetection: https://github.com/tensorflow/tfjs-models/tree/master/hand-pose-detection#keypoint-diagram

## Aula03
- Projeto Solar Hands: https://github.com/liady/solar-hands
- Indices dos dedos da API do tensorflow: https://github.com/tensorflow/tfjs-models/tree/a345f0c58522af25d80153ec27c6e999e45fdd42/hand-pose-detection#keypoint-diagram
- elementFromPoint API: https://developer.mozilla.org/en-US/docs/Web/API/Document/elementFromPoint

## Aula04
- Projeto publicado: https://erickwendel.github.io/semana-javascript-expert07-pre/classes/class04/
- Pergunta no Stack Overflow: https://stackoverflow.com/a/54212926/4087199
- PseudoStyler: https://github.com/TSedlar/pseudo-styler
  #####################################################------------------#############################################################################
  Pre-reqs
Este projeto foi criado usando Node.js v19.6
O ideal é que você use o projeto em ambiente Unix (Linux). Se você estiver no Windows, é recomendado que use o Windows Subsystem Linux pois nas aulas são mostrados comandos Linux que possam não existir no Windows.
Importante
Todo dia às 18hrs estou subindo o código das aulas do dia corrente em classes. Se você for iniciar o projeto, remova a pasta classes para iniciar do zero!
Running
Execute npm ci na pasta que contém o arquivo package.json para restaurar os pacotes
Execute npm start e em seguida vá para o seu navegador em http://localhost:3000 para visualizar a página acima
Checklist Features
Titles List

[] - Campo para pesquisa não deve travar ao digitar termo de pesquisa
[] - Deve desenhar mãos na tela e fazer com que elementos em segundo plano continuem sendo clicáveis 🙌
[] - Deve disparar scroll up quando usar a palma das mãos abertas 🖐
[] - Deve disparar scroll down quando usar a palma das mãos fechadas ✊
[] - Deve disparar click no elemento mais próximo quando usar gesto de pinça 🤏🏻
[] - Ao mover elementos na tela, deve disparar evento :hover em elementos em contexto
Video Player

[] - Deve ser possivel de reproduzir ou pausar videos com o piscar de olhos 😁
[] - Todo processamento de Machine Learning deve ser feito via Web worker
Desafios
[] - Aula 01 - Diferenciar piscada de olhos entre olho direito e esquerdo e atualizar log para mostrar qual olho que piscou.
[] - Aula 02 - Reconhecer gestos de mãos individuais e printar no log
[] - Aula 03 - Corrigir Banner de titulo de video, para ficar atrás do desenho das mãos e se tornar clicável
[] - Aula 04 - Usar as mãos virtuais também no Video Player
Desafio plus: implementar testes unitários e alcançar 100% de coverage (avançado)

Links mostrados nos aulas:
Reuni todos os links em referências
Considerações
Tire suas dúvidas sobre os desafios em nossa comunidade, o objetivo é você aprender de forma divertida. Surgiu dúvidas? Pergunte por lá!

Ao completar qualquer um dos desafios, envie no canal #desafios da comunidade no Discord

FAQ
browser-sync está lançando erros no Windows e nunca inicializa:
Solução: Trocar o browser-sync pelo http-server.
instale o http-server com npm i -D http-server
no package.json apague todo o comando do browser-sync e substitua por npx http-server .
agora o projeto vai estar executando na :8080 então vá no navegador e tente acessar o http://localhost:8080/ A unica coisa, é que o projeto não vai reiniciar quando voce alterar algum código, vai precisar dar um F5 na página toda vez que alterar algo
Erro no navegador de Webgl is not supported on this device
Digite chrome://gpu/ no Chrome para verificar se o webgl está habilitado.
Possíveis soluções:
Opção 1: Habilitar a aceleração de hardware quando dispponível
Chrome => Settings > System > Use hardware acceleration when available
Firefox => Browser options > Performance > Use hardware acceleration when available
Opção 2: Atualizar driver da placa de vídeo
Veja detalhes no webgl-is-not-supported-on-chrome-firefox
Opção 3: Trocar de WebGL para CPU (mais lento) ou Web Assembly
https://blog.tensorflow.org/2020/03/introducing-webassembly-backend-for-tensorflow-js.html
(agradecimentos ao usuario Volpin em nossa comunidade do Discord)
Créditos ao Layout
Interface baseada no projeto Streaming Service de gunnarhawk
