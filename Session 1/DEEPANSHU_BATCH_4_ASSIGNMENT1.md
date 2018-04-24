# Convolution

"In mathematics, It is a mathematical operation on two functions to produce a third function."

A convolution is a mathematical operation that represents a signal passing through a LTI (Linear and Time-Invariant) system or filter. If we have a signal s(t) passing through a system with impulse response h(t), the output is the convolution of s(t) with h(t). The convolution is simply the integral of the product of the two functions (in this example the functions are s(t) and h(t)), where one is reversed.

![Visual comparison of convolution, cross-correlation and autocorrelation](https://upload.wikimedia.org/wikipedia/commons/2/21/Comparison_convolution_correlation.svg)

Convolution is similar to cross-correlation. For discrete real valued signals, they differ only in a time reversal in one of the signals. For continuous signals, the cross-correlation operator is the adjoint operator of the convolution operator.

It has applications that include probability, statistics, computer vision, natural language processing, image and signal processing, engineering, and differential equations.

Convolution and related operations are found in many applications in science, engineering and mathematics.

1. In Image Processing - It plays an important role in many important algorithms in edge detection and related processes.
2. In Digital Data Processing - Savitzky-Golay smoothing filters are used for the analysis of spectroscopic data. They can improve signal-to-noise ratio with minimal distortion of the spectra.
3. In Acoustics, reverberation is the convolution of the original sound with echoes from objects surrounding the sound source.
4. In Electrical Engineering - The convolution of one function with a second function gives the output of a linear time-invariant systems.
5. In Physics - A convolution operation makes an appearance, wherever there is a linear system with a "superposition principle".


# 1 x 1 Convolutions

1 x 1 convolution simply mean Just one filter with size 1x1 . 1x1 convolution leads to dimension reductionality.
For example, an image of 200 x 200 with 50 features on convolution with 20 filters of 1x1 would result in size of 200 x 200 x 20.

![Convolution with kernel of size 3x3](https://raw.githubusercontent.com/iamaaditya/iamaaditya.github.io/master/images/conv_arithmetic/full_padding_no_strides_transposed.gif)
Convolution with kernel of size 3x3

## 1x1 filters proposes two main purposes.

1. Add more nonlinearity to the representation learned by the previous layer so that supposedly enhance the representation of the network.

2. As used by the well known inception nets, it reduces the dimensions of the previous layer for faster computation and less information loss.

1x1 filter does not consider spatial information but takes channels into account.

## More Uses

1. 1x1 Convolution can be combined with Max pooling.

![Visual comparison of convolution, cross-correlation and autocorrelation](https://raw.githubusercontent.com/iamaaditya/iamaaditya.github.io/master/images/conv_arithmetic/numerical_max_pooling.gif)
Pooling with 1x1 convolution

2. 1x1 Convolution with higher strides leads to even more redution in data by decreasing resolution, while losing very little non-spatially correlated information.

![Visual comparison of convolution, cross-correlation and autocorrelation](https://raw.githubusercontent.com/iamaaditya/iamaaditya.github.io/master/images/conv_arithmetic/no_padding_strides.gif)
1x1 convolution with strides

3. Replace fully connected layers with 1x1 convolutions as Yann LeCun believes they are the same.


# How to create an account on GitHub and upload a sample project

GitHub is an online browser based distributed version control system for software developers using the Git revision control system.

## Create an account

If you already have a Github.com account you are ready to get started. Otherwise, you can set up your free account by following these steps:

1. Access Github.com. Go to the Github sign up page.
2. Enter a username, valid email address, and password in the supplied field. Use at least one lowercase letter, one number, and seven characters. Then click Sign up for GitHub.
3. Choose a plan. Select the Unlimited public repositories for free option.
4. You will receive a verification email at the address provided.
5. Click the emailed link to complete the verification process.
6. You finished! Your GitHub account created!

## Upload a sample project

Once you’ve signed in, you’ll create a new repository to get started. Follow the below steps to upload project on github.

1. Click the "New Repository" button in the "Your Repositories" pane on right side of the page.
2. On the new repository screen, you need to give this repository a special name to generate your project repo and an optional description and homepage URL.
3. Select the "Public" option to create a free public repo that anyone can access, or select the "Private" option to upgrade to a paid account and create a private repository.
4. Click the "Create Repository" button to create your repo.
5. You will get your github repo URL in both https and ssh network protocol. Copy the URL to add in your project later.
6. Create sample project in your system. Go inside to that sample project by command prompt or terminal.
7. Initialize the git using this command: git init
8. Add remote url which you obtained in 5th Step using this command: git remote add origin URL
9. Commit the code and add message to it using this command: git commit -m "Initial Commit"
10. Pust the code to your github profile using this command: git push origin master
11. Write this command to check your status of your repo: git status

"master" is a default branch name.
"origin" is a default remote repository name.
