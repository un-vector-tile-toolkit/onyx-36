# onyx-36
customized onyx to read the smaller ZL module (2 levels) for specific use

## background  
Although many mbtiles are good at ZL6 module, ZL4 and ZL 5 work well for sparce area 

## install
```console
npm install -g pm2
git clone git@github.com:un-vector-tile-toolkit/onyx-36
cd onyx-36
npm install
mkdir config
vi config/default.hjson
```

## an example of config/default.hjson
```console
{
  morganFormat: tiny
  htdocsPath: htdocs
  port: 3000
  privkeyPath: /somewhere/privkey.pem
  fullchainPath: /somewhere/fullchain.pem
  chainPath: /somewhere/chain.pem
  logDirPath: log
  tz: {
    tapioca: 6
  }
  defaultZ: 6
  mbtilesDir: /somewhere/mbtiles
  fontsDir: /somewhere/fonts
}
```

I use \*.pem files from [Let's Encrypt](https://letsencrypt.org/).

## run
```console
./pmserve.sh
```

## stop
```console
./pmstop.sh
```