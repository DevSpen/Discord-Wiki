# Timestamps

### Introduction

Timestamp markdown is a 'internationalized' way of displaying times/dates. The information is rendered according to the end-user's timezone and locale. You can find [unix timestamps here](https://www.unixtimestamp.com/), these are what we use for timestamp markdown. Unix timestamps and epoch seconds generally mean the same thing. 

Although, unix time and epoch time are often used synonymously, they do have different meanings. Logistically speaking, the epoch represents Unix time '0' \(midnight at the start of 1 January 1970\). Unix time, or the Unix timestamp, represents to the number of seconds that have elapsed since the epoch.

### Examples

Here are some examples of timestamp markdown:  
`<t:epoch_seconds>` - &lt;t:1563758772&gt;

![Non-Styled Timestamp](../.gitbook/assets/image%20%283%29.png)

`<t:epoch_seconds:style>` - &lt;t:1563758772:R&gt;

![Relative Styled Timestamp](../.gitbook/assets/image%20%284%29.png)

{% hint style="success" %}
Both regular users and bots can use Timestamp Markdown!
{% endhint %}

### Styling

Here's a list of available timestamp styles from the [Discord Developer Documentation](https://discord.com/developers/docs/reference#message-formatting-timestamp-styles):

| Style | Example Output | Description |
| :--- | :--- | :--- |
| t | 16:20 | Short Time |
| T | 16:20:30 | Long Time |
| d | 20/04/2021 | Short Date |
| D | 20 April 2021 | Long Date |
| f | 20 April 2021 16:20 | Short Date/Time |
| F | Tuesday, 20 April 2021 16:20 | Long Date/Time |
| R | 2 months ago | Relative Time |

### Timestamp Markdown in Code

Below is a example of how Timestamp Markdown could be used when coding Discord Bots.

```javascript
let sec = Math.floor(Date.now() / 1000);
// unstyled:
message.channel.send(`<t:${sec}>`);
// styled:
message.channel.send(`<t:${sec}:F>`);
// This example is in discord.js.
```

