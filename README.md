
# One line of ruby code solutions
Showcasing the power and chainability of the ruby language

## Multiplication table (times tables)

```ruby
def print_multi_table(n)
  (1..n).each { |a| puts (1..n).map { |b| (a * b).to_s.rjust(n.to_s.length * 2) }.join("\s") }
end
```
Which results in (e.g ```n = 15```):
```ruby
   1    2    3    4    5    6    7    8    9   10   11   12   13   14   15
   2    4    6    8   10   12   14   16   18   20   22   24   26   28   30
   3    6    9   12   15   18   21   24   27   30   33   36   39   42   45
   4    8   12   16   20   24   28   32   36   40   44   48   52   56   60
   5   10   15   20   25   30   35   40   45   50   55   60   65   70   75
   6   12   18   24   30   36   42   48   54   60   66   72   78   84   90
   7   14   21   28   35   42   49   56   63   70   77   84   91   98  105
   8   16   24   32   40   48   56   64   72   80   88   96  104  112  120
   9   18   27   36   45   54   63   72   81   90   99  108  117  126  135
  10   20   30   40   50   60   70   80   90  100  110  120  130  140  150
  11   22   33   44   55   66   77   88   99  110  121  132  143  154  165
  12   24   36   48   60   72   84   96  108  120  132  144  156  168  180
  13   26   39   52   65   78   91  104  117  130  143  156  169  182  195
  14   28   42   56   70   84   98  112  126  140  154  168  182  196  210
  15   30   45   60   75   90  105  120  135  150  165  180  195  210  225

```

## Drawing a tree
```ruby
def print_tree(n, char)
  ((1..n).each { |x| puts (char * 2 * x).to_s.ljust(n + x).rjust(2 * n) })
end
```

Prints something like this:
```ruby
          ..          
         ....         
        ......        
       ........       
      ..........      
     ............     
    ..............    
   ................   
  ..................  
 .................... 
......................
```

## Fibonacci numbers
This solution comes from [Toptal's blog](https://www.toptal.com/ruby/interview-questions)
```ruby
def fibonacci(n)
  (1..n).inject([0, 1]) { |fib| fib << fib.last(2).inject(:+) }
end
```

Resulting in:
```ruby
[0, 1, 1, 2, 3, 5, 8]
```

