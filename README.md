# scratch-the-dura
Begin to learn how to leverage Git, Docker, Jupyter, and various neuroinformatics tools for performing exciting science!

## The Desiderata
A valuable feature of science, in particular computationally-driven science, is reproducibility. When performing or reproducing
analyses there are several key features that can make this reproducibility particularly effective. Some of these are:

- the ability for anyone to download/access all tools and data used
- the ability for anyone to install or use the tools and data on their own
- interactive demonstrations showing how to use tools and interact with data
- the ability to test the robustness of findings/claims

Leveraging several popular open-source or accessible tools, all of these requirements can be easily met, providing a solid
base upon which we can develop, test, extend, or distribute scientific findings.

## The Solution
We propose one possible model for achieving all of these requirements - note that there are alternatives to each of these tools that
may be better for specific circumstances or applications, and the selected were chosen simply based upon popularity and general
usefulness.

To share data and code, we use Github\*. To ensure anybody can install and use our tool, we use Docker. To provide interactive
demonstrations, we use Jupyter Notebooks. To enable testing the robustness of our claims, we integrate analyses with Jupyter Widgets.

\**Note: Github is generally **not** an ideal place to store data, but in this particular example we are leveraging the Github LFS service
and the data files being stored are small. In practice, storing data through either a public repository or on the Cloud are better solutions.*

