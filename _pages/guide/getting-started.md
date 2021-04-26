---
autogenerated: true
title: User Guide/Getting Started
description: test description
---

{% include displaytitle content='Getting Started' %}

This part provides basic information on ImageJ installation, troubleshooting and update strategies. It discusses [Fiji↓](#sub:Fiji-intro)[↓](#nom-fiji) and [ImageJ2↓](#sub:ImageJ2intro) as well as third-party software related to ImageJ. Being impossible to document all the capabilities of ImageJ without exploring technical aspects of image processing, external resources allowing willing readers to know more about digital signal processing are also provided.

Introduction
------------

ImageJ is a [public domain](/ij/disclaimer.html) Java image processing and analysis program inspired by [NIH Image](/software/nih-image) for the Macintosh. It runs, either as an online applet or as a downloadable application, on any computer with a Java 1.5 or later virtual machine. [Downloadable distributions](/ij/download.html) are available for Windows, Mac OS X and Linux. It can display, edit, analyze, process, save and print 8--bit, 16--bit and 32--bit images. It can read many image formats including TIFF, GIF, JPEG, BMP, DICOM, FITS and 'raw'. It supports 'stacks' (and hyperstacks), a series of images that share a single window. It is multithreaded, so time-consuming operations such as image file reading can be performed in parallel with other operations<span class="FootOuter"><span class="SupFootMarker"> \[A\] </span><span class="HoverFoot"><span class="SupFootMarker"> \[A\] </span>A somehow outdated list of ImageJ's features is available [here](/ij/features.html)</span></span.

It can calculate area and pixel value statistics of user-defined selections. It can measure distances and angles. It can create density histograms and line profile plots. It supports standard image processing functions such as contrast manipulation, sharpening, smoothing, edge detection and median filtering.

It does geometric transformations such as scaling, rotation and flips. Image can be zoomed up to 32 : 1 and down to 1 : 32. All analysis and processing functions are available at any magnification factor. The program supports any number of windows (images) simultaneously, limited only by available memory.

Spatial calibration is available to provide real world dimensional measurements in units such as millimeters. Density or gray scale calibration is also available.

ImageJ was designed with an open architecture that provides extensibility via Java plugins. Custom acquisition, analysis and processing plugins can be developed using ImageJ's built in editor and Java compiler. User-written plugins make it possible to solve almost any image processing or analysis problem.

Being public domain open source software, an ImageJ user has the [four essential freedoms](http://wikieducator.org/The_right_license/The_essential_freedoms) defined by the Richard Stallman in 1986: 1) The freedom to run the program, for any purpose; 2) The freedom to study how the program works, and change it to make it do what you wish; 3) The freedom to redistribute copies so you can help your neighbor; 4) The freedom to improve the program, and release your improvements to the public, so that the whole community benefits.

ImageJ is being developed on Mac OS X using its built in editor and Java compiler, plus the *BBEdit* editor and the *Ant* build tool. The source code is freely [available](/ij/developer/source/index.html). The author, Wayne Rasband (&lt;wsr@nih.gov&gt;), is a Special Volunteer at the National Institute of Mental Health, Bethesda, Maryland, USA.

<div class="See">

[History of ImageJ](/about#history)

</div>

Installing and Maintaining ImageJ
---------------------------------

ImageJ can be downloaded from [here](/ij/download.html). Details on how to install ImageJ on [↓](#index-Linux)[Linux](/ij/docs/install/linux.html), [Mac OS 9](/ij/docs/install/mac.html), [↓](#index-Mac-OS-X)[Mac OS X](/ij/docs/install/osx.html) and [↓](#index-Windows-(OS))[Windows](/ij/docs/install/windows.html) <span class="bibcites">[1]([#biblio-1)\]</span> are available [here](/ij/docs/install/) ({% include bc path="Help | [Installation...↓](#sub:Installation...)" %} command). Specially useful are the platform-specific *Troubleshooting* and *Known Problems* sections. [↓](#index-Fiji)[Fiji↓](#sub:Fiji-intro) installation is described at <https://fiji.sc/wiki/index.php/downloads.

The downloaded package may not contain the latest bug fixes so it is recommended to upgrade ImageJ right after a first installation. [↓Updating](#index-Updates) IJ[↓](#nom-ij) consists only of running {% include bc path="Help | [Update ImageJ...↓](#sub:Update-ImageJ...)" %}, which will install the latest <span class="Filename">[ij.jar](/ij/upgrade/)</span> in the ImageJ folder (on Linux and Windows) or inside the ImageJ.app (on Mac OS X).

{% include bc path="Help | [Update ImageJ...↓](#sub:Update-ImageJ...)" %} can be used to upgrade (or downgrade) the <span class="Filename">ij.jar</span> file to *release updates* or *daily builds*. Release updates are announced frequently on the [IJ news website](/ij/notes.html) and are labelled alphabetically (e.g., v. 1.43m). Typically, these releases contain several new features and bug fixes, described in detail on the [ImageJ News page](/ij/notes.html). *Daily builds,* on the other hand, are labelled with numeric sub-indexes (e.g., v. 1.43n4) and are often released without documentation. Nevertheless, if available, release notes for daily builds can be found [here](/ij/source/release-notes.html). When a release cycle ends (v. 1.42 ended with 1.42q, v. 1.43 with 1.43u, etc.) an *installation package* is created, downloadable from [here](/ij/download.html). Typically, this package is bundled with a small list of add-ons ([Macros↓](#sub:Macros-ExtendingIJ), [Scripts↓](#sub:Scripts) and [Plugins↓](#sub:Plugins)).

<div class="See">

[Luts, Macros and Tools Updater](/ij/macros/toolsets/Luts%20Macros%20and%20Tools%20Updater.txt), a macro toolset that performs live-updating of [macros](/ij/macros/) listed on the ImageJ web site

</div>

### ImageJDistributions

ImageJ alone is not that powerful: it's real strength is the vast repertoire of [Plugins↓](#sub:Plugins) that extend ImageJ's functionality beyond its basic core. The many hundreds, probably thousands, freely available plugins from contributors around the world play a pivotal role in ImageJ's success <span class="bibcites">[<span class="bib-index">112</span>]([#biblio-162)\]</span>. Running {% include bc path="Help | [Update ImageJ...↓](#sub:Update-ImageJ...)" %}, however, will not update any of the plugins you may have installed<span class="FootOuter"><span class="SupFootMarker"> \[B\] </span><span class="HoverFoot"><span class="SupFootMarker"> \[B\] </span>Certain plugins, however, provide self-updating mechanisms (e.g., [ObjectJ](http://simon.bio.uva.nl/objectj/) and the [↓](#index-Bio-Formats)[OME Bio-Formats](http://loci.wisc.edu/software/bio-formats)).</span></span>.

ImageJ add-ons ([Plugins↓](#sub:Plugins), [Scripts↓](#sub:Scripts) and [Macros↓](#sub:Macros-ExtendingIJ)) are available from several sources ([ImageJ's plugins page](/ij/plugins/) \[{% include bc path="Help | [Plugins...↓](#sub:Plugins...)" %}\], [ImageJ Information and Documentation Portal](http://imagejdocu.tudor.lu/doku.php?id=plugin:start) and [Fiji's webpage](https://fiji.sc/wiki/index.php/Category:Plugins), among others) making manual updates of a daunting task. This reason alone, makes it extremely convenient the use of [ImageJDistributions↑](#sec:ImageJ-Distributions) bundled with a pre-organized collection of add-ons.

Below is a list of the most relevant projects that address the seeming difficult task of organizing and maintaining ImageJ beyond its basics. If you are a life scientist and have doubts about which distribution to choose you should opt for [Fiji↓](#sub:Fiji-intro). It is heavily maintained, offers an automatic updater, improved scripting capabilities and ships with powerful plugins. More specialized adaptations of ImageJ are discussed in [Software Packages Built on Top of ImageJ↓](#sub:Other-Software-Packages).

#### Fiji

[Fiji](https://fiji.sc/)[↓](#index-Fiji) (*Fiji Is Just ImageJ---Batteries included*) is a distribution of ImageJ together with Java, Java 3D and several plugins organized into a coherent menu structure. Citing its developers, "Fiji compares to ImageJ as Ubuntu compares to Linux". The main focus of Fiji is to assist research in life sciences, targeting image registration, stitching, segmentation, feature extraction and 3D visualization, among others. It also supports many scripting languages (BeanScript, Clojure, Jython, Python, Ruby, *see* [Scripting in Other Languages↓](#sec:ScriptingOtherLang)). Importantly, Fiji ships with a [convenient updater](https://fiji.sc/wiki/index.php/Update_Fiji) that knows whether your files are up-to-date, obsolete or locally modified. [Comprehensive documentation](https://fiji.sc/wiki/index.php/Documentation) is available for most of its plugins. The Fiji project was presented publicly for the first time at the [ImageJ User and Developer Conference](http://imagejconf.tudor.lu/doku.php) in November 2008.

#### MBF ImageJ

The [↓](#index-MBF-ImageJ)[↓](#index-ImageJ-for-Microscopy)[MBF ImageJ bundle](http://www.macbiophotonics.ca/imagej/) or *ImageJ for Microscopy* (formerly [WCIF-ImageJ](http://www.uhnres.utoronto.ca/facilities/wcif/imagej/)) features a collection of plugins and macros, collated and organized by Tony Collins at the MacBiophotonics facility, McMaster University. It is accompanied by a [comprehensive manual](http://www.macbiophotonics.ca/imagej/) describing how to use the bundle with light microscopy image data. It is a great resource for microscopists but is not maintained actively, lagging behind the development of core ImageJ.

Note that you can add plugins from MBF ImageJ to Fiji, combining the best of both programs. Actually, you can use multiple ImageJ distributions simultaneously, assemble your own ImageJ bundle by gathering the plugins that best serve your needs (probably, someone else at your institution already started one?) or create symbolic links to share plugins between different installations.

<div class="See">

[Description of all ImageJ-related projects](/about)

</div>

### Related Software

#### Software Packages Built on Top of ImageJ

<div class="Description">

<span class="Description-entry">**Bio7**</span> [Bio7](http://bio7.org/) is an integrated development environment for [↓ecological](#index-Bio7) modeling with a main focus on individual based modeling and spatially explicit models. Bio7 features: Statistical analysis (using R); Spatial statistics; Fast communication between [↓R](#index-R-(GNU-S)) and Java; BeanShell and Groovy support; Sensitivity analysis with an embedded flowchart editor and creation of 3D OpenGL (Jogl) models (*see also* RImageJ in [ImageJ Interoperability↓](#sec:ImageJ-Interoperability)).

</div>
<div class="Description">

<span class="Description-entry">BoneJ</span> [BoneJ](http://bonej.org/) [↓is](#index-BoneJ) a collection of tools for trabecular geometry and whole bone shape analysis.

</div>
<div class="Description">

<span class="Description-entry">**<span class="formula"><span class="unknown">\\micro</span></span>Manager**</span> [Micro-Manager](http://www.micro-manager.org/) is a software package for control of automated microscopes. It lets you execute common microscope image acquisition strategies such as time-lapses, multi-channel imaging, z-stacks, and combinations thereof. [↓](#index-Micro_Manager)<span class="formula"><span class="unknown">\\micro</span></span>Manager works with microscopes from all four major manufacturers, most scientific-grade cameras and many peripherals used in microscope imaging.

</div>
<div class="Description">

<span class="Description-entry">MRI--CIA***'</span> ***'[MRI Cell Image Analyzer](http://www.mri.cnrs.fr/index.php?m=38), developed by the Montpellier RIO Imaging facility (CNRS), is a rapid image analysis application development framework, adding visual scripting interface to ImageJ's capabilities. It can create batch applications as well as interactive applications. The applications include the topics "DNA combing", "quantification of stained proteins in cells", "comparison of intensity ratios between nuclei and cytoplasm" and "counting nuclei stained in different channels".

</div>
<div class="Description">

<span class="Description-entry">**ObjectJ**</span> [ObjectJ](http://simon.bio.uva.nl/objectj/index.html), the successor of [object-image](http://simon.bio.uva.nl/Object-Image/object-image.html), supports graphical vector objects that non-destructively mark images on a transparent layer. Vector objects can be placed manually or by macro commands. Composite objects can encapsulate different color-coded marker structures in order to bundle features that belong together. ObjectJ provides back-and-forth navigation between results and images. The results table supports statistics, sorting, color coding, qualifying and macro access.

</div>
<div class="Description">

<span class="Description-entry">**SalsaJ**</span> [SalsaJ](http://www.euhou.net/index.php?option=com_content&task=view&id=7&Itemid=9) is a student-friendly software developed specifically for the [EU-HOU project](http://www.euhou.net/). It is dedicated to image handling and analysis of astronomical images in the classroom. [↓SalsaJ](#index-SalsaJ) has been translated into several languages.

</div>
<div class="Description">

<span class="Description-entry">**[TrakEM]( )2**</span> [TrakEM2](http://www.ini.uzh.ch/~acardona/trakem2.html) is a program for morphological [↓data](#index-Data-mining) mining, three-dimensional [↓modeling](#index-Modeling) and image stitching, registration, editing and annotation <span class="bibcites">[<span class="bib-index">7</span>]([#biblio-57)\]</span>. [↓](#index-TrakEM2)[↓TrakEM](#index-Fiji)2 is [distributed with Fiji](https://fiji.sc/wiki/index.php/plugins/trakem2) and [capable of](http://www.ini.uzh.ch/~acardona/trakem2_manual.html):

<div class="vspace" style="height: -8pt;">
</div>
</div>

-   <div class="Description">

    <span class="Description-entry">**3D modeling**</span> Objects in 3D, defined by sequences of contours, or profiles, from which a skin, or mesh, can be constructed, and visualized in 3D.

    </div>
    <div class="Description">

    <span class="Description-entry">**Relational modeling**</span> The extraction of the map that describes links between objects. For example, which neuron contacts which other neurons through how many and which synapses.

    </div>

<div class="See">

[↓](#index-BioImageXD)[BioImageXD](http://www.bioimagexd.net/), [↓](#index-Endrov)[Endrov](http://www.endrov.net/), [↓](#index-Image-SXM)[Image SXM](http://www.liv.ac.uk/%7Esdb/ImageSXM/)

</div>

#### ImageJ Interoperability

Several packages exist that allow ImageJ to [↓interact](#index-Interoperability) with other applications/environments:

<div class="Description">

<span class="Description-entry">Bitplane Imaris</span> [ImarisXT](http://www.bitplane.com/go/products/imarisxt) can load and execute ImageJ plugins. [↓](#index-Imaris)[bpImarisAdapter](http://www.bitplane.com/go/products/imarisxt/xtensions/imagej) (Windows only and requiring valid licenses for Imaris and ImarisXT) allows the exchange of images between Imaris and ImageJ.

</div>
<div class="Description">

<span class="Description-entry">CellProfiler</span> [↓](#index-CellProfiler)[CellProfiler](http://www.cellprofiler.org/) <span class="bibcites">[<span class="bib-index">11</span>]([#biblio-61)\]</span> features [RunImageJ](http://cellprofiler.org/CPmanual/RunImageJ.html), a module that allows ImageJ plugins to be run in a CellProfiler pipeline.

</div>
<div class="Description">

<span class="Description-entry">Icy</span> [Icy](http://www.bioimageanalysis.org/icy/), an open source community software for [↓bio](#index-Icy)-imaging, executes ImageJ plugins with almost 100% plugin compatibility.

</div>
<div class="Description">

<span class="Description-entry">Knime</span> [↓](#index-Knime) [Knime](http://knime.org/) ([↓Konstanz](#nom-knime) Information Miner) contains several image processing nodes ([↓](#nom-knip)[KNIP](http://tech.knime.org/community/image-processing)[↓](#index-KNIP)) that are capable of executing ImageJ plugins and macros.

</div>
<div class="Description">

<span class="Description-entry">Open Microscopy Environment</span> [↓All](#nom-ome) [Open Microscopy Environment](http://www.openmicroscopy.org/) projects such as [↓](#index-Bio-Formats)[Bio-Formats](http://www.openmicroscopy.org/site/products/bio-formats), [VisBio](http://www.openmicroscopy.org/site/products/visbio) and [OMERO](http://www.openmicroscopy.org/site/products/omero) integrate well with ImageJ.

</div>
<div class="Description">

<span class="Description-entry">RImageJ --- R bindings for ImageJ</span> Bindings between ImageJ and [↓](#index-R-(GNU-S))[R (GNU S)](http://www.r-project.org/) — The free software environment for statistical computing and graphics. The documentation for RImageJ is available at http://cran.r-project.org/web/packages/RImageJ/RImageJ.pdf (*see also* Bio7 in [Software Packages Built on Top of ImageJ↑](#sub:Other-Software-Packages)).

</div>
<div class="Description">

<span class="Description-entry">MIJ --- Matlab--ImageJ bi-directional communication</span> A Java package for bi-directional data exchange between [↓Matlab](#index-MATLAB) and ImageJ, allowing to exchange images between the two imaging software. [↓MIJ](#index-MIJ) also allows MATLAB to access all built-in functions of ImageJ as well as third-party ImageJ plugins. The developers provide more information on the [MIJ](http://bigwww.epfl.ch/sage/soft/mij/) and [Matlab File Exchange](http://www.mathworks.com/matlabcentral/fileexchange/32344-hardware-accelerated-3d-viewer-for-matlab) websites. [Fiji↑](#sub:Fiji-intro) features <span class="code">[Miji.m](https://fiji.sc/wiki/index.php/Miji)</span>, which makes even more convenient to use the libraries and functions provided by Fiji's components from within Matlab.

</div>
<div class="See">

[ImageJ related links](/ij/links.html), list of [related imaging software](http://developer.imagej.net/category/web-links/related-imaging-software) on the [ImageJ2↓](#sub:ImageJ2intro) website

</div>

### ImageJ2

[ImageJ2](/software/imagej2) is a [federally funded](/about/funding), [multi-institution](/about/contributors) project dedicated to the development of the next-generation version of ImageJ: "[↓ImageJ](#index-ImageJ2)2". [↓](#index-ImageJ2)[↓ImageJ](#index-ImageDev)2 is a complete rewrite of ImageJ, that includes the current, stable version ImageJ ("ImageJ1") with a compatibility layer so that old-style plugins and macros can run the same as they currently do in ImageJ1. Below is a [summary](/ImageJ2_grant_proposal) of the original ImageJ2 project aims:

-   To create the next generation version of ImageJ and improve its core architecture based on the needs of the community.
-   To ensure ImageJ remains useful and relevant to the broadest possible community, maintaining backwards compatibility with ImageJ1 as close to 100% as possible.
-   Expand functionality by interfacing ImageJ with existing open-source programs.
-   To lead ImageJ development with a clear vision, avoiding duplication of efforts
-   To provide a central online resource for ImageJ: program downloads, a plugin repository, developer resources and more.

You can follow the ImageJ2 [project news](/news) for updates on the project.

Getting Help
------------

### Help on Image Analysis

[↓](#index-Ethics)[↓Below](#index-Acceptable-manipulation) is a list of online resources (in no particular order) related to image processing and scientific image analysis, complementing the list of [external resources on the IJ web site](/ij/links.html).

#### Ethics in Scientific Image Processing

-   [Online learning Tool for Research Integrity and Image Processing](http://www.ori.dhhs.gov/education/products/RIandImages/default.html)  
    This website, created by the [Office of Research Integrity](http://ori.dhhs.gov/), explains what is appropriate in image processing in science and what is not.
-   [Digital Imaging: Ethics (at the Cellular Imaging Facily Core, SEHSC)](http://swehsc.pharmacy.arizona.edu/exppath/micro/digimage_ethics.php)  
    This website, compiled by Douglas Cromey at the University of Alabama -- Birmingham, discusses thoroughly the topic of digital imaging ethics. It is recommended for all scientists. The website contains links to several external resources, including:
    <div class="vspace" style="height: -8pt;">
    </div>

    1.  [What's in a picture? The temptation of image manipulation](http://www.jcb.org/cgi/reprint/166/1/11) (2004) M Rossner and K M Yamada, J Cell Biology 166(1):11--15, <doi:10.1083/jcb.200406019>
    2.  [Not picture-perfect](http://www.nature.com/nature/journal/v439/n7079/full/439891b.html) (2006), Nature 439, 891--892, <doi:10.1038/439891b>.

#### Scientific Image Processing

-   [What you need to know about scientific image processing](https://fiji.sc/wiki/index.php/IP_Principles)  

Simple and clear, this [Fiji↑](#sub:Fiji-intro) webpage explains basic aspects of scientific image processing.

-   [imagingbook.com](http://www.imagingbook.com)  

Web site of *Digital Image Processing: An Algorithmic Introduction using Java* by Wilhelm Burger and Mark Burge <span class="bibcites">[<span class="bib-index">114</span>]([#biblio-164)\]</span>. This technical book provides a modern, self-contained, introduction to digital image processing techniques. Numerous complete Java implementations are provided, all of which work within ImageJ.

-   [Hypermedia Image Processing Reference (HIPR2)](http://homepages.inf.ed.ac.uk/rbf/HIPR2/)  

Developed at the Department of Artificial Intelligence in the University of Edinburgh, provides on-line reference and tutorial information on a wide range of image processing operations.

-   [IFN wikipage](https://ifn.mpi-cbg.de/wiki/ifn/index.php/Imaging_Facility_Network)  

The Imaging Facility Network (IFN) in Biopolis Dresden provides access to advanced microscopy systems and image processing. The website hosts high quality [teaching material](https://ifn.mpi-cbg.de/wiki/ifn/index.php/Teaching_Material) and useful links to external resources.

-   [stereology.info](http://www.stereology.info/)  

Stereology Information for the Biological Sciences, designed to introduce both basic and advanced concepts in the field of stereology.

<div class="See">

ImageJ Related Publications on page [1↓](#sec:IJ-related-pub)

</div>

### Help on ImageJ

Below is a list of the ImageJ [↓help](#index-Help-resources) resources that complement this guide (*see* [$↓](#sec:Guide-Formats)). Specific documentation on advanced uses of ImageJ (macro programming, plugin development, etc.) is discussed in [Extending ImageJ↓](#sec:Extending-ImageJ).

1.  The ImageJ [online documentation pages](/ij/docs/)  
    Can be accessed via the {% include bc path="Help | [Documentation...↓](#sub:Documentation...)" %} command.
2.  The [↓](#index-Fiji)[Fiji↑](#sub:Fiji-intro) webpage:  
    https://fiji.sc/
3.  The ImageJ Information and Documentation Portal (ImageJ wikipage):  
    http://imagejdocu.tudor.lu/doku.php
4.  Video [↓tutorials](#index-Tutorials) on the ImageJ Documentation Portal and the Fiji YouTube channel:  
    http://imagejdocu.tudor.lu/doku.php?id=video:start&s%5B%5D=video> and <http://www.youtube.com/user/fijichannel. New ImageJ users will probably profit from [Christine Labno's video tutorial](http://imagejdocu.tudor.lu/doku.php?id=video:beginner_help:imagej_beginner_s_tutorial).
5.  The [↓ImageJ](#index-MBF-ImageJ) for Microscopy manual  
    http://www.macbiophotonics.ca/imagej/
6.  Several online documents, most of them listed
    [here](/ij/links.html) and [here](/ij/docs/examples/).
7.  Mailing lists and forums:[↓](#index-Mailing-lists)
    1.  [**ImageJ**](/ij/list.html)  
        General user and developer discussion about ImageJ. Can be accessed via the {% include bc path="Help | [Mailing List...↓](#sub:List-Archives...)" %} command. This list is also mirrored at [Nabble](http://imagej.1557.n6.nabble.com/) and [Gmane](http://dir.gmane.org/gmane.comp.java.imagej). You may find it easier to search and browse the list archives on these mirrors. Specially useful are the [RSS feeds](Feed___rss.gmane.org_topics_excerpts_gmane.comp.java.imagej) and the *[frames and threads](http://news.gmane.org/gmane.comp.java.imagej)* view provided by Gmane.
    2.  [**Image.sc Forum**](https://forum.image.sc/tag/imagej)
        Scientific Community Image Forum, the official forum of many scientific imaging software projects including ImageJ.

#### Using Mailing-lists

If you are having problems with ImageJ, you should inquiry about them in the appropriated [↓list](#index-Help-resources). The ImageJ mailing list is an unmoderated forum subscribed by a knowledgeable worldwide user community with <span class="formula"><span class="unknown">\\thickapprox</span></span>2000 advanced users and developers. To have your questions promptly answered you should consider the following:

1.  Read the documentation files (described earlier in this section) before posting. Because there will always be a natural lag between the implementation of key features and their documentation it may be wise to check briefly the ImageJ news website ({% include bc path="Help | [ImageJ News...↓](#sub:ImageJ-News...)" %}).
2.  Look up the mailing list archives ({% include bc path="Help | [Mailing List...↓](#sub:List-Archives...)" %}). Most of your questions may have already been answered.
3.  If you think you are facing a [↓bug](#index-Bug-(reporting)) try to upgrade to the latest version of ImageJ ({% include bc path="Help | [Update ImageJ...↓](#sub:Update-ImageJ...)" %}). You should also check if you are running the latest version of the Java Virtual Machine for your operating system. Detailed instructions on how to submit a bug report are found [here](/ij/docs/faqs.html#bug).
4.  Remember that in most cases you can find answers within your own ImageJ installation without even connecting to the internet since the heuristics for finding commands or writing macros have been significantly improved in later versions (*see* [Finding Commands↓](#sec:Finding-Commands) and [Extending ImageJ↓](#sec:Extending-ImageJ)).
5.  As with any other mailing list, you should always follow basic [netiquette](http://en.wikipedia.org/wiki/Netiquette), namely:
    1.  Use descriptive subject lines — *Re: Problem with Image&gt;Set Scale command* is much more effective than a general *Re: Problem.*
    2.  Stay on topic — Do not post off-topic messages, unrelated to the message thread.
    3.  Be careful when sending attachments — Refrain from attaching large files. Use, e.g., a [file hosting service](http://en.wikipedia.org/wiki/File_hosting_service#comparison-of-notable-file-hosting-services) instead.
    4.  Edit replies — You should include only the minimum content that is necessary to provide a logical flow from the question to the answer, i.e., quote only as much as absolutely necessary and relevant.