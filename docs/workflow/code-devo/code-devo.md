---
layout: default
title: Developing a derivative
parent: Proposed Workflow
nav_order: 2.2
permalink: /docs/workflow/code-devo
---

# Developing a derivative
Two key principles:
1. **Never modify raw/original data files.** Always read raw data in to your environment and write to a new file. Be a good data steward, and save it somewhere safe that is accessible to others (as appropriate--ask your PI) and is regularly backed-up (i.e., not on your local drive).
2. **Never create a derivative manually (i.e., doing it "by hand")--this limits reproducibility and increases the risk of human error.** We get it--when trying to do something new, it may feel like you could accomplish it much faster by hand then by figuring out how to script it. **But**, we promise that the upfront cost to learn how to create a derivative via a script is worth it. First, you'll learn a new and likely transferable skill. Second, you can be confident that the transformation/alteration is applied accurately to all of the observations. Third, you'll create a script that you could apply to another, similar dataset later.

## What if I want to develop several, related derivatives?
If you're thinking of creating several, closely related derivatives, we think it makes sense to include the code to develop all of them in the same script. But they should be entered into the log as separate derivatives.

## Best and "good enough" practices
### Variable naming
Thoughtful variable naming can prevent future headaches. 


### Documentation
Code documentation should explain *why*, rather that *what*. 
#### Other forms of documentation
[Docstrings](https://peps.python.org/pep-0257/) exist for a module, function, class, or method definition in Python

### Code formatting
There are specific style guides and conventions for different languages.
* Python: [PEP8](https://peps.python.org/pep-0008/)
* R: the [tidyverse style guide](https://style.tidyverse.org/index.html)
* Matlab: [Matlab style guidelines 2.0](https://www.mathworks.com/matlabcentral/fileexchange/46056-matlab-style-guidelines-2-0?s_tid=blogs_rc_6)

There are some automatic formatters (e.g., [blue](https://blue.readthedocs.io/en/latest/) and [black](https://black.readthedocs.io/en/stable/) for Python, [formatR](https://yihui.org/formatr/) for R) that can help you quickly learn how to improve your code. ***At a minimum***, we think it's important to try to at least format your code consistently 1) within a script, 2) between your scripts, and 3) between scripts from your team members. Converging on consistent formatting is a great goal!