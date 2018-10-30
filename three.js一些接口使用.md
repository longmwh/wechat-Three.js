#PlaneBufferGeometry
##示例
var geometry = new THREE.PlaneBufferGeometry( 5, 20, 32 );
var material = new THREE.MeshBasicMaterial( {color: 0xffff00, side: THREE.DoubleSide} );
var plane = new THREE.Mesh( geometry, material );
scene.add( plane );

##构造函数
PlaneBufferGeometry(width : Float, height : Float, widthSegments : Integer, heightSegments : Integer)
width — Width along the X axis. Default is 1.
height — Height along the Y axis. Default is 1.
widthSegments — Optional. Default is 1. 宽分割为几份
heightSegments — Optional. Default is 1.高分割为几份


密码