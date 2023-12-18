# Job Artifacts and Outputs

## Understanding Artifacts

<p align="center"><img src ="images/job-artifacts-intro.png" /></p>

### Uploading Artifacts

To upload certain output files as artifacts, we make use of a GitHub action called [upload-artifact](https://github.com/actions/upload-artifact)

The relative paths for artifacts are rooted against the current working directory.

:warning: Changing the current working directory at the job level will not be affect `upload-artifact` action. For `upload-artifact@v4` action, the **current working directory will always be the root of the current project**.

### Downloading Artifacts

To download artifacts, the `download-artifact` GitHub Action can be used. 

:warning: This action will unpack all the contents of the zipped artifact in the current working directory of a job.
