# blog-post-generator

Generates a blog post based on a given topic and tone.

## Usage

1. **Variables**: Fill in the following variables to use this prompt:
   - **topic**: The main topic of the blog post.
   - **tone**: The tone of the blog post. (Options: professional, casual)
   - **wordCount**: The approximate length of the blog post. (Options: 500, 1000)

2. **Example Input**:
   ```json
   {
     "topic": "example-value",
     "tone": "professional",
     "wordCount": "500"
   }
   ```

3. **Example Output**:
   ```markdown
   Write a {tone} blog post about {topic}...
   ```

## Variables

## Variables

| Name        | Description                              | Type   | Required | Options              |
| ----------- | ---------------------------------------- | ------ | -------- | -------------------- |
| `topic`     | The main topic of the blog post.         | string | true     | -                    |
| `tone`      | The tone of the blog post.               | string | true     | professional, casual |
| `wordCount` | The approximate length of the blog post. | number | true     | 500, 1000            |

## Extensions

This prompt includes the following extensions:
- **seoKeywords**: A list of SEO keywords to include in the blog post.

## Dependencies

This prompt has no dependencies.

---

For more details, see the [Prompt Schema Documentation](../schemas/prompt-schema.json).