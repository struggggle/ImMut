#### Experimental Setup
- **Android app subjects.**
16 actively maintained apps being well-verified by an existing static IID issue detector are selected as our evaluation subjects, they are:

|	Index	|	Image size	|	Download site	|
|	------	|	------		|	------		|
|	1	|	960×800 (0.76MPixels)	|	[download site](https://github.com/anonymouswhom/ImMut/tree/main/Inject-image-resources)	|
|	2	|	1920×1600 (3.1MPixels)	|	[download site](https://github.com/anonymouswhom/ImMut/tree/main/Inject-image-resources)	|
|	3	|	2835×2120 (6.0MPixels)	|	[download site](https://github.com/anonymouswhom/ImMut/tree/main/Inject-image-resources)	|
|	4	|	4032×3016 (12.2MPixels)	|	[download site](https://github.com/anonymouswhom/ImMut/tree/main/Inject-image-resources)	|


- **Injected image resource.**
Four images are prepared and will be injected to validate proper downsampling:

|	Index	|	App name	|	Version		|	Download site	|
|	------	|	------		|	------		|	------		|
|	1	|	 Conversations	|	2.9.6		|	[download site](https://github.com/anonymouswhom/ImMut/tree/main/Inject-image-resources)|
|	2	|	 Tusky		|	13.1		|	[download site](https://github.com/anonymouswhom/ImMut/tree/main/Inject-image-resources)|
|	3	|	 Kiss		|	3.15.5		|	[download site](https://github.com/anonymouswhom/ImMut/tree/main/Inject-image-resources)|
|	4	|	 CycleStreets	|	3.7.2		|	[download site](https://github.com/anonymouswhom/ImMut/tree/main/Inject-image-resources)|
|	5	|	 Qksms		|	3.8.1		|	[download site](https://github.com/anonymouswhom/ImMut/tree/main/Inject-image-resources)|
|	6	|	 Easy xkcd	|	7.3.9		|	[download site](https://github.com/anonymouswhom/ImMut/tree/main/Inject-image-resources)|
|	7	|	 Twidere	|	4.1.6		|	[download site](https://github.com/anonymouswhom/ImMut/tree/main/Inject-image-resources)|
|	8	|	 Newsblur	|	10.2.0		|	[download site](https://github.com/anonymouswhom/ImMut/tree/main/Inject-image-resources)|
|	9	|	 Antennapod	|	2.1.2		|	[download site](https://github.com/anonymouswhom/ImMut/tree/main/Inject-image-resources)|
|	10	|	 MoneyMangerEx	|	3.4		|	[download site](https://github.com/anonymouswhom/ImMut/tree/main/Inject-image-resources)|
|	11	|	 Slide4Reddit	|	6.6.1		|	[download site](https://github.com/anonymouswhom/ImMut/tree/main/Inject-image-resources)|
|	12	|	 Passandroid	|	3.5.6		|	[download site](https://github.com/anonymouswhom/ImMut/tree/main/Inject-image-resources)|
|	13	|	 SlideShow	|	2.9.0		|	[download site](https://github.com/anonymouswhom/ImMut/tree/main/Inject-image-resources)|
|	14	|	 MTG Family	|	3.6.6		|	[download site](https://github.com/anonymouswhom/ImMut/tree/main/Inject-image-resources)|
|	15	|	 Muzei		|	3.4.3		|	[download site](https://github.com/anonymouswhom/ImMut/tree/main/Inject-image-resources)|
|	16	|	 WordPress	|	16.3		|	[download site](https://github.com/anonymouswhom/ImMut/tree/main/Inject-image-resources)|

- **Functional test cases.**
51 functional test cases provided by a recruited post-graduate student that can cover major functionalities of the Android app subjects.


|	Index	|	App name	|	Functional test cases		|	Download site	|
|	------	|	------		|	------		|	------		|
|	1	|	 Conversations	|	(#1) Send an image (#2) Send images (#3) Login		|	[download site](https://github.com/anonymouswhom/ImMut/tree/main/Functional-test-cases)|
|	2	|	 Tusky		|	(#4) Add a note (#5) Open an image (#6) Open comment group (#7) Browse posts		|	[download site](https://github.com/anonymouswhom/ImMut/tree/main/Functional-test-cases)|
|	3	|	 Kiss		|	(#8) Click item	|	[download site](https://github.com/anonymouswhom/ImMut/tree/main/Functional-test-cases)|
|	4	|	 CycleStreets	|	(#9) Add a photo (#10) Swipe blogs (#11) Open a blog (#12) Open photomap		|	[download site](https://github.com/anonymouswhom/ImMut/tree/main/Functional-test-cases)|
|	5	|	 Qksms		|	(#13) Send an image (#14) Create contact (#15) Browse content		|	[download site](https://github.com/anonymouswhom/ImMut/tree/main/Functional-test-cases)|
|	6	|	 Easy xkcd	|	(#16) Browse cartoons (#17) Browse items		|	[download site](https://github.com/anonymouswhom/ImMut/tree/main/Functional-test-cases)|
|	7	|	 Twidere	|	(#18) Login (#19) Open a blog		|	[download site](https://github.com/anonymouswhom/ImMut/tree/main/Functional-test-cases)|
|	8	|	 Newsblur	|	(#20) Browse saved stories(1) (#21) Browse saved stories(2) (#22) Browse saved stories(3) (#23) Change list style (#24) Open profile (#25) Change List Style&open Story		|	[download site](https://github.com/anonymouswhom/ImMut/tree/main/Functional-test-cases)|
|	9	|	 Antennapod	|	(#26) Browse podcase(1) (#27) Browse podcase(2) (#28) Browse podcase(3) (#29) Open addPodcast (#30) Open addPodcasts		|	[download site](https://github.com/anonymouswhom/ImMut/tree/main/Functional-test-cases)|
|	10	|	 MoneyMangerEx	|	(#31) Create count (#32) Browse menu		|	[download site](https://github.com/anonymouswhom/ImMut/tree/main/Functional-test-cases)|
|	11	|	 Slide4Reddit	|	(#33) Browse themes (#34) Browse images (#35) Browse blogs		|	[download site](https://github.com/anonymouswhom/ImMut/tree/main/Functional-test-cases)|
|	12	|	 Passandroid	|	(#36) Add a pass (#37) Edit pass details pass (#38) Add passes		|	[download site](https://github.com/anonymouswhom/ImMut/tree/main/Functional-test-cases)|
|	13	|	 SlideShow	|	(#39) Browse images(1) (#40) Browse images(2) (#41) Browse images(3) (#42) Open image list (#43) Open pictureInPicture		|	[download site](https://github.com/anonymouswhom/ImMut/tree/main/Functional-test-cases)|
|	14	|	 MTG Family	|	(#44) Open “MoJhoSto”		|	[download site](https://github.com/anonymouswhom/ImMut/tree/main/Functional-test-cases)|
|	15	|	 Muzei		|	(#45) Set myPhotos (#46) Set singleArtwork		|	[download site](https://github.com/anonymouswhom/ImMut/tree/main/Functional-test-cases)|
|	16	|	 WordPress	|	(#47) Open media menu (#48) Open media (#49) Setting an image (#50) Edit a blog (#51) View a blog		|	[download site](https://github.com/anonymouswhom/ImMut/tree/main/Functional-test-cases)|
