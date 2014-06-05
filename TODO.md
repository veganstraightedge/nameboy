# make it interactive
    if ARGV.length == 1
      puts "I need to use your access.enom.com password"
      puts "I don't save or store your password anywhere"
      puts "Coo? Cool."
      puts
      puts "What is your current password"
      @current_password     = gets
      puts "What do you want your new password to be?"
      @new_password         = gets
      puts "What was that new password again?"
      confirm_@new_password = gets
   
      unless @new_password == @new_password
        abort "
        OH NOES! You mistyped one of your passwords.
        Start over and try again.
        "
      end
   
      puts "What is the URL of your domains file?"
      @url                  = gets
    end

# write tests
