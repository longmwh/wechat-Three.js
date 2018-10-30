Sprite 
=============
__总是面向摄像机，没有阴影__

    var spriteMap = new THREE.TextureLoader().load( "sprite.png" );
    var spriteMaterial = new THREE.SpriteMaterial( { map: spriteMap, color: 0xffffff } );
    var sprite = new THREE.Sprite( spriteMaterial );
    scene.add( sprite );

__构造函数__
    Sprite(material:Material)

_center:Vector   the sprite's anchor point 图片的锚点_

    SpriteMaterial
    var spriteMap = new THREE.TextureLoader.load("textures/sprite.png");
    var spriteMaterial = new THREE.ApriteMaterial({map:spriteMap,color:0xffffff});
    var sprite = new THREE.Sprite(spriteMaterial);
    sprite.scale.set(200,200,1);
    scene.add(sprite);
