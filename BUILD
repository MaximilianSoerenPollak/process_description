# *******************************************************************************
# Copyright (c) 2025 Contributors to the Eclipse Foundation
#
# See the NOTICE file(s) distributed with this work for additional
# information regarding copyright ownership.
#
# This program and the accompanying materials are made available under the
# terms of the Apache License Version 2.0 which is available at
# https://www.apache.org/licenses/LICENSE-2.0
#
# SPDX-License-Identifier: Apache-2.0
# *******************************************************************************
load("@score_cr_checker//:cr_checker.bzl", "copyright_checker")

# *******************************************************************************
# Copyright (c) 2025 Contributors to the Eclipse Foundation
#
# See the NOTICE file(s) distributed with this work for additional
# information regarding copyright ownership.
#
# This program and the accompanying materials are made available under the
# terms of the Apache License Version 2.0 which is available at
# https://www.apache.org/licenses/LICENSE-2.0
#
# SPDX-License-Identifier: Apache-2.0
# *******************************************************************************
load("@score_format_checker//:macros.bzl", "use_format_targets")
load("@score_docs_as_code//:docs.bzl", "docs")

package(default_visibility = ["//visibility:public"])

# Enables formatting targets
#'bazel test //:format.check'
#'bazel run //:format.fix'
use_format_targets()

copyright_checker(
    name = "copyright",
    srcs = glob(
        [
            "process/**",
            "BUILD",
            "MODULE.bazel",
        ],
        exclude = ["process/trustable/**"],
        allow_empty = True
    ),
    config = "@score_cr_checker//resources:config",
    template = "@score_cr_checker//resources:templates",
    visibility = ["//visibility:public"],
)

docs (
    source_dir = "process",
)
