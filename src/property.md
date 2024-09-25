# Property
Properties are the characteristics of a Prim 

A property can be a:
* Attribute 
* Relationship
## Example

### USD file 
```python 
#usda 1.0

def Xform "hello"
{
    def Sphere "sphere"
    {
    }
}

```
### Code
```python 
from pxr import Usd
stage = Usd.Stage.Open('HelloUSD.usda')
xform = stage.GetPrimAtPath('/hello')
sphere = stage.GetPrimAtPath('/hello/sphere')

print(xform.GetPropertyNames())
# ['proxyPrim', 'purpose', 'visibility', 'xformOpOrder']
print(sphere.GetPropertyNames())
# ['doubleSided', 'extent', 'orientation', 'primvars:displayColor', 'primvars:displayOpacity', 'proxyPrim', 'purpose', 'radius', 'visibility', 'xformOpOrder']
```

![alt text](property.png)

```admonish note title="Further Reading"
* Namespaced Properties (`Eg: primvars:displayColor`)
* Setting Properties
* Setting Property Order
```



