FROM mcr.microsoft.com/devcontainers/jekyll

USER root

# The Jekyll image currently contains an obsolete Yarn APT repository
# whose signing key is no longer valid.
RUN rm -f /etc/apt/sources.list.d/yarn.list
