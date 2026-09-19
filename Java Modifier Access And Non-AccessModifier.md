Modifiers

Access Modifier
1. private
2. package-private | default
3. protected
4. public

Non-Access Modifiers
1. abstract
2. static
3. final
4. volatile
5. transient
6. synchronized
7. sealed (Java 17+)
8. non-sealed (Java 17+)

Access Modifier Scope  
1. private
2. package-private / default
3. protected
4. public


```
private      → only inside same class
default      → only inside same package (package-private)
protected    → same package + subclasses (even different package)
public       → everywhere
```


| Access location                  | Public | Protected | Default(package private) | Private |
| -------------------------------- | ------ | --------- | ------------------------ | ------- |
| Same class                       | Yes    | Yes       | Yes                      | Yes     |
| Subclass in same package         | Yes    | Yes       | Yes                      | No      |
| Other classes in same package    | Yes    | Yes       | Yes                      | No      |
| Subclasses in other package      | Yes    | Yes       | No                       | No      |
| Non-subclasses in other packages | Yes    | No        | No                       | No      |