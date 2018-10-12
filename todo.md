* upgrade to ruby 2.4
* adjust Specs
  - make validity specs easier to understand
  - adjust to use `expect` syntax
* XML is outdated 
* is `attr_accessor` a code smell? (no encapsulation)
* ordering of methods in the file (should initialisation be closer to the top)
* should the structure be revised to take into account the new position in the course
  - students have now encountered TDD, i.e. writing their own failing specs in the acceptance-unit cycle assignment?


pseudo code on encapsulation:

no encapsulation
```
data = [{a => 1}, {b => 2}]

data[0][a] = 6
```
objects have encapsulation if attr_accessor not used

```rb
class Obj

  attr_accessor :a

  def initialize(a)
    @a = a
  end
  
  def foo
    @a +=1
  end
end

obj = Obj.new

obj.a = 7
```
