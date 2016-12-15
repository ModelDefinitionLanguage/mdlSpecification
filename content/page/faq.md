+++
title = "Frequently Asked Questions (FAQ)"
date = 2016-11-28T10:55:00Z
author = "Mike K Smith"
+++
## Why MDL?
### Why design a whole new language (MDL) to describe models?
The MDL has been designed to allow users to specify models in a consistent language,
regardless of the target tool they prefer to use for a given task (e.g. estimation),
and regardless of whether they intend to use the model for estimation, simulation,
or optimal design. This eliminates the transcoding needed today when using a model
in a different tool or for a different purpose.

MDL is also designed to be clear and explicit about model features, concentrating
on WHAT the model is saying rather than mechanics of HOW values are calculated.
This should mean that MDL is easier to share across disciplines, for example
between pharmacologists and statisticians or vice versa. Neither discipline should
have to learn tools used by the other in order to share models.

### Will the new language (MDL) really be better than existing languages?
The MDL is better than existing languages in the sense that it allows models to 
be specified in the same language, regardless of the target tool to be used for 
a given task (e.g. estimation), and regardless of whether the model is intended 
to be used for estimation, simulation, or optimal design, or all of the above. 
No existing language today allows this.

### Why would modellers want to learn a new language (MDL)?
Experienced modellers, who apply several different tools in their work, would 
want to learn MDL to get the benefit of not having to transcode models for use 
in different tools or for different purpose.

Beginners or less experienced modellers would want to learn MDL because this 
will allow them to work with several different tools without having to learn 
several different languages.

MDL is an Open Source language - it will be possible for the user community to 
contribute to MDL, to extend MDL, to evolve MDL. This is not possible with 
proprietary languages. They key thing is that changes within MDL map to 
[PharmML](http://pharmml.org) features, in order to facilitate down-stream 
conversion to target software like NONMEM, Monolix, etc.

### But I only use NONMEM...
You might only use NONMEM for estimation, but you might want to use other tools 
for simulation, like PKPDsim, RxODE, mlxR, mrgsolve... At that point you will
need to recode the model from NMTRAN to C++, or R ODE representation using
the deSolve package. 

You might also be interested in the open source tools for estimation, like
saemix, nlmixr, Stan etc. These tools do not have the same level of use as 
NONMEM, but they represent a useful set of tools that are freely available for
nonlinear mixed effect modelling. These might be useful to illustrate your models
to anyone in the world, without assuming that they have licenses for proprietary
tools.

## How can I get started with MDL?

### Are there any examples and descriptions of the new DDMoRe languages available?
When installing the Interoperability Framework, it comes with a UseCases project
folder pre-installed in the workspace. Within this folder are examples of models
in MDL and associated R scripts showing how to use these models for typical
modelling tasks. These models are also available via [SourceForge git repository](https://sourceforge.net/p/ddmore/use.cases/ci/master/tree/MDL/Product5.1/).

### What tools are available for writing MDL?
An [MDL-Editor](http://downloads.mdl.community/repository/mdl-ide/products/1.6.0/) 
is available for download. This is a cross-platform, Eclipse-based Integrated 
Development Environment (IDE) for writing MDL models incorporating syntax 
highlighting and grammar checks. It is available for Windows (
[32bit](http://downloads.mdl.community/repository/mdl-ide/products/1.6.0/eu.ddmore.mdleditor.site-1.6.0-SNAPSHOT-win32.win32.x86.zip) and 
[64bit](http://downloads.mdl.community/repository/mdl-ide/products/1.6.0/eu.ddmore.mdleditor.site-1.6.0-SNAPSHOT-win32.win32.x86_64.zip)), 
[Linux](http://downloads.mdl.community/repository/mdl-ide/products/1.6.0/eu.ddmore.mdleditor.site-1.6.0-SNAPSHOT-linux.gtk.x86_64.zip) and 
[Mac OS](http://downloads.mdl.community/repository/mdl-ide/products/1.6.0/eu.ddmore.mdleditor.site-1.6.0-SNAPSHOT-macosx.cocoa.x86_64.zip). Simply download the zip file and unzip to an appropriate location. 
An update site has been configured within Eclipse so that future updates to the 
MDL-Editor can be retrieved from within Eclipse without having to download 
another zip file. 

The MDL Editor can be used to develop models using MDL and to export these models
to PharmML, ready for upload to the DDMoRe repository: <http://repository.ddmore.eu>.

### But what if I want to run the models?
At the [ddmore.eu](http://ddmore.eu/instructions/user-guides)
website you'll also find instructions for downloading and installing the DDMoRe 
Interoperability Framework Standalone Execution Environment (SEE) demonstrator.
The SEE installers are available from [Sourceforge](https://sourceforge.net/projects/ddmore/files/install/SEE/Demonstrator-2.0.0/).
The SEE is a DDMoRe demonstration product which includes R, NONMEM, Monolix, 
BUGS, PFIM, PopED, simulx (from the `mlxR` R package). The SEE is only available 
for Windows at present.

### What resources are there to help me learn MDL and use the editor / SEE?
A [YouTube playlist](https://www.youtube.com/playlist?list=PL_GGUkhbiP3t0Q7wTqkQdMAw7yuC8xWa-) 
is available for videos detailing how to get started with the software.

A set of Use Case examples is provided with the SEE, which are also available on 
[SourceForge](https://sourceforge.net/p/ddmore/use.cases/ci/master/tree/MDL/Product5.1/).

### But won't it take ages for me to learn MDL...?
DDMoRe training courses devoted two days to learning about MDL, and language
basics. Following these two days, the majority of learners were able to encode
models and with support from the example Use Cases, documentation and the user
community were able to encode the majority of MDL models that you see in the 
[DDMoRe repository](http://repository.ddmore.eu).

## Converting existing code

### Can I translate code from NONMEM/other software into MDL without coding from
scratch?
For NONMEM, a tool is available for translating NMTRAN code into MDL. The tool 
is available at http://nmtran-to-mdl.mango-solutions.com/. Please, read the help
documentation since some additional information, and certain NMTRAN structure is
required to obtain a valid MDL. Alternatively, you can use the tool to generate 
a template that you can further modify within the Interoperability Framework.

## Contributing and extending MDL definition

### How can I report a problem with MDL?
Issues, bugs, feature requests, suggestions can be logged via 
the [Github Issues page](https://github.com/ModelDefinitionLanguage/website/issues).
Please label your item with "Website", "MDL Language", or "MDL-Editor" and the type
of issue ("bug","enhancement","help wanted","invalid","question") so that we can
direct it to the right place for action.  

### How can I contribute to MDL development?
MDL is an open language, which depends on community involvement to help refine 
it, extend it and to ensure that it is useful to the community in expressing
the models that you use. We're very happy for you to help us contribute to the 
MDL community, website, language. This can be through:  
  * submitting bugs and issues, feature requests  
  * by refining the MDL documentation; or by adding new example Use Cases to 
illustrate features  
  * suggesting grammar and syntax features and changes. The way to do this is to 
contribute to the Github repositories.Github maintains a useful ["Getting Started"](https://guides.github.com/activities/hello-world/)
guide if you need help on how to contribute to the repositories.  