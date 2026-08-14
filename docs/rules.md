# Rules for Writing Documentation

## Language

The documentation uses U.K. English for spellings and grammar.

Abbreviations should not be used (for example, shouldn't, can't, won't) and neither should emoticons.

Although the documents are not currently translated, they should be written as if they could be. That means consideration of the language used...can it be understood and translated unambiguously? For example, "configure" should be used rather than "set up" as "set up" can be misunderstood. This might sound silly, but translation is not always done in context, and people can put single words into Google Translate (for example) and get random results! Idioms, colloquialisms, and foreign expressions (including Latin) should also be avoided; for example, use "exactly" or "precisely" rather than the Latin "verbatim".

Language style will vary between documents. For example, the Language Reference Guide needs to be very precise and official whereas a User Guide can include less formal statements such as "You might notice that...".

Do **not** use an apostrophe when pluralising an acronym ("CPU's today are..." = WRONG)

Try to make documents future-proof (especially with respect to dates/version numbers, "coming soon", and so on). Variables can help with this!

Write so that a sentence cannot be misread. Avoid "so" when you mean "therefore", which is ambiguous; use "therefore", "meaning that", or another unambiguous connective. Set connectives such as "therefore" and "that is" off with commas, for example, "the setting is, therefore, still in effect".

Gloss a short code or abbreviation the first time it is shown, for example, "if `Format` is `'D'` (which stands for *Data*)".

Use the Oxford (serial) comma before the final item in a list of three or more items, for example, "the major release, minor release, and build number".

Keep the phrasing of parallel items consistent: entries in a list, rows in a table, or the descriptions of two related things should share the same structure and wording so the reader can compare them easily.

State what is true now, not how it came to be. Prefer "X is also known as Y" to "X was previously (or formerly) called Y".

Use "that" to introduce a restrictive clause and "which" for a non-restrictive one; use "if" for a condition and "whether" for a choice between alternatives.

Do not use "for example" and "and so on" in the same list: give a few examples or trail off with "and so on", but not both.

## Terminology

The following table lists correct terminology and terms to avoid. A complete list of the [approved names for glyphs and primitive functions/operators](https://docs.dyalog.com/latest/CheatSheet%20-%20Nomenclature%20-%20Functions%20and%20Operators.pdf) is also available.

**NOTE:** Although these terms are the correct ones to use, the documentation must always reflect the software. For example, if a field in the software uses "pdf" then the documentation should also use "pdf" when referring to that field content; the software usage always takes precedence.

|**Use**|**Avoid**|
|---|---|
|large-span file|64-bit file|
|small-span file|32-bit file|
|Dyalog (referring to the product)|Dyalog APL|
|Dyalog Ltd (referring to the company)|Dyalog|
|PDF|pdf|
|.NET|.Net, .net, any other variation|
|dfn (Dfn when starting a sentence)|dynamic function, d-fn, D-fn, Dfn (unless starting a sentence)|
|dop (Dop when starting a sentence)|dynamic operator, d-op, D-op|
|Edit window (a window); the Editor (the tool)|Edit Window|
|Trace window (a window); the Debugger (the tool, docked in Standard mode)|Trace Window, Tracer|
|for example|eg, e.g., eg.|
|that is|ie, i.e., ie.|
|note|NB, N.B.|
|and so on|etc, etc.|
|Boolean|boolean|
|UNIX|Unix, unix|
|configuration parameter|environment variable|

"Editor" and "Debugger" name the tools; "Edit window" and "Trace window" name individual windows. Use "Session window" when you mean the window; bare "Session" is ambiguous, as it can also mean the session file, the session object (`⎕SE`), or the running interpreter. When introducing a configuration parameter, use the full term "configuration parameter", not just "parameter".

  
Best practice:

|**Use**|**Avoid**|
|---|---|
|can, might|may|
|want|wish|

## Dyalog-specific Terms

"Dyalog":

- Dyalog = the product
- Dyalog APL = the language
- Dyalog Ltd = the company

Syntax:

- System functions should be written in upper case, for example, ⎕OFF
- System commands should be written in upper case, for example, )CLEAR
- User commands should be written in upper camel case, with user command groups wtirren in upper case, for example, ]LINK.GetItemName
- Configuration parameters should be written in upper case if cross-platform; some of them are written in mixed case on Microsoft Windows, although this not case sensitive so upper case works there too. See the appropriate _Dyalog for `<operating system>` Installation and Configuration Guide_ for operating-system-specific casing if you're documenting a configuration parameter on a particular platform.

## Acronyms

Industry-standard abbreviations and acronyms can be used without explanation, for example, HTTP or XML.

When you use an acronym that is not an industry standard for the first time, write the full word or phrase in its entirety and then enclose its abbreviation or acronym in parentheses. Afterwards, use the abbreviation or acronym alone. For example, "...the Dyalog Remote Communicator (DRC). The DRC can be...".

## Ordinal Numbers

**NOTE:** The documentation, like the default Dyalog Session, uses an index origin of 1.

Ordinal numbers:

- should have postscripts rather than superscripts as superscripts can be hard to read, for example, 3rd.
- should be written as numbers rather than words when referring to something that is 11 or greater OR that is in a list, for example, "the 75th element in the vector" or "the 4th line of code"
- should be written as words rather than numbers when referring to something that is 10 or smaller AND not part of a list, for example, "the first time you do this" or "on the sixth day".

If an algebraic term is being used instead of the number, then it should be italicised to distinguish it from the postscript, for example, "the _i_th term" or "the _n_th time".

## Imaginary Numbers

The imaginary part should be prefixed with a capital letter J (that is how the session returns it), for example, 0J4.

## Lists

Lists can ordered or unordered. You should:

- use an ordered (numbered) list when the order in which steps are taken is important.
- use an unordered (bulleted) list when the order does not matter.

Lists can be nested to a depth of three.

Use full stops for your list items if they complete a sentence (in this situation the list items should start with lower case letters), otherwise leave them without a full stop. In all ordered lists and most unordered lists, full stops will usually be appropriate.

A list is not a single sentence split across its items. Where the items share a common logic, state it once in the lead-in line (or an admonition) above the list and let each item stand alone, rather than stringing the items together with connective phrases or trailing semicolons. For example, introduce a precedence order with "Each source overrides those below it:" and then list the bare source names.

## Third-party Products

Legally, the owner of the product ought to be included the first time that a product is mentioned - this applies to every paragraph. For example, when writing about something that's on the Windows system, "Microsoft Windows" must be used the first time in the paragraph and just "Windows" can be used after that. However, if Windows is referred to in the subsequent paragraph, it needs to be "Microsoft Windows" again.

## Describing Parameters and Values

State a parameter's default value inline, in parentheses, for example, "(the default)".

Describe a Boolean parameter with a parallel "whether ... or not" phrase that gives both values and marks the default, for example, "specifies whether (`1`) or not (`0`, the default) to enable multi-line input". Where it helps, add a sentence explaining what the default means, for example, "the default is `1`, meaning that multi-line input is enabled".

## Deprecations

Describe a deprecated feature consistently:

- state that it has been deprecated and is scheduled for removal in a future release;
- name the replacement (or the configuration parameter that reinstates the previous behaviour) and link to it;
- link to the relevant _Release Notes_ for guidance on identifying the deprecated usage in existing code.

For example: "`739⌶` has been deprecated and is scheduled for removal in a future release. Its functionality is now provided by [`⎕SYSTEM.Directories.Temp`](#)."

## Notes

Various icons are used in the documentation to emphasise specific material. Notes are also used to differentiate between operating-system-specific behaviour in cross-platform documents. See [Notes](./style.md#notes).

Do not overuse notes. Only use an admonition when the content is a genuine aside (a hint, a warning, a piece of information set apart from the main flow). Content that belongs in the main narrative should be written as an ordinary paragraph, not wrapped in an admonition.

## Miscellaneous

Full stops should be followed by a single space, not a double space.

When using a dash in a sentence, use an en-dash not a hyphen. Write a numeric range with an unspaced en-dash, for example, "1–2147483647".

Separate paragraphs with a single blank line. Do not leave two or more consecutive blank lines, as it makes the source messy.

Number footnotes in the order in which they are first referenced on the page.

Refer to files supplied under the installation directory using the `[DYALOG]` placeholder, for example, **[DYALOG]/ws/dfns.dws**.

Make sure visible (rendered) parentheses are balanced.

## Contributing

- Associate every pull request with an issue.
- Name a branch after the issue it addresses, as `<issue-id>-slug`.
- Close the issue from the merge message (`Closes #N`), not from a commit message.

## Libraries: Operating System Differences

- Microsoft Windows: Dynamic Link Library (.dll)
- Linux/UNIX: Shared/static library (.so)
- macOS: Shared/static library (.a)
