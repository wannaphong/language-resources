# OpenFst, OpenGrm & Thrax
#
# It is possible to configure the Bazel workspace so that dependencies
# will be downloaded automatically. Unfortunately, the following fails
# with an HTTP 403 status code:
#
# new_http_archive(
#   name = "openfst",
#   url = "http://openfst.org/twiki/pub/FST/FstDownload/openfst-1.5.0.tar.gz",
#   sha256 = "01c2b810295a942fede5b711bd04bdc9677855c846fedcc999c792604e02177b",
#   build_file = "openfst.BUILD",
# )
#
# Work around this via a GitHub mirror of OpenFst:

new_git_repository(
    name = "openfst",
    build_file = "openfst.BUILD",
    remote = "https://github.com/mjansche/openfst.git",
    tag = "1.5.0",
)

# This does not work either; downloading fails with a 403 status code:
#
# new_http_archive(
#   name = "thrax",
#   url = "http://www.openfst.org/twiki/pub/GRM/ThraxDownload/thrax-1.1.0.tar.gz",
#   sha256 = "ce99d5b9b67b0d4ef3c9d7003aebad37f31235ef03191a44b11facd8e1b917da",
#   build_file = "thrax.BUILD",
# )

new_git_repository(
    name = "thrax",
    build_file = "thrax.BUILD",
    remote = "https://github.com/mjansche/thrax.git",
    tag = "1.1.0",
)
