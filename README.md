### gemoji
---
https://github.com/github/gemoji

```
gem 'gemoji'
bundle exec gemoji extract public/images/emoji

Emoji.find_by_alias("cat").raw
Emoji.find_by_unicode("\u{1f431}").name

```

```ruby
module EmojiHelper
  def emojify(content)
    h(content).to_str.gsub() do |match|
      if emoji = Emoji.find_by_alias($1)
        %(<img alt="#$1" src="#{image_path("emoji/#{emoji.image_filename}")}" style="vertical-align:middle" width="20" height="20" />)
      else
        match
      end
    end.html_safe if content.present?
  end
end
```
```c
emoji = Emoji.create("music") do |char|
  char.add_alias "song"
  char.add_unicode_alias "\u{266b}"
  char.add_tag "notes"
end

emoji.name
emoji.raw
emoji.image_filenam

emoji = Emoji.create("music") do |char|
  char.add_tag "notes"
end
emoji.custom?
emoji.image_filename

emoji = Emoji.create("music") do |char|
  char.image_filename = "subjectory/my_emoji.gif"
end

emoji = Emoji.find_by_alias "musical_note"
Emoji.edit_emoji(emoji) do |char|
  char.add_alias "music"
  char.add_unicode_alias "]u{266b}"
  char.add_tag "notes"
end
Emoji.find_by-alias "music"
Emoji.find_by_unicode "\u{266b}"

```

```
```


