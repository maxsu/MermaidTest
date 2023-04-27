# Instructions

To render Mermaid in github hosted markdown files:

1. Create a repo with the markdown file
2. Wrap the code in a \`\`\`mermaid {}\`\`\` block:

> Note: This does not work in gists 🥲

# Example 

Mardown:

    Fig. 1. The Build system from hell
    
    [image](https://user-images.githubusercontent.com/25123/234838310-7b91dd15-d6f1-4375-b890-a9482c99b6f0.png)

    ```mermaid
    graph 
        A["your files"] --> B["autoscan*"] --> C["configure.scan"] --> D["configure.ac"] 
        
        E["local macros"] & F["acinclude.m4"] --> G["aclocal*"] --> H["aclocal.m4"]

        D["configure.ac"] & H["aclocal.m4"] & I["acsite.m4"] 
            --> J["autoreconf"]
        --> K["autoconf*"] & L["autoheader*"]

        L["autoheader*"]  --> M["config.h.in"]

        K["autoconf*"] & M["config.h.in"]  & N["Makefile.in"]
            --> O["configure*"] 
        --> P["config.cache"] & Q["config.log"] & R["config.status*"]

        R["config.status*"] --> S["config.h"] & T["Makefile"]

        T["Makefile"] --> U["make*"]
    ```

Output:


Fig. 1. Autotools. The Build system from hell

 [image](https://user-images.githubusercontent.com/25123/234838310-7b91dd15-d6f1-4375-b890-a9482c99b6f0.png)


```mermaid
graph 
    A["your files"] --> B["autoscan*"] --> C["configure.scan"] --> D["configure.ac"] 

    E["local macros"] & F["acinclude.m4"] --> G["aclocal*"] --> H["aclocal.m4"]

    D["configure.ac"] & H["aclocal.m4"] & I["acsite.m4"] 
        --> J["autoreconf"]
    --> K["autoconf*"] & L["autoheader*"]

    L["autoheader*"]  --> M["config.h.in"]

    K["autoconf*"] & M["config.h.in"]  & N["Makefile.in"]
        --> O["configure*"] 
    --> P["config.cache"] & Q["config.log"] & R["config.status*"]

    R["config.status*"] --> S["config.h"] & T["Makefile"]

    T["Makefile"] --> U["make*"]
```
