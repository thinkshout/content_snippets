## ABOUT
The content_snippets module serves a simple purpose: it provides a way to make
text that is added to the site in code easily editable by content editors. Most
of the text that displays on a Drupal site is part of an editable block, menu,
node, or other entity, but there are always exceptions: an error message or help
text on a custom form; etc. This is useful when the developer does not have
finalized text and would like to proceed anyway, or when the text might be
subject to change in the future.

## USAGE
This module provides menu item under "Content" called "Snippets" and an
administrative item under "Configuration" called "Content Snippets Admin". Each
of these areas has an appropriately named permission.

The Admin is a place to create new snippets, which can then be edited on the
Content page. Once the snippet has a value, you can use that value anywhere in
your custom code.

In PHP, access it by calling `content_snippets_retrieve($snippetname)`, or by
pulling straight from configuration:
`\Drupal::config('content_snippets.content')->get($snippetname);`

In Twig templates, snippets are available as variables:
`{{ contentSnippets.snippetname }}`

Your snippets are also available via Tokens: [content_snippets:snippetname]
