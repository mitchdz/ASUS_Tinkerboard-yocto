# Build guide

```bash
git clone git://git.yoctoproject.org/poky -b gatesgarth

cd poky

git clone git://git.yoctoproject.org/meta-rockchip -b gatesgarth
git clone git://git.yoctoproject.org/meta-arm -b gatesgarth
git clone git://git.openembedded.org/meta-python2 -b gatesgarth
git clone git://git.openembedded.org/meta-openembedded -b gatesgarth
git clone https://github.com/mitchdz/meta-asus-tinkerboard-mitchdz

cd ../

mkdir -p build && cd build

# use meta-asus-tinkerboard-mitchdz local.conf.sample and bblayers.conf.sample
sed -i 's/poky/smes/g' ../asus-tinkerboard-mitchdz/.templateconf
. ../poky/oe-init-build-env .

bitbake core-image
```


# ASUS Tinker Board specifications summary

## Processor
* Rockchip RK3288 Cortex-A17 Quad-core SoC
	* Quad-core up to 1.6GHz or single-core up to 1.8GHz.
	* The CPU will operate at full capacity, take note of heat dissipation and AC adaptor stability.

## GPU
* ARM Mali-T764 GPU

## Display
* 1 x HDMI (up to 4K)
* 1 x 15-pint MIPI DSI (up to 1080p)
	* iGPU only supports H.264/H.265 4K hardware decoders

## Memory Size
* Dual-CH LPDDR3 2GB

## Storage
* Micro SD(TF) card slot


## Connectivity
* RTL8211E-VB-CG GB LAN 
* AW-NB1777NF 802.1 b/g/n wireless 
* BT 4.0 + EDR

## AUDIO
* RTL ALC4040 Codec with 1 x 3.5mm audio jack

## USB
* 4 x USB 2.0 ports

## Camera Interface
* 1 x 15-pin MIPI CSI slot for camera

## Internal headers
* 1 x 40-pin header
	* up to 28 x GPIO pins
	* up to 2 x SPI bus
	* up to 2 x 12C bus
	* up to 4 x UART
	* up to 2 x PWM
	* up to 1 x PCM/12S
	* 2 x 5V power pins
	* 2 x 3.3V power pins
	* 8 x ground pins
* 1 x 2-pin contact point
	* 1 x PWM signal
	* 1 x S/PDIF signal

## Power Connector
* Micro USB

## OS Support
* Debian

## Dimension
* 3.37" x 2.125"

## Warrant
* 1 year


