
* 要注意使用SDWebImage在自定义图片组件上加载图片时, 会碰到该图片组件卸载的情况下, 内存缓存仍没有释放的问题(默认使用了内存缓存)
  此时则需要, 使用SDWebImage里提供的根据cacheKey(即是图片请求地址全路径)来删除该图片的内存缓存, 使内存进行释放

* 要注意使用Universal-Image-Loader时, 图片组件卸载后, 内存即会释放(默认不使用内存缓存, 防止OOM)