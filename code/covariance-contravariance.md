# Covariance, contravariance, etc.

Sites
- https://eli.thegreenplace.net/2018/covariance-and-contravariance-in-subtyping/ 
- https://blog.daftcode.pl/covariance-contravariance-and-invariance-the-ultimate-python-guide-8fabc0c24278
- https://blog.magrathealabs.com/pythons-covariance-and-contravariance-b422c63f57ac

```
abstract type Vertebrate end
abstract type Mammal <: Vertebrate end

struct Bird <: Vertebrate end
struct Dog <: Mammal end

f1(x::Mammal) = Dog()
f2(x::Vertebrate) = Bird()
```
