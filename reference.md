# Reference

## Style Guides

<details><summary><code>client.styleGuides.<a href="/src/api/resources/styleGuides/client/Client.ts">listStyleGuides</a>() -> MarkupAI.StyleGuideResponse[]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve all style guides associated with your organization.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.styleGuides.listStyleGuides();
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `StyleGuides.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.styleGuides.<a href="/src/api/resources/styleGuides/client/Client.ts">createStyleGuide</a>({ ...params }) -> MarkupAI.StyleGuideResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create a new style guide that can be used in checks, suggestions, and rewrites.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.styleGuides.createStyleGuide({
    file_upload: fs.createReadStream("/path/to/your/file"),
    name: "name",
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `MarkupAI.StyleGuideRequestBody`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `StyleGuides.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.styleGuides.<a href="/src/api/resources/styleGuides/client/Client.ts">getStyleGuide</a>(styleGuideId) -> MarkupAI.StyleGuideResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve a specific style guide by ID, including its metadata such as `name` and `status`.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.styleGuides.getStyleGuide("style_guide_id");
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**styleGuideId:** `string` — The ID of the style guide.

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `StyleGuides.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.styleGuides.<a href="/src/api/resources/styleGuides/client/Client.ts">deleteStyleGuide</a>(styleGuideId) -> void</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Delete a style guide by ID.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.styleGuides.deleteStyleGuide("style_guide_id");
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**styleGuideId:** `string` — The ID of the style guide.

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `StyleGuides.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.styleGuides.<a href="/src/api/resources/styleGuides/client/Client.ts">updateStyleGuide</a>(styleGuideId, { ...params }) -> MarkupAI.StyleGuideResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update the name and/or terminology domain IDs of an existing style guide.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.styleGuides.updateStyleGuide("style_guide_id");
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**styleGuideId:** `string` — The ID of the style guide.

</dd>
</dl>

<dl>
<dd>

**request:** `MarkupAI.BodyStyleGuidesUpdateStyleGuide`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `StyleGuides.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

## Style Checks

<details><summary><code>client.styleChecks.<a href="/src/api/resources/styleChecks/client/Client.ts">createStyleCheck</a>({ ...params }) -> MarkupAI.WorkflowResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Analyze text for grammar, style, and clarity issues.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.styleChecks.createStyleCheck({
    file_upload: fs.createReadStream("/path/to/your/file"),
    dialect: "american_english",
    style_guide: "style_guide",
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `MarkupAI.StyleCheckRequestBody`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `StyleChecks.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.styleChecks.<a href="/src/api/resources/styleChecks/client/Client.ts">getStyleCheck</a>(workflowId) -> MarkupAI.StyleCheckResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve style check results.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.styleChecks.getStyleCheck("workflow_id");
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**workflowId:** `string`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `StyleChecks.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

## Style Suggestions

<details><summary><code>client.styleSuggestions.<a href="/src/api/resources/styleSuggestions/client/Client.ts">createStyleSuggestion</a>({ ...params }) -> MarkupAI.WorkflowResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get suggested corrections for text.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.styleSuggestions.createStyleSuggestion({
    file_upload: fs.createReadStream("/path/to/your/file"),
    dialect: "american_english",
    style_guide: "style_guide",
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `MarkupAI.StyleSuggestionRequestBody`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `StyleSuggestions.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.styleSuggestions.<a href="/src/api/resources/styleSuggestions/client/Client.ts">getStyleSuggestion</a>(workflowId) -> MarkupAI.SuggestionResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve suggestion results.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.styleSuggestions.getStyleSuggestion("workflow_id");
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**workflowId:** `string`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `StyleSuggestions.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

## Style Rewrites

<details><summary><code>client.styleRewrites.<a href="/src/api/resources/styleRewrites/client/Client.ts">createStyleRewrite</a>({ ...params }) -> MarkupAI.WorkflowResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Rewrite text with style corrections applied.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.styleRewrites.createStyleRewrite({
    file_upload: fs.createReadStream("/path/to/your/file"),
    dialect: "american_english",
    style_guide: "style_guide",
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `MarkupAI.StyleRewriteRequestBody`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `StyleRewrites.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.styleRewrites.<a href="/src/api/resources/styleRewrites/client/Client.ts">getStyleRewrite</a>(workflowId) -> MarkupAI.RewriteResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve rewrite results.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.styleRewrites.getStyleRewrite("workflow_id");
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**workflowId:** `string`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `StyleRewrites.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

## Terminology

<details><summary><code>client.terminology.<a href="/src/api/resources/terminology/client/Client.ts">exportTerminology</a>() -> unknown</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Exports all term sets, terms and domains to CSV. The exported CSV follows the same format as the CSV import.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.terminology.exportTerminology();
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `Terminology.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.terminology.<a href="/src/api/resources/terminology/client/Client.ts">importTerminology</a>({ ...params }) -> MarkupAI.ImportSummary</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Uploads a CSV or ACTIF XML file and imports terminology.

**CSV Format Requirements:**

- CSV must include columns: Prohibited, Preferred, Context-Dependent, Instructions, Domains
- The first row must contain the column headers in the exact same order as shown above
- Multiple values within a single cell should be separated by semicolons with a space (e.g., term1; term2; term3)
- Empty cells are allowed
- The CSV import format is the same as the CSV export format.
  </dd>
  </dl>
  </dd>
  </dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.terminology.importTerminology({
    file: fs.createReadStream("/path/to/your/file"),
    delete_existing: true,
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `MarkupAI.BodyTerminologyImportTerminology`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Terminology.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.terminology.<a href="/src/api/resources/terminology/client/Client.ts">searchTerminology</a>({ ...params }) -> MarkupAI.TerminologySearchResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Searches the text for relevant terminology and returns matched term sets.

Term sets are matched if any word sequence (up to 5 words) in the text is similar to one of the terms of the term set.
The similarity measure used is a trigram similarity of 0.5 or higher between the word sequence and the term.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.terminology.searchTerminology({
    query: "query",
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `MarkupAI.TerminologySearchTerminologyRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Terminology.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.terminology.<a href="/src/api/resources/terminology/client/Client.ts">listTermSets</a>({ ...params }) -> MarkupAI.PaginatedTermSetsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get a pageable list of term sets with all their associated terms and domains.

The search filter searches the term set instructions and term text fields.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.terminology.listTermSets({
    page: 1,
    page_size: 1,
    search_term: "search_term",
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `MarkupAI.TerminologyListTermSetsRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Terminology.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.terminology.<a href="/src/api/resources/terminology/client/Client.ts">createTermSet</a>({ ...params }) -> MarkupAI.TermSetResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create a new term set. Terms and domains are linked to term sets.
The term set instructions text will be used to determine whether a term should be flagged in the text and what the term replacement should be.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.terminology.createTermSet({
    instructions: "instructions",
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `MarkupAI.TermSetCreateRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Terminology.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.terminology.<a href="/src/api/resources/terminology/client/Client.ts">getTermSet</a>(termSetId) -> MarkupAI.TermSetWithTerms</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.terminology.getTermSet("term_set_id");
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**termSetId:** `string` — UUID of the term set

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Terminology.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.terminology.<a href="/src/api/resources/terminology/client/Client.ts">deleteTermSet</a>(termSetId) -> void</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.terminology.deleteTermSet("term_set_id");
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**termSetId:** `string` — UUID of the term set

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Terminology.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.terminology.<a href="/src/api/resources/terminology/client/Client.ts">updateTermSet</a>(termSetId, { ...params }) -> MarkupAI.TermSetResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.terminology.updateTermSet("term_set_id");
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**termSetId:** `string` — UUID of the term set

</dd>
</dl>

<dl>
<dd>

**request:** `MarkupAI.TermSetUpdateRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Terminology.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.terminology.<a href="/src/api/resources/terminology/client/Client.ts">createTerm</a>(termSetId, { ...params }) -> MarkupAI.TermResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create terms that should be matched in the text. The term types are:

- **preferred**: this is the preferred term for the associated term set
- **prohibited**: this term should not be used to talk about the term set
- **context_dependent**: this term is correct in certain cases, but incorrect in others, the instructions field of the term set should explain when the term is correct and when it is incorrect
  </dd>
  </dl>
  </dd>
  </dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.terminology.createTerm("term_set_id", {
    term: "term",
    type: "preferred",
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**termSetId:** `string` — UUID of the term set

</dd>
</dl>

<dl>
<dd>

**request:** `MarkupAI.TermCreateRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Terminology.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.terminology.<a href="/src/api/resources/terminology/client/Client.ts">getTerm</a>(termSetId, termId) -> MarkupAI.TermResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.terminology.getTerm("term_set_id", "term_id");
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**termSetId:** `string` — UUID of the term set

</dd>
</dl>

<dl>
<dd>

**termId:** `string` — UUID of the term

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Terminology.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.terminology.<a href="/src/api/resources/terminology/client/Client.ts">updateTerm</a>(termSetId, termId, { ...params }) -> MarkupAI.TermResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.terminology.updateTerm("term_set_id", "term_id", {
    term: "term",
    type: "preferred",
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**termSetId:** `string` — UUID of the term set

</dd>
</dl>

<dl>
<dd>

**termId:** `string` — UUID of the term

</dd>
</dl>

<dl>
<dd>

**request:** `MarkupAI.TermUpdateRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Terminology.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.terminology.<a href="/src/api/resources/terminology/client/Client.ts">deleteTerm</a>(termSetId, termId) -> void</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.terminology.deleteTerm("term_set_id", "term_id");
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**termSetId:** `string` — UUID of the term set

</dd>
</dl>

<dl>
<dd>

**termId:** `string` — UUID of the term

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Terminology.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.terminology.<a href="/src/api/resources/terminology/client/Client.ts">listDomains</a>({ ...params }) -> MarkupAI.PaginatedDomainsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.terminology.listDomains({
    page: 1,
    page_size: 1,
    search: "search",
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `MarkupAI.TerminologyListDomainsRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Terminology.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.terminology.<a href="/src/api/resources/terminology/client/Client.ts">createDomain</a>({ ...params }) -> MarkupAI.DomainResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.terminology.createDomain({
    name: "name",
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `MarkupAI.DomainCreateRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Terminology.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.terminology.<a href="/src/api/resources/terminology/client/Client.ts">getDomain</a>(domainId) -> MarkupAI.DomainResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.terminology.getDomain("domain_id");
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**domainId:** `string` — UUID of the domain

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Terminology.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.terminology.<a href="/src/api/resources/terminology/client/Client.ts">deleteDomain</a>(domainId) -> void</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.terminology.deleteDomain("domain_id");
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**domainId:** `string` — UUID of the domain

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Terminology.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.terminology.<a href="/src/api/resources/terminology/client/Client.ts">updateDomain</a>(domainId, { ...params }) -> MarkupAI.DomainResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.terminology.updateDomain("domain_id");
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**domainId:** `string` — UUID of the domain

</dd>
</dl>

<dl>
<dd>

**request:** `MarkupAI.DomainUpdateRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Terminology.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>
