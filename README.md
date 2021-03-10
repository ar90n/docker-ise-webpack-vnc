# docker-ise-webpack-vnc
ISE Webpack in Docker image

## How to build image
Download Xilinx_ISE_DS_Lin_14.7_1015_1.tar [this page](from https://www.xilinx.com/products/design-tools/ise-design-suite/ise-webpack.html).
And then clone this repository and run the docker build command with following options.

```bash
$ git clone git@github.com:ar90n/docker-ise-webpack-vnc.git
$ cd docker-ise-webpack-vnc
$ docker build -t docker-ise-webpack-vnc -f `pwd`/Dockerfile  <Path to the parent directory of Xilinx_ISE_DS_Lin_14.7_1015_1.tar>
```

## How to run
Generate and download your ISE Webpack License file from [this page](https://xilinx.com/getlicense.html).

```bash
$ docker run -it --rm -p 6080:80 -v <Path to license file>:/root/.Xilinx/Xilinx.lic docker-ise-webpack-vnc
```

And then you can access to `http://<docker host>:6080` to use ISE Webpack via VNC. 


## License
[Apache License 2.0](http://www.apache.org/licenses/LICENSE-2.0.txt)
