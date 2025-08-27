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

<details><summary><code>client.styleGuides.<a href="/src/api/resources/styleGuides/client/Client.ts">createStyleGuide</a>(file_upload, { ...params }) -> MarkupAI.StyleGuideResponse</code></summary>
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
await client.styleGuides.createStyleGuide(fs.createReadStream("/path/to/your/file"), {
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

**file_upload:** `File | fs.ReadStream | Blob`

</dd>
</dl>

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

Update the name of an existing style guide.

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
await client.styleGuides.updateStyleGuide("style_guide_id", {
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

**styleGuideId:** `string` — The ID of the style guide.

</dd>
</dl>

<dl>
<dd>

**request:** `MarkupAI.BodyUpdateStyleGuideV1StyleGuidesStyleGuideIdPatch`

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

<details><summary><code>client.styleChecks.<a href="/src/api/resources/styleChecks/client/Client.ts">createStyleCheck</a>(file_upload, { ...params }) -> MarkupAI.WorkflowResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Start a style and brand check workflow. Returns a workflow ID to use for polling results.

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
await client.styleChecks.createStyleCheck(fs.createReadStream("/path/to/your/file"), {
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

**file_upload:** `File | fs.ReadStream | Blob`

</dd>
</dl>

<dl>
<dd>

**request:** `MarkupAI.CreateStyleCheckV1StyleChecksPostRequest`

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

Retrieve the results of a style and brand check workflow. Returns `running` or `complete` status.

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

<details><summary><code>client.styleSuggestions.<a href="/src/api/resources/styleSuggestions/client/Client.ts">createStyleSuggestion</a>(file_upload, { ...params }) -> MarkupAI.WorkflowResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Start a style and brand suggestion workflow. Returns a workflow ID to use for polling results.

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
await client.styleSuggestions.createStyleSuggestion(fs.createReadStream("/path/to/your/file"), {
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

**file_upload:** `File | fs.ReadStream | Blob`

</dd>
</dl>

<dl>
<dd>

**request:** `MarkupAI.CreateStyleSuggestionV1StyleSuggestionsPostRequest`

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

Retrieve the results of a style and brand suggestion workflow. Returns `running` or `complete` status.

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

<details><summary><code>client.styleRewrites.<a href="/src/api/resources/styleRewrites/client/Client.ts">createStyleRewrite</a>(file_upload, { ...params }) -> MarkupAI.WorkflowResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Start a style and brand rewrite workflow. Returns a workflow ID to use for polling results.

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
await client.styleRewrites.createStyleRewrite(fs.createReadStream("/path/to/your/file"), {
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

**file_upload:** `File | fs.ReadStream | Blob`

</dd>
</dl>

<dl>
<dd>

**request:** `MarkupAI.CreateStyleRewriteV1StyleRewritesPostRequest`

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

Retrieve the results of a rewrite workflow. Returns `running` or `complete` status.

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
