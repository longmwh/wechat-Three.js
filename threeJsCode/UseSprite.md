**使用PlaneGeometry播放帧动画**


    var planeGeo = new THREE.PlaneGeometry(16, 16);
    var texture = new THREE.TextureLoader().load("images/prize_491.png");
    var planeMaterial = new THREE.MeshBasicMaterial({
      map: texture,
      transparent: true,
      opacity: 1
    });
    let plane = new THREE.Mesh(planeGeo, planeMaterial);
    plane.position.x = 0;
    plane.position.y = 0;
    plane.position.z = 0;
    this.scene.add(plane);

    var self = this;
    self.index = 1;
    self._texture2 = [];
    for (var i = 0; i < 24; i++) {
        var strTexture = "images/CueHoleEffect_207/CueHoleEffect_207_" + (i) + ".png";
        var texture = new THREE.TextureLoader().load(strTexture);
        self._texture2.push(texture);
    }
    window.setInterval(function() {
        plane.material.map = self._texture2[self.index - 1];
        self.index++;
        if (self.index > 24) {
            self.index = 1;
        }
    }, 100);

_通过创建一个PlaneGeometry对象，然后定时修改Plane的material上面的map来修改Plane显示的图片，这样就实现了帧动画_

_注意：要将plane材质属性transparent设置为true，这样图片中透明部分才不会显示出来_

_可以修改材质中的opacity属性来设置图片的透明度，实现渐隐效果_

__使用Sprite播放帧动画和使用plane播放帧动画类似，只是把创建plane修改为创建Sprite对象__

