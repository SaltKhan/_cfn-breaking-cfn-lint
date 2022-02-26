# _cfn-breaking-cfn-lint
A yaml file breaking a version of cfn-lint

WSL Ubuntu 20.04

Python 3.8.10

cfn-lint 0.58.1

`cfn-lint -t eks-nodegroup.yaml --debug`

# Debug output
```
2022-02-27 01:31:19,445 - cfnlint - DEBUG - Looking for CFLINTRC before attempting to load
2022-02-27 01:31:19,447 - cfnlint - DEBUG - Validating User CFNLINTRC
2022-02-27 01:31:19,447 - cfnlint - DEBUG - Validating CFNLINTRC config with given JSONSchema
2022-02-27 01:31:19,447 - cfnlint - DEBUG - Schema used: {'$id': 'https://github.com/aws-cloudformation/cfn-python-lint/blob/main/src/cfnlint/data/CfnLintCli/config/schema.json', '$schema': 'http://json-schema.org/draft-07/schema#', 'additionalProperties': False, 'description': 'CFNLINTRC configuration schema', 'properties': {'append_rules': {'description': 'Location of directories to append rules from', 'items': {'type': 'string'}, 'type': 'array'}, 'configure_rules': {'additionalProperties': False, 'description': 'Configure rules', 'patternProperties': {'^.*$': {'patternProperties': {'^.*$': {'anyOf': [{'type': 'string'}, {'type': 'integer'}, {'type': 'boolean'}, {'items': {'type': 'string'}, 'type': 'array'}, {'items': {'type': 'integer'}, 'type': 'array'}, {'items': {'type': 'string'}, 'type': 'boolean'}]}}, 'type': 'object'}}, 'type': 'object'}, 'ignore_checks': {'description': 'List of checks to ignore', 'items': {'type': 'string'}, 'type': 'array'}, 'ignore_templates': {'description': 'Templates to ignore', 'items': {'type': 'string'}, 'type': 'array'}, 'include_checks': {'description': 'List of checks to include', 'items': {'type': 'string'}, 'type': 'array'}, 'mandatory_checks': {'description': 'List of mandatory checks to enforce', 'items': {'type': 'string'}, 'type': 'array'}, 'merge_configs': {'description': 'Merges lists between configuration layers', 'type': 'boolean'}, 'custom_rules': {'description': 'custom rule file to use', 'type': 'string'}, 'output_file': {'description': 'Path to the file to write the main output to', 'type': 'string'}, 'override_spec': {'description': 'Path to spec file to override with', 'type': 'string'}, 'regions': {'description': 'Regions to test against', 'items': {'type': 'string'}, 'type': 'array'}, 'registry_schemas': {'description': 'One or more directories of CloudFormation Registry Resource Schemas', 'items': {'type': 'string'}, 'type': 'array'}, 'templates': {'description': 'Templates to lint', 'items': {'type': 'string'}, 'type': 'array'}}, 'title': 'CFNLINTRC JSON Schema', 'type': 'object'}
2022-02-27 01:31:19,447 - cfnlint - DEBUG - Config used: {}
2022-02-27 01:31:19,449 - cfnlint - DEBUG - CFNLINTRC looks valid!
2022-02-27 01:31:19,449 - cfnlint - DEBUG - Validating Project CFNLINTRC
2022-02-27 01:31:19,449 - cfnlint - DEBUG - Validating CFNLINTRC config with given JSONSchema
2022-02-27 01:31:19,449 - cfnlint - DEBUG - Schema used: {'$id': 'https://github.com/aws-cloudformation/cfn-python-lint/blob/main/src/cfnlint/data/CfnLintCli/config/schema.json', '$schema': 'http://json-schema.org/draft-07/schema#', 'additionalProperties': False, 'description': 'CFNLINTRC configuration schema', 'properties': {'append_rules': {'description': 'Location of directories to append rules from', 'items': {'type': 'string'}, 'type': 'array'}, 'configure_rules': {'additionalProperties': False, 'description': 'Configure rules', 'patternProperties': {'^.*$': {'patternProperties': {'^.*$': {'anyOf': [{'type': 'string'}, {'type': 'integer'}, {'type': 'boolean'}, {'items': {'type': 'string'}, 'type': 'array'}, {'items': {'type': 'integer'}, 'type': 'array'}, {'items': {'type': 'string'}, 'type': 'boolean'}]}}, 'type': 'object'}}, 'type': 'object'}, 'ignore_checks': {'description': 'List of checks to ignore', 'items': {'type': 'string'}, 'type': 'array'}, 'ignore_templates': {'description': 'Templates to ignore', 'items': {'type': 'string'}, 'type': 'array'}, 'include_checks': {'description': 'List of checks to include', 'items': {'type': 'string'}, 'type': 'array'}, 'mandatory_checks': {'description': 'List of mandatory checks to enforce', 'items': {'type': 'string'}, 'type': 'array'}, 'merge_configs': {'description': 'Merges lists between configuration layers', 'type': 'boolean'}, 'custom_rules': {'description': 'custom rule file to use', 'type': 'string'}, 'output_file': {'description': 'Path to the file to write the main output to', 'type': 'string'}, 'override_spec': {'description': 'Path to spec file to override with', 'type': 'string'}, 'regions': {'description': 'Regions to test against', 'items': {'type': 'string'}, 'type': 'array'}, 'registry_schemas': {'description': 'One or more directories of CloudFormation Registry Resource Schemas', 'items': {'type': 'string'}, 'type': 'array'}, 'templates': {'description': 'Templates to lint', 'items': {'type': 'string'}, 'type': 'array'}}, 'title': 'CFNLINTRC JSON Schema', 'type': 'object'}
2022-02-27 01:31:19,449 - cfnlint - DEBUG - Config used: {}
2022-02-27 01:31:19,450 - cfnlint - DEBUG - CFNLINTRC looks valid!
2022-02-27 01:31:19,450 - cfnlint - DEBUG - User configuration loaded as
2022-02-27 01:31:19,450 - cfnlint - DEBUG - {}
2022-02-27 01:31:19,450 - cfnlint - DEBUG - Project configuration loaded as
2022-02-27 01:31:19,450 - cfnlint - DEBUG - {}
2022-02-27 01:31:19,451 - cfnlint - DEBUG - Merging configurations...
2022-02-27 01:31:19,453 - cfnlint - DEBUG - Begin linting of file: eks-nodegroup.yaml
```
# Stacktrace
```
Traceback (most recent call last):
  File "/usr/local/bin/cfn-lint", line 8, in <module>
    sys.exit(main())
  File "/usr/local/lib/python3.8/dist-packages/cfnlint/__main__.py", line 27, in main
    matches = list(cfnlint.core.get_matches(filenames, args))
  File "/usr/local/lib/python3.8/dist-packages/cfnlint/core.py", line 121, in get_matches
    (template, rules, errors) = get_template_rules(filename, args)
  File "/usr/local/lib/python3.8/dist-packages/cfnlint/core.py", line 205, in get_template_rules
    (template, errors) = cfnlint.decode.decode(filename)
  File "/usr/local/lib/python3.8/dist-packages/cfnlint/decode/__init__.py", line 28, in decode
    template = cfn_yaml.load(filename)
  File "/usr/local/lib/python3.8/dist-packages/cfnlint/decode/cfn_yaml.py", line 246, in load
    return loads(content, filename)
  File "/usr/local/lib/python3.8/dist-packages/cfnlint/decode/cfn_yaml.py", line 224, in loads
    template = loader.get_single_data()
  File "/usr/local/lib/python3.8/dist-packages/yaml/constructor.py", line 51, in get_single_data
    return self.construct_document(node)
  File "/usr/local/lib/python3.8/dist-packages/yaml/constructor.py", line 55, in construct_document
    data = self.construct_object(node)
  File "/usr/local/lib/python3.8/dist-packages/yaml/constructor.py", line 100, in construct_object
    data = constructor(self, node)
  File "/usr/local/lib/python3.8/dist-packages/cfnlint/decode/cfn_yaml.py", line 81, in construct_yaml_map
    value = self.construct_object(value_node, False)
  File "/usr/local/lib/python3.8/dist-packages/yaml/constructor.py", line 100, in construct_object
    data = constructor(self, node)
  File "/usr/local/lib/python3.8/dist-packages/cfnlint/decode/cfn_yaml.py", line 81, in construct_yaml_map
    value = self.construct_object(value_node, False)
  File "/usr/local/lib/python3.8/dist-packages/yaml/constructor.py", line 100, in construct_object
    data = constructor(self, node)
  File "/usr/local/lib/python3.8/dist-packages/cfnlint/decode/cfn_yaml.py", line 81, in construct_yaml_map
    value = self.construct_object(value_node, False)
  File "/usr/local/lib/python3.8/dist-packages/yaml/constructor.py", line 100, in construct_object
    data = constructor(self, node)
  File "/usr/local/lib/python3.8/dist-packages/cfnlint/decode/cfn_yaml.py", line 81, in construct_yaml_map
    value = self.construct_object(value_node, False)
  File "/usr/local/lib/python3.8/dist-packages/yaml/constructor.py", line 102, in construct_object
    data = constructor(self, tag_suffix, node)
  File "/usr/local/lib/python3.8/dist-packages/cfnlint/decode/cfn_yaml.py", line 202, in multi_constructor
    return dict_node({tag_suffix: constructor(node)}, node.start_mark, node.end_mark)
  File "/usr/local/lib/python3.8/dist-packages/yaml/constructor.py", line 129, in construct_sequence
    return [self.construct_object(child, deep=deep)
  File "/usr/local/lib/python3.8/dist-packages/yaml/constructor.py", line 129, in <listcomp>
    return [self.construct_object(child, deep=deep)
  File "/usr/local/lib/python3.8/dist-packages/yaml/constructor.py", line 100, in construct_object
    data = constructor(self, node)
  File "/usr/local/lib/python3.8/dist-packages/cfnlint/decode/cfn_yaml.py", line 122, in construct_yaml_seq
    obj, = SafeConstructor.construct_yaml_seq(self, node)
  File "/usr/local/lib/python3.8/dist-packages/yaml/constructor.py", line 408, in construct_yaml_seq
    data.extend(self.construct_sequence(node))
  File "/usr/local/lib/python3.8/dist-packages/yaml/constructor.py", line 129, in construct_sequence
    return [self.construct_object(child, deep=deep)
  File "/usr/local/lib/python3.8/dist-packages/yaml/constructor.py", line 129, in <listcomp>
    return [self.construct_object(child, deep=deep)
  File "/usr/local/lib/python3.8/dist-packages/yaml/constructor.py", line 100, in construct_object
    data = constructor(self, node)
  File "/usr/local/lib/python3.8/dist-packages/cfnlint/decode/cfn_yaml.py", line 106, in construct_yaml_map
    mapping[key] = value
TypeError: unhashable type: 'dict_node'
```