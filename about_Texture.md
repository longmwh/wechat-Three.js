Texture
==========
Create a texture to apply to a surface or as a reflection or refraction map.

__构造函数__
    Texture( image, mapping, wrapS, wrapT, magFilter, minFilter, format, type, anisotropy, encoding )

_例子_
// load a texture, set wrap mode to repeat
    var texture = new THREE.TextureLoader().load( "textures/water.jpg" );
    texture.wrapS = THREE.RepeatWrapping;
    texture.wrapT = THREE.RepeatWrapping;
    texture.repeat.set( 4, 4 );

