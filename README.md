# setup-codeartifact
Setups code artifact credentials and env vars

### Usage
```yaml
...

jobs:

  ...

  - name: Configure AWS Credentials
      uses: aws-actions/configure-aws-credentials@v1
      with:
        aws-access-key-id: ${{ secrets.AWS_ACCESS_KEY_ID }}
        aws-secret-access-key: ${{ secrets.AWS_SECRET_ACCESS_KEY }}
        aws-region: us-east-1

  ...

  - uses: soluciones-algoritmicas/setup-codeartifact@v1
      with:
        domain: my-codeartifact-domain
        domain-owner: 123456789
        region: us-east-1
        repository: my-codeartifact-repository

  ...
```
