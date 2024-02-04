ICONS := \
	logo_16x16.png \
	logo_24x24.png \
	logo_32x32.png \
	logo_48x48.png \
	logo_64x64.png

ANDROID_LAUNCHER := \
	logo_48x48.png \
	logo_-72x72.png \
	logo_96x96.png \
	logo_144x144.png \
	logo_192x192.png

IPHONE_LAUNCHER := \
	logo_60x60.png \
	logo_120x120.png

IPAD_LAUNCHER := \
	logo_76x76.png \
	logo_152x152.png

ALL_ICONS := $(ICONS) $(ANDROID_LAUNCHER) $(IPHONE_LAUNCHER) $(IPAD_LAUNCHER)

all: $(ALL_ICONS)

logo_16x16.png: icon-sm.svg
	convert -density 90 \
		-background transparent "$<" "$@"
logo_24x24.png: icon-sm.svg
	convert -density 135 \
		-background transparent "$<" "$@"
logo_32x32.png: icon-sm.svg
	convert -density 180 \
		-background transparent "$<" "$@"

logo_%.png: icon.svg
	convert -density $$[`echo $* | cut -d x -f 1` * 90 / 48] \
		-background transparent "$<" "$@"

clean:
	rm -f *.png
