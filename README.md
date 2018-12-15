# Be.Vlaanderen.Basisregisters.Utilities.ToStringBuilder

Concat given properties of the object into a string

## Usage

```csharp
public class Test
{
    public int Number { get; set; }
    public bool IsTrue { get; set; }

    public override string ToString()
    {
        return ToStringBuilder.ToString(new object[] {Number, IsTrue});
    }
}
```

```csharp
...
public override string ToString() => ToStringBuilder.ToString(Fields);

public IEnumerable<object> Fields()
{
    yield return Number;
    yield return IsTrue;
}
...
```
