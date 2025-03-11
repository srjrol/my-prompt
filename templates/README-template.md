# {{metadata.name}}

{{metadata.description}}

## Author
- **Username**: [{{metadata.author.username}}](https://github.com/{{metadata.author.username}})
- **Avatar**: ![Avatar]({{metadata.author.avatarUrl}})

## Usage

1. **Variables**: Fill in the following variables to use this prompt:
   {{#each prompt.variables}}

   - **{{name}}**: {{description}} {{#if options}}(Options: {{options}}){{/if}}
     {{/each}}

2. **Example Input**:

   ```json
   {
     {{#each prompt.variables}}
     "{{name}}": "{{#if options}}{{options.[0]}}{{else}}example-value{{/if}}"{{#unless @last}},{{/unless}}
     {{/each}}
   }
   ```

3. **Example Output**:
   ```markdown
   {{prompt.template}}
   ```

## Variables

| Name | Description | Type | Required | Options |
| ---- | ----------- | ---- | -------- | ------- |

{{#each prompt.variables}}
| `{{name}}` | {{description}} | {{type}} | {{required}} | {{#if options}}{{options}}{{else}}-{{/if}} |
{{/each}}

## Extensions

{{#if extensions}}
This prompt includes the following extensions:
{{#each extensions}}

- **{{@key}}**: {{description}}
  {{/each}}
  {{else}}
  This prompt has no extensions.
  {{/if}}

## Dependencies

{{#if metadata.dependencies}}
This prompt depends on the following:
{{#each metadata.dependencies}}

- **{{@key}}**: {{this}}
  {{/each}}
  {{else}}
  This prompt has no dependencies.
  {{/if}}

---

For more details, see the [Prompt Schema Documentation](../schemas/prompt-schema.json).
