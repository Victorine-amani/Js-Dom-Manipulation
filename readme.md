            How the carousel works
We grab all the HTML elements we need with document.getElementById()
We set the myIndex to 0 – this is the variable that keeps track of which item of the carousel is currently shown
we assign all the items in the carousel to the variable x
x becomes like an array or a container that holds all the pictures representing all the items in the carousel
x.length 
the carousel will not display anything until the function is run
this will call each element increamenting by 1 to the next one
when my index gets to the last item in the container it will start from the beggining looping again through the array
the setTimeOut sets the time of the transitions between the images , after every three seconds (3000) the function will be called again allowing the carousel to move to the next image




var myObject = {
    name: "Lovelace",
    func: function() {
        var self = this;
        console.log("outer func:  this.name = " + this.name);
        console.log("outer func:  self.name = " + self.name);
        (function() {
            console.log("inner func:  this.name = " + this.name);
            console.log("inner func:  self.name = " + self.name);
        }());
    }
};
myObject.func();

The output of the code above will be:
outer func: this.name = Lovelace
outer func: self.name = Lovelace
inner func: this.name = undefined
inner func: self.name = Lovelace



variables declared in the outer func can be accesed by the inner func since they're in the same scope hence when using self.name it will look at the self declared by the outer func and print out lovelace
but then this. is an implicit parameter meaning it only belongs to the function it has been declared
Inside inner func, this does not refer to the this of outer func, because inner func has its own this.
and since this. has not been declared in the inner func it brings back the undefined error 

