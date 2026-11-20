# Experiment 7: Using OSINT Tools for Reconnaissance

## Aim

To use Google search operators and Shodan for passive reconnaissance and understand the public information these tools may reveal.

## Requirements and scope

- Browser and internet connection
- Google Search and Shodan

All searches in this experiment were restricted to `example.com`, a reserved domain for documentation examples. No real organization or public service was targeted, and no active scans or service connections were performed. Use other targets only with explicit authorization.

## Theory

### Google search operators

Google operators help narrow pages already in its index. The `site:` operator limits results to a domain, while `filetype:` searches for a kind of file. In this authorized example, `site:example.com` returned Example Domain pages, and `site:example.com filetype:pdf` returned no matching documents.

![Google results limited to the reserved example.com domain](Screenshots/01-google-example-domain.png)

![No PDF documents found for the reserved example.com domain](Screenshots/04-google-example-pdf.png)

Operators such as `intitle:` and `inurl:` can narrow results by page title or URL. Only snippets were reviewed; no login pages or sensitive material were opened. The `cache:` operator is deprecated and no longer retrieves cached pages.

![Google explanation that the cache operator is deprecated](Screenshots/13-google-cache-example-domain.png)

### Shodan

Shodan indexes information about internet-connected hosts and services, including ports and service banners. Searches in this experiment included `hostname:example.com` to stay within the reserved domain. Shodan required sign-in or reported its search-usage limit, so no host records or service details could be reviewed. A submitted query does not prove that a matching asset exists.

![Shodan sign-in requirement for the scoped hostname query](Screenshots/02-shodan-example-hostname.png)

![Shodan search-usage limit for the scoped organization query](Screenshots/15-shodan-org-example.png)

## Procedure

### Step 1: Search with Google

Run operator examples using the reserved domain, for example:

```text
site:example.com
site:example.com filetype:pdf
site:example.com intitle:"index of"
site:example.com inurl:login
```

Review snippets only and do not try to access private or sensitive material. Results can change as Google's index is updated.

### Step 2: Search with Shodan

Add `hostname:example.com` to each query to keep searches within the reserved scope. Query types included hostname, service, organization, port, and product searches.

## Result

Google returned pages for the reserved domain and no matches for the example PDF query. Shodan's access limits prevented viewing filtered results; no IP addresses, open ports, or service banners were verified. Any sample results shown in the presentation are illustrative only.

## Conclusion

This experiment demonstrated how Google and Shodan can support passive reconnaissance within a safe scope. Search results alone do not confirm an exposure or vulnerability. The presentation's Nmap/Nessus material is a separate experiment and was not performed here.

Adapted with permission from [4316sushil39's source repository](https://github.com/4316sushil39/Offensive-and-defensive-security-COM-502-/tree/main/Exp-7).
