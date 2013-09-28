# Debugging Feeds

Feeds are unique snowflakes that change over time; today's issue may be gone tomorrow. If you experience an issue, please follow these guidelines to capture a copy of the feed.

1. Download a copy of the feed:

        curl -sv "$FEED_URL" 2> headers.txt | xmllint --format - > feed.xml

    If the feed contains an syntax error, don't try to pretty-print it:

        curl -sv "$FEED_URL" 2> headers.txt > feed.xml

    This will save a copy of the feed and the request's headers

2. Create a [Gist][gist]. If you have the [gist command line tool][gist-cli] installed:

        gist feed.xml headers.txt

3. Include a link to the gist when you [create an issue][create-issue]

[gist]: https://gist.github.com/
[create-issue]: https://github.com/feedbin/support/issues/new
[gist-cli]: http://defunkt.io/gist/
