# Ruby
Ruby cheat sheet \
Hi My name is Jawad a.k.a Iori it's my first time i write about a programming langauge and i will start with ruby and make a cheat sheet  because we learn a lot of langauge but we forget them if we try to read another one 
I hope this can help you to .
\
\
Ruby is a dynamic, interpreted, reflective, object-oriented, general-purpose programming language. 
It was designed and developed in the mid-1990s by Yukihiro "Matz" Matsumoto in Japan.(wikipedia)
\
\
I/O :\
var=gets\
puts var\
1-# Comments\
#blablabla \
or \
=begin\ 
comment 1\
comment 2\
comment 3\
.....\
=end \
2-everything is an object :(Numbers and strings are objects )\
puts 3.class   => FixNum \
puts :option.class  => symbol\
puts "I'm a string".class => string  \
puts 3.to_s    => "3"\
puts 2.to_f   =>  2.00\
puts 3.to_i   => 3 \
3-Arithmetic :\
puts 2*3 => 6 \
puts 1+1 => 2 \
etc \
4-Special values :\
nil   => mean nothing to see here\
true  => truth\
false => falsehood\
puts nil.class  => nilclass\
puts true.class => trueclass\
puts false.class => falseclass\
5-equality and inequality :\
 1 == 1  =>true \
 1 != 2  =>false\
 !nil \
 !true \
 !false\
 6-comparisons:\
 1<2\
 2>1\
 1<=1\
 etc \
7-Placeholder:\
placeholder="Student "\
puts "i'm a #{placeholder} at school "\
8-Combining strings \
"hello" + "bro"  =>hello bro \
"hello" + 2 => error just strings \
"hello" + 2.to_s  => hello 2 \
9-variables :\
x=101 \
#we can do multiple assignement \
x=y=101 \
x => 101 \
y =>101\
10-symblos are objects \
var = :option \
var == :option => true \
var1 = :option \
var1 == var => true \
var  == 'option' => false \
11-Arrays \
Array =[1,2,3]\
puts Array => 1 \n 2 \n 3 \
puts Array.inspect => [1,2,3]\
Array << 4  #add 4 to an Array [1,2,3,4]\
Array[0] and Array.[] 0  => returns value 1 \
Array[-1] =>return last value in our case value 4 \
Array[1..3]  #range \
12-Hashes are Ruby's primary dictionary with keys/value pairs.\
hash={'a'=>'1','b'=>'2'}\
puts hash.keys #=> ['a','b']\
puts hash.values #=> ['1','2']\ 
since ruby's 1.9 when using symbols as keys :\ 
new_hash = { defcon: 3, action: true}\
puts new_hash.keys #=>defcon action\
Arrays and Hashes share a lot of useful methods such  as map ,each ,count ...\
#  Control structure:
if 1==2 \
 puts "true "\
elseif 1==1 \
 puts "false"\
end\

for counter in (1..10)\
   puts "Nmbr #{counter}"\
end \

(1..10).each do |counter|\
  puts "Nmbr #{counter}"\
end   \
or we can just use all in brackets\
(1..10).each {|counter| puts "Nmbr #{counter}"}\
\
iterators data using each \
Array.each do |counter|\
  puts "Nmbr #{counter}"\
end\
 also hashes:\
 hash.each do |key, value|\
  puts "#{key} is #{value}"\
end\
\
counter = 1\
while counter<=5  do\
   puts #{counter}\
   counter++\
end   \
\
##=>switch:\
 case x \
 when 'A'\
 puts "A"\
 when 'B'\
 puts "B"\
 else\
 puts "nothing"\
 end\
 #=>Another example :\
 grade = 82\
case grade\
    when 90..100\
      puts "Sad!"\
    when 80...90\
      puts "OK job" \
    else\
      puts "You failed!"\
end\

# Functions:
1- \
def hello\
  puts "hello world "\
end \
 hello => hello world \
2-\
def sum(x,y)\
  x + y\
end\
sum 2,4 #=> 6\
sum sum(3,4), 5 #=>12\
##yield\
called with the 'yield ' keyword \
def surround \
  puts "{"\
  yield\
  puts "}"\
end\
surround {puts "hello "}\
Output:    { hello } \
##Pass a list of arguments\
def fct(*Array)\
Array.each{|counter| puts "#{counter}" } \
end\
##Define a class\
class Pro\
#class variable shared by all \
 @@all = "all"\
 #method initializer\
def initialise(name,age)\
  @name=name\
  @age=age \
 end \
 #Basic Setter and getter methods \
 def name=(name)\
    @name=name\
 end\
 def name \
   @name\
 end       \
 #Getter/setter methods can also be created \
 attr_reader :name\
 attr_writer :name\
#A class method uses self to distinguish from\
def self.sms(msg)\
   puts "#{msg}"\
end\
end \
\
#Instantiate a class\
jim = Pro.new("Jim ",0)\
#files\
aFile = File.new("input.txt", "r")\
if aFile\
   content = aFile.sysread(20)\
   puts content\
else\
   puts "Unable to open file!"\
end\
File.open("filename", "mode") do |aFile|\
   #... process the file\
end\
example:\
#!/usr/bin/ruby\
file =File.open("input.txt", "r")\
if file \
	content =file.sysread(20)\
	puts content\
else\
 puts "error to open #{file} file  "	\
end
References:
** https://pine.fm/LearnToProgram **
