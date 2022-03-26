# Ruby CheatSheet


# Everything in ruby is an object


### Write/Read file
    write_handler = File.new("newfile.out", "w")
    write_handle.puts("sometext").to_s
    write_handle.close
    data_from_file = File.read("newfile.out")
    puts "Data from file: " + data_from_file

### Comments
    =begin
    my comments
    =end

    # Comments

### if-else condition

```
if (xxx)
    puts...
elsif (xxx)
    puts...
else
    puts...
end
```

### Comparision
    puts "5 <=> 10 = " + (5 <=> 10).to_s

### Loop

    loop do
        x += 1

        next unless (x%2) == 0
        puts x

        break if x >= 10
    end

    while y <= 10   # until y <= 10
        xxx
    end

    for num in nums
        puts "# {num} , " # print - no new line
    end

### Array
    arr = ["a", "b", "c"]
    arr = Array.new
    arr = Array.new(5, "a")

    arr.each do |str|
        puts "Get a string #{str}"
    end

    (0..5).each do |i|
        puts "#{i}"
    end

    
### Hash
    number_hash = {"PI" => 3.14, "e" => 2.718}
    puts number_hash["PI"]

### Functions  (pass by value)
```
def add_num(num_1,num_2)
    return num_1.to_i + num_2.to_i
end
```

### Exception
```
age = 12
def check_age (age)
    raise ArgumentError, "Enter pos number" unless age > 0
end

begin
    check_age(-1)

rescue ArgumentError
    puts "Impossible age"
end
```

### tring 
    mystr.upcase
    mystr.downcase
    mystr.swapcase
    mystr.chop # remove last char
    mystr.chomp('ab') # remove ab from last
    mystr.delete("a") # delete every a
    arr = mystr.split(/ /) # split by space

### Symbol: Strings that can't be changed
    :mysymbl


### Arithmetic Operators
    puts "1 + 1 = " + (1+1).to_s

### Define float (14 digits)
    num = 1.000


---

ref
http://www.newthinktank.com/2015/02/ruby-programming-tutorial/


