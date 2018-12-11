


使用three.js展示界面时，可以使用多个camera，
例如：可以使用一个camera（PerspectiveCamera）显示3d界面，一个camera（OrthographicCamera）来展示2d界面

      var renderer = new THREE.WebGLRenderer(wxfun.WebGLRendererParameters({
        'antialias': true
      }));
      renderer['setPixelRatio'](window.devicePixelRatio);
      renderer['setSize'](window.innerWidth, window.innerHeight);
      container['appendChild'](renderer['domElement']);
      renderer['shadowMap']['enabled'] = true;
      renderer['setClearColor'](0xFFFFFF, 1);
      //需要将autoClear 设置为false,
      renderer['autoClear'] = false;
      //renderer['autoClearColor'] = false;



    此处将renderer['autoClear']设置为false是为了不自动清理最后一个camera之前的camera渲染出来的界面，
    renderer['autoClear'] = false;
    这里将renderer['autoClear']设置为false后，renderer不会自动清理界面，需要我们在调用
    renderer['render'](this.scene, this.camera);之前
    手动调用renderer["clear"]();来清理上一帧绘制出的界面


   