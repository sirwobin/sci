# Developing SCI

## Workflow

### Start with an issue before writing code

Before writing any code, please create an issue first that describes the problem
you are trying to solve with alternatives that you have considered. A little bit
of prior communication can save a lot of time on coding. Keep the problem as
small as possible. If there are two problems, make two issues. We discuss the
issue and if we reach an agreement on the approach, it's time to move on to a
PR.

### Follow up with a pull request

Post a corresponding PR with the smallest change possible to address the
issue. Then we discuss the PR, make changes as needed and if we reach an
agreement, the PR will be merged.

### Tests

Each bug fix, change or new feature should be tested well to prevent future
regressions.  To run the test suite under various platforms, use the scripts
provided in `scripts/test/*`.  You will need a JVM, the [clojure tools](https://clojure.org/guides/install_clojure),
and [Leiningen](https://leiningen.org/) installed as a base minimum.  The
native tests should be executed with [GraalVM](https://www.graalvm.org/downloads/).
To run the CLJS tests you will also need [node JS](https://nodejs.org/en/download/)
installed.

### Force-push

Please do not use `git push --force` on your PR branch for the following
reasons:

- It makes it more difficult for others to contribute to your branch if needed.
- It makes it harder to review incremental commits.
- Links (in e.g. e-mails and notifications) go stale and you're confronted with:
  this code isn't here anymore, when clicking on them.
- CircleCI doesn't play well with it: it might try to fetch a commit which
  doesn't exist anymore.
- Your PR will be squashed anyway.
