# tiny-url
Tiny URL solution design, Implementation

## **Functional Requirements:**

1. Given a URL, our service should generate a shorter and unique alias of it. This is called a short link. This link should be short enough to be easily copied and pasted into applications.
2. When users access a short link, our service should redirect them to the original link.
3. Users should optionally be able to pick a custom short link for their URL.
4. Links will expire after a standard default timespan (2*weeks). Users should be able to specify the expiration time.
5. No need for a user login. Its a new system so the number of users coming is unexpected

## **Non-Functional Requirements:**

1. The system should be highly available. This is required because all the URL redirections will fail if our service is down.
2. URL redirection should happen in real-time with minimal latency.
3. Shortened links should not be guessable (not predictable).

**Extended Requirements:**

1. Analytics; e.g., how many times a redirection happens?
2. Our service should also be accessible through REST APIs by other services.
