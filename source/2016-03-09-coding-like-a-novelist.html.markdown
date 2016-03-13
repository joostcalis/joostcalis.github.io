---
title: Coding like a novelist
date: 2016-03-09
tags: ruby
layout: article
---



So January 31st was the first day of the bootcamp. And well let's just say I was nervous. Kind of like going to highschool for the first time when you're 12 nervous.    

I had prepared as much as I could with some codecademy courses about Ruby, Ruby on Rails and JavaScript. But basically this whole coding thing was new to me.     
### **First week**
The first week we mainly focused on simple Ruby code to run in the terminal. As the week progressed the nerves settled down and I started realizing how much fun it was to run into problems and then fixing them even if it took 20 tries to get there. In this first week though, I also developed something completely new to me which I'm sure other starting developers have encountered too. A weird new fear for the Enter key! When you don't really know what you're doing yet and haven't even heard of the concept of testing, pressing that Enter key after writing code for 30 minutes with no clue if it will work becomes quite a thing.        
### **About that novelist**
The main project for this week was building a simple store with a shopping cart. Which gets me to the title of this entry. It hadn't really sunk in with me yet that while coding, you may wanna split things up in a lot of small methods or functions. Instead of trying to explain what I mean myself, I think I'll let the initial code of that store speak for itself:

```ruby
def store (receipt)
  menu = {
    A: {  name: "cigs",
          price: 6,
          max: 10
       },
    B: {  name: "Milkpowder",
          price: 15,
          max: 2
       },
    C: {  name: "Wine",
          price: 10,
          max: 4
       },
    D: {  name: "Beer",
          price: 3,
          max: 6
       },
  }

  puts "Select a product:\n\n"
  menu.each do |id, product|
    puts "#{id}) #{product[:name]}, price: $#{product[:price]}"
  end

fruit = gets.chomp.upcase.to_sym
while fruit != :A && fruit != :B && fruit != :C && fruit != :D
  puts "input invalid, please try again\n\n"
  puts "Select a product:\n\n"
  menu.each do |id, product|
    puts "#{id}) #{product[:name]}, price: $#{product[:price]}"
  end
  fruit = gets.chomp.upcase.to_sym
end

puts "How many would you like?"
amount = gets.chomp.to_i

fruit1 = menu[fruit][:name]
item_price = menu[fruit][:price]
total_price = item_price * amount
receipt += total_price

puts "you have selected #{amount} item(s) of #{fruit1}. One item costs $#{item_price},-. So your selection costs $#{total_price},-"
puts "add this to your shoppingcart? (y/n)"
add = gets.chomp.downcase
if add == "y"
puts "your complete order now costs $#{receipt},-"
else
store(receipt-total_price)
return
end
puts "would you like to buy something else? (y/n)"
something_else = gets.chomp.downcase

if something_else == "n"

  puts "Ok that will be $#{receipt},- please. Would you like to pay with pin or cash?"
  payment_choice = gets.chomp.downcase
  while payment_choice != "pin" && payment_choice != "cash"

    puts "Sorry we dont accept #{payment_choice}. Please choose between pin or cash"
    payment_choice = gets.chomp.downcase

end
  if payment_choice == "pin"

    puts "For paying with pin I have to charge 1 euro extra so your bill will be $#{receipt + 1},-"

  elsif payment_choice == "cash"

    puts "cash is always good! thanks for visiting my store"

  end

elsif something_else == "y"

  store(receipt)

end
end
store(0)
end
```

That's right...One long method full of if statements! why not right....

But hey it worked and I was proud of that :)
