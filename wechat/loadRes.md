
__用于加载json格式的模型__
    let modelLoader = new THREE.JSONLoader();
    modelLoader['load'](url, function(geometry, materials) {
                
    }


__加载ArrayBuffer类型的数据__
        var loader = new THREE.FileLoader();
        loader['setResponseType']('arraybuffer');
        loader['load'](url,
            // onLoad callback
            function(data) {
                //成功的回调
            },
            // onProgress callback
            function(xhr) {
            console.log((xhr.loaded / xhr.total * 100) + '% loaded');
            },
            // onError callback
            function(err) {
            console.error('An error happened');
            }
        );

