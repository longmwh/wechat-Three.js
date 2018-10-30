Texture
Create a texture to apply to a surface or as a reflection or refraction map.
构造函数
Texture( image, mapping, wrapS, wrapT, magFilter, minFilter, format, type, anisotropy, encoding )

例子
// load a texture, set wrap mode to repeat
var texture = new THREE.TextureLoader().load( "textures/water.jpg" );
texture.wrapS = THREE.RepeatWrapping;
texture.wrapT = THREE.RepeatWrapping;
texture.repeat.set( 4, 4 );

