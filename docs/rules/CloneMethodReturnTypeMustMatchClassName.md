# CloneMethodReturnTypeMustMatchClassName
**Category:** `pmd`<br/>
**Rule Key:** `pmd:CloneMethodReturnTypeMustMatchClassName`<br/>


-----

<p>Minimum Language Version: java 1.5</p>
<p>
  If a class implements cloneable the return type of the method clone() must be the class name. That way, the caller of
  the clone method doesn’t need to cast the returned clone to the correct type.
</p>
<p>
  Note: This is only possible with Java 1.5 or higher.
</p>

<p>Examples:</p>
<pre>
public class Foo implements Cloneable {
    @Override
    protected Object clone() { // Violation, Object must be Foo
    }
}

public class Foo implements Cloneable {
    @Override
    public Foo clone() { //Ok
    }
}
</pre>
