```
HashSet <string> name = new HashSet<string>();

HashSet <string> last = new HashSet<string>();

name.Add("Joseph");

last.Add("Smith");

# We will have to create a third set to save the element of the union of the other two sets:

HashSet <string> fullname = new HashSet<string>(name);

fullname.UnionWith(last);

foreach (var i in fullname)
{
    Console.Write(i + " ")
}// Will print Joseph Smith
```