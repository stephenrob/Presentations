### Containers for Software Preservation
<br>
<span style="font-size:0.8em;">Stephen Robinson</span>
<br>
<span style="font-size: 0.6em;">Digital Developer - Projects & Operations / Lancaster University Library</span>

Note:
Not a researcher, generally don't develop for research projects but issues of ensuring software can continually be run are common across business and research

---

+++?image=https://octodex.github.com/images/femalecodertocat.png
<!-- .slide: data-background-transition="none" -->
<span style="color: gray; font-size:0.3em; position: fixed; bottom: 10px; left: 40%; z-index: 999">the <b>Female Codertocat </b> by [jeejkang](https://github.com/jeejkang)</span>

Note:
Start a couple of steps back, been developing software locally, preparing it for use and testing it

+++?image=https://upload.wikimedia.org/wikipedia/commons/8/87/Octicons-git-pull-request.svg
<!-- .slide: data-background-transition="none" -->
<span style="color: gray; font-size:0.3em; position: fixed; bottom: 10px; left: 10%; z-index: 999">By GitHub (https://github.com/github/octicons) [MIT (http://opensource.org/licenses/mit-license.php) or OFL (http://scripts.sil.org/cms/scripts/page.php?item_id=OFL_web)], via Wikimedia Commons</span>

Note:
All the code is ready and on Github and you've put it into the preservation system

+++?image=https://octodex.github.com/images/welcometocat.png
<!-- .slide: data-background-transition="none" -->
<span style="color: gray; font-size:0.3em; position: fixed; bottom: 10px; left: 40%; z-index: 999">the <b>Welcometocat </b> by [jglovier](https://github.com/jglovier) & [JohnCreek](https://github.com/JohnCreek)</span>

Note:
All is well your research has been published and your being cited.

---
## 2 Years Later

Note:
2 years later and you're working on something else and

+++?image=https://octodex.github.com/images/inspectocat.jpg
<!-- .slide: data-background-transition="none" -->
<span style="color: gray; font-size:0.3em; position: fixed; bottom: 10px; left: 40%; z-index: 999">the <b>Inspectocat </b> by [jasoncostello](https://github.com/jasoncostello)</span>

Note:
Others are looking at your code trying to reproduce your results or you are looking to reuse the software

+++

- Pull the code from GitHub |
- Retrieve the code from preservation system |
- Install the dependencies |

+++?image=https://octodex.github.com/images/deckfailcat.png
<!-- .slide: data-background-transition="none" -->
<span style="color: gray; font-size:0.3em; position: fixed; bottom: 10px; left: 40%; z-index: 999">the <b>Deckfailcat </b> by [mattgraham](https://github.com/mattgraham)</span>

Note:
FAIL - your new computer or OS doesn't support things your code depends on / your dependencies aren't available anymore, happens across all areas of software development and use

---

### Options

- Update the dependencies |
- Keep a machine/device around running it |
- Use Containers |

Note:
3 main options, some are better than others

+++

### Updating the dependencies

- Takes time |
- Breaking API changes |
- Logic changes |

Note:
Logic changes might happen as you update to new APIs or might be in underlying libraries that you don't even look at

+++

### Keeping the computer around

![Apple Mac](https://pbs.twimg.com/media/C4x43dSWMAI3jWU.jpg:small)

+++

### Using Containers

- Package the code |
- AND it's dependencies |
- <span>run this <b>anywhere</b></span> |

Note:
allow packing everything together including the dependencies

---

## Why Containers?

Allows the combination of:

- Source Code |
- Language Version |
- Dependant Libraries |
- System Libraries & Tools |

<span class="fragment">Into a single image that can be run anywhere</span>

--- 

## Preserving Containers

<span class="fragment" style="font-size: 0.8em;">Put the generated container image into the preservation system</span>
<br>
<span class="fragment" style="font-size: 0.8em;">Only half the problem</span>
<br>
<span class="fragment" style="font-size: 0.8em;">Still need to run the container image in the future</span>

Note:
The obvious of preserving the container image is only 1/2 the problem still need to run the container or no better than before

+++

### The Docker Problem

- Widely adopted and supported |
- Commercial company |
- Great for business |
- Not so great for preservation |

+++

### Open Container Initiative

> <span class="fragment">An open governance structure for the express purpose of creating open industry standards around container formats and runtime</span>

Note:
Launched by Docker, CoreOS and other leaders in the container industry

+++

### Image Format (OCI Image)

- Donated by Docker |
- Image Manifest |
- Image Configuration |
- 1+ Filesystem Serializations |

Note:
Image Manifest - contains metadata about the contents and dependencies of the image inc filesystem serializations
Image Configuration - information such as application arguments, environments, etc
Filesystem Serialization - archives that will be unpacked to make up the final runnable filesystem

+++

### Container Runtime (OCI-R)

- runC |
- Donated by Docker |

Note:
runC - a CLI tool for spawning and running containers according to the OCI specification

---

## OCI and Preservation

- OCI under Linux Foundation |
- No single commercial entity |
- Open format and runtime |

Note:
No commercial entity means the future usability is not under licenced conditions or at further cost

+++

Open and sustainable preservation option ensuring we can run containers in the future