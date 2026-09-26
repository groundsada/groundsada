```python
from dataclasses import dataclass
from typing import Tuple

class Meta(type):
    def __new__(cls, name, bases, attrs):
        new_cls = super().__new__(cls, name, bases, attrs)
        return dataclass(unsafe_hash=True, frozen=True)(new_cls)

class Bio(metaclass=Meta):
    name        : str = "Mohammad Firas Sada"
    designation : str = "Research Networking Systems Software Engineer"
    focus       : str = "HPC & AI/ML | FPGA | Cloud & DevOps"
    employer    : str = "ESnet (LBNL)"
    base        : str = "remote (always)"

class Stack(metaclass=Meta):
    languages   : Tuple[str, ...] = ("Bash", "Python", "C", "P4")
    platforms   : Tuple[str, ...] = ("Kubernetes", "NRP", "SENSE")
    network     : Tuple[str, ...] = ("eBPF", "sFlow", "segment routing", "SmartNICs")
    hardware    : Tuple[str, ...] = ("FPGA", "Qualcomm Cloud AI 100")

class Social(metaclass=Meta):
    site        : str = "groundsada.github.io"
    blog        : str = "groundsada.github.io/blog"
    github      : str = "groundsada"
    linkedin    : str = "msada"
    instagram   : str = "firas_sada"
```

<p>
<a href="https://groundsada.github.io"><img src="btn-site.svg" alt="site" /></a>
<a href="https://groundsada.github.io/blog"><img src="btn-blog.svg" alt="blog" /></a>
<a href="https://www.linkedin.com/in/msada"><img src="btn-linkedin.svg" alt="linkedin" /></a>
<a href="https://www.instagram.com/firas_sada/"><img src="btn-instagram.svg" alt="instagram" /></a>
</p>