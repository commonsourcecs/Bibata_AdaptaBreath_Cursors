pkgname=bibata-adaptabreath-cursors-git
pkgver=0.3.1
pkgrel=1
pkgdesc="Bibata Based Cursor Themes Made For AdaptaBreath."
arch=('any')
url="https://gitlab.com/cscs/Bibata_AdaptaBreath_Cursors/"
license=('GPL')
makedepends=('inkscape' 'xorg-xcursorgen' 'gtk-engine-murrine')
source=("https://gitlab.com/cscs/Bibata_AdaptaBreath_Cursors/-/archive/master/Bibata_AdaptaBreath_Cursors-master.tar.gz")
sha256sums=(SKIP)

build() {
	cd "$srcdir/Bibata_AdaptaBreath_Cursors-master"

# Bibata Default
RAWSVGS_Bibata="src/Bibata_AdaptaBreath/svgs"
INDEX_Bibata="src/Bibata_AdaptaBreath/cursor.theme"
INDEX1_Bibata="src/Bibata_AdaptaBreath/index.theme"

# Bibata AdaptaBreathLuna

RAWSVGS_Bibata_AdaptaBreathLuna="src/Bibata_AdaptaBreathLuna/svgs"
INDEX_Bibata_AdaptaBreathLuna="src/Bibata_AdaptaBreathLuna/cursor.theme"
INDEX1_Bibata_AdaptaBreathLuna="src/Bibata_AdaptaBreathLuna/index.theme"

ALIASES="src/cursorList"


echo -ne "Checking Requirements...\\r"

if  ! type "inkscape" > /dev/null ; then
    echo -e "\\nFAIL: inkscape must be installed"
    exit 1
fi

if  ! type "xcursorgen" > /dev/null ; then
    echo -e "\\nFAIL: xcursorgen must be installed"
    exit 1
fi
echo -e "Checking Requirements... DONE"



echo -ne "Making Folders... $BASENAME\\r"
DIR11X_Bibata="build/Bibata_AdaptaBreath/96x96"
DIR10X_Bibata="build/Bibata_AdaptaBreath/88x88"
DIR9X_Bibata="build/Bibata_AdaptaBreath/80x80"
DIR8X_Bibata="build/Bibata_AdaptaBreath/72x72"
DIR7X_Bibata="build/Bibata_AdaptaBreath/64x64"
DIR6X_Bibata="build/Bibata_AdaptaBreath/56x56"
DIR5X_Bibata="build/Bibata_AdaptaBreath/48x48"
DIR4X_Bibata="build/Bibata_AdaptaBreath/40x40"
DIR3X_Bibata="build/Bibata_AdaptaBreath/32x32"
DIR2X_Bibata="build/Bibata_AdaptaBreath/28x28"
DIR1X_Bibata="build/Bibata_AdaptaBreath/24x24"

DIR11X_Bibata_AdaptaBreathLuna="build/Bibata_AdaptaBreathLuna/96x96"
DIR10X_Bibata_AdaptaBreathLuna="build/Bibata_AdaptaBreathLuna/88x88"
DIR9X_Bibata_AdaptaBreathLuna="build/Bibata_AdaptaBreathLuna/80x80"
DIR8X_Bibata_AdaptaBreathLuna="build/Bibata_AdaptaBreathLuna/72x72"
DIR7X_Bibata_AdaptaBreathLuna="build/Bibata_AdaptaBreathLuna/64x64"
DIR6X_Bibata_AdaptaBreathLuna="build/Bibata_AdaptaBreathLuna/56x56"
DIR5X_Bibata_AdaptaBreathLuna="build/Bibata_AdaptaBreathLuna/48x48"
DIR4X_Bibata_AdaptaBreathLuna="build/Bibata_AdaptaBreathLuna/40x40"
DIR3X_Bibata_AdaptaBreathLuna="build/Bibata_AdaptaBreathLuna/32x32"
DIR2X_Bibata_AdaptaBreathLuna="build/Bibata_AdaptaBreathLuna/28x28"
DIR1X_Bibata_AdaptaBreathLuna="build/Bibata_AdaptaBreathLuna/24x24"

OUTPUT_Bibata="$(grep --only-matching --perl-regex "(?<=Name\=).*$" $INDEX_Bibata)"
OUTPUT_Bibata=${OUTPUT_Bibata// /_}
OUTPUT_Bibata_AdaptaBreathLuna="$(grep --only-matching --perl-regex "(?<=Name\=).*$" $INDEX_Bibata_AdaptaBreathLuna)"
OUTPUT_Bibata_AdaptaBreathLuna=${OUTPUT_Bibata_AdaptaBreathLuna// /_}


mkdir -p "$DIR11X_Bibata" "$DIR10X_Bibata" "$DIR9X_Bibata" "$DIR8X_Bibata" "$DIR7X_Bibata" "$DIR6X_Bibata" "$DIR5X_Bibata" "$DIR4X_Bibata" "$DIR3X_Bibata" "$DIR2X_Bibata" "$DIR1X_Bibata"

mkdir -p "$DIR11X_Bibata_AdaptaBreathLuna" "$DIR10X_Bibata_AdaptaBreathLuna" "$DIR9X_Bibata_AdaptaBreathLuna" "$DIR8X_Bibata_AdaptaBreathLuna" "$DIR7X_Bibata_AdaptaBreathLuna" "$DIR6X_Bibata_AdaptaBreathLuna" "$DIR5X_Bibata_AdaptaBreathLuna" "$DIR4X_Bibata_AdaptaBreathLuna" "$DIR3X_Bibata_AdaptaBreathLuna" "$DIR2X_Bibata_AdaptaBreathLuna" "$DIR1X_Bibata_AdaptaBreathLuna"

mkdir -p "$OUTPUT_Bibata/cursors"
mkdir -p "$OUTPUT_Bibata_AdaptaBreathLuna/cursors"
echo 'Making Folders... DONE';


for CUR in src/config/*.cursor; do
    BASENAME=$CUR
    BASENAME=${BASENAME##*/}
    BASENAME=${BASENAME%.*}

    echo -ne "\033[0KGenerating simple cursor pixmaps OF Bibata AdaptaBreath... $BASENAME\\r"

    inkscape -w 24 -h 24 --without-gui -f $RAWSVGS_Bibata/"$BASENAME".svg -e "$DIR1X_Bibata/$BASENAME.png" > /dev/null
    inkscape -w 28 -h 28 --without-gui -f $RAWSVGS_Bibata/"$BASENAME".svg -e "$DIR2X_Bibata/$BASENAME.png" > /dev/null
    inkscape -w 32 -h 32 --without-gui -f $RAWSVGS_Bibata/"$BASENAME".svg -e "$DIR3X_Bibata/$BASENAME.png" > /dev/null
    inkscape -w 40 -h 40 --without-gui -f $RAWSVGS_Bibata/"$BASENAME".svg -e "$DIR4X_Bibata/$BASENAME.png" > /dev/null
    inkscape -w 48 -h 48 --without-gui -f $RAWSVGS_Bibata/"$BASENAME".svg -e "$DIR5X_Bibata/$BASENAME.png" > /dev/null
    inkscape -w 56 -h 56 --without-gui -f $RAWSVGS_Bibata/"$BASENAME".svg -e "$DIR6X_Bibata/$BASENAME.png" > /dev/null
    inkscape -w 64 -h 64 --without-gui -f $RAWSVGS_Bibata/"$BASENAME".svg -e "$DIR7X_Bibata/$BASENAME.png" > /dev/null
    inkscape -w 72 -h 72 --without-gui -f $RAWSVGS_Bibata/"$BASENAME".svg -e "$DIR8X_Bibata/$BASENAME.png" > /dev/null
    inkscape -w 80 -h 80 --without-gui -f $RAWSVGS_Bibata/"$BASENAME".svg -e "$DIR9X_Bibata/$BASENAME.png" > /dev/null
    inkscape -w 88 -h 88 --without-gui -f $RAWSVGS_Bibata/"$BASENAME".svg -e "$DIR10X_Bibata/$BASENAME.png" > /dev/null
    inkscape -w 96 -h 96 --without-gui -f $RAWSVGS_Bibata/"$BASENAME".svg -e "$DIR11X_Bibata/$BASENAME.png" > /dev/null


done
    echo -e "\033[0KGenerating simple cursor pixmaps OF Bibata AdaptaBreath... DONE"

for CUR in src/config/*.cursor; do
    BASENAME=$CUR
    BASENAME=${BASENAME##*/}
    BASENAME=${BASENAME%.*}

    echo -ne "\033[0KGenerating simple cursor pixmaps OF Bibata AdaptaBreathLuna.. $BASENAME\\r"

    inkscape -w 24 -h 24 --without-gui -f $RAWSVGS_Bibata_AdaptaBreathLuna/"$BASENAME".svg -e "$DIR1X_Bibata_AdaptaBreathLuna/$BASENAME.png" > /dev/null
    inkscape -w 28 -h 28 --without-gui -f $RAWSVGS_Bibata_AdaptaBreathLuna/"$BASENAME".svg -e "$DIR2X_Bibata_AdaptaBreathLuna/$BASENAME.png" > /dev/null
    inkscape -w 32 -h 32 --without-gui -f $RAWSVGS_Bibata_AdaptaBreathLuna/"$BASENAME".svg -e "$DIR3X_Bibata_AdaptaBreathLuna/$BASENAME.png" > /dev/null
    inkscape -w 40 -h 40 --without-gui -f $RAWSVGS_Bibata_AdaptaBreathLuna/"$BASENAME".svg -e "$DIR4X_Bibata_AdaptaBreathLuna/$BASENAME.png" > /dev/null
    inkscape -w 48 -h 48 --without-gui -f $RAWSVGS_Bibata_AdaptaBreathLuna/"$BASENAME".svg -e "$DIR5X_Bibata_AdaptaBreathLuna/$BASENAME.png" > /dev/null
    inkscape -w 56 -h 56 --without-gui -f $RAWSVGS_Bibata_AdaptaBreathLuna/"$BASENAME".svg -e "$DIR6X_Bibata_AdaptaBreathLuna/$BASENAME.png" > /dev/null
    inkscape -w 64 -h 64 --without-gui -f $RAWSVGS_Bibata_AdaptaBreathLuna/"$BASENAME".svg -e "$DIR7X_Bibata_AdaptaBreathLuna/$BASENAME.png" > /dev/null
    inkscape -w 72 -h 72 --without-gui -f $RAWSVGS_Bibata_AdaptaBreathLuna/"$BASENAME".svg -e "$DIR8X_Bibata_AdaptaBreathLuna/$BASENAME.png" > /dev/null
    inkscape -w 80 -h 80 --without-gui -f $RAWSVGS_Bibata_AdaptaBreathLuna/"$BASENAME".svg -e "$DIR9X_Bibata_AdaptaBreathLuna/$BASENAME.png" > /dev/null
    inkscape -w 88 -h 88 --without-gui -f $RAWSVGS_Bibata_AdaptaBreathLuna/"$BASENAME".svg -e "$DIR10X_Bibata_AdaptaBreathLuna/$BASENAME.png" > /dev/null
    inkscape -w 96 -h 96 --without-gui -f $RAWSVGS_Bibata_AdaptaBreathLuna/"$BASENAME".svg -e "$DIR11X_Bibata_AdaptaBreathLuna/$BASENAME.png" > /dev/null

done
    echo -e "\033[0KGenerating simple cursor pixmaps OF Bibata AdaptaBreathLuna... DONE"

    echo -ne "\033[0KGenerating Animated Cursor Bibata AdaptaBreath... \\r"
for i in 01 02 03 04 05 06 07 08 09 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31 32 33 34 35 36 37 38 39 40 41 42 43 44 45
do
    echo -ne "\033[0KGenerating animated cursor pixmaps For Bibata AdaptaBreath Process... $i / 45 \\r"

    inkscape -w 24 -h 24 --without-gui -f $RAWSVGS_Bibata/progress-$i.svg -e "$DIR1X_Bibata/progress-$i.png" > /dev/null
    inkscape -w 28 -h 28 --without-gui -f $RAWSVGS_Bibata/progress-$i.svg -e "$DIR2X_Bibata/progress-$i.png" > /dev/null
    inkscape -w 32 -h 32 --without-gui -f $RAWSVGS_Bibata/progress-$i.svg -e "$DIR3X_Bibata/progress-$i.png" > /dev/null
    inkscape -w 40 -h 40 --without-gui -f $RAWSVGS_Bibata/progress-$i.svg -e "$DIR4X_Bibata/progress-$i.png" > /dev/null
    inkscape -w 48 -h 48 --without-gui -f $RAWSVGS_Bibata/progress-$i.svg -e "$DIR5X_Bibata/progress-$i.png" > /dev/null
    inkscape -w 56 -h 56 --without-gui -f $RAWSVGS_Bibata/progress-$i.svg -e "$DIR6X_Bibata/progress-$i.png" > /dev/null
    inkscape -w 64 -h 64 --without-gui -f $RAWSVGS_Bibata/progress-$i.svg -e "$DIR7X_Bibata/progress-$i.png" > /dev/null
    inkscape -w 72 -h 72 --without-gui -f $RAWSVGS_Bibata/progress-$i.svg -e "$DIR8X_Bibata/progress-$i.png" > /dev/null
    inkscape -w 80 -h 80 --without-gui -f $RAWSVGS_Bibata/progress-$i.svg -e "$DIR9X_Bibata/progress-$i.png" > /dev/null
    inkscape -w 88 -h 88 --without-gui -f $RAWSVGS_Bibata/progress-$i.svg -e "$DIR10X_Bibata/progress-$i.png" > /dev/null
    inkscape -w 96 -h 96 --without-gui -f $RAWSVGS_Bibata/progress-$i.svg -e "$DIR11X_Bibata/progress-$i.png" > /dev/null

done
    echo -e "\033[0KGenerating animated cursor pixmaps For Bibata AdaptaBreath Process... DONE"

for i in 01 02 03 04 05 06 07 08 09 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31 32 33 34 35 36 37 38 39 40 41 42 43 44 45
do
    echo -ne "\033[0KGenerating animated cursor pixmaps For Bibata AdaptaBreath Wait... $i / 45 \\r"

    inkscape -w 24 -h 24 --without-gui -f $RAWSVGS_Bibata/wait-$i.svg -e "$DIR1X_Bibata/wait-$i.png" > /dev/null
    inkscape -w 28 -h 28 --without-gui -f $RAWSVGS_Bibata/wait-$i.svg -e "$DIR2X_Bibata/wait-$i.png" > /dev/null
    inkscape -w 32 -h 32 --without-gui -f $RAWSVGS_Bibata/wait-$i.svg -e "$DIR3X_Bibata/wait-$i.png" > /dev/null
    inkscape -w 40 -h 40 --without-gui -f $RAWSVGS_Bibata/wait-$i.svg -e "$DIR4X_Bibata/wait-$i.png" > /dev/null
    inkscape -w 48 -h 48 --without-gui -f $RAWSVGS_Bibata/wait-$i.svg -e "$DIR5X_Bibata/wait-$i.png" > /dev/null
    inkscape -w 56 -h 56 --without-gui -f $RAWSVGS_Bibata/wait-$i.svg -e "$DIR6X_Bibata/wait-$i.png" > /dev/null
    inkscape -w 64 -h 64 --without-gui -f $RAWSVGS_Bibata/wait-$i.svg -e "$DIR7X_Bibata/wait-$i.png" > /dev/null
    inkscape -w 72 -h 72 --without-gui -f $RAWSVGS_Bibata/wait-$i.svg -e "$DIR8X_Bibata/wait-$i.png" > /dev/null
    inkscape -w 80 -h 80 --without-gui -f $RAWSVGS_Bibata/wait-$i.svg -e "$DIR9X_Bibata/wait-$i.png" > /dev/null
    inkscape -w 88 -h 88 --without-gui -f $RAWSVGS_Bibata/wait-$i.svg -e "$DIR10X_Bibata/wait-$i.png" > /dev/null
    inkscape -w 96 -h 96 --without-gui -f $RAWSVGS_Bibata/wait-$i.svg -e "$DIR11X_Bibata/wait-$i.png" > /dev/null

done
    echo -e "\033[0KGenerating animated cursor pixmaps For Bibata AdaptaBreath Wait... DONE"
    echo -ne "\033[0KGenerating Animated Cursor Bibata AdaptaBreath... DONE \\r"

    echo -ne "\033[0KGenerating Animated Cursor Bibata AdaptaBreathLuna... \\r"
for i in 01 02 03 04 05 06 07 08 09 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31 32 33 34 35 36 37 38 39 40 41 42 43 44 45
do
    echo -ne "\033[0KGenerating animated cursor pixmaps For Bibata AdaptaBreathLuna Process... $i / 45 \\r"

    inkscape -w 24 -h 24 --without-gui -f $RAWSVGS_Bibata_AdaptaBreathLuna/progress-$i.svg -e "$DIR1X_Bibata_AdaptaBreathLuna/progress-$i.png" > /dev/null
    inkscape -w 28 -h 28 --without-gui -f $RAWSVGS_Bibata_AdaptaBreathLuna/progress-$i.svg -e "$DIR2X_Bibata_AdaptaBreathLuna/progress-$i.png" > /dev/null
    inkscape -w 32 -h 32 --without-gui -f $RAWSVGS_Bibata_AdaptaBreathLuna/progress-$i.svg -e "$DIR3X_Bibata_AdaptaBreathLuna/progress-$i.png" > /dev/null
    inkscape -w 40 -h 40 --without-gui -f $RAWSVGS_Bibata_AdaptaBreathLuna/progress-$i.svg -e "$DIR4X_Bibata_AdaptaBreathLuna/progress-$i.png" > /dev/null
    inkscape -w 48 -h 48 --without-gui -f $RAWSVGS_Bibata_AdaptaBreathLuna/progress-$i.svg -e "$DIR5X_Bibata_AdaptaBreathLuna/progress-$i.png" > /dev/null
    inkscape -w 56 -h 56 --without-gui -f $RAWSVGS_Bibata_AdaptaBreathLuna/progress-$i.svg -e "$DIR6X_Bibata_AdaptaBreathLuna/progress-$i.png" > /dev/null
    inkscape -w 64 -h 64 --without-gui -f $RAWSVGS_Bibata_AdaptaBreathLuna/progress-$i.svg -e "$DIR7X_Bibata_AdaptaBreathLuna/progress-$i.png" > /dev/null
    inkscape -w 72 -h 72 --without-gui -f $RAWSVGS_Bibata_AdaptaBreathLuna/progress-$i.svg -e "$DIR8X_Bibata_AdaptaBreathLuna/progress-$i.png" > /dev/null
    inkscape -w 80 -h 80 --without-gui -f $RAWSVGS_Bibata_AdaptaBreathLuna/progress-$i.svg -e "$DIR9X_Bibata_AdaptaBreathLuna/progress-$i.png" > /dev/null
    inkscape -w 88 -h 88 --without-gui -f $RAWSVGS_Bibata_AdaptaBreathLuna/progress-$i.svg -e "$DIR10X_Bibata_AdaptaBreathLuna/progress-$i.png" > /dev/null
    inkscape -w 96 -h 96 --without-gui -f $RAWSVGS_Bibata_AdaptaBreathLuna/progress-$i.svg -e "$DIR11X_Bibata_AdaptaBreathLuna/progress-$i.png" > /dev/null

done
    echo -e "\033[0KGenerating animated cursor pixmaps For Bibata AdaptaBreathLuna Process... DONE"

for i in 01 02 03 04 05 06 07 08 09 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31 32 33 34 35 36 37 38 39 40 41 42 43 44 45
do
    echo -ne "\033[0KGenerating animated cursor pixmaps For Bibata AdaptaBreathLuna Wait... $i / 45 \\r"

    inkscape -w 24 -h 24 --without-gui -f $RAWSVGS_Bibata_AdaptaBreathLuna/wait-$i.svg -e "$DIR1X_Bibata_AdaptaBreathLuna/wait-$i.png" > /dev/null
    inkscape -w 28 -h 28 --without-gui -f $RAWSVGS_Bibata_AdaptaBreathLuna/wait-$i.svg -e "$DIR2X_Bibata_AdaptaBreathLuna/wait-$i.png" > /dev/null
    inkscape -w 32 -h 32 --without-gui -f $RAWSVGS_Bibata_AdaptaBreathLuna/wait-$i.svg -e "$DIR3X_Bibata_AdaptaBreathLuna/wait-$i.png" > /dev/null
    inkscape -w 40 -h 40 --without-gui -f $RAWSVGS_Bibata_AdaptaBreathLuna/wait-$i.svg -e "$DIR4X_Bibata_AdaptaBreathLuna/wait-$i.png" > /dev/null
    inkscape -w 48 -h 48 --without-gui -f $RAWSVGS_Bibata_AdaptaBreathLuna/wait-$i.svg -e "$DIR5X_Bibata_AdaptaBreathLuna/wait-$i.png" > /dev/null
    inkscape -w 56 -h 56 --without-gui -f $RAWSVGS_Bibata_AdaptaBreathLuna/wait-$i.svg -e "$DIR6X_Bibata_AdaptaBreathLuna/wait-$i.png" > /dev/null
    inkscape -w 64 -h 64 --without-gui -f $RAWSVGS_Bibata_AdaptaBreathLuna/wait-$i.svg -e "$DIR7X_Bibata_AdaptaBreathLuna/wait-$i.png" > /dev/null
    inkscape -w 72 -h 72 --without-gui -f $RAWSVGS_Bibata_AdaptaBreathLuna/wait-$i.svg -e "$DIR8X_Bibata_AdaptaBreathLuna/wait-$i.png" > /dev/null
    inkscape -w 80 -h 80 --without-gui -f $RAWSVGS_Bibata_AdaptaBreathLuna/wait-$i.svg -e "$DIR9X_Bibata_AdaptaBreathLuna/wait-$i.png" > /dev/null
    inkscape -w 88 -h 88 --without-gui -f $RAWSVGS_Bibata_AdaptaBreathLuna/wait-$i.svg -e "$DIR10X_Bibata_AdaptaBreathLuna/wait-$i.png" > /dev/null
    inkscape -w 96 -h 96 --without-gui -f $RAWSVGS_Bibata_AdaptaBreathLuna/wait-$i.svg -e "$DIR11X_Bibata_AdaptaBreathLuna/wait-$i.png" > /dev/null

done
    echo -e "\033[0KGenerating animated cursor pixmaps For Bibata AdaptaBreathLuna Wait... DONE"
    echo -ne "\033[0KGenerating Animated Cursor Bibata AdaptaBreathLuna... DONE \\r"

echo -ne "Generating cursor theme...\\r"
for CUR in src/config/*.cursor; do
    BASENAME=$CUR
    BASENAME=${BASENAME##*/}
    BASENAME=${BASENAME%.*}

    ERR="$( xcursorgen -p build/Bibata_AdaptaBreath "$CUR" "$OUTPUT_Bibata/cursors/$BASENAME" 2>&1 )"

    if [[ "$?" -ne "0" ]]; then
        echo "FAIL: $CUR $ERR"
    fi

    ERR="$( xcursorgen -p build/Bibata_AdaptaBreathLuna "$CUR" "$OUTPUT_Bibata_AdaptaBreathLuna/cursors/$BASENAME" 2>&1 )"

    if [[ "$?" -ne "0" ]]; then
        echo "FAIL: $CUR $ERR"
    fi

done
echo -e "Generating cursor theme... DONE"


echo -ne "Generating shortcuts...\\r"
while read -r ALIAS ; do
    FROM=${ALIAS% *}
    TO=${ALIAS#* }

    if [ -e "$OUTPUT_Bibata/cursors/$FROM" ] ; then
        continue
    fi
    ln -s "$TO" "$OUTPUT_Bibata/cursors/$FROM"

    if [ -e "$OUTPUT_Bibata_AdaptaBreathLuna/cursors/$FROM" ] ; then
        continue
    fi
    ln -s "$TO" "$OUTPUT_Bibata_AdaptaBreathLuna/cursors/$FROM"

done < $ALIASES
echo -e "\033[0KGenerating shortcuts... DONE"


echo -ne "Copying Theme Index...\\r"

    if ! [ -e "$OUTPUT_Bibata/$INDEX_Bibata" ] ; then
        cp $INDEX_Bibata "$OUTPUT_Bibata/cursor.theme"
        cp $INDEX1_Bibata "$OUTPUT_Bibata/index.theme"
    fi

    if ! [ -e "$OUTPUT_Bibata_AdaptaBreathLuna/$INDEX_Bibata_AdaptaBreathLuna" ] ; then
        cp $INDEX_Bibata_AdaptaBreathLuna "$OUTPUT_Bibata_AdaptaBreathLuna/cursor.theme"
        cp $INDEX1_Bibata_AdaptaBreathLuna "$OUTPUT_Bibata_AdaptaBreathLuna/index.theme"
    fi
echo -e "\033[0KCopying Theme Index... DONE"
}

package() {
	mkdir -p "$pkgdir/usr/share/icons"
	mv "$srcdir/Bibata_AdaptaBreath_Cursors-master/Bibata_AdaptaBreath" "$pkgdir/usr/share/icons/Bibata_AdaptaBreath"
	mv "$srcdir/Bibata_AdaptaBreath_Cursors-master/Bibata_AdaptaBreathLuna" "$pkgdir/usr/share/icons/Bibata_AdaptaBreathLuna"
} 
