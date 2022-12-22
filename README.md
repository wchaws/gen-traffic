# gen-traffic

A simple HTTP traffic generator triggered by Github Action periodically.

## Use cases

- Load testing.
- Traffic analysis.
- Real world traffic generation.

## How to use it?

1. Fork this repository to your own GitHub repository.
2. Edit `urls.txt`. Each line in the file is a URL. This tool will randomly pick some URLs from the file.

   > **Warning**
   > For security reasons, DO NOT COMMIT YOUR HOSTNAME into this repo.
   > Instead, use a `$HOST` as a PLACEHOLDER in the `urls.txt`.
   > Then, add a Github Secret in your repository settings by following [this doc](https://docs.github.com/en/actions/security-guides/encrypted-secrets#creating-encrypted-secrets-for-a-repository).
3. Git commit and go!

## FAQs

1. Q: What is the interval between triggering requests?
   
   A: By default is 10 minutes, but you can change this in `.github/workflows/traffic.yml`.

2. Q: How do I manually trigger requests?
   
   A: Please see this [guide](https://docs.github.com/en/actions/managing-workflow-runs/manually-running-a-workflow).

3. Q: How to stop triggering?
   
   A: To stop triggering, delete `schedule` in `.github/workflows/traffic.yml` and git commit.
