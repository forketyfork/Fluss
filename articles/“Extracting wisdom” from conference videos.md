from:: [“Extracting wisdom” from conference videos | Lobsters](https://lobste.rs/s/z5karh/extracting_wisdom_from_conference)
url:: [“Extracting wisdom” from conference videos – Gonçalo Valério](https://blog.ovalerio.net/archives/2900)
on:: 2024-07-12 17:01

The author describes his setup for summarizing conference video contents from YouTube, so that it's easier for him to decide what to spend his time on. He takes the video transcript, feeds it into a local llama3:8b model installed via ollama, and uses the Fabric framework for croud-sourced prompts, like "extract wisdom".

The takeaway is that the results are not great, the model often focuses only on small part of the video, highlights suprefluous or unimportant stuff, or misinterprets what's being said.

In general, the article is not very illuminating, but I've picked up ollama and fabric from this article.

It's funny that the summarization is something I always try to do by hand, as it's part of working on content and understanding it, and this is exactly why I've created this repository.