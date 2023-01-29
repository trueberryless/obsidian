## Textarea with Binding
Firstly, let's create a textarea which binds it's value to a string in @code {}.

```html
<textarea class="form-control" @bind-value="Text" @bind-value:event="oninput"></textarea>
```

```c#
@code {
	public string Text { get; set; } = String.Empty;
}
```

## Install Markdig
Then, install Markdig and use it, to convert Markdown to HTML:

```html
<div>
	@((MarkupString) Preview)
</div>
```

```c#
@code {
	public string Preview => Markdown.ToHtml(Text);
}
```

## All together

```html
<textarea class="form-control" @bind-value="Text" @bind-value:event="oninput"></textarea>
<div>
	@((MarkupString) Preview)
</div>
```

```c#
@code {
	public string Text { get; set; } = String.Empty;
	public string Preview => Markdown.ToHtml(Text);
}
```
