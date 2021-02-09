# pixel-artist

### A toy API to convert any bitmap image in to RGB colours!

-----
[![Node](https://img.shields.io/badge/Javascript-Enabled-lightgreen.svg)](https://shields.io/) 
<!-- ![](screenshots/2021-02-08-22-44-12.png) -->
<img src="screenshots/2021-02-08-22-44-12.png" height="700">
## Demo

#### View a demo at [https://pixel-artist.herokuapp.com](https://pixel-artist.herokuapp.com)

#### Or try it with a random unsplash image

##### [https://pixel-artist.herokuapp.com/api/?cols=32&https://source.unsplash.com/random](https://pixel-artist.herokuapp.com/api/?cols=32&url=https://source.unsplash.com/520x640/?portrait)

## Install & run
#### Node
```bash
npm install
npm start
```
<img src="screenshots/2021-02-08-22-54-08.png" height="300">

#### Docker-compose 
```
docker-compose up
```
![](screenshots/2021-02-08-22-50-04.png)
#### Docker
```bash
docker build -t pixel-artist .
docker run -it --rm -p 80:6451 pixel-artist:latest 
```
<img src="screenshots/2021-02-08-22-52-16.png" height="500">
#### Open `localhost:80`
<img src="screenshots/2021-02-08-22-52-16.png" height="500">
![](screenshots/2021-02-08-22-47-58.png)
## Usage

Reach the hosted API at

```
https://pixel-artist.herokuapp.com/api/?cols=x&url=y
```

It accepts two parameters, columns: `cols` (min `4` max `64` default `32`); and `url` for any valid bitmap image

Fewer columns, the faster! Returns a multidimensional array and some meta data:

```json
{
   "pixels":[
      [
         "rgb(160, 144, 169)",
         "rgb(130, 114, 137)",
         "rgb(85, 108, 128)",
         "rgb(229, 244, 253)"
      ],
      [
         "rgb(208, 205, 220)",
         "rgb(162, 152, 149)",
         "rgb(150, 158, 173)",
         "rgb(123, 137, 152)"
      ],
      ...
   ],
   "meta":{
      "cols":4,
      "rows":5,
      "title":"Starry Night, Van Gogh"
   }
}
```

## Examples
|   | | |    
|---|---|--|
| [![Demo 1](public/screengrabs/thumbs/demo_1.png)](public/screengrabs/demo_1.png) | [![Demo 3](public/screengrabs/thumbs/demo_3.png)](public/screengrabs/demo_3.png) | [![Demo 4](public/screengrabs/thumbs/demo_4.png)](public/screengrabs/demo_4.png)
 | 
| [![Demo 2](public/screengrabs/thumbs/demo_2.png)](public/screengrabs/demo_2.png) | [![Demo 6](public/screengrabs/thumbs/demo_6.png)](public/screengrabs/demo_6.png) | [![Demo 7](public/screengrabs/thumbs/demo_7.png)](public/screengrabs/demo_7.png) |
| [![Demo 5](public/screengrabs/thumbs/demo_5.png)](public/screengrabs/demo_5.png) | [![Demo 9](public/screengrabs/thumbs/demo_9.png)](public/screengrabs/demo_9.png) | [![Demo 10](public/screengrabs/thumbs/demo_10.png)](public/screengrabs/demo_10.png) |
| [![Demo 11](public/screengrabs/thumbs/demo_11.png)](public/screengrabs/demo_11.png) | [![Demo 12](public/screengrabs/thumbs/demo_12.png)](public/screengrabs/demo_12.png) | [![Demo 13](public/screengrabs/thumbs/demo_13.png)](public/screengrabs/demo_13.png) |  
| [![Demo 14](public/screengrabs/thumbs/demo_14.png)](public/screengrabs/demo_14.png) | [![Demo 15](public/screengrabs/thumbs/demo_15.png)](public/screengrabs/demo_15.png) | [![Demo 16](public/screengrabs/thumbs/demo_16.png)](public/screengrabs/demo_16.png) | 
| [![Demo 17](public/screengrabs/thumbs/demo_17.png)](public/screengrabs/demo_17.png) | [![Demo 18](public/screengrabs/thumbs/demo_18.png)](public/screengrabs/demo_18.png) | [![Demo 19](public/screengrabs/thumbs/demo_19.png)](public/screengrabs/demo_19.png) | 
| [![Demo 20](public/screengrabs/thumbs/demo_20.png)](public/screengrabs/demo_20.png) | [![Demo 21](public/screengrabs/thumbs/demo_21.png)](public/screengrabs/demo_21.png) | [![Demo 22](public/screengrabs/thumbs/demo_22.png)](public/screengrabs/demo_22.png) |

# Development
### how to publish docker image to docker hub
```bash
git clone https://github.com/blackspike/pixel-artist.git

cd pixel-artist

docker build . -t wisehackermonkey/pixel-artist:latest

docker login

docker push wisehackermonkey/pixel-artist:latest 
```
# Contributors
<a href="https://github.com/blackspike/pixel-artist/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=blackspike/pixel-artist" />
</a>

Made with [contributors-img](https://contrib.rocks).


## License

#### This project is licensed under the [![License: Unlicense](https://img.shields.io/badge/license-Unlicense-blue.svg)](http://unlicense.org/).



