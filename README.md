# test
a test repo for testing random things


> [!TIP]  
> Docs: https://common.codeyourfuture.io



```bash
hugo new site org-<your-org-name>
cd org-<your-org-name>
```

2. Initialise your new site as a hugo module, as only modules can import modules:

```zsh
hugo mod init github.com/CodeYourFuture/curriculum/org-<your-org-name>
```

Then add the common theme and content modules as hugo modules to hugo.toml:

```toml
[module]
  [[module.imports]]
    path = "github.com/CodeYourFuture/curriculum/common-theme"
  [[module.imports]]
    path = "github.com/CodeYourFuture/curriculum/common-content"
    [[module.imports.mounts]]
      source = "en"
      target = "content"
``` 


