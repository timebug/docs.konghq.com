---
# This file is for profiling an individual Kong extension.
# Duplicate this file in your own *publisher path* on your own branch.
# Your publisher path is relative to _app/_hub/.
# The path must consist only of alphanumeric characters and hyphens (-).
#
# The following YAML data must be filled out as prescribed by the comments
# on individual parameters. Also see documentation at:
# https://github.com/Kong/docs.konghq.com
# Remove inapplicable entries and superfluous comments as needed

name: # (required) The name of your extension.
  # Use capitals and spaces as needed.
publisher: # (required) The name of the entity publishing this extension.
  # Use capitals and spaces as needed.
  # If you are an individual, you might choose to use your GitHub handle, or your name.
  # If this is being published and supported by a company, please use your company name.
  # Note that every extension by a given publisher must have the exact same value.

categories: # (required) Uncomment ONE that applies.
  #- authentication
  #- security
  #- traffic-control
  #- serverless
  #- analytics-monitoring
  #- transformations
  #- logging
  #- deployment
# Array format only; if your plugin applies to multiple categories,
# uncomment the most applicable category.

type: # (required) String, one of:
  # plugin          | extensions of the core platform
  # integration     | extensions of the Kong Admin API

desc: # (required) 1-liner description; max 80 chars
description: #|
  # (required) extended description.
  # Use YAML piple notation for extended entries.
  # EXAMPLE long text format (do not use this entry)
  # description: |
  #   Maintain an indentation of two (2) spaces after denoting a block with
  #   YAML pipe notation.
  #
  #   Lorem Ipsum is simply dummy text of the printing and typesetting
  #   industry. Lorem Ipsum has been the industry's standard dummy text ever
  #   since the 1500s.

#support_url:
  # (Optional) A specific URL of your own for this extension.
  # Defaults to the url setting in your publisher profile.

#source_url:
  # (Optional) If your extension is open source, provide a link to your code.

#license_type:
  # (Optional) For open source, use the abbreviations in parentheses at:
  # https://opensource.org/licenses/alphabetical

#license_url:
  # (Optional) Link to your custom license.

#privacy_policy:
  # (Optional) If you have a custom privacy policy, place it here

#privacy_policy_url:
  # (Optional) Link to a remote privacy policy

#terms_of_service:
  # (Optional) Text describing your terms of service.

#terms_of_service_url:
  # (Optional) Link to your online TOS.

# COMPATIBILITY
# In the following sections, list Kong versions as array items.
# Versions are categorized by Kong edition and their known compatibility.
# Unlisted Kong versions will be considered incompatible.
# Uncomment at least one of 'community_edition' or 'enterprise_edition'.
# Add array-formatted lists of versions under their appropriate subsection.

kong_version_compatibility: # required
  #community_edition: # optional
    #compatible:
  #enterprise_edition: # optional
    #compatible:

# EXAMPLE kong_version_compatibility block: this example shows how to indicate
# various compatibilities. Also see other extension files in _app/_hub/ for more examples.
#kong_version_compatibility:
#  community_edition:
#    compatible:
#      - 0.12.x
#      - 0.13.x
#      - 0.14.x
#  enterprise_edition:
#    compatible:
#      - 0.32-x
#      - 0.33-x
#      - 0.34-x

#########################
# PLUGIN-ONLY SETTINGS below this line
# If your plugin is an extension of the core platform, ALL of the following
# lines must be completed.
# If NOT defined as a 'plugin' in line 32, delete all lines up to '# BEGIN MARKDOWN CONTENT'

params: # metadata about your plugin
  name: # name of the plugin in Kong (may differ from name: above)
  api_id:
    # boolean - whether this plugin can be applied to an API [[this needs more]]
  service_id:
    # boolean - whether this plugin can be applied to a Service.
    # Affects generation of examples and config table.
  consumer_id:
    # boolean - whether this plugin can be applied to a Consumer.
    # Affects generation of examples and config table.
  route_id:
    # whether this plugin can be applied to a Route.
    # Affects generation of examples and config table.
  protocols:
    # List of protocols this plugin is compatible with.
    # Valid values: "http", "https", "tcp", "tls"
    # Example: ["http", "https"]
  dbless_compatible:
    # Degree of compatibility with DB-less mode. Three values allowed:
    # 'yes', 'no' or 'partially'
  dbless_explanation:
    # Optional free-text explanation, usually containing details about the degree of
    # compatibility with DB-less.

  config: # Configuration settings for your plugin
    - name: # setting name
      required: # string - setting required status
        # options are 'yes', 'no', or 'semi'
        # 'semi' means dependent on other settings
      default: # any type - the default value (non-required settings only)
      value_in_examples:
        # If the field is to appear in examples, this is the value to use.
        # A required field with no value_in_examples entry will resort to
        # the one in default.
      description:
        # Explain what this setting does.
        # Use YAML's pipe (|) notation for longer entries.

  #  - name: # add additional setting blocks as needed, each demarcated by -
  extra:
    # This is for additional remarks about your configuration.
###############################################################################
# END YAML DATA
# Beneath the next --- use Markdown (redcarpet flavor) and HTML formatting only.
#
# The remainder of this file is for free-form description, instruction, and
# reference matter.
# If you include headers, your headers MUST start at Level 2 (parsing to
# h2 tag in HTML). Heading Level 2 is represented by ## notation
# preceding the header text. Subsequent headings,
# if you choose to use them, must be properly nested (eg. heading level 2 may
# be followed by another heading level 2, or by heading level 3, but must NOT be
# followed by heading level 4)
###############################################################################
# BEGIN MARKDOWN CONTENT
---

## Your first heading will go here
