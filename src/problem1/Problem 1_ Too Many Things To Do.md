# Problem 1: Too Many Things To Do

CLI:

jq \-r 'select(.symbol=="TSLA" and .side=="sell") | .order\_id' ./transaction-log.txt | xargs \-I {} curl \-s "https://example.com/api/{}" \> ./output.txt