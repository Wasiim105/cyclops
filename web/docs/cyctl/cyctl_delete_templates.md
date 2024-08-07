# cyctl delete templates

Delete one or more templates

### Synopsis

The delete templates command allows you to remove one or more templates from the Cyclops API.

```
cyctl delete templates [template_name] [flags]
```

### Examples

```
# Delete a single module
cyctl delete modules module1

# Delete multiple modules
cyctl delete modules module1 module2 module3
```

### Options

```
  -h, --help   help for templates
```

### SEE ALSO

* [cyctl delete](cyctl_delete.md)	 - Delete custom resources like modules, templates, and templateauthrules

###### Auto generated by spf13/cobra on 29-Jul-2024
