# R

<iframe src="https://www.youtube.com/embed/MG1lZhixbS4" width="100%" height="200px"></iframe>

It looks like the `jupyter` command is being run inside the R session, which won't work. The `jupyter kernelspec list` command should be run in your terminal, not within the R console.

### Step-by-Step Instructions

1. **Register IRKernel in R**:
    - Open R from your terminal:
      ```bash
      R
      ```
    - Register the IRKernel:
      ```R
      IRkernel::installspec(user = TRUE)
      ```

2. **Exit the R session**:
    ```R
    q()
    ```

3. **Check available Jupyter kernels in your terminal**:
    ```bash
    jupyter kernelspec list
    ```

This should show the list of installed Jupyter kernels, including the `ir` kernel for R.

### Summary of Commands
1. **Open R and install the IRKernel**:
    ```bash
    R
    ```

    Inside the R console:
    ```R
    IRkernel::installspec(user = TRUE)
    q()
    ```

2. **Check Jupyter kernels in the terminal**:
    ```bash
    jupyter kernelspec list
    ```

This should resolve your issue and confirm that the R kernel is registered and available in Jupyter.

```{tableofcontents}
```
